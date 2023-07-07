---
title: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen
description: Dieser Artikel beschreibt verschiedene Komplexitätsstufen in Kommissionier- und Versandprozessen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Exemplarische Vorgehensweise: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen

In [!INCLUDE[prod_short](includes/prod_short.md)] kommissionieren und versenden Sie Artikel wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden.

|Art|Ausgangsprozess|Kommissionierung erforderlich|Warenausgang erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Die Kommissionierung und den Versand aus der Auftragszeile buchen|||Keine dedizierte Lageraktivität.|  
|B|Die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg buchen|Aktiviert||Basis: Auftragsbezogene Logistik|  
|U|Die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg buchen||Aktiviert|Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg buchen|Aktiviert|Aktiviert|Erweitert|  

Weitere Informationen finden Sie unter [Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md).

In der folgenden Vorgehensweise wird Methode B in der vorhergegangenen Tabelle beschrieben.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise

Bei Basis-Lagerkonfigurationen gilt Folgendes: Wenn ein Lagerort so eingerichtet wurde, dass Kommissionierung erforderlich ist, jedoch Warenausgang nicht erforderlich ist, verwenden Sie die Seite **Lagerkommissionierung**, um Kommissionier- und Warenausgangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen. Der ausgehende Herkunftsbeleg kann ein Verkaufsauftrag, eine Einkaufsreklamation, ein ausgehender Umlagerungsauftrag, ein Fertigungsauftrag oder ein Komponentenbedarf sein.  

In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

- Einrichten des SÜD-Lagerorts für die Lagerkommissionierung.  
- Erstellen eines Verkaufsauftrags für den Debitor 10000 für 30 AMSTERDAM Lampen.  
- Freigeben des Verkaufsauftrags für Lagerdurchlaufzeit.  
- Erstellen einer Lagerkommissionierung basierend auf einem freigegebenen Herkunftsbeleg.  
- Erfassen der Lagerplatzumlagerung aus dem Lager und gleichzeitig Buchen der Verkaufslieferung für den ursprünglichen Verkaufsauftrag.  

## <a name="roles"></a>Rollen

Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:  

- Lagerortleiter  
- Auftragsverarbeitung  
- Lagermitarbeiter  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a>Hintergrund

Ellen, die Lagermanagerin bei CRONUS, richtet das SÜD-Lager für grundlegende Komissionierungshandlung ein, in dem Lagermitarbeiter ausgehende Aufträge einzeln verarbeiten. Martha, die Verkaufsauftragsbearbeiterin, erstellt einen Verkaufsauftrag für 30 Einheiten des Artikels 1928-S, die dem Debitor 10000 aus dem SÜD-Lager geliefert werden. John, der Lagermitarbeiter muss sicherstellen, dass die Lieferung an den Debitor vorbereitet und geliefert wird. John verwaltet alle beteiligten Aufgaben auf der Seite **Lagerkommissionierung**, das automatisch auf die Lagerplätze verweist, in denen 1928-S gespeichert wird.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a>Einrichten der Lagerplatzcodes

Nachdem Sie den Standort eingerichtet haben, müssen Sie zwei Lagerplätze hinzufügen.

#### <a name="to-setup-the-bin-codes"></a>So richten Sie die Lagerplatzcodes ein

1. Wählen Sie die Aktion **Lagerplätze** aus.
2. Erstellen Sie zwei Lagerplätze mit den Codes *S-01-0001* und *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a>Machen Sie sich selbst zum Lagermitarbeiter am Standort SÜD

Um diese Funktion nutzen zu können, müssen Sie sich selbst dem Lagerort als Lagermitarbeiter hinzufügen. 

