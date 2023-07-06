---
title: Eine MwSt.-Abrechnung einrichten
description: 'In diesem Thema erfahren Sie, wie Sie eine MwSt.-Abrechnungsvorlage und die Namen der MwSt.-Abrechnungen festlegen, um den sich ändernden Anforderungen der Steuerbehörden gerecht zu werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="set-up-vat-statement-templates-and-vat-statement-names"></a><a name="set-up-vat-statement-templates-and-vat-statement-names"></a><a name="set-up-vat-statement-templates-and-vat-statement-names"></a>Vorlagen für Umsatzsteuerabrechnungen und Namen von Umsatzsteuerabrechnungen einrichten

Steuerbehörden kann Anforderungen für die Buchung der MwSt ändern und ändert diese auch. Vorlagen für Umsatzsteuerbescheinigungen und Namen von Umsatzsteuerbescheinigungen können Ihnen helfen, sich auf bevorstehende Änderungen vorzubereiten und einen reibungslosen Übergang zu den neuen Anforderungen zu schaffen. Sie können MwSt.-Abrechnungsvorlagen verwenden, um verschiedene Berichte einzurichten, wenn Sie die Abrechnung drucken möchten. Jede MwSt.-Abrechnungsvorlage kann mehrere MwSt.-Abrechnungsnamen haben, die wiederum die Berechnungen definieren, und Sie können einen neuen MwSt.-Abrechnungsnamen erstellen, wenn sich die Anforderungen ändern. Beispielsweise kann ein Name die MwSt für dieses Jahr basierend auf dem aktuellen Bedarf berechnen, und ein anderer Name kann die MwSt basierend auf Anforderungen für das nächste Jahr berechnen. Namen sind auch eine Art, Aufzeichnungen von MwSt.-Abrechnungsformaten zu behalten, beispielsweise damit Sie prüfen können, wie Sie die MwSt in vorherigen Jahren berechnet haben.

## <a name="to-define-a-vat-statement"></a><a name="to-define-a-vat-statement"></a><a name="to-define-a-vat-statement"></a>So definieren Sie eine Umsatzsteuerabrechnung

MwSt.-Abrechnungen lassen Sie den MwSt.-Abrechnungsbetrag für eine bestimmte Periode berechnen (zum Beispiel ein Quartal).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MWSt.-Abrechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das Feld **Name**, und wählen Sie dann **Neu** auf der Seite **MwSt.-Abrechnungsnamen** aus.
3. Füllen Sie die entsprechenden Felder aus. Normalerweise möchten Sie eine Einstellung für jede Kombination aus MwSt.-Geschäftsbuchungsgruppe / MwSt.-Produktbuchungsgruppe haben. Für Zeilennummern ist es sinnvoll, gleichwertige Nummern oder Codes wie in Ihrer offiziellen MwSt.-Abrechnung zu verwenden [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Sie können die Informationen setzen, die in der Abrechnung enthalten sind, je nachdem, was Sie im Feld **Art** auswählen. **Kontosumme** ist hilfreich, wenn Sie die MwSt von einem bestimmten Konto möchten.
**MwSt.-Summe** ruft die MwSt der Konten ab, die zur Auswahl auf **Buchungsart**, **VAT Bus. Buchungsgruppe** und/oder den Feldern **VAT Prod. Buchungsgruppe** zugeordnet werden. **Rubrikensumme** ermöglicht Ihnen die Eingabe von einem schnellen Filterkriterium oder Wert im Feld **Rubrikensumme**. Weitere Informationen finden Sie unter [Suchen, filtern und sortieren von Daten](ui-enter-criteria-filters.md). **Beschreibung** ist oft verwendet, um eine Benachrichtigung der Abrechnung hinzuzufügen. Sie könnten sie beispielsweise als Überschrift verwenden, wenn Sie Zeilenzusammenzählung verwendet haben.

## <a name="to-preview-the-vat-statement"></a><a name="to-preview-the-vat-statement"></a><a name="to-preview-the-vat-statement"></a>So zeigen Sie eine Vorschau der Mehrwertsteuerabrechnung an

Nachdem Sie eine MwSt.-Abrechnung eingeben haben, können Sie diese in der Vorschau anzeigen, um sicherzustellen, dass sie die Anforderungen erfüllt.
> [!Tip]
> Es wird empfohlen, einen Abschnitt in der MwSt.-Abrechnung mit **Typ** **MwSt.-Posten insgesamt** zu haben und einen weiterer Abschnitt unten mit **Typ** **Konto – insgesamt** zu haben, um die Beträge basierend auf der Tabelle **MwSt.-Posten** im Vergleich zum Betrag in **Sachkonten** abzugleichen. Sie können auch den Bericht **Fibu – MwSt.Abstimmung** für diesen Zweck verwenden.

1. Wählen Sie **Vorschau** aus.
2. Geben Sie einen Datumsfilter ein, um die Abrechnung auf einen bestimmten Zeitraum zu begrenzen. Weitere Informationen darüber, wie die Seite anpassen, damit der Datumsfilter angezeigt wird, finden Sie unter [Daten suchen, filtern und sortieren](ui-enter-criteria-filters.md).
3. Sie können verschiedene Optionen wählen, um die Art der MwSt.-Posten zu bestimmten, die in der Abrechnung enthalten sein sollen.
4. Für die Zeilen, für die im Feld **Art** der Eintrag **MwSt.-Summe** angezeigt wird, kann eine Übersicht der MwSt.-Posten angezeigt werden, wenn Sie im Feld **Spaltenbetrag** den Betrag auswählen.
5. Sie können Personalisierung verwenden, um weitere Felder in den Posten anzuzeigen. Zum Beispiel die Unrealisierte Bemessungsgrundlage und Unrealisierter MwSt.-Betrag, wenn Sie unrealisierte MwSt. verwenden.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)  
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Lokale Funktion in Business Central](about-localization.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
