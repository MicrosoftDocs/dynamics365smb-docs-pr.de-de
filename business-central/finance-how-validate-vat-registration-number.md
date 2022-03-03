---
title: Umsatzsteuer-Identifikationsnummer überprüfen
description: Lassen Sie Business Central die MwSt.-Registrierungsnummern Ihrer Kontakte, Kunden und Kreditoren validieren, basierend auf dem EU VIES VAT Number Validation Service.
author: andregu
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 249, 575, 1279
ms.date: 06/16/2021
ms.author: andregu
ms.openlocfilehash: fce9a7d934012f3dbd65ee323f881767aeeadd8d
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142133"
---
# <a name="validate-vat-registration-numbers"></a>Umsatzsteuer-Identifikationsnummer überprüfen

Es ist wichtig, dass die MwSt-IdNr., die Sie für Debitoren, Kreditoren und Kontakte haben, gültig sind, wenn Sie [!INCLUDE [prod_short](includes/prod_short.md)] in Ländern verwenden, die MwSt. verwenden. Beispielsweise ändern Mandanten ihren Steuerschuldstatus, und in einigen Ländern verlangen die Steuerbehörde möglicherweise Berichte, wie der **EU-Verkaufsübersichts**-Bericht, der die MwsT-IdNr., aufführt, die Sie verwenden, wenn Sie Geschäftsbeziehungen unterhalten.

Die Europäische Berechnung stellt den MwSt Nummern-Überprüfungsdienst auf der Website bereit, der öffentlich und frei ist. [!INCLUDE [prod_short](includes/prod_short.md)] kann Ihnen diesen Schritt ersparen und Sie können den VIES-Dienst nutzen, um MwSt. Nummern für Debitoren, Kreditoren und Kontakte und andere Unternehmensinformationen nachzuverfolgen. Der Service in [!INCLUDE [prod_short](includes/prod_short.md)] wird **EU MwSt Reg.Nr. Validierungsservice** genannt. Er ist auf der Seite **Dienstverbindungen** verfügbar, und Sie können ihn sofort nutzen. Der Service ist frei und eine zusätzliche Anmeldung ist nicht erforderlich.

## <a name="configure-the-service-to-verify-vat-registration-numbers-automatically"></a>Konfigurieren Sie den Dienst so, dass die Umsatzsteuer-Identifikationsnummern automatisch überprüft werden

Um den **EU-USt-IdNr.-Überprüfungsdienst** zu aktivieren, öffnen Sie den Eintrag auf der Seite **Dienstverbindung**. Wenn das Feld **Dienstendpunkt** noch nicht ausgefüllt ist, verwenden Sie die Aktion **Standardendpunkt festlegen**. Legen Sie dann das Feld **Aktiviert** fest, und Sie sind startklar.  

> [!IMPORTANT]
> Um den Validierungsdienst zu aktivieren, müssen Sie Administratorrechte haben.

Richten Sie optional Vorlagen für die Arten von MwSt.-bezogenen Daten ein, die der Dienst ebenfalls prüfen soll. Weitere Informationen finden Sie unter dem Abschnitt [Validierungsvorlagen](#validation-templates).

Wenn Sie unseren Service verwenden, erfassen wir eine Historie der MwSt.-Nummern und Überprüfungen für jeden Debitor, Kreditor oder Kontakt im **MwSt-Registrierungsprotokoll**, damit Sie diese einfacher verfolgen können. Das Protokoll ist auf jeden Debitor zugeschnitten. Beispielsweise ist das Protokoll für die Prüfung hilfreich, dass Sie geprüft haben, dass die aktuelle Mehrwertsteuernummer korrekt ist. Wenn Sie eine Mehrwertsteuernummer überprüfen, spiegelt der **Anforderungs-Bezeichner** im Protokoll, dass Sie Aktionen ausgeführt haben.

Sie finden das USt-Registrierungsprotokoll auf den Karten Debitor, Kreditor oder Kontakt, auf dem Inforegister **Rechnungsstellung**, indem Sie im Feld **USt-ID** die Suchschaltfläche wählen.  

Es gibt mehrere Dinge zu beachten bezüglich dem VIES MwSt Überprüfungsservice:

* Dieser Webdienst verwendet das HTTP-Protokoll, d. h., dass die Daten, die durch den Service übertragen werden, nicht verschlüsselt werden.  
* Sie erfahren möglicherweise Ausfallzeiten für den Service, für die Microsoft nicht verantwortlich ist. Der Service ist Teil eines EU-Netzwerks eines nationalen MwST-Registers.

> [!IMPORTANT]
> Es liegt in Ihrer Verantwortung, die Gültigkeit der Daten zu überprüfen. Gelegentlich werden fehlerhafte Daten vom VIES VAT Number Validation Service zurückgegeben. Wenn die Validierung fehlschlägt, validieren Sie die Umsatzsteuer-Identifikationsnummern auf der [Webseite ](https://ec.europa.eu/taxation_customs/vies/), drucken Sie das Ergebnis aus oder speichern Sie es an einem freigegebenen Speicherort. Fügen Sie dann den Link zum Datensatz für Ihren Debitoren, Kreditoren oder Kontakt hinzu. Weitere Informationen finden Sie unter [Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten](ui-how-add-link-to-record.md).

## <a name="validation-templates"></a>Validierungsvorlagen

Mit dem VIES-Service können Sie auch andere Unternehmensinformationen wie die Adresse sowie die Umsatzsteuer-Identifikationsnummer überprüfen. Erstellen Sie auf der Seite **USt-IdNr.-Validierungsvorlagen** einen Eintrag für jedes Land, für das Sie eine weitere Validierung erhalten möchten, und geben Sie dann die Informationen an, für die Sie eine automatische Validierung erhalten möchten.  

Fügen Sie beispielsweise einen Eintrag für Spanien hinzu, in dem Sie eine Validierung für Name, Straße, Stadt und Postleitzahl erhalten möchten, und einen weiteren Eintrag für Deutschland, in dem Sie beispielsweise nur eine Validierung für die Postleitzahl wünschen. Legen Sie dann auf der Seite **USt.-ID Validierungsdienst Einrichtung** die Standardvorlage fest.  

> [!NOTE]
> Stellen Sie immer sicher, dass die Standardvorlage Ihren Anforderungen entspricht. Sie können die Standardeinstellung ändern, um sie Ihren Anforderungen anzupassen, z. B. die Validierung für alle Felder oder keine Felder.

Wenn Sie das nächste Mal eine Umsatzsteuer-Identifikationsnummer angeben, überprüft der Service die Nummer und alle zusätzlichen Daten, die in Ihren Validierungsvorlagen festgelegt sind. Wenn sich die angegebenen Werte von den vom Service zurückgegebenen Werten unterscheiden, werden die Details in der Liste **Validierungsdetails** angezeigt, auf der Sie die Werte akzeptieren oder zurücksetzen können.  

## <a name="see-also"></a>Siehe auch

[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)  
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Lokale Funktion in Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
