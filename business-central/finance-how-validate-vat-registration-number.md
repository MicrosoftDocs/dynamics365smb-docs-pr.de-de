---
title: Eine Umsatzsteuer-Identifikationsnummer überprüfen | Microsoft-Dokumentation
description: Eine Umsatzsteuer-Identifikationsnummer überprüfen
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: f4d5023acba2e0cc5600b3f6675c3dcc325489d7
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992225"
---
# <a name="validate-a-vat-registration-number"></a>Eine Umsatzsteuer-Identifikationsnummer überprüfen

## <a name="to-verify-vat-registration-numbers"></a>MwSt-IdNr. prüfen
Es ist wichtig, dass die MwSt-IdNr., die Sie für Debitoren, Kreditoren und Kontakte haben, gültig sind. Beispielsweise ändern Mandanten ihren Steuerschuldstatus, und in einigen Ländern verlangen die Steuerbehörde möglicherweise Berichte, wie der EU-Verkaufsübersichts-Bericht, der die MwsT-IdNr., aufführt, die Sie verwenden, wenn Sie Geschäftsbeziehungen unterhalten.

Die Europäische Berechnung stellt den MwSt Nummern-Überprüfungsdienst auf der Website bereit, der öffentlich und frei ist. [!INCLUDE[d365fin](includes/d365fin_md.md)] kann Ihnen diesen Schritt ersparen und Sie können den VIES-Dienst nutzen, um MwSt. Nummern für Debitoren, Kreditoren und Kontakte direkt vom Debitor, Kreditor und den Kontaktkarten zu prüfen und nachzuverfolgen. Der Service in [!INCLUDE[d365fin](includes/d365fin_md.md)] wird **EU MwSt Reg.Nr. Validierungsservice** genannt. Er ist auf der Seite **Dienstverbindungen** verfügbar, und Sie können ihn sofort nutzen. Der Service ist frei und die Anmeldung ist nicht erforderlich.

Um den **EU-USt-IdNr.-Überprüfungsdienst** zu aktivieren, öffnen Sie den Eintrag auf der Seite **Dienstverbindung**. Das Feld **Dienstendpunkt** sollte bereits ausgefüllt sein. Wenn nicht, können Sie die Aktion **Standardendpunkt festlegen** verwenden. Legen Sie dann das Feld **Aktiviert** fest, und Sie sind startklar.

> [!Note]
> Um den MwSt Reg. Nr. Überprüfungs-Dienst zu aktivieren, müssen Sie Administratorrechte haben.

Wenn Sie unseren Service verwenden, erfassen wir eine Historie der MwSt.-Nummern und Überprüfungen für jeden Debitor, Kreditor oder Kontakt im **MwSt-Registrierungsprotokoll**, damit Sie diese einfacher verfolgen können. Das Protokoll ist auf jeden Debitor zugeschnitten. Beispielsweise ist das Protokoll für die Prüfung hilfreich, dass Sie geprüft haben, dass die aktuelle Mehrwertsteuernummer korrekt ist. Wenn Sie eine Mehrwertsteuernummer überprüfen, spiegelt der **Anforderungs-Bezeichner** im Protokoll, dass Sie Aktionen ausgeführt haben.

Sie finden das USt-Registrierungsprotokoll auf den Karten Debitor, Kreditor oder Kontakt, auf dem Inforegister **Rechnungsstellung**, indem Sie im Feld **USt-ID** die Suchschaltfläche wählen.  

Mit dem Service sparen Sie auch Zeit, wenn Sie einen Kreditor oder Debitor erstellen. Wenn Sie die Umsatzsteuernummer des Debitoren kennen, können Sie sie in das Feld **USt-ID** auf den Karten Debitor oder Kreditor eintragen. Wir tragen den Debitorennamen für Sie ein. Einige Länder liefern auch Mandantenadressen in einem strukturierten Format. In jenen Ländern ergänzen wir auch die Adresse.  

Es gibt mehrere Dinge zu beachten bezüglich dem VIES MwSt Überprüfungsservice:

* Dieser Webdienst verwendet das HTTP-Protokoll, d. h., dass die Daten, die durch den Service übertragen werden, nicht verschlüsselt werden.  
* Sie erfahren möglicherweise Ausfallzeiten für den Service, für die Microsoft nicht verantwortlich ist. Der Service ist Teil eines EU-Netzwerks eines nationalen MwST-Registers.

## <a name="see-also"></a>Siehe auch  
[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)      
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Lokale Funktion in Business Central](about-localization.md)
