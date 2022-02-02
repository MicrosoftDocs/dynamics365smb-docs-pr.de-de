---
title: Mehrwertsteuer einrichten
description: Überprüfen Sie, ob Sie die MwSt für Verkäufe und Einkäufe korrekt berechnen, buchen und melden. Es wird empfohlen, dass Sie diesen Einrichtungsleitfaden verwenden, um die MwSt einzurichten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 10, 1877, 470, 471, 472
ms.date: 12/28/2021
ms.author: bholtorf
ms.openlocfilehash: af73c229ec8c9ebb9e530012360ce6baa7495fd8
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972827"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Berechnungen einrichten und Buchungsmethoden für Mehrwertsteuer

Verbraucher und Geschäfte bezahlen Mehrwertsteuer (MwSt), wenn Sie Waren oder Dienstleistungen einkaufen. Der zu bezahlende MwSt-Betrag kann abhängig von verschiedenen Faktoren variieren. In [!INCLUDE[prod_short](includes/prod_short.md)] legen Sie die Sätze fest, die für die Berechnung der Steuerbeträge auf der Grundlage der folgenden Parameter verwendet werden sollen:

* An wen Sie verkaufen  
* Von wem Sie kaufen  
* Was Sie verkaufen  
* Was Sie kaufen  

Sie können die Berechnungen der MwSt manuell einrichten, aber das kann heikel und zeitaufwendig sein. Damit es möglichst einfach ist, stellen wir Ihnen einen Anleitungsfaden **MwSt.-Einrichtung** bereit, der Sie durch die einzelnen Schritte führt. Es wird empfohlen, dass Sie diesen Einrichtungsleitfaden verwenden, um die MwSt einzurichten.

> [!NOTE]  
> Hinweis: Sie können den Leitfaden nur nutzen, wenn Sie eine "Meine Unternehmen" erstellt haben, und keine Transaktionen gebucht haben, die Mehrwertsteuer beinhalten. Sonst wäre es sehr einfach, versehentlich unterschiedliche Mehrwertsteuersätze zu verwenden und mit Mehrwertsteuer verknüpfte Berichte würden ungenau.  

Wenn Sie MwSt-Berechnungen einrichten möchten oder einfach mehr über jeden Schritt erfahren möchten, enthält dieses Thema Beschreibungen jedes Schrittes.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Verwenden der Anleitung zur unterstützten Einrichtung der Mehrwertsteuer, um die Mehrwertsteuer festzulegen (empfohlen)

Es wird empfohlen, dass Sie die unterstützte Einrichtung der MwSt verwenden, um die MwSt in [!INCLUDE[prod_short](includes/prod_short.md)]einzurichten.

Um die unterstützte Einrichtung zu starten, gehen Sie folgendermaßen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Unterstützte Einrichtung** ein.  
2. Wählen Sie **MwSt Einrichtung** aus, und führen Sie die Schritte aus.
3. Wenn Sie die unterstützte Einrichtung abgeschlossen haben, besuchen Sie die Seite **MwSt.-Buchungseinrichtung** und prüfen Sie, ob Sie entsprechend den lokalen Anforderungen in Ihrer Version von [!INCLUDE [prod_short](includes/prod_short.md)] weitere Felder ausfüllen müssen. Weitere Informationen finden Sie unter [Lokale Funktion in Business Central](about-localization.md)  

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Umsatzsteuer-Identifikationsnummern für Ihr Land oder Ihre Region festlegen

Um zu helfen sicherzustellen, dass Personal gültige MwSt-IdNr. eingeben, können Sie die MwSt-IdNr für die Länder oder die Bereiche verwenden, in denen Sie Geschäfte tätigen. [!INCLUDE[prod_short](includes/prod_short.md)] zeigt eine Fehlermeldung an, wenn jemand einen Fehler macht oder ein Format verwendet, das für das Land bzw. die Region falsch ist.

Um MwSt-Nr. einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Länder/Regionen** ein.
2. Wählen Sie das Land bzw. die Region, und wählen die **MwSt Reg. Nr. Formaten** Aktion aus.
3. Im Feld **Formate** definieren Sie das Format, indem Sie einen oder mehrere der folgenden Zeichen eingeben:  

