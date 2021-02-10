---
title: Umsatzsteuer-Identifikationsnummer überprüfen
description: Lassen Sie Business Central den VIES-Service verwenden, um die Umsatzsteuer-Identifikationsnummern automatisch für Sie zu validieren.
author: kielkenny
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 80e955e96a64c5a0bd91d0a72297b32d67ff4ab6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750556"
---
# <a name="validate-vat-registration-numbers"></a>Umsatzsteuer-Identifikationsnummer überprüfen

Es ist wichtig, dass die MwSt-IdNr., die Sie für Debitoren, Kreditoren und Kontakte haben, gültig sind. Beispielsweise ändern Mandanten ihren Steuerschuldstatus, und in einigen Ländern verlangen die Steuerbehörde möglicherweise Berichte, wie der EU-Verkaufsübersichts-Bericht, der die MwsT-IdNr., aufführt, die Sie verwenden, wenn Sie Geschäftsbeziehungen unterhalten.

Die Europäische Berechnung stellt den MwSt Nummern-Überprüfungsdienst auf der Website bereit, der öffentlich und frei ist. [!INCLUDE[prod_short](includes/prod_short.md)] kann Ihnen diesen Schritt ersparen und Sie können den VIES-Dienst nutzen, um MwSt. Nummern für Debitoren, Kreditoren und Kontakte direkt vom Debitor, Kreditor und den Kontaktkarten zu prüfen und nachzuverfolgen. Der Service in [!INCLUDE[prod_short](includes/prod_short.md)] wird **EU MwSt Reg.Nr. Validierungsservice** genannt. Er ist auf der Seite **Dienstverbindungen** verfügbar, und Sie können ihn sofort nutzen. Der Service ist frei und die Anmeldung ist nicht erforderlich.

## <a name="to-verify-vat-registration-numbers"></a>MwSt-IdNr. prüfen

Um den **EU-USt-IdNr.-Überprüfungsdienst** zu aktivieren, öffnen Sie den Eintrag auf der Seite **Dienstverbindung**. Das Feld **Dienstendpunkt** sollte bereits ausgefüllt sein. Wenn nicht, können Sie die Aktion **Standardendpunkt festlegen** verwenden. Legen Sie dann das Feld **Aktiviert** fest, und Sie sind startklar.

> [!NOTE]
> Um den MwSt Reg. Nr. Überprüfungs-Dienst zu aktivieren, müssen Sie Administratorrechte haben.

Wenn Sie unseren Service verwenden, erfassen wir eine Historie der MwSt.-Nummern und Überprüfungen für jeden Debitor, Kreditor oder Kontakt im **MwSt-Registrierungsprotokoll**, damit Sie diese einfacher verfolgen können. Das Protokoll ist auf jeden Debitor zugeschnitten. Beispielsweise ist das Protokoll für die Prüfung hilfreich, dass Sie geprüft haben, dass die aktuelle Mehrwertsteuernummer korrekt ist. Wenn Sie eine Mehrwertsteuernummer überprüfen, spiegelt der **Anforderungs-Bezeichner** im Protokoll, dass Sie Aktionen ausgeführt haben.

Sie finden das USt-Registrierungsprotokoll auf den Karten Debitor, Kreditor oder Kontakt, auf dem Inforegister **Rechnungsstellung**, indem Sie im Feld **USt-ID** die Suchschaltfläche wählen.  

Mit dem Service sparen Sie auch Zeit, wenn Sie einen Kreditor oder Debitor erstellen. Wenn Sie die Umsatzsteuernummer des Debitoren kennen, können Sie sie in das Feld **USt-ID** auf den Karten Debitor oder Kreditor eintragen. Wir tragen den Debitorennamen für Sie ein. Einige Länder liefern auch Mandantenadressen in einem strukturierten Format. In jenen Ländern ergänzen wir auch die Adresse.  

Es gibt mehrere Dinge zu beachten bezüglich dem VIES MwSt Überprüfungsservice:

* Dieser Webdienst verwendet das HTTP-Protokoll, d. h., dass die Daten, die durch den Service übertragen werden, nicht verschlüsselt werden.  
* Sie erfahren möglicherweise Ausfallzeiten für den Service, für die Microsoft nicht verantwortlich ist. Der Service ist Teil eines EU-Netzwerks eines nationalen MwST-Registers.

> [!IMPORTANT]
> Es liegt in Ihrer Verantwortung, die Gültigkeit der Daten zu überprüfen. Gelegentlich werden fehlerhafte Daten vom VIES VAT Number Validation Service zurückgegeben. Wenn die Validierung fehlschlägt, validieren Sie die Umsatzsteuer-Identifikationsnummern auf der [Webseite ](https://ec.europa.eu/taxation_customs/vies/), drucken Sie das Ergebnis aus oder speichern Sie es an einem freigegebenen Speicherort. Fügen Sie dann den Link zum Datensatz für Ihren Debitoren, Kreditoren oder Kontakt hinzu. Weitere Informationen finden Sie unter [Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten](ui-how-add-link-to-record.md).

## <a name="see-also"></a>Siehe auch

[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)  
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Lokale Funktion in Business Central](about-localization.md)  
