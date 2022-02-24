---
title: Problembehandlung mit Selbstregistrierung | Microsoft Docs
description: Erfahren Sie die wichtigsten Gründe, warum Sie möglicherweise nicht in der Lage sind, die Registrierung für Business Central abzuschließen sowie Möglichkeiten, diese zu umgehen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/11/2020
ms.author: edupont
ms.openlocfilehash: 5537bda3e30d6441880479c82faf4797d00aff9a
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527858"
---
# <a name="troubleshooting-self-service-sign-up"></a>Problembehandlungs-Selbstbedienungs-Registrierung
Die Anmeldung für [!INCLUDE[d365fin](includes/d365fin_md.md)] ist einfach und kann sehr schnell vorgenommen werden. Sie können ein freies Konto erstellen, wenn es sich um eine vorhandene Organisation handelt. Dieser Artikel bezieht sich Probleme an, die Sie möglicherweise für die die Anmeldung haben.

## <a name="what-email-address-can-i-use-with-business-central"></a>Welche E-Mail-Adresse kann ich mit Business Central verwenden?
[!INCLUDE[d365fin](includes/d365fin_md.md)] erfordert eine Arbeits- oder Schul-E-Mail-Adresse, um sich anzumelden. [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt keine E-Mail-Adressen, die von E-Mail-Diensten für Endverbraucher oder Telekommunikationsanbietern bereitgestellt werden. Dieses schließt outlook.com, hotmail.com, gmail.com und andere ein.

Wenn Sie versuchen, sich mit einer persönlichen E-Mail-Adresse anzumelden, erhalten Sie eine Nachricht, in der Sie aufgefordert werden, eine Arbeits- oder Schul-E-Mail-Adresse zu verwenden.

## <a name="troubleshooting"></a>Problembehebung
In vielen Fällen kann das Registrieren für [!INCLUDE[d365fin](includes/d365fin_md.md)] mit folgendem Registrierungsprozess erfolgen. Es gibt jedoch verschiedene Gründe, warum Sie möglicherweise nicht in der Lage sind, die Selbstregistrierung abzuschließen. Die folgende Tabelle fasst einige der meisten allgemeinen Ursachen zusammen, die verhindern können, wieso Sie möglicherweise nicht in der Lage sind, die Anmeldung abzuschließen und Arten, wie Sie die diese Probleme umgehen können.

| Symptom / Fehlermeldung | Codes und Problemumgehung |
| --------------------- | -------------------- |
| Für Office 365-E-Mail-Adressen, die nicht in den USA erfasst werden, erhalten Sie eine Meldung wie die Folgende während der Anmeldung:<br /><br />**Das funktioniert nicht, wir unterstützen Ihr Land oder Region nicht.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt derzeit nur Office 365 E - Mail - Konten, die in einer beschränkten Anzahl Märkten erfasst werden. Weitere Informationen finden Sie unter [Regionale Verfügbarkeit](#regional-availability). |
| Persönliche E-Mail-Adressen wie nancy@gmail.com werden nicht unterstützt. Sie erhalten eine Meldung wie die Folgende während der Anmeldung:<br /><br />**Sie haben eine persönliche E-Mail-Adresse eingegeben: Geben Sie die Arbeits-E-Mail-Adresse ein, sodass wir die Daten der Unternehmung speichern können.**<br> Oder <br> **Diese sieht wie eine persönliche E-Mail-Adresse aus. Geben Sie Ihre Arbeitsadresse ein, so können wir Sie mit anderen in Ihrem Unternehmens verknüpfen. Und sorgen Sie sich nicht. Wir geben Ihre Adresse niemandem weiter** |[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt keine E-Mail-Adressen, die von E-Mail-Diensten für Endverbraucher oder Telekommunikationsanbietern bereitgestellt werden. Um die Anmeldung abzuschließen, versuchen Sie eine E-Mail-Adresse zu verwenden, die von Ihrer Arbeit oder Schule zugeordnet ist. Wenn Sie sich immer noch nicht anmelden können und bereit sind, eine erweiterte Einrichtung abzuschließen, können Sie sich für ein neues Probeabonnement des neuen Office 365 anmelden und diese E-Mail-Adresse verwenden, um sich anzumelden. |
| .gov- oder .mil-E-Mail-Adressen: Sie erhalten Sie eine Meldung wie die Folgende für die Anmeldung:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] nicht verfügbar: [!INCLUDE[d365fin](includes/d365fin_md.md)] nicht für Benutzer mit .gov oder .mil-E-Mail-Adressen. Verwenden Sie eine andere Arbeits-E-Mail-Adressen- oder kehren Sie zu einem späteren Zeitpunkt zurück.** <br>Oder <br>**Wir können Ihre Anmeldung nicht beenden. Sie sieht so aus, als ob [!INCLUDE[d365fin](includes/d365fin_md.md)] zurzeit nicht für die Arbeit oder Schule verfügbar ist.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt derzeit keine .gov oder .mil-Adressen. |
| Der Selbstregistrierungsprozess ist nicht aktiviert. Sie erhalten eine Meldung wie die Folgende während der Anmeldung:<br /><br />**Wir können Ihre Anmeldung nicht beenden. Ihre IT-Abteilung hat für die Anmeldung abgeschaltet für [!INCLUDE[d365fin](includes/d365fin_md.md)]. Erkundigen Sie sich bei ihnen, um die Anmeldung zu beenden.** <br>Oder <br> **Diese sieht wie eine persönliche E-Mail-Adresse aus. Geben Sie Ihre Arbeitsadresse ein, so können wir Sie mit anderen in Ihrem Unternehmens verknüpfen. Und sorgen Sie sich nicht. Wir geben Ihre Adresse niemandem weiter** |Der IT-Administrator Ihrer Organisation hat die Selbstregistrierung für [!INCLUDE[d365fin](includes/d365fin_md.md)] deaktiviert. Wenden Sie sich zu Abschließen der Anmeldung an Ihren IT-Administrator und bitten Sie ihn, den Anweisungen auf [dieser Seite](/dynamics365/business-central/dev-itpro/developer/devenv-business-central-manage-selfservice-signups) zu folgen, um vorhandenen Benutzern die Registrierung bei [!INCLUDE[d365fin](includes/d365fin_md.md)] und neuen Benutzern den Beitritt zu Ihrem vorhandenen Mandanten zu erlauben. Möglicherweise haben Sie das selbe Problem, wenn Sie sich bei Office 365 über einen Partner anmeldeten. |
| E-Mail-Adresse ist keine Office 365-ID Sie erhalten eine Meldung wie die Folgende während der Anmeldung:<br /><br />**Wir können Sie nicht im contoso.com finden. Verwenden Sie eine andere ID bei der Arbeit oder an der Schule? Versuchen Sie, sich damit anzumelden, falls dies nicht geht, wenden Sie sich an die IT-Abteilung** |Ihre Organisation verwendet IDs, um sich bei Office 365 und anderen Microsoft-Services anzumelden, die anders sind als Ihre E-Mail-Adresse. Beispielsweise kann Ihre E-Mail-Adresse Nancy.Smith@contoso.com lauten, aber Ihre ID ist nancys@contoso.com. Um die Anmeldung abzuschließen, verwenden Sie die ID, die Ihre Organisation zugewiesen hat, um sich bei Office 365 oder anderen Microsoft-Dienstleistungen anzumelden. Wenn Sie nicht wissen, was das ist, wenden Sie sich an Ihren IT-Administrator. Wenn Sie sich immer noch nicht anmelden können und bereit sind, eine erweiterte Einrichtung abzuschließen, können Sie sich für ein neues Probeabonnement des neuen Office 365 anmelden und diese E-Mail-Adresse verwenden, um sich anzumelden. |
| Wenn Ihr Office 365 Konto bei einem unterstützten Land erfasst ist und Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden, während Sie in einem anderen Land sind, erhalten Sie eine Meldung wie die Folgendes während der Anmeldung:<br /><br />**Das funktioniert nicht, wir unterstützen Ihr Land oder Region nicht.**| Das Office 365 Abonnement Ihrer Organisation ist mit einem bestimmten Land im Verwaltungsportal Office 365 erfasst. Die Anmeldeerfahrung für [!INCLUDE[d365fin](includes/d365fin_md.md)] nutzt die Sprache und das Gebietsschema, die Ihr aktueller Browser verwendet und infolgedessen, können Sie die Fehlermeldung erhalten, obwohl Sie in einem unterstützten Land sind. Fragen Sie Ihren IT-Administrator, das Land zu überprüfen, das im Organisationsprofil im [Office 365 Verwaltungsportal](https://portal.office.com/adminportal/home#/companyprofile) angegeben ist. Sie müssen möglicherweise ein anderes Konto verwenden für [!INCLUDE[d365fin](includes/d365fin_md.md)].|

## <a name="regional-availability"></a>Regionale Verfügbarkeit

[!INCLUDE[prodshort](includes/prodshort.md)] ist in einer Reihe von Ländern oder Regionen mit Lokalisierung verfügbar, die entweder von Microsoft oder einem anerkannten Lokalisierungspartner bereitgestellt wird. Eine vollständige Liste der unterstützten Länder und Regionen finden Sie unter [Verfügbarkeit nach Ländern/Regionen und unterstützte Übersetzungen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  

Eine Übersicht der aktuell unterstützten Märkte für Dynamics 365 insgesamt, finden Sie im Stapel [Internationale Verfügbarkeit von Microsoft Dynamics 365](/dynamics365/get-started/availability). Einen Überblick über die lokalen Funktionen in [!INCLUDE[prodshort](includes/prodshort.md)] finden auf der Angebotsseite [Lokale Funktionen](about-localization.md).  

## <a name="see-also"></a>Siehe auch

[Willkommen bei [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Lokale Funktionalität](about-localization.md)  
[Verfügbarkeit in Ländern/Regionen und unterstützte Übersetzungen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  
[Internationale Verfügbarkeit von Microsoft Dynamics 365](/dynamics365/get-started/availability)  