* **#** Erfordert eine einstellige Nummer.  
* **@** Erfordert einen Buchstaben. Bei diesem Format wird nicht zwischen Groß- und Kleinschreibung unterschieden.  
* **?** Erlaubt jegliches Zeichen.  

    > [!Tip]
    > Sie können andere Zeichen verwenden, sofern sie immer im Land- oder Bereichsformat vorkommen. Wenn Sie beispielsweise eine Periode oder einen Bindestrich zwischen und Nummern einfügen möchten, können Sie ##.####.### oder @@-###-### definieren.  

## <a name="set-up-vat-business-posting-groups"></a>MwSt.-Geschäftsbuchungsgruppen festlegen

MwSt.-Geschäftsbuchungsgruppen sollten die Märkte darstellen, in denen Sie Geschäfte mit Debitoren und Kreditoren tätigen, und definieren, wie die Mehrwertsteuer in jedem Zielmarkt berechnet und gebucht werden. Beispiele von MwSt.-Produktbuchungsgruppen sind **Inland** und **Europäischen Union (EU)**.  

Verwenden Sie aussagekräftige Codes, an die Sie sich leicht erinnern können, z. B. **EU** **Nicht-EU** oder **Inland**. Der Code muss eindeutig sein. Sie können beliebig viele Codes einrichten, aber es ist nicht möglich, denselben Code zweimal in einer Tabelle zu verwenden.

Um eine Umsatzsteuer-Buchungsgruppe einzurichten, gehen Sie wie folgt vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Geschäftsbuchungsgrp. ein** und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus.

Sie richten Vorgabe MwSt.-Geschäftsbuchungsgruppen ein, indem Sie sie mit den Geschäftsbuchungsgruppen verbinden. [!INCLUDE[prod_short](includes/prod_short.md)] fügt automatisch die MwSt Geschäftsbuchungsgruppe hinzu, wenn Sie die Geschäftsbuchungsgruppe einem Debitor, Kreditor oder Sachkonto zuweisen.

## <a name="set-up-vat-product-posting-groups"></a>Legen Sie MwSt.-Produktbuchungsgruppen fest

Mithilfe der MwSt.-Produktbuchungsgruppencodes wird die Berechnung und Buchung der MwSt. gemäß der Art des gekauften Artikels oder der Art der verkauften Ressourcen bestimmt.  
Es ist sinnvoll, Codes zu verwenden, an die man sich einfach erinnern kann, und die die Werte, wie **Keine MwSt** oder **Null**, **MwSt** oder **Reduziert** für 10% MwSt beschreiben, und **MwSt 25** oder **Standard** für 25% zu verwenden.

Um eine MwSt.-Geschäftsbuchungsgruppe festzulegen, gehen Sie wie folgt vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Produktbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinieren Sie MwSt.-Buchungsgruppen in MwSt.-Buchungseinrichtungen

[!INCLUDE[prod_short](includes/prod_short.md)] berechnet MwSt.-Beträge in Verkaufs- und Einkaufsberichten basierend auf MwSt.-Buchungsmatrix Einrichtung, die Kombinationen von Mehrwertsteuergeschäfts und -Produktbuchungsgruppen sind. Für jede Kombination können Sie den MwSt.-Prozentsatz, die MwSt.-Berechnungsart und die Sachkontonummern für die Buchung der MwSt. für Verkäufe, Käufe und Erwerbssteuer eingeben. Sie können auch angeben, ob die MwSt. neu berechnet wird, wenn Skonto angewandt oder erhalten wird.  

Sie können beliebig viele Codes einrichten. Wenn Sie MwSt.-Buchungsmatrixeinrichtungen mit ähnlichen Attributen in Gruppen zusammenfassen möchten, können Sie für jede Gruppe ein **MwSt.-Kennzeichen** erstellen und das Kennzeichen dann den Gruppenmitgliedern zuweisen.

Um MwSt.-Buchungseinrichtungen zu kombinieren, gehen Sie folgendermaßen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Buchungseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Weisen Sie VAT-Buchungsgruppen standardmäßig mehreren Entitäten zu

