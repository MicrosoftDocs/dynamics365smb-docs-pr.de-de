---
title: 'Designdetails: Ausgehender Lagerfluss | Microsoft Docs'
description: "Der ausgehende Fluss in das Lager beginnt mit einer Anforderung der freigegebenen Herkunftsbelege, die Artikel aus dem Lagerort B zu bringen, entweder, um an eine externe Partei oder an einen anderen Unternehmensstandort geliefert zu werden. Vom Lagerbereich werden Lageraktivitäten auf verschiedene Komplexitätsebenen ausgeführt, um die Artikel zu den Lieferdocks zu bringen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 068ed0057b6c12beebfa35951b6c1ffbd6ac556b
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-outbound-warehouse-flow"></a>Designdetails: Ausgehender Lagerfluss
Der ausgehende Fluss in das Lager beginnt mit einer Anforderung der freigegebenen Herkunftsbelege, die Artikel aus dem Lagerort B zu bringen, entweder, um an eine externe Partei oder an einen anderen Unternehmensstandort geliefert zu werden. Vom Lagerbereich werden Lageraktivitäten auf verschiedene Komplexitätsebenen ausgeführt, um die Artikel zu den Lieferdocks zu bringen.  

 Jeder Artikel wird durch einen entsprechenden eingehenden Herkunftsbeleg gekennzeichnet und an diesen angepasst. Die folgenden ausgehenden Herkunftsbelege sind verfügbar:  

- Verkaufsauftrag  
- Ausgehender Umlagerungsauftrag.  
- Einkaufsreklamation  
- Serviceauftrag  

Darüber hinaus behandeln die folgenden internen Herkunftsbelege diese Funktion wie ausgehende Quellen:  

- Fertigungsauftrag mit Komponentenbedarf  
- Montageauftrag mit Komponentenbedarf  

 Die letzten beiden Belege repräsentieren ausgehende Ströme aus dem Lager in interne Betriebsbereiche. Weitere Informationen über die Lagerverarbeitung für interne eingehende und ausgehende Prozesse finden Sie unter [Designdetails: Interner Lagerfluss](design-details-internal-warehouse-flows.md)  

 Prozesse und UI-Belege in ausgehenden Warenflüssen unterscheiden sich in grundlegenden und erweiterten Lagerfunktionen. Der wichtigste Unterschied besteht darin, dass Aktivitäten in der einfachen Logistik Auftrag für Auftrag durchgeführt werden, und in der erweiterten Logistik für mehrere Aufträge konsolidiert werden. Weitere Informationen über verschiedene Lagerkomplexitätsebenen finden Sie unter [Designdetails: Lager-Übersicht](design-details-warehouse-setup.md).  

 In [!INCLUDE[d365fin](includes/d365fin_md.md)] können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.  

|Methode|Eingangsprozess|Lagerplätze|Kommissionierungen|Lieferungen|Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Beitragsentnahme und -Lieferung aus der Auftragszeile|X|||2|  
|F|Buchen Sie die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg||X||3|  
|L|Buchen Sie die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg|||X|4/5/6|  
|T|Buchen Sie die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg||X|X|4/5/6|  

 Die Auswahl eines Ansatzes hängt von den akzeptierten Methoden des Unternehmens und seiner Komplexität ab. In einer Auftrag-für-Auftrag-Umgebung mit einfachen Prozessen und einfacher Lagerplatzstruktur eignet sich Methode A, Kommissionierung und Versand von der Auftragszeile. In anderen Auftrag-für-Auftrag-Unternehmen,, in denen Artikel für einen Auftrag aus mehr als einem Lagerplatz stammen können, oder wo Lagerarbeiter nicht mit Auftragsbelegen arbeiten können, ist die Verwendung separater Kommissionierbelege sinnvoll, Methode B. Wenn der Kommissionier- und Lieferungsprozess eines Unternehmens mehrere Auftragsprozesse und daher mehr Kontrolle erfordert, könnte sich das Unternehmen entscheiden, ein Lagerlieferungsdokument und ein Lagerkommissionierdokument zu verwenden, um die Kommissionierung und die Lieferung voneinander zu trennen, Methoden C und D.  

 In den Methoden werden A, B und C werden die Aktionen der Kommissionierung und der Lieferung in einem Schritt zusammengefasst, wenn der entsprechende Beleg als geliefert gebucht wird. In Methode D wird zuerst die Kommissionierung erfasst, dann wird die Lieferung zu einem späteren Zeitpunkt aus einem anderen Beleg gebucht.  

