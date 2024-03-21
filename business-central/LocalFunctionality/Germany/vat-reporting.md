---
title: MwSt.-Berichterstattung in der deutschen Version
description: MwSt.-Berichte können in der deutschen Version elektronisch an Steuerbehörden übermittelt werden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '11016, 11017, 11019, 11025, 11026, 11027, 11028'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# MwSt.-Berichterstattung in der deutschen Version

Sie können dann das VAT-Dokument an die Schnittstelle des Onlineportals „Elektronische Steuererklärungen (ELSTER)“ der deutschen Finanzämter übermitteln. Sie können eine MwSt-Erklärung als XML-Datei generieren und exportieren und dann direkt an das ELSTER-Portal senden. Weitere Informationen finden Sie unter [Gewusst wie: Einrichten von Umsatzsteuervoranmeldungen](how-to-set-up-and-export-sales-vat-advance-notifications.md).  

Folgende lokale MwSt.-Erklärungen können gedruckt werden:  

|Bericht|Beschreibung|  
|------------|---------------------------------------|  
|**MwSt.-Abrechnung Meldung**|Eine einfache MwSt.-Erklärung. Die MwSt.-Abrechnung erfolgt mithilfe der ELSTER-Funktion. Die Beträge werden nach steuerpflichtiger Basis und steuerpflichtigem Betrag aufgeteilt.<br /><br /> Dient als Basis für die MwSt.-Erfassung für einen ausgewählten Zeitraum und wird gemäß der MwSt.-Abrechnung in der Tabelle MwSt.-Abrechnungszeile gedruckt. Verwenden Sie **Datumstyp der Periode**, um den Datumstyp der Periode anzugeben, ab der MwSt.-Posten in der Stapelverarbeitung erfasst werden. Basierend auf Ihrer Auswahl kann die Aussage basieren auf **Buchungsdatum**, **Belegdatum** oder **MwSt.-Datum**.<br /><br /> Verwenden Sie diesen Bericht in Verbindung mit der MwSt.-Korrekturen.|  
|**UVA Kontennachweis**|Bestätigt, dass Posten im MwSt.-Abrechnungsformular auch in Finanzbuchhaltungskonten gebucht werden.<br /><br /> Wählen Sie zur Überprüfung der MwSt. im Fenster Umsatzsteuervoranmeldung für das MwSt.-Abrechnungsformular und die Umsatzsteuervoranmeldung die gleichen Einstellungen aus.|  
|**MwSt.-Abrechnung Schema**|Diese Erklärung kann auf der Seite **MwSt.-Abrechnung** abgerufen werden.<br /><br /> Druckt die Einstellungen in der MwSt.-Abrechnung. Druckt die Einstellungen in der MwSt.-Abrechnung. Mithilfe des Berichts können die Merkmale von **MwSt Kontennachweis** gedruckt werden.|  

## Siehe auch

[Umsatzsteuervoranmeldungen](how-to-set-up-and-export-sales-vat-advance-notifications.md)  
[Melden von MwSt. an die Steuerbehörden](../../finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](../../finance-work-with-vat.md)  
[Richten Sie Berichte für MwSt ein](how-to-set-up-reports-for-vat-and-intrastat.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
