---
title: Designdetailsg Einehender Lagerfluss | Microsoft Docs
description: "Der eingehende Fluss in ein Lager beginnt, wenn Artikel im Lager des Unternehmensstandorts ankommen, entweder aus externen Quellen oder von einem anderen Standort des Unternehmens. Ein Mitarbeiter registriert die Artikel, normalerweise, indem er einen Barcode scannt. Vom empfangenden Dock werden Lageraktivitäten auf verschiedene Komplexitätsebenen ausgeführt, um die Artikel in den Lagerbereich zu bringen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0ea4ec611a9b66f192a9b311d878591085c31c03
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-inbound-warehouse-flow"></a>Designdetails: Eingehender Lagerfluss
Der eingehende Fluss in ein Lager beginnt, wenn Artikel im Lager des Unternehmensstandorts ankommen, entweder aus externen Quellen oder von einem anderen Standort des Unternehmens. Ein Mitarbeiter registriert die Artikel, normalerweise, indem er einen Barcode scannt. Vom empfangenden Dock werden Lageraktivitäten auf verschiedene Komplexitätsebenen ausgeführt, um die Artikel in den Lagerbereich zu bringen.  

 Jeder Artikel wird durch einen entsprechenden eingehenden Herkunftsbeleg gekennzeichnet und an diesen angepasst. Die folgenden eingehenden Herkunftsbelege sind verfügbar:  

- Einkaufsbestellung  
- Ausgehende Umlagerungsaufträge  
- Verkaufsreklamation  

Darüber hinaus behandeln die folgenden internen Herkunftsbelege diese Funktion wie eingehende Quellen:  

- Fertigungsauftrag mit Ausgabebuchung  
- Montageauftrag mit Ausgabebuchung  

Die letzten beiden repräsentieren eingehende Ströme zum Lager aus internen Betriebsbereichen. Weitere Informationen über die Lagerverarbeitung für interne eingehende und ausgehende Prozesse finden Sie unter [Designdetails: Interner Lagerfluss](design-details-internal-warehouse-flows.md)  

Prozesse und UI-Belege in eingehenden Warenflüssen unterscheiden sich in grundlegenden und erweiterten Lagerfunktionen. Der wichtigste Unterschied besteht darin, dass Aktivitäten in der einfachen Logistik Auftrag für Auftrag durchgeführt werden, und in der erweiterten Logistik für mehrere Aufträge konsolidiert werden. Weitere Informationen über verschiedene Lagerkomplexitätsebenen finden Sie unter [Designdetails: Lager-Übersicht](design-details-warehouse-setup.md).  