## <a name="basic-warehouse-configurations"></a>Grundlegende Lagerhauskonfigurationen  
 Das folgende Diagramm zeigt die ausgehenden Lagerflüsse nach Belegtyp im Rahmen der einfachen Logistik an. Die Nummern im Diagramm entsprechen den Schritten in den Abschnitten, die dem Diagramm folgen.  

 ![Ausgehender Fluss in der grundlegenden Lagerfunktion](media/design_details_warehouse_management_outbound_basic_flow.png "Ausgehender Fluss in der grundlegenden Lagerfunktion")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1: Freigeben des Herkunftsbelegs:/Kommissionierung oder Umlagerung erstellen  
 Wenn ein Benutzer, der für Herkunftsbelege zuständig ist, etwa einen Verkaufsauftragsbearbeiter oder ein Produktionsplaner, für die ausgehende Lageraktivität bereit ist, gibt er den Herkunftsbeleg frei, um den Lagermitarbeitern zu signalisieren, dass verkaufte Artikel oder Komponenten kommissioniert und in die angegebenen Lagerplätze eingelagert werden können. Alternativ erstellt der Benutzer im Push-Verfahren Lagerkommissionierungs- oder Umlagerungsdokumente für die einzelnen Auftragszeilen, basierend auf angegebenen Lagerplätzen und zu verarbeitenden Mengen.  

> [!NOTE]  
>  Lagerbestandsumlagerungen werden verwendet, um Artikel in der einfachen Logistik in interne Vorgangsbereiche zu verschieben, basierend auf Herkunftsbelegen oder ad hoc.  

### <a name="2-create-outbound-request"></a>2: Eingehende erwartete Lagerbewegung erstellen  
 Wenn der ausgehende Herkunftsbeleg freigegeben wird, wird eine ausgehende erwartete Lagerbewegung automatisch erstellt. Enthält Referenzen zur Herkunftsbelegart und -Nummer und kann nicht dem Benutzer angezeigt werden.  

### <a name="3-create-inventory-pick-or-movement"></a>3: Lagerbestandskommissionierung oder Umlagerung erstellen  
 Im Fenster **Lagerkommissionierung** oder **Lagerbestandsumlagerung** erhält der Lagermitarbeiter, im Pull-Verfahren, die offenen Herkunftsbelegzeilen basierend auf den eingehenden Lageranfragen. Oder die Kommissionierzeilen wurden bereits, im Push-Verfahren, von dem Benutzer erstellt, der für den Herkunftsbeleg verantwortlich ist.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4: Kommissionierung buchen oder Lagerbestandsumlagerung registrieren  
 In jeder Zeile für Artikel, die kommissioniert oder umgelagert wurden, sei es teilweise oder vollständig, füllt der Lagermitarbeiter das Feld**Menge** aus und bucht die Lagerkommissionierung oder registriert die Lagerbestandsumlagerung. Herkunftsbelege, die mit der Kommissionierung verknüpft sind, werden als geliefert oder verbraucht gebucht. Herkunftsbelege, die mit Lagerbestandsumlagerungen verknüpft sind, werden nicht gebucht.  

 Für Bestandskommissionierungen werden negative Artikelposten erstellt, es werden Lagerposten erstellt, und die Kommissionieranforderung wird gelöscht, wenn sie vollständig bearbeitet ist. Beispielsweise wird das Feld **Menge versendet** auf der Zeile des ausgehenden Herkunftsbelegs aktualisiert. Ein Beleg der gebuchten Lieferung wird erstellt, der beispielsweise den Verkaufsauftrag und die gelieferten Artikel angezeigt.  

## <a name="advanced-warehouse-configurations"></a>erweiterte Lagerhauskonfigurationen  
 Das folgende Diagramm zeigt die ausgehenden Lagerflüsse nach Belegtyp im Rahmen der einfachen Logistik an. Die Nummern im Diagramm entsprechen den Schritten in den Abschnitten, die dem Diagramm folgen.  

 ![Ausgehender Fluss in der erweiterten Lagerfunktion](media/design_details_warehouse_management_outbound_advanced_flow.png "Ausgehender Fluss in der erweiterten Lagerfunktion")  

### <a name="1-release-source-document"></a>1: Freigeben des Herkunftsbelegs  
 Wenn ein Benutzer, der für Herkunftsbelege verantwortlich ist, etwa ein Verkaufsauftragsbearbeiter oder ein Produktionsplaner, für eine ausgehende Lageraktivität bereit ist, gibt er den Herkunftsbeleg frei, um den Lagermitarbeitern zu signalisieren, das verkaufte Artikel oder Komponenten kommissiooniert und in die angegebenen Lagerplätze eingelagert werden können.  

### <a name="2-create-outbound-request"></a>2: Eingehende erwartete Lagerbewegung erstellen  
 Wenn der eingehende Herkunftsbeleg freigegeben wird, wird eine ausgehende erwartete Lagerbewegung automatisch erstellt. Enthält Referenzen zur Herkunftsbelegart und -Nummer und kann nicht dem Benutzer angezeigt werden.  