#### <a name="to-make-yourself-a-warehouse-employee"></a>So machen Sie sich selbst zum Lagermitarbeiter

  1. Wählen Sie die ![Glühbirne, die zuerst die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
  2. Wählen Sie das Feld **Benutzer-ID** und dann Ihr eigenes Benutzerkonto auf der Seite **Lagermitarbeiter** aus.
  3. Wählen Sie im Feld **Lagerortcode** „SÜD“ aus.  
  4. Wählen Sie das Feld **Standard** und dann die Schaltfläche **Ja** aus.  

### <a name="making-item-1928-s-available"></a>Artikel 1928-S verfügbar machen

Führen Sie die folgenden Schritte aus, um den Artikel LS-1928 SÜD-Standort verfügbar zu machen:  

  1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion als zweite öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Element Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  
  2. Öffnen Sie das Standardjournal, und erstellen Sie dann zwei Artikel Buch.-Blattzeilen mit den folgenden Informationen über das Arbeitsdatum (23. Januar).  

        |Postentyp|Artikelnummer|Lagerortcode|Lagerplatzcode|Menge|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Zugang|1928-S|SÜD|S-01-0001|20|  
        |Zugang|1928-S|SÜD|S-01-0002|20|  

        Das Feld **Lagerplatzcode** in den Verkaufszeilen ist standardmäßig ausgeblendet, daher müssen Sie es anzeigen. Dazu müssen Sie die Seite personalisieren. Weitere Informationen finden Sie unter [So starten Sie die Personalisierung einer Seite über das Banner Personalisierung](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

  3. Wählen Sie **Aktionen**, dann **Buchung** und anschließend die Option **Buchen** aus.  
  4. Wählen Sie die Schaltfläche **Ja** aus.  

## <a name="creating-the-sales-order"></a>Erstellen des Verkaufsauftrags

Verkaufsaufträge sind die häufigste Art des ausgehenden Herkunftsbelegs.  

### <a name="to-create-the-sales-order"></a>Den Verkaufsauftrag erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion als dritte öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Erstellen Sie einen Verkaufsauftrag für den Debitor 10000 auf das Arbeitsdatum (23. Januar) mit den folgenden Verkaufszeilen.  

    |Artikel|Lagerortcode|Menge|  
    |----|-------------|--------|  
    |1928-S|SÜD|30|  

     Fahren Sie fort, das Lager zu informieren, dass die Verkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.  

4. Wählen Sie die Aktion **Freigabe** aus.  

    John fährt fort, die Verkaufsartikel zu kommissionieren und zu liefern.  

## <a name="picking-and-shipping-items"></a>Kommissionierung und Versand von Artikeln

Auf der Seite **Lagerkommissionierung** können Sie alle ausgehenden Lageraktivitäten für einen bestimmten Herkunftsbeleg, wie einen Verkauf, verwalten. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>So kommissionieren Sie Artikel und liefern diese aus

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet viertens.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerkommissionierungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.  

    Stellen Sie sicher, dass das Feld **Nr.** auf dem Inforegister **Allgemein** ausgefüllt ist.
3. Wählen Sie das Feld **Quellendokument** , und wählen Sie **Verkaufsauftrag** aus.  
4. Wählen Sie das Feld **Herkunftsnr.** aus, wählen Sie die Zeile für den Verkauf an Debitor 10000 aus, und wählen Sie dann die Schaltfläche **OK**.  

    Alternativ auf der Registerkarte Aktionen, in der Gruppe Funktion, wählen Sie **Herkunftsbeleg holen** und wählen Sie die Auftrag aus.  
5. Wählen Sie die Aktion **Die zu verarbeitende Menge automatisch ausfüllen**.  

    Alternativ im Feld **Menge zu verarbeiten** geben Sie 10 und 20 jeweils auf den zwei Lagerkommissionierzeilen ein.  
6. Wählen Sie die Aktion **Buchen** und **Versand** und klicken Sie anschließend auf die Schaltfläche **OK**.  

    Die 30 Lautsprecher werden nun erfasst, wie von den Lagerplätzen S-01-0001 und S-01-0002 kommissioniert, und es wird ein negativer Artikelposten erstellt, der gebuchte Verkaufslieferung anzeigt.  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Siehe auch

[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md)  
[Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designdetails: Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md)  
[Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