Wenn Sie identische MwSt.-Buchungsgruppen für mehrere Einheiten übernehmen möchten, können Sie [!INCLUDE[prod_short](includes/prod_short.md)] festlegen, um dies standardmäßig durchzuführen. Es gibt mehrere Möglichkeiten, dies zu tun:

* Sie können MwSt.-Geschäftsbuchungsgruppen allgemeinen Geschäftsbuchungsgruppen oder Debitoren- oder Kreditorenvorlagen zuweisen.
* Sie können MwSt.-Produktbuchungsgruppen allgemeinen Produktbuchungsgruppen zuweisen  

Die MwSt- Geschäfts- oder - Produktbuchungsgruppe wird zugewiesen, wenn Sie eine Geschäfts- oder eine Produktbuchungsgruppe für einen Debitor, einen Kreditor, einen Artikel oder eine Ressource auswählen.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Zuweisen von MwSt.-Buchungsgruppen zu Konten, Kunden, Lieferanten, Elementen und Ressourcen

Die folgenden Abschnitten beschreiben, wie die MwSt.-Buchungsgruppen einzelnen Einheiten zugewiesen werden.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>So weisen Sie MwSt.-Buchungsgruppen einzelnen Sachkonten zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnet Sie die **Sachkontokarte** für das Konto.  
3. Wählen Sie im Inforegister **Buchen** im Feld **Buchungsart** entweder **Verkauf** oder **Einkauf** aus.  
4. Wählen Sie die MwSt.-Buchungsgruppen aus, die Sie für das Verkaufs- bzw. das Wareneingangskonto verwenden möchten.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Um MwSt-Geschäftsbuchungsgruppen Debitoren und Kreditoren zuzuweisen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kunde** oder **Kreditor** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Karte **Debitor** oder **Debitor** erweitern Sie das Inforegister **Fakturierung**.  
3. Wählen Sie die MwSt-Geschäftsbuchungsgruppe aus.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Um MwSt-Produktbuchungsgruppen einzelnen Artikeln und Ressourcen zuzuweisen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element** oder **Ressource** ein und wählen Sie dann den zugehörigen Link.  
2. Führen Sie einen der folgenden Schritte aus:  

    * Auf der Karte **Artikel** erweitern Sie das Inforegister **Preis und Buchung**, und wählen Sie dann **Mehr anzeigen**, um das Feld **MwSt Produktbuchungsgruppe** anzuzeigen.  
    * Erweitern Sie auf der Karte **Ressource** das Inforegister **Fakturierung**.  
3. Wählen Sie die MwSt-Produktbuchungsgruppe aus.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Festlegen von Klauseln zur Erläuterung der MwSt.-Befreiung oder von nicht standardmäßigen MwSt.-Sätzen

Sie richten eine MwSt.-Klausel ein, um Informationen über die Art der MwSt. zu beschreiben, die angewendet wird. Die Informationen werden möglicherweise aufgrund behördlicher Regulierungen verlangt. Nachdem Sie eine MwSt.-Klausel festgelegt und sie einer MwSt.-Buchungsmatrix zugeordnet haben, wird die MwSt.-Klausel in allen gedruckten Verkaufsbelegen, die diese MwSt.-Buchungsmatrix Einrichtungsgruppe haben, wie etwa eine Verkaufsrechnung, angezeigt.

Bei Bedarf können Sie auch festlegen, wie Mehrwertsteuerklauseln in andere Sprachen übersetzt werden. Wenn Sie dann für einen Debitor einen Verkaufsbeleg erstellen und ausdrucken, der ein MwSt.-Kennzeichen enthält, enthält der gedruckte Beleg die MwSt.-Klausel in übersetzter Form. Der auf der Kundenkarte angegebene Sprachcode bestimmt die Sprache.

Wenn in verschiedenen Arten von Dokumenten, wie Rechnungen oder Gutschriften, nicht standardisierte Mehrwertsteuersätze verwendet werden, müssen Unternehmen in der Regel einen Freistellungstext (Mehrwertsteuerklausel) einfügen, aus dem hervorgeht, warum ein ermäßigter Mehrwertsteuersatz oder ein Nullsteuersatz berechnet wurde. Sie können je nach Belegart, wie z.B. Rechnung oder Gutschrift, unterschiedliche Mehrwertsteuerklauseln definieren, die in Geschäftsdokumente aufgenommen werden sollen. Sie tun dies bei den **MwSt.-Klauseln nach Belegtyp** Seite.