### <a name="3-create-warehouse-shipment"></a>3: Erstellen Sie einen neuen Warenausgang  
 Im Fenster **Lagerhaus Versand**erhält der Lieferungsmitarbeiter, der verantwortlich ist, die offenen Herkunftsbelegzeilen basierend auf der ausgehenden Lageranfrage. Einige Herkunftsbelegzeilen können zu einem Lieferungsbeleg zusammengefasst werden.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4: Lieferung freigeben/Kommissionierung erstellen  
 Der Versandarbeiter, der verantwortlich ist, gibt den Warenausgang frei, so dass die Lagerarbeiter Kommissionierungen für die jeweilige Lieferung erstellen oder koordinieren können.  

 Oder der Benutzer erstellt Kommissionierungsbelege für einzelne Lieferungszeilen, im Push-Verfahren, basierend auf angegebenen Lagerplätzen und Mengen, die verarbeitet werden sollen.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5: Internen Vorgang freigeben/Kommissionierung erstellen  
 Der Benutzer, der für interne Arbeitsgänge zuständig ist, gibt einen internen Herkunftsbeleg frei, wie einen Produktions- und Montageauftrag, dodass die Lagermitarbeiter Kommissionierungen für den fraglichen internen Vorgang erstellen oder koordinieren können.  

 Oder der Benutzer erstellt Kommissionierungsbelege für einzelne Fertigungs- oder Montageaufträge, im Push-Verfahren, basierend auf angegebenen Lagerplätzen und Mengen, die verarbeitet werden sollen.  

### <a name="6-create-pick-request"></a>6: Kommissionieranforderung erstellen  
 Wenn der ausgehende Herkunftsbeleg freigegeben wird, wird eine Kommissionieranforderung automatisch erstellt. Enthält Referenzen zur Herkunftsbelegart und -Nummer und kann nicht dem Benutzer angezeigt werden. Abhängig von den Einstellungen erstellt der Verbrauch von einem Fertigungs- oder Montageauftrag auch eine eine Kommissionieranforderung, um die erforderlichen Komponenten aus dem Bestand zu kommissionieren.  

### <a name="7-generate-pick-worksheet-lines"></a>7: Kommissioniervorschlagszeilen generieren  
 Der Benutzer, der für das Koordinieren von Kommissionierungen zuständig ist, ruft Kommissionierzeilen im **Kommissioniervorschlag** basierend auf Entnahmeanforderungen von Warenausgängen oder internen Arbeitsgänge mit Komponentenverbrauch ab. Der Benutzer wählt die zu kommissionierenden Zeilen und bereitet die Kommissionierungen vor, indem er angibt, aus welchen Lagerplätzen entnommen und in welche Lagerplätze eingelagert wird, und wie viele Einheiten bewegt werden. Die Lagerplätze können durch Einrichtung des Lagerorts oder der Arbeitsgangsressource vordefiniert werden.  

 Der Benutzer gibt Entnahmemethoden für optimierte Lagerdurchlaufzeit an und verwendet dann eine Funktion, um die entsprechenden Kommissionierungsbelege zu erstellen, die verschiedenen Lagermitarbeitern zugeordnet werden, die Kommissionierungen ausführen. Wenn die Kommissionierungen vollständig zugeordnet sind, werden die Zeilen im **Kommissioniervorschlag**gelöscht.  

### <a name="8-create-warehouse-pick-documents"></a>8: Kommissionierungsbelege erstellen  
 Der Lagermitarbeiter, der die Kommissionierungen ausführt, erstellt im Pull-Verfahren einen Kommissionierungsbeleg auf Grundlages des freigegebenen Herkunftsbelegs. Oder der Kommissionierbeleg wird erstellt und dem Lagermitarbeiter im Push-Verfahren zugeteilt.  

### <a name="9-register-warehouse-pick"></a>9: Kommissionierung registrieren  
 In jeder Zeile für Artikel, die kommissioniert oder umgelagert wurden, sei es teilweise oder vollständig, füllt der Lagermitarbeiter das Feld **Menge** im Fenster **Kommissioniervorschlag** aus und erfasst dann die Lagerbestandsumlagerung.  

 Lagerplatzposten werden erstellt, und die Kommissionierzeilen werden gelöscht, wenn sie vollständig bearbeitet sind. Der Kommissionierbeleg bleibt offen, bis die gesamte Menge des zugehörigen Warenausgangs erfasst ist. Das Feld **Abgerufene Menge** auf den Warenausgangszeilen wird entsprechend aktualisiert.  

### <a name="10-post-warehouse-shipment"></a>10: Warenausgangsübersicht  
 Wenn alle Artikel in dem Warenausgangsbeleg als für die angegebenen Lieferungslagerplätze kommissioniert erfasst sind, bucht der zuständige Versandarbeiter den Warenausgang. Negative Artikelposten werden erstellt. Beispielsweise wird das Feld **Menge versendet** auf der Zeile des ausgehenden Herkunftsbelegs aktualisiert.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Logistik](design-details-warehouse-management.md)