In [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die eingehenden Prozesse für das Empfangen und Einlagern auf vier Arten mit verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausführen.  

|Methode|Eingangsprozess|Lagerplätze|Geb. Umlag.-Eingänge|Einlagerungen|Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|X|||2|  
|F|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"|||X|3|  
|L|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg||X||4/5/6|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg||X|X|4/5/6|  

Die Auswahl eines Ansatzes hängt von den akzeptierten Methoden des Unternehmens und seiner Komplexität ab. In einer Auftrag-für-Auftrag-Lagerumgebung, in der die meisten der Lagermitarbeiter direkt mit Auftragsbelegen arbeiten, entscheidet sich ein Unternehmen möglicherweise anschließend, Methode A zu verwenden. Ein Auftrag-für-Auftrag-Lager, das einen komplexeren Einlagerungsprozess hat, oder das dedizierte Lagermitarbeiter hat, um die Lagerverwaltung durchzuführen, könnte sich entscheiden, seine Einlagerungsfunktionen von der Auftragsdokumentmethode B zu trennen. Darüber hinaus kann es für Unternehmen, die die Verarbeitung mehrerer Aufträge planen müssen, nützlich sein, Lagereingangsdokumente, Methoden C und D, zu verwenden.  

In den Methoden werden A, B und C werden die Aktionen des Eingangs und der Einlagerung in einem Schritt zusammengefasst, wenn der entsprechende Beleg als eingegangen gebucht wird. In Methode D wird der Eingang zuerst gebucht, um die Bestandszunahme zu erkennen sowie, dass Artikel zum Verkauf verfügbar sind. Der Lagermitarbeiter registriert die Einlagerung, um Artikel für die Kommissionierung bereitzustellen.  

## <a name="basic-warehouse-configurations"></a>Grundlegende Lagerhauskonfigurationen  
Das folgende Diagramm zeigt die eingehenden Lagerflüsse nach Belegtyp im Rahmen der einfachen Logistik an. Die Nummern im Diagramm entsprechen den Schritten in den Abschnitten, die dem Diagramm folgen.  

![Eingehender Fluss in der grundlegenden Lagerfunktion](media/design_details_warehouse_management_inbound_basic_flow.png "design_details_warehouse_management_inbound_basic_flow")  

### <a name="1-release-source-document--create-inventory-put-away"></a>1. Freigeben des Herkunftsbelegs/Einlagerung erstellen  
Wenn Artikel im Lager erhalten werden, gibt der Benutzer, der für die Lieferung verantwortlich ist, den Herkunftsbeleg frei, etwa eine Bestellung oder einen eingehender Umlagerungsauftrag, um dem Lagerpersonal zu signalisieren, dass die eingegangenen Artikel im Lager eingelagert werden können. Oder der Benutzer erstellt Einlagerungsbelege für einzelne Auftragszeilen, im Push-Verfahren, basierend auf angegebenen Lagerplätzen und Mengen, die verarbeitet werden sollen.  

### <a name="2-create-inbound-request"></a>2: Eingehende erwartete Lagerbewegung erstellen  
Wenn der eingehende Herkunftsbeleg freigegeben wird, wird eine Einlagerungsanforderung automatisch erstellt. Enthält Referenzen zur Herkunftsbelegart und -Nummer und kann nicht dem Benutzer angezeigt werden.  

### <a name="3-create-inventory-put-away"></a>3: Erstellen Sie eine neue Lagereinlagerung  
Im Fenster **Lagereinlagerung** erhält der Lagermitarbeiter im Pull-Verfahren die offenen Herkunftsbelegzeilen basierend auf den eingehenden Lageranfragen. Oder die Einlagerungszeilen wurden bereits, im Push-Verfahren, von dem Benutzer erstellt, der für den Herkunftsbeleg verantwortlich ist.  

### <a name="4-post-inventory-put-away"></a>4: Lagereinlagerungsübersicht  
In jeder Zeile für Artikel, die kommissioniert oder umgelagert wurden, sei es teilweise oder vollständig, füllt der Lagermitarbeiter das Feld **Menge** aus und bucht dann die Lagereinlagerung. Herkunftsbelege, die mit der Einlagerung verknüpft sind, werden als eingegangen gebucht.  

Positive Bestandskommissionierungen sowie Lagerposten werden erstellt, und die Einlagerungsanforderung wird gelöscht, wenn sie vollständig bearbeitet ist. Beispielsweise wird das Feld **Menge empfangen**auf der Zeile des eingehenden Herkunftsbelegs aktualisiert. Ein Beleg des gebuchten Wareneingangs wird erstellt, der beispielsweise die Einkaufsbestellung und die eingegangenen Artikel angezeigt.  

## <a name="advanced-warehouse-configurations"></a>erweiterte Lagerhauskonfigurationen  
Das folgende Diagramm zeigt die eingehenden Lagerflüsse nach Belegtyp im Rahmen der einfachen Logistik an. Die Nummern im Diagramm entsprechen den Schritten in den Abschnitten, die dem Diagramm folgen.  

![Eingehender Fluss in der erweiterten Lagerfunktion](media/design_details_warehouse_management_inbound_advanced_flow.png "design_details_warehouse_management_inbound_advanced_flow")  

### <a name="1-release-source-document"></a>1: Freigeben des Herkunftsbelegs  
Wenn Artikel im Lager erhalten werden, gibt der Benutzer, der für die Lieferung verantwortlich ist, den Herkunftsbeleg frei, etwa eine Bestellung oder einen eingehender Umlagerungsauftrag, um dem Lagerpersonal zu signalisieren, dass die eingegangenen Artikel im Lager eingelagert werden können.  

### <a name="2-create-inbound-request"></a>2: Eingehende erwartete Lagerbewegung erstellen  
Wenn der eingehende Herkunftsbeleg freigegeben wird, wird eine Einlagerungsanforderung automatisch erstellt. Enthält Referenzen zur Herkunftsbelegart und -Nummer und kann nicht dem Benutzer angezeigt werden.  

### <a name="3-create-warehouse-receipt"></a>3: Wareneingang erstellen  
Im Fenster **Wareneingang** erhält der Benutzer, der für den Wareneingang der Artikel verantwortlich ist, die offenen Herkunftsbelegzeilen basierend auf der eingehenden Lageranfrage. Einige Herkunftsbelegzeilen können zu einem Wareneingangsbeleg zusammengefasst werden.  

Der Benutzer füllt das Feld **Verarbeitungsmenge** aus und wählt die empfangende Zone und den Lagerplatz nach Bedarf aus.  

### <a name="4-post-warehouse-receipt"></a>4: Buchen Sie den Wareneingang.  
Der Benutzer bucht den Wareneingang. Positive Artikelposten werden erstellt. Beispielsweise wird das Feld **Menge empfangen**auf der Zeile des eingehenden Herkunftsbelegs aktualisiert.  

### <a name="5-create-warehouse-internal-put-away"></a>5: Erstellen Sie eine neue interne Einlagerungsanforderung  
Der Benutzer, der für die Einlagerung aus internen Vorgängen zuständig ist, erstellt eine interne Einlagerungsanforderung für Artikel, die im Lager eingelagert werden müssen Lager, wie Produktions- oder Montageausstoß. Der Benutzer gibt Menge, Zone und Lagerplatz an, aus denen Artikel eingelagert werden sollen, eventuell mit der Funktion **Lagerplatzinhalt holen**. Der Benutzer gibt die interne Einlagerungsanforderung frei, wodurch eine eingehende erwartete Lagerbewegung erstellt wird, sodass die Aufgabe in Einlagerungsbelegen oder im Einlagerungsarbeitsblatt abgerufen werden kann.  

### <a name="6-create-put-away-request"></a>6: Einlagerungsanforderung  
Wenn der eingehende Herkunftsbeleg gebucht wird, wird eine Einlagerungsanforderung automatisch erstellt. Enthält Referenzen zur Herkunftsbelegart und -Nummer und kann nicht dem Benutzer angezeigt werden. Abhängig von den Einstellungen erstellt die Ausgabe eines Fertigungsauftrags auch eine Einlagerungsanforderung, um die fertigen Artikel im Lagerbestand einzulagern.  

### <a name="7-generate-put-away-worksheet-lines-optional"></a>7: Einlagerungsvorschlagszeilen generieren (optional)  
Der Benutzer, der für das Koordinieren von Einlagerungen zuständig ist, ruft **Einlagerungszeilen** in Einlagerungsvorschlag basierend auf gebuchten Wareneinängen oder internen Arbeitsgängen mit Ausgabe ab. Der Benutzer wählt die einzulagernden Zeilen und bereitet die Einlagerungen vor, indem er angibt, aus welchen Lagerplätzen entnommen und in welche Lagerplätze eingelagert wird, und wie viele Einheiten bewegt werden. Die Lagerplätze können durch Einrichtung des Lagerorts oder der Arbeitsgangsressource vordefiniert werden.  

Wenn alle Einlagerungen geplant und den Lagermitarbeitern zugeteilt sind, erstellt der Benutzer die Einlagerungsbelege. Vollständig zugeordnete Einlagerungszeilen werden aus dem **Einlagerungsvorschlag** gelöscht.  

> [!NOTE]  
>  Wenn das Feld **Einlagerungsvorschlag** auf der Artikelkarte nicht ausgewählt ist, werden Einlagerungsbelege direkt basierend auf den gebuchten Wareneingängen erstellt. In diesem Fall wird Schritt 7 weggelassen.  

### <a name="8-create-warehouse-put-away-document"></a>8: Einlagerungsbeleg erstellen  
Der Lagermitarbeiter, der Einlagerungen ausführt, erstellt im Pull-Verfahren einen Einlagerungsbeleg auf Grundlages des gebuchten Wareneingangs. Oder der Einlagerungsbeleg wird erstellt und dem Lagermitarbeiter im Push-Verfahren zugeteilt.  

### <a name="9-register-warehouse-put-away"></a>9: Wareneingangsverzeichnis  
In jeder Zeile für Artikel, die kommissioniert oder umgelagert wurden, sei es teilweise oder vollständig, füllt der Lagermitarbeiter das Feld **Menge** im Fenster **Kommissioniervorschlag** aus und erfasst dann die Lagerbestandsumlagerung.  

Lagerplatzposten werden erstellt, und die Einlagerungszeilen werden gelöscht, wenn sie vollständig bearbeitet sind. Der Einlagerungsbeleg bleibt offen, bis die gesamte Menge des zugehörigen gebuchten Warenzugangs erfasst ist. Das Feld **Menge eingelagert** auf den Wareneingangsauftragszeilen wird aktualisiert.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Logistik](design-details-warehouse-management.md)