Sie können eine MwSt.-Klausel ändern oder löschen, und Ihre Änderungen werden in einem generierten Bericht angezeigt. [!INCLUDE[prod_short](includes/prod_short.md)] bewahrt jedoch keinen Verlauf der Änderung auf. In dem Bericht werden die MwSt.-Klauselbeschreibungen für alle Zeilen im Bericht neben dem MwSt.-Betrag und der MwSt.-Bemessungsgrundlage gedruckt und angezeigt. Wenn eine MwSt.-Klausel nicht für eine oder mehrere Zeilen des Verkaufsbelegs festgelegt wurde, wird der gesamte Abschnitt weggelassen, wenn der Bericht gedruckt wird.

### <a name="to-set-up-vat-clauses"></a>Einrichten von MwSt.-Klauseln

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Klauseln** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **MwSt.-Klauseln** erstellen Sie eine neue Zeile.  
3. Geben Sie im Feld **Code** eine Kennung für die Klausel ein. Nutzen Sie diesen Code, um die Klausel der MwSt-Buchungsgruppe zuzuweisen.  
4. Geben Sie im Feld **Beschreibung** den Text für die Mehrwertsteuerbefreiung ein, den Sie für Belege, die Mehrwertsteuer enthalten können, anzeigen möchten. Geben Sie im Feld **Beschreibung 2** bei Bedarf weiteren Text ein. Der Text wird auf neuen Belegzeilen angezeigt.
5. Wählen Sie die Aktion **Beschreibung nach Dokumenttyp**.
6. Über die **MwSt-Klausel von Doc. Typ** Seite, füllen Sie die Felder aus, um festzulegen, welcher MwSt.-Befreiungstext für welche Dokumentart angezeigt werden soll.  
7. Optional: Um die MwSt-Klausel sofort einem Setup für die Mehrwertsteuerbuchung zuzuordnen, wählen Sie **Einrichtung**, und wählen Sie dann die Klausel. Wenn Sie warten möchten, können Sie die Klausel später auf der Seite **MwSt.-Buchungsmatrix** zuordnen.  
8. Optional: Um zu bestimmen wie die Mehrwertsteuerklausel übersetzt wird, wählen Sie die Aktion **Übersetzungen**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>So weisen Sie eine MwSt.-Klausel einer Buchungsgruppe zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Buchungseinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. In der Spalte **MwSt.-Klausel** wählen Sie die Klausel, die für jede MwSt.-Buchungseinrichtung gilt.  

### <a name="to-specify-translations-for-vat-clauses"></a>Um Beschreibungen für Mehrwertsteuerklauseln festzulegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Klauseln** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Übersetzung** aus.  
3. Im **Sprachcode** Feld wählen Sie die Sprache aus, in die Sie übersetzen.  
4. Geben Sie in den Feldern **Beschreibung** und **Beschreibung 2** den Text ein, der eine Übersetzung der Beschreibungen ist. Dieser Text wird in den übersetzten MwSt.-Berichten angezeigt.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Erstellen Sie eine MwSt.-Buchungseinrichtung zur Behandlung der Import-MwSt.

Sie verwenden die Funktion *Import-MwSt.*, wenn Sie einen Beleg buchen müssen, bei dem der gesamte Betrag aus Mehrwertsteuer besteht. Sie sehen dies, wenn Sie eine MwSt.-Rechnung für importierte Waren von der Steuerbehörde erhalten.  

Gehen Sie folgendermaßen vor, um Codes für die Einfuhrsteuerfelder festzulegen:  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Produktbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite MwSt Produktbuchungsgruppe richten Sie eine neue MwSt.-Produktbuchungsgruppen für Einfuhrsteuer ein.  
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Buchungseinrichtung** ein und wählen Sie dann den zugehörigen Link.  
4. Auf der Seite MwSt Buchungseinrichtung erstellen Sie eine neue Zeile oder nutzen einen bestehende MwSt-Buchungsgruppe in Kombination mit der neuen MwSt.-Produktbuchungsgruppe für die Einfuhrsteuer.  
5. Wählen Sie im Feld **MwSt.-Berechnungsart** **Volle MwSt.** aus.  
6. Geben Sie im Feld **Vorsteuerkonto** das Sachkonto an, auf das Sie Einfuhrumsatzsteuer buchen wollen. Alle anderen Konten sind optional.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Verwenden Sie die Erwerbsbesteuerung für den Handel zwischen EU-Ländern oder -Regionen

