---
title: "So geht es: Fertigungsstècklisten herstellen | Microsoft Docs"
description: "In einer Fertigungsstückliste sind Stammdaten enthalten, mit denen die Komponenten und Unterbaugruppen beschrieben werden, die bei der Fertigung eines übergeordneten Artikels verwendet werden. Sobald ein Fertigungsauftrag für diesen übergeordneten Artikel erstellt wurde, wird über die entsprechende Fertigungsstückliste die Berechnung des Materialbedarfs gesteuert, die im Fenster **Prod. Bestellkomponenten** dargestellt wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e56c6d07bcb501e3e461c9b16a6b5be8e2b68834
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="create-production-boms"></a>Fertigungsauftrag erstellen
In einer Fertigungsstückliste sind Stammdaten enthalten, mit denen die Komponenten und Unterbaugruppen beschrieben werden, die bei der Fertigung eines übergeordneten Artikels verwendet werden. Sobald ein Fertigungsauftrag für diesen übergeordneten Artikel erstellt wurde, wird über die entsprechende Fertigungsstückliste die Berechnung des Materialbedarfs gesteuert, die im Fenster **Prod. Bestellkomponenten** dargestellt wird.

[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt auch Montagestücklisten. Montageaufträge werden für die Produktion von Endartikeln aus Komponenten in einem einfachen Prozess verwendet, der mit einer oder mehreren grundlegenden Ressourcen, die keine Maschinen oder Arbeitsplatzgruppen sind, oder ganz ohne Ressourcen durchgeführt werden kann. Beispielsweise könnte ein Montagevorgang lauten, zwei Weinflaschen und einen Sack Kaffee zu kommissionieren und sie als Geschenkartikel zu verpacken. Weitere Informationen finden Sie im Abschnitt "Montagestücklisten- oder Fertigungsstückliste" im Abschnitt [Mit Stücklisten arbeiten](inventory-how-work-BOMs.md)  

Bevor Sie einen Arbeitsplan erstellen können, muss Folgendes verfügbar sein:  

- Artikelkarten wurden für übergeordnete Artikel erstellt, die an der Fertigung teilnehmen. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).
- Die Ressourcen sind eingerichtet. Weitere Informationen finden Sie unter [Einrichten von Arbeitsplatzgruppen und Arbeitsplätzen](production-how-to-set-up-work-and-machine-centers.md)

## <a name="to-create-a-production-bom"></a>Erstellen Sie eine neue Fertigungsstückliste.  
1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Fertigungsstücklisten** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wenn Sie die Fertigungsstückliste bearbeiten möchten, setzen Sie das Feld **Status** auf **Neu** oder **In Entwicklung**. Um den Arbeitsplan zu aktivieren, setzen Sie das Feld **Status** auf **Zertifiziert**.  

    So füllen Sie die Fertigungsstücklistenzeilen aus
