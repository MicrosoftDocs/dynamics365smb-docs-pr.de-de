---
title: Anlagen verwalten
description: 'Erfassen Sie Reparaturen und Wartungen einer Anlage, um deren Wert zu erhalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="maintain-fixed-assets"></a>Anlagen verwalten

Instandhaltungskosten sind Betriebsausgaben für Maßnahmen zur Erhaltung des Zustands Ihrer Anlagen. Im Gegensatz zu Kapitalerhöhungen erhöht die Instandhaltung nicht den Wert Ihrer Anlagen.

Bei jedem Service, der für eine Anlage durchgeführt wird, werden die entsprechenden Daten wie Servicedatum, Kreditorennummer und Telefonnummer der Wartungsfirma erfasst. Sie geben Wartungsinformationen auf mehreren Seiten ein:

* Anlagenkarte
* Bestellung
* Einkaufsrechnung
* Anlagen-Fibu Buch.-Blatt

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Verwenden Sie die Aktion **Anlagen indexieren**, um Wartungskosten neu zu berechnen.

## <a name="record-a-maintenance-cost-directly-on-a-fixed-asset"></a>Wartungskosten für eine Anlage direkt erfassen

Jedes Mal, wenn eine Wartung ausgeführt wurde, wie z. B. ein Servicebesuch, können Sie diese auf der Seite **Wartungsregistrierung** erfassen.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Anlage aus, für die Sie die Wartung übernehmen möchten und wählen Sie dann die Aktion **Wartungsregistrierung** aus.
3. Füllen Sie auf der Seite **Wartungsregistrierung** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Wartungskosten aus einem Anlagen Fibu Buch.-Blatt buchen

1. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Afa-Buch Übersicht** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das AfA-Buch aus, das der Anlage zugewiesen ist, und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Stellen Sie auf der Seite **AfA-Buchkarte** sicher, dass das Kontrollkästchen **Wartung** nicht aktiviert ist, damit Sie keine Wartungskosten im Sachkonto buchen.
4. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.  
5. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus.
6. Wählen Sie im Feld **Anlagenbuchungsart** die **Wartung**.
7. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung einer Wartung eingerichtet wird.

    > [!NOTE]  
    > Schritt 7 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Kto. Wartung** das Sollkonto im Sachkonto und das Feld **Gegenkto. Wartung** enthält das Sachkonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Wählen Sie die Aktion **Buchen**.

## <a name="record-maintenance-cost-from-a-purchase-invoice"></a>Wartungskosten aus einer Einkaufsrechnung erfassen

Anhand der folgenden Schritte wird beschreiben, wie Sie Wartungskosten für eine Anlage aus einer Einkaufsrechnung erfassen. Die Schritte sind für eine Bestellung ähnlich.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie auf dem Inforegister **Zeilen** im Feld **Art** die Option **Anlage** aus.
4. Wählen Sie im Feld **Nr.** die Anlage aus, und geben Sie dann die Menge und die Kosten an.
5. Wählen Sie im Feld **Anlagenbuchungsart** die Option **Wartung** aus.
6. Buchen Sie die Einkaufsrechnung.

## <a name="follow-up-on-service-visits"></a>Servicebesuche verfolgen

Sie können den Bericht **Wartung – Nächster Service** drucken, um die Anlagen aufzulisten, die die ein Service geplant ist. Sie können diesen Bericht auch verwenden, wenn Sie das Feld **Nächstes Servicedatum** auf den Anlagenkarten aktualisieren möchten.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus Symbol. Geben Sie **Wartung Nächste Wartung** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder **Startdatum** und **Enddatum** aus.  
3. Wählen Sie die Schaltfläche **Drucken** oder **Vorschau**.

## <a name="monitor-maintenance-costs"></a>Wartungskosten überwachen

Sie können Statistiken anzeigen, um die Wartungskosten zu überwachen.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage aus, für die Sie die Wartungskosten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.
3. Wählen Sie auf der Seite **Anlagen-AfA-Bücher** das relevante Anlagen-AfA-Buch aus, und dann die Aktion **Statistik**.
4. Klicken Sie zum Öffnen auf der Seite **Anlagenstatistik** auf das Feld **Wartung**.

Verwenden Sie die Seite **Wartungsposten**, um die Posten anzuzeigen, aus denen sich der Betrag im Feld **Wartung** zusammensetzt.

## <a name="view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Wartungskosten für mehrere Anlagen anzeigen oder drucken

Im Bericht **Wartungsanalyse** können Sie auswählen, ob Wartungen basierend auf ein, zwei oder drei Wartungscodes für ein bestimmtes Datum oder ein Datumsintervall überprüft werden sollen. Der Bericht kann die Gesamtsumme für alle ausgewählten Anlagen oder eine Summe für jede einzelne Anlage anzeigen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Wartungsanalyse** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus.
3. Wählen Sie die Schaltfläche **Drucken** oder **Vorschau**.

## <a name="view-maintenance-ledger-entries"></a>Wartungsposten anzeigen

Sie können ausserdem die Wartungskosten erkunden, wenn Sie die Wartungsposten anzeigen.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage aus, für die Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.
3. Wählen Sie auf der Seite **Anlagen-AfA-Bücher** das relevante Anlagen-AfA-Buch aus, und dann die Aktion **Wartungsposten**.

## <a name="view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Wartungsposten für mehrere Anlagen anzeigen oder drucken

Sie können im Bericht **Wartungsdetails** Wartungsposten für eine oder mehrere Anlagen anzeigen oder drucken.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Wartungsdetails** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus.
3. Wählen Sie die Schaltfläche **Drucken** oder **Vorschau**.

## <a name="see-also"></a>Siehe auch

[Anlagen](fa-manage.md)  
[Einrichten von Anlagen](fa-setup.md)  
[Finanzen](finance.md)  
[Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