Gewisse Unternehmen müssen Erwerbssteuer abführen, wenn Sie Handel mit anderen Ländern innerhalb der EU betreiben. Die Regel gilt beispielsweise für Einkäufe aus EU-Ländern/-Regionen und Verkäufe an EU-Länder/-Regionen.  

> [!NOTE]  
> Diese Regel gilt für den Handel mit Unternehmen, die in einem anderen EU-Land/in einer anderen EU-Region als umsatzsteuerpflichtig registriert sind. Wenn Sie direkt mit Verbrauchern in anderen EU-Ländern/-Regionen Geschäfte tätigen, sollten Sie sich bei den Steuerbehörden über die geltenden Regeln für die MwSt. informieren.  

> [!TIP]  
> Sie können überprüfen, ob ein Unternehmen als umsatzsteuerpflichtig registriert ist, wenn Sie den EU-MwSt.ID-Nr. -Überprüfungsdienst verwenden. Der Service ist in [!INCLUDE[prod_short](includes/prod_short.md)] kostenlos verfügbar. Weitere Informationen finden Sie unter [Überprüfen von MwSt.-Registrierungsnummern](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Verkäufe in EU-Länder oder Regionen

Auf Verkäufe an umsatzsteuerpflichtige Unternehmen in anderen EU-Ländern/-Regionen wird keine MwSt. berechnet. Der Wert derartiger Verkäufe an EU-Länder/-Regionen muss separat auf der MwSt.-Abrechnung ausgewiesen werden.  

Um MwSt. bei Verkäufen in EU-Länder/-Regionen korrekt zu berechnen, gehen Sie folgendermaßen vor:  

* Richten Sie eine Zeile für Verkäufe mit den gleichen Informationen ein, wie zuvor für Einkäufe beschrieben. Wenn im Fenster MwSt.-Buchungsmatrix Einrichtung bereits Zeilen für Einkäufe aus EU-Ländern/-Regionen eingerichtet wurden, können Sie diese Zeilen auch für Verkäufe verwenden.  
* Weisen Sie die MwSt.-Geschäftsbuchungsgruppen im Feld **MwSt.-Geschäftsbuchungsgruppe** auf dem Inforegister **Fakturierung** der Debitorenkarte jedes EU-Debitors zu. Sie sollten auch die USt-IdNr. des Debitors im Feld **USt-IdNr.** im Inforegister **Außenhandel** eingeben.  

Wenn Sie einen Verkauf an einen Debitor in einem anderen EU-Land/einer anderen EU-Region buchen, wird der MwSt.-Betrag berechnet und ein MwSt.-Posten mit Informationen zur Erwerbssteuer und zur MwSt.-Bemessungsgrundlage (der zur Berechnung der MwSt. verwendete Betrag) erstellt. Auf die MwSt.-Konten in der Finanzbuchhaltung werden keine Posten gebucht.

## <a name="vat-rounding-for-documents"></a>MwSt.-Rundung für Belege

Beträge in Belegen, die noch nicht gebucht sind, werden gerundet und auf eine Weise angezeigt, die der endgültigen Rundung bereits gebuchter Beträge entspricht. Die MwSt. wird für einen vollständigen Beleg berechnet, d.h., dass MwSt., die in dem Beleg berechnet wird, auf der Summe aller Zeilen mit derselben MwSt.-ID im Beleg basiert.

## <a name="see-also"></a>Siehe auch

[Vorlagen für MwSt.-Abrechnungen und Namen für MwSt.-Abrechnungen festlegen](finance-how-setup-vat-statement.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)  
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Arbeiten mit dem Tool zur Änderung des MwSt.-Satzes](finance-how-use-vat-rate-change-tool.md)  
[Umsatzsteuer-Identifikationsnummern überprüfen](finance-how-validate-vat-registration-number.md)  
[Lokale Funktion in Business Central](about-localization.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
