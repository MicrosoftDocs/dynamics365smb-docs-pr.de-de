---
title: 'Exemplarische Vorgehensweise: Eingang und Einlagerung in Basis-Lagerkonfigurationen'
description: 'Erfahren Sie mehr über die verschiedenen Möglichkeiten, eingehende Prozesse für das Empfangen und Einlagern zu handhaben.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Exemplarische Vorgehensweise: Eingang und Einlagerung in Basis-Lagerkonfigurationen

In [!INCLUDE[prod_short](includes/prod_short.md)] erhalten Sie Artikel und lagern sie, wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden ein.

|Art|Eingangsprozess|Wareneingang erforderlich|Einlagerung erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|||Keine dedizierte Lageraktivität.|  
|B|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"||Aktiviert|Basis: Auftragsbezogene Logistik|  
|U|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg|Aktiviert||Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg|Aktiviert|Aktiviert|Erweitert|  

Weitere Informationen finden Sie unter [Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md).

In der folgenden Vorgehensweise wird Methode B in der vorhergegangenen Tabelle beschrieben.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise

Bei Basis-Lagerkonfigurationen gilt Folgendes: Wenn ein Lagerort so eingerichtet wurde, dass die Bearbeitung der Einlagerung erforderlich ist, die des Wareneingangs jedoch nicht erforderlich ist, verwenden Sie die Seite **Lagereinlagerung**, um Einlagerungs- und Wareneingangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen. Die folgenden Belege sind eingehenden Herkunftsbelege:

* Einkaufsbestellung
* Verkaufsreklamation
* Ausgehende Umlagerungsaufträge
* Produktionsauftrag mit einlagerungsbereitem Ausgang

> [!NOTE]
> Obwohl die Einstellungen **Kommissionierung erforderlich** und **Einlagerung erforderlich** genannt werden, können Sie weiterhin Wareneingänge und Lieferungen direkt aus den Quellgeschäftsunterlagen an Lagerorten, in denen Sie diese Kontrollkästchen aktivieren.  

In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

* Richten Sie den SILBERNEN Lagerort für Lagereinlagerungen ein.  
* Richten Sie den SILBERNEN Lagerort für Lagerplatzbehandlung ein.  
* Definieren Sie einen Standardlagerplatz für Artikel LS-81. (LS-75 ist bereits in CRONUS eingerichtet.)  
* Erstellen Sie eine Bestellung für den Kreditor 10000 für 40 Lautsprecher.  
* Überprüfen Sie, dass Lagerplätze der Einlagerung durch Einrichtung voreingestellt werden.  
* Geben Sie die Bestellung für Lagerdurchlaufzeit frei.  
* Erstellen Sie eine Lagereinlagerung basierend auf einem freigegebenen Herkunftsbeleg.  
* Überprüfen Sie, dass Lagerplätze der Einlagerung von der Einkaufsbestellung übernommen werden.  
* Erfassen Sie die Lagerplatzumlagerung in das Lager und Buchen der Einkaufslieferung für die ursprüngliche Einkaufsbestellung.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a>Rollen

Die folgenden Benutzerrollen führen die Aufgaben durch, die in dieser exemplarischen Vorgehensweise demonstriert werden:  

* Lagerortleiter  
* Einkäufer  
* Lagermitarbeiter  

## <a name="prerequisites"></a>Voraussetzungen

Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

* CRONUS International Ltd.-Daten  
* Ein Lagermitarbeiter am Lagerort SILVER zu sein. Sich selbst einzurichten Einrichten, führen Sie die folgenden Schritte aus:  

    1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
    2. Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr Benutzerkonto auf der Seite **Benutzer** aus.  
    3. Wählen Sie im Feld **Lagerortcode** **SILVER** ein.  
    4. Aktivieren Sie das Kontrollkästchen **Standard**.  

## <a name="story"></a>Hintergrund

