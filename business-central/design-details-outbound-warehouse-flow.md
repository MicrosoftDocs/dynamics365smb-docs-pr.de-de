---
title: Überblick über ausgehende Lagerprozesse
description: Dieser Artikel beschreibt den ausgehenden Lager-Workflow.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes"></a><a name="outbound-warehouse-processes"></a>Ausgehende Lagerprozesse

Ausgehende Prozesse in Lagern starten, wenn Sie einen Herkunftsbeleg freigeben, um Artikel aus einem Lagerort zu entnehmen. Zum Beispiel, um die Artikel entweder irgendwohin zu versenden oder sie an einen anderen Firmenlagerort zu bringen. Grundsätzlich besteht der Prozess des Ausgangs von ausgehenden Aufträgen aus zwei Aktivitäten:

* Kommissionieren von Artikeln aus den Regalen.
* Versand von Artikeln aus dem Lager.

Die Herkunftsbelege für den ausgehenden Lagerfluss sind:  

* Verkaufsauftrag  
* Ausgehender Umlagerungsauftrag.  
* Einkaufsreklamation  
* Serviceauftrag  

> [!NOTE]
> Produktions- und Montageaufträge mit Komponentenbedarf stellen ebenfalls ausgehende Herkunftsbelege dar. Produktions- und Montageaufträge sind etwas anders, da es sich in der Regel um interne Prozesse handelt, die keinen Versand beinhalten. Stattdessen werden sie verwendet, um produzierte Artikel einzulagern oder die für die Montage eines Artikels erforderlichen Komponenten zu einem Montagebereich zu transportieren. Erfahren Sie mehr über diese Prozesse unter [Designdetails: Interne Lagerflüsse](design-details-internal-warehouse-flows.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)] kommissionieren und versenden Sie Artikel wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden.

|Art|Ausgangsprozess|Kommissionierung erforderlich|Warenausgang erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Die Kommissionierung und den Versand aus der Auftragszeile buchen|||Keine dedizierte Lageraktivität.|  
|B|Die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg buchen|Aktiviert||Basis: Auftragsbezogene Logistik|  
|U|Die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg buchen||Aktiviert|Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg buchen|Aktiviert|Aktiviert|Erweitert|  

Der zu wählende Ansatz hängt von Ihren Lagermethoden und dem Niveau seiner Organisationskomplexität ab. Im Folgenden finden Sie einige Beispiele, die Ihnen bei der Entscheidung helfen könnten.

* In einer Auftrag-für-Auftrag-Umgebung mit einfachen Prozessen und einer einfachen Lagerplatzstruktur eignet sich Methode A, Kommissionierung und Versand von der Auftragszeile.
* Wenn Artikel für eine Auftragsposition aus mehr als einem Lagerplatz stammen oder Lagerarbeiter nicht mit Auftragsbelegen arbeiten können, ist die Verwendung separater Kommissionierungsbelege angemessen, Methode B.
* Wenn Ihre Kommissionierungs- und Versandprozesse mehrere Bestellungen umfassen und mehr Kontrolle und Übersicht erfordern, können Sie einen Lagerversandbeleg und einen Lagerkommissionierungsbeleg verwenden, um die Kommissionierungs- und Versandaufgaben zu trennen, Methoden C und D.  

In den Methoden werden A, B und C werden die Aktivitäten für Kommissionierung und Lieferung in einem Schritt zusammengefasst, wenn der Beleg als geliefert gebucht wird. In Methode D erfassen Sie zuerst die Kommissionierung, dann buchen Sie die Lieferung später aus einem anderen Beleg.

> [!NOTE]
> Lagerkommissionierungen und Lagerbestandskommissionierungen klingen zwar ähnlich, sind aber unterschiedliche Dokumente und werden in unterschiedlichen Prozessen verwendet.
> * Die in Methode B verwendete Lagerbestandskommissionierung verbucht zusammen mit der Registrierung von Kommissionierungsinformationen auch den Versand des Herkunftsbelegs.
> * Die in Methode D verwendete Lagerkommissionierung kann nicht gebucht werden und erfasst nur die Kommissionierung. Die Erfassung macht die Artikel für Warenausgabe verfügbar bucht den Versand aber nicht. Im ausgehenden Fluss erfordert die Lagerkommissionierung einen Warenausgang.

## <a name="no-dedicated-warehouse-activity"></a><a name="no-dedicated-warehouse-activity"></a>Keine dedizierte Lageraktivität

Die folgenden Artikel enthalten Informationen zum Verarbeiten von Wareneingängen für Herkunftsbelege, wenn Sie keine dedizierten Lageraktivitäten haben.

