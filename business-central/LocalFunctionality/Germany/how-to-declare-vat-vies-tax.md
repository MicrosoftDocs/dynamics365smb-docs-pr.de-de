---
title: 'Wie Sie die MwSt-VIES-Erklärung erstellen [DE]'
description: 'So erstellen Sie den MwSt.-VIES-Erklärungsbericht, um Informationen über Verkaufstransaktionen mit anderen Ländern/Regionen der Europäischen Union (EU) zu senden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/18/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="declare-vat-vies-tax-in-the-german-version"></a>MwSt-VIES-Steuererklärung in der deutschen Version

[!INCLUDE[prod_short](../../includes/prod_short.md)] enthält den **EU-Verkaufsübersicht**-Bericht, mit dem Sie Informationen zu Verkaufstransaktionen mit anderen Ländern oder Regionen innerhalb der Europäischen Union (EU) an das System der Zoll- und Steuerbehördenlisten übermitteln können. Im Bericht werden Informationen in dem Format angezeigt, das auch in der Erklärungsliste der Zoll- und Steuerbehörden verwendet wird.  

Abhängig vom Volumen der verkauften Waren oder Dienstleistungen an andere EU-Länder/Regionen, müssen Sie monatliche, zweimonatliche oder vierteljährliche Meldungen senden. Hat das Unternehmen Verkäufe von mehr als 100.000 Euro pro Quartal, müssen Sie eine monatliche Meldung senden. Hat das Unternehmen Verkäufe von weniger als 100.000 Euro pro Quartal, müssen Sie eine monatliche Meldung senden. Weitere Informationen finden Sie unter [BZSt-Website](https://go.microsoft.com/fwlink/?LinkId=204368).  

Der Bericht basiert auf Daten in der Tabelle "MwSt.-Posten".  

## <a name="to-declare-vat-vies-tax"></a>So erstellen Sie eine zusammenfassende Meldung

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **VAT-VIES Zusammenf. Meldung – Formular – DE** ein und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie auf der Seite **Zusammenf. Meldung MwSt-Vies-Formular** im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Meldezeitraum**|Geben Sie den Zeitraum an, den der Bericht umfasst. Dies kann ein Monat, eine zweimonatige Periode, ein Quartal oder das Kalenderjahr sein.|  
    |**Datum der Unterschrift**|Dient zum Eingeben des Datums, an dem die MwSt-VIES-Erklärung gesendet wird.|  
    |**Berichtigte Anmeldung**|Ein Häkchen im Kontrollkästchen bedeutet, dass es sich um eine korrigierte Fassung einer bereits abgegebenen zusammenfassenden MwSt-VIES-Erklärung handelt.|  
    |**Beträge in Berichtswährung ausgeben**|Gibt an, ob die ausgewerteten Beträge in der zusätzlichen Berichtswährung angezeigt werden. Weitere Informationen finden Sie unter zusätzliche Berichtswährung.|  
    |**Auf monatliche Meldung umstellen**|Wenn es ausgewählt wird, hat Ihr Unternehmen Verkäufe von mehr als 100.000 Euro pro Quartal und Sie müssen von einem Quartalsbericht zu einem monatlichen Bericht migrieren. **Wichtig:** Wählen sie nur dieses Feld aus, wenn Sie zum ersten Mal einen monatlichen Bericht senden.|  
    |**Monatliche Meldung widerrufen**|Wird dieses Kontrollkästchen aktiviert, wollen Sie vom monatlichen Bericht zu einem anderen Meldezeitraum wechseln.<br /><br /> Wenn Sie beispielsweise zuvor monatliche Erklärungen eingereicht haben, aber die EU-Umsätze weniger als 100.000 Euro pro Quartal betragen, wählen Sie das Feld und wählen Sie anschließend eines der Quartale im **Meldezeitraum** aus.|  

3.  Wählen Sie im Inforegister **MwSt.-Abrechnungszeile** die entsprechenden Filter aus.  

    > [!NOTE]  
    >  Um diesen Bericht ausführen, müssen Sie das **Buchungsdatum** als Filter auswählen und den Wert des Buchungsdatums eingegeben.  

## <a name="see-also"></a>Weitere Informationen

[MwSt.-Abrechnung](vat-reporting.md)  
[Melden von MwSt. an die Steuerbehörden](../../finance-how-report-vat.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