Ellen, die Einkäuferin bei der CRONUS AG ist, erstellt eine Bestellung für 10 Einheiten des Artikels LS-75 und 30 Einheiten des Artikels LS-81 von dem Kreditor 10000, um zum SILVER-Lagerhaus geliefert zu werden. Wenn die Lieferung im Lager eingeht, lagert John, der Lagermitarbeiter, die Artikel in die Standardlagerplätze ein, die für die Artikel eingerichtet sind. Wenn John Einlagerungen bucht, werden die Artikel gebucht als im Lager erhalten und verfügbar zum Verkauf oder anderen Bedarf.  

## <a name="setting-up-the-location"></a>Einrichten des Lagerorts

Einstellungen auf der Seite **Lagerortkarte** definieren die Warenflüsse des Unternehmens.  

### <a name="to-set-up-the-location"></a>So richten Sie den Standort ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie die Karte für den Standort SILVER.  
3. Aktivieren Sie den Schalter **Einlagerung erforderlich**.  

    Richten Sie einen Vorgabelagerplatz für die beiden Artikelnummern ein, um zu steuern, wo sie eingelagert werden.  

4. Wählen Sie die Aktion **Lagerplätze** aus.  
5. Wählen Sie die erste Zeile, für den Lagerplatz **S-01-0001**, und wählen die **Inhalt**-Aktion aus.  

    Beachten Sie auf der Seite **Lagerplatzinhalt**, dass der Artikel **LS-75** bereits als Inhalt im Lagerplatz S-01-0001 eingerichtet wurde.  

6. Wählen Sie die Aktion **Neu** aus.  
7. Wählen Sie die Felder **Fest** und **Standard** .  
8. Geben Sie im Feld **Belegnr.** den Wert **LS-81** ein.  

## <a name="create-the-purchase-order"></a>Die Einkaufsbestellung erstellen

Bestellungen sind die häufigste Art des eingehenden Herkunftsbelegs.  

### <a name="to-create-the-purchase-order"></a>Bestellung erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Erstellen Sie eine Bestellung für den Kreditor 10000 auf das Arbeitsdatum (23. Januar) mit den folgenden Einkaufszeilen.  

    |Artikel|Lagerortcode|Lagerplatzcode|Menge|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|SILBER|S-01-0001|10|  
    |LS-81|SILBER|S-01-0001|30|  

    > [!NOTE]  
    > Der Lagerplatzcode wird automatisch gemäß der Einrichtung eingegeben, die Sie im [Aufstellung Lagerort](#setting-up-the-location)-Abschnitt erstellt haben.  

    Als Nächstes informieren Sie das Lager, dass die Einkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.  

4. Wählen Sie die Aktion **Freigabe** aus.  

    Der Warenausgang von Lautsprechern vom Kreditoren 10000 ist im SILBERNEN Lager eingetroffen, und John fährt fort, um sie einzulagern.  

## <a name="receive-and-put-the-items-away"></a>Artikel erhalten und einlagern

Verwenden Sie die Seite **Lagereinlagerung** , um alle eingehenden Lageraktivitäten für einen bestimmten Herkunftsbeleg, wie einen Einkauf, zu verwalten.  

### <a name="to-receive-and-put-the-items-away"></a>Artikel erhalten und einlagern

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagereinlagerungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie das Feld **Herkunftsdokument** , und wählen Sie **Einkaufsauftrag** aus.  
4. Wählen Sie das Feld **Herkunftsnr.** aus, wählen Sie die Zeile für den Einkauf von Kreditor 10000 aus, und wählen Sie dann die Schaltfläche **OK**.  

    Alternativ können Sie auch die Aktion **Quellbeleg holen** wählen und dann die Bestellung auswählen.  

5. Wählen Sie die Aktion **Die zu verarbeitende Menge automatisch ausfüllen**.  

    Alternativ im Feld **Menge zu verarbeiten** geben Sie 10 und 30 jeweils auf den zwei Lagerkommissionierzeilen ein.  

6. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Lieferung und Rechnung**, und wählen Sie dann die Schaltfläche **OK** aus.  

    Die 40 Lautsprecher werden nun erfasst, wie von den Lagereinlagerungsplätzen S-01-0001 kommissioniert, und ein positiver Artikelposten wird, die gebuchte Einkaufslieferung reflektierend, erstellt.  

## <a name="see-also"></a>Siehe auch

[Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md)  
[Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designdetails: Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md)  
[Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