5. Wählen Sie im Feld **Art** aus, ob es sich bei dem Artikel in der Fertigungsstücklistenzeile um einen normalen Artikel oder um eine Fertigungsstückliste handelt. In diesem Fall muss die Fertigungsstückliste bereits als zertifizierte Fertigungsstückliste vorhanden sein.  
6.  Geben Sie im Feld **Nr.** den zu verwendenden Artikel bzw. die zu verwendende Fertigungsstückliste, und wählen Sie sie aus (bzw. geben Sie sie im Feld ein).  
7.  Geben Sie im Feld **Komponentenmenge** ein, wie viele Einheiten des Artikels zum übergeordneten Artikel gehören, z. B. 4 Räder für 1 Auto.  
8.  Im Feld **Ausschuss %** können Sie einen festen Prozentsatz für die Komponenten eingeben, die im Fertigungsvorgang voraussichtlich als Ausschuss anfallen. Sobald die Komponenten in einem freigegebenen Fertigungsauftrag verbraucht werden können, wird dieser Prozentsatz auf einem Produktionsprotokoll im Feld **Verbrauchsmenge** zur erwarteten Menge addiert. Weitere Informationen finden Sie unter [Verbrauch und Ausgabe](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Der Ausschussprozentsatz steht für Komponenten, die während der Fertigung bei der Kommissionierung aus dem Lagerbestand als Ausschuss anfallen, wohingegen der Ausschussprozentsatz in Arbeitsgängen für die als Ausschuss anfallende Istmenge vor der Lageraufnahme steht.  

9.  Geben Sie im Feld **Verbindungscode** einen Code für die Verbindung der Komponente mit einem bestimmten Arbeitsgang ein. Weitere Informationen finden Sie im Abschnitt "Verbindungslinks erstellen im Abschnitt [Routings erstellen](production-how-to-create-routings.md)
10. Wenn Sie aus einer vorhandenen Fertigungsstückliste Zeilen kopieren möchten, klicken Sie auf Aktionen, Funktion, **Fertigungsstückliste kopieren**, um vorhandene Zeilen auszuwählen.  
11.  Überprüfen Sie die Fertigungsstückliste.  
12.  Sie können die neue Fertigungsstückliste an die Karte des betreffenden übergeordneten Artikels anhängen. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Um den Einstandspreis für den Artikel über die Artikelkarte neu zu berechnen, wählen Sie die Aktion **Produktion** und wählen Sie dann **Stückl. Einst.-Preis berechnen** aus.  

## <a name="to-create-a-new-versions-of-a-production-bom"></a>Neue Versionen von Fertigungsstücklisten erzeugen
Neue Versionen von Fertigungsstücklisten werden verwendet, wenn zum Beispiel ein Artikel durch einen anderen Artikel ersetzt wird oder wenn ein Kunde eine spezielle Version des Produkts anfordert. Das Versionsprinzip ermöglicht die Verwaltung verschiedener Versionen einer Fertigungsstückliste. Die Struktur der Fertigungsstücklistenversion entspricht der Struktur der Fertigungsstückliste. Der grundsätzliche Unterschied besteht in der zeitlichen Gültigkeit der Versionen. Die Gültigkeit wird durch das Startdatum definiert.  

Das Startdatum bestimmt den Start der Periode, in welcher die Version gültig ist. In allen anderen Fällen ist das Startdatum ein Filterkriterium für Berechnungen und Prüfungen. Die Fertigungsstücklistenversion ist gültig, bis die nächste Version aufgrund ihres Startdatums gültig wird.  

1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Fertigungsstücklisten** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die zu kopierende Fertigungsstückliste, und wählen Sie die **Versionen** Aktion aus.  
3.  Wählen Sie auf der Registerkarte **Start** in der Gruppe **Neu** die Option **Neu** aus.  
4. Füllen Sie die Felder je nach Bedarf aus.
5. Geben Sie im Feld **Versionscode** eine eindeutige Kennung der Version ein. Beliebige Kombinationen von Ziffern und Buchstaben können verwendet werden.  

    Die neu erstellte Version erhält automatisch den Status **Neu**.
6. Wenn die Stücklistenversion abgeschlossen ist wird der **Status** auf **Zertifiziert** festgelegt.  

Die zeitliche Gültigkeit der Version wird durch das **Startdatum** bestimmt.  

> [!NOTE]  
>  Wählen Sie die Option **Artikel** in **Art**, um einen Artikel aus den Artikelstammdaten in Ihre Fertigungsstückliste zu übernehmen. Wenn der Artikel eine Fertigungsstückliste hat, wodurch das Feld **Fert.-Stücklistennr.** auf der Artikelkarte ausgefüllt wird, wird diese Fertigungsstückliste ebenfalls berücksichtigt.  
>   
>  Wählen Sie die Option **Fertigungsstückliste**, wenn Sie eine Phantomstückliste in der Zeile verwenden möchten.  
>   
>  Phantomstücklisten ermöglichen die Strukturierung des Produkts. Diese Fertigungsstückliste führt niemals zu einem Fertigprodukt, sondern wird ausschließlich zur Ermittlung des abhängigen Bedarfs verwendet. Phantomstücklisten haben keinen Eintrag in den Artikelstammdaten.

## <a name="quantity-calculation-formula-on-production-boms"></a>Mengen-Formel in Fertigungsstücklisten  
Die Menge wird unter Berücksichtigung unterschiedlicher Dimensionen, die ebenfalls in die Zeilen Fertigungsstücklisten eingegeben werden, berechnet. Die Dimensionen beziehen sich auf eine Bestelleinheit des entsprechenden Artikels. Die Länge, Breite, Tiefe und das Gewicht können als Dimensionen eingegeben werden.  

Die Spalten "Formel", "Länge", "Breite", "Tiefe" und "Gewicht" werden nicht angezeigt, da sie nur von wenigen Anwendern benötigt werden. Wenn Sie die Berechnung der Menge verwenden wollen, dann müssen Sie diese Spalten einblenden.  

Die Beziehung der einzelnen Komponenten wird durch die Formel festgelegt. Folgende Möglichkeiten stehen als Formel zur Verfügung:  

-  **Leer** Keine Berücksichtigung der Dimensionen. (Menge = Komponentenmenge)  
-  **Länge:** Menge = Länge x Komponentenmenge  
-  **Länge x Breite** - Menge = Länge x Breite x Komponentenmenge  
-  **Länge x Breite x Tiefe** - Menge = Länge x Breite x Tiefe x Komponentenmenge  
-  **Gewicht**- Menge = Gewicht pro Komponentenmenge  

### <a name="example"></a>Beispiel  
In einer Fertigungsstückliste werden siebzig Metallteile mit den Abmessungen Länge = 0,20 m und Breite = 0,15 m benötigt. Die Werte werden folgendermaßen eingegeben: Formel = Länge * Breite, Länge = 20, Breite = 15, Komponentenmenge = 70. Die Menge ergibt sich aus: Komponentenmenge pro Länge x Breite, dies ergibt, Menge = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also"></a>Siehe auch  
[Routings erstellen](production-how-to-create-routings.md)   
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planung](production-planning.md)   
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