* [Produkt verkaufen](sales-how-sell-products.md)
* [Umlagerungsaufträge](inventory-how-transfer-between-locations.md)
* [Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen](purchasing-how-process-purchase-returns-cancellations.md)
* [Erstellen von Serviceaufträgen](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations"></a><a name="basic-warehouse-configurations"></a>Grundlegende Lagerhauskonfigurationen

Das folgende Diagramm zeigt die ausgehenden Lagerprozesse für verschiedene Belegtypen bei der Basislagerkonfiguration an. Die Nummern im Diagramm entsprechen den Schritten in den Abschnitten, die dem Diagramm folgen.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Zeigt die Schritte in einem grundlegenden ausgehenden Fluss in einem Lager.":::

### <a name="1-release-a-source-document"></a><a name="1-release-a-source-document"></a>1: Ein Herkunftsbeleg freigeben

Wenn Sie die Aktion **Freigeben** für einen Herkunftsbeleg verwenden, z. B. einen Verkaufs- oder Umlagerungsauftrag, sind die Artikel auf dem Beleg bereit, im Lager bearbeitet zu werden. Zum Beispiel kommissionieren und in den auf dem Beleg angegebenen Lagerplatz legen. Alternativ können Sie Belege für Lagerbestandskommissionierung für einzelne Auftragszeilen, im Push-Verfahren, basierend auf angegebenen Lagerplätzen und Mengen, die verarbeitet werden sollen, erstellen.  

### <a name="2-create-an-inventory-pick"></a><a name="2-create-an-inventory-pick"></a>2: Eine Lagerbestandkommissionierung erstellen

Auf der Seite **Lagerbestandskommissionierung** ruft der Lagermitarbeiter die Herkunftsbelegzeilen im Pull-Verfahren ab. Oder die Kommissionierzeilen wurden bereits, im Push-Verfahren, von dem Benutzer erstellt, der für den Herkunftsbeleg verantwortlich ist.  

### <a name="3-post-an-inventory-pick"></a><a name="3-post-an-inventory-pick"></a>3: Eine Lagerbestandskommissionierung buchen

In jeder Zeile für Artikel, die kommissioniert oder umgelagert wurden, sei es teilweise oder vollständig, füllen Sie das Feld **Menge** aus und buchen Sie dann die Lagerbestandskommissionierung. Herkunftsbelege, die mit der Kommissionierung verknüpft sind, werden als geliefert oder verbraucht gebucht.  

Für Bestandskommissionierungen werden negative Artikelposten erstellt, es werden Lagerposten erstellt, und die Kommissionieranforderung wird gelöscht, wenn sie vollständig bearbeitet ist. Beispielsweise wird das Feld **Menge versendet** auf der Zeile des ausgehenden Herkunftsbelegs aktualisiert. Ein Beleg der gebuchten Lieferung wird erstellt, der beispielsweise den Verkaufsauftrag und die gelieferten Artikel angezeigt.  

## <a name="advanced-warehouse-configurations"></a><a name="advanced-warehouse-configurations"></a>Erweiterte Lagerhauskonfigurationen

Das folgende Diagramm zeigt die ausgehenden Lagerprozesse für verschiedene Belegtypen bei der erweiterten Lagerkonfiguration an. Die Nummern im Diagramm entsprechen den Schritten in den Abschnitten, die dem Diagramm folgen.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Zeigt die Schritte in einem erweiterten ausgehenden Lagerfluss.":::

### <a name="1-release-a-source-document-1"></a><a name="1-release-a-source-document-1"></a>1: Ein Herkunftsbeleg freigeben

Das Freigeben eines Herkunftsbelegs in erweiterten Konfigurationen bewirkt dasselbe wie bei Basiskonfigurationen. Die Artikel werden für die Bewegung im Lager verfügbar. Sie können beispielsweise einer Sendung beigelegt werden.  

### <a name="2-create-a-warehouse-shipment"></a><a name="2-create-a-warehouse-shipment"></a>2: Erstellen Sie einen Warenausgang

Rufen Sie auf der Seite **Warenausgang** die Zeilen aus dem veröffentlichten Herkunftsbeleg ab. Sie können Zeilen aus mehreren Herkunftsbelegen in einer Warenausgabe zusammenfassen.  

### <a name="3-create-a-warehouse-pick"></a><a name="3-create-a-warehouse-pick"></a>3: Erstellen Sie eine Lagerkommissionierung

Erstellen Sie auf der Seite **Warenausgang** Lagerkommissionierungsaktivitäten für Warenausgänge auf eine von zwei Arten:

- Im Push-Verfahren, bei dem Sie die Aktion **Kommissionierung erstellen** verwenden. Wählen Sie die zu kommissionierenden Zeilen und bereiten Sie die Kommissionierungen vor, indem sie beispielsweise angeben, aus welchen Lagerplätzen entnommen und in welche Lagerplätze eingelagert wird, und wie viele Einheiten bewegt werden. Die Lagerplätze können für den Lagerort oder die Ressource vordefiniert werden.
- Im Pull-Verfahren, bei dem Sie die Aktion **Freigeben** verwenden. Auf der Seite **Kommissionierungsarbeitsblatt** können Lagermitarbeiter die Aktion **Lagerdokumente abrufen** verwenden, um ihre zugewiesenen Kommissionierungen abzurufen. Wenn die Kommissionierungen vollständig erfasst sind, werden die Zeilen im **Kommissionierarbeitsblatt** gelöscht.

### <a name="4-register-a-warehouse-pick"></a><a name="4-register-a-warehouse-pick"></a>4: Eine Lagerkommissionierung erfassen

Auf der Seite **Lagerkommissionierung** füllt ein Lagermitarbeiter das Feld **Menge** für jede Zeile aus, die sie vollständig oder teilweise kommissioniert haben, und erfasst dann die Kommissionierung.

Lagerplatzposten werden erstellt, und die Kommissionierungszeilen werden gelöscht, wenn die vollständige Menge kommissioniert wurde. Der Kommissionierungsbeleg bleibt offen, bis die gesamte Menge des Warenausgangs erfasst ist. Das Feld **Abgerufene Menge** auf den Warenausgangszeilen wird entsprechend aktualisiert.  

### <a name="5-post-the-warehouse-shipment"></a><a name="5-post-the-warehouse-shipment"></a>5: Den Warenausgang buchen

Wenn alle Artikel in dem Warenausgangsbeleg als kommissioniert erfasst sind, bucht der Lagermitarbeiter den Ausgang. Durch das Buchen werden die Artikelposten aktualisiert, um die Verringerung des Lagerbestands widerzuspiegeln. Beispielsweise wird das Feld **Menge versendet** auf der Zeile des ausgehenden Herkunftsbelegs aktualisiert.  

## <a name="see-also"></a><a name="see-also"></a>Weitere Informationen

[Logistik](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
