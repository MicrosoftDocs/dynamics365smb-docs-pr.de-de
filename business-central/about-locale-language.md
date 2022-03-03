---
title: Mehrsprachigkeit und Lokalisierung
description: Erfahren Sie, wie die Sprache und Region die Benutzeroberfläche in Business Central beeinflussen. Um der Benutzeroberfläche die Sprache zu ändern, wechseln Sie zur Seite Meine Einstellungen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture, region, regional settings
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5187d4f98360d7cf43300f86eda9e99dcbda4063
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323136"
---
# <a name="changing-language-and-region"></a>Ändern der Sprache und der Region

[!INCLUDE[prod_short](includes/prod_short.md)] ist in einer Reihe von Märkten und Sprachen auf der ganzen Welt erhältlich. In den Märkten, in denen [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar ist, stehen eine Reihe von regulatorischen Funktionen zur Verfügung, um Unternehmen bei regulatorischen Belastungen zu unterstützen. [!INCLUDE[prod_short](includes/prod_short.md)] kann in verschiedenen Sprachen angezeigt werden, und Sie können die zum Anzeigen von Text verwendete Sprache ändern. Die Änderung tritt sofort in Kraft, sobald Sie automatisch ab- und wieder angemeldet wurden. Die Einstellung trifft auf Sie zu und nicht auf alle in Ihrer Unternehmung.  

Wenn Sie die kanadische Version von [!INCLUDE[prod_short](includes/prod_short.md)] verwenden, können Sie die Benutzeroberfläche in Englisch, Deutsch, Französisch oder in einer anderen Sprache anzeigen, in allen anderen Aspekten ist es jedoch weiterhin die kanadische Version von [!INCLUDE[prod_short](includes/prod_short.md)]. Es ist nicht dasselbe wie, sagen wir [!INCLUDE[prod_short](includes/prod_short.md)] im Vereinigten Königreich, wo die Funktionen an die Anforderungen dieses Marktes angepasst wurden.  

Um der Benutzeroberfläche die Sprache zu ändern, wechseln Sie zur Seite **Meine Einstellungen**. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md#language). 

> [!NOTE]  
> Die Auswahl der Sprachen wird auf Ihre Einstellung in Ihrem Microsoft 365-Profil zurückgesetzt, wenn Ihr Administrator Benutzer von Microsoft 365 mit [!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert.

Die Änderung der Texte in den Daten der Anwendung ist kein Bestandteil der Multilanguagefunktionalität. Dies ist durch das Design der Anwendung bedingt. Beispiele für solche Texte sind die Namen der Artikel oder Bemerkungen für einen Debitor. D. h. diese Textarten werden nicht übersetzt.  

> [!NOTE]  
> Da  [!INCLUDE[prod_short](includes/prod_short.md)] nur einen Zeichensatz für Daten unterstützt. Daher werden einige Zeichen in Ihrer Umgebung möglicherweise nicht unterstützt und beim Abrufen von Daten, die mit einem anderen Zeichensatz eingegeben wurden, können möglicherweise Probleme auftreten. Ihre Umgebung unterstützt möglicherweise nur englische und russische Zeichen, und wenn Sie Daten in einer anderen Sprache eingeben, werden diese möglicherweise nicht ordnungsgemäß gespeichert. Wenden Sie sich an den zuständigen Systemadministrator, und erkundigen Sie sich nach den Sprachen, die von Ihrer Installation für Ihr [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt werden.  

## <a name="changing-your-region-setting"></a>Ändern der Einstellungen für Ihre Region
Die Region unterscheidet sich von der Sprache und von gesetzlichen Vorschriften in den lokalen Märkten. Die Region bestimmt, wie Ihre Daten in Bezug auf das Kommatrennzeichen, die Ausrichtung nach links oder rechts und auf bestimmte andere Einstellungen dargestellt werden. Die Region bestimmt auch einige der Systemelemente im Browser, z. B. die Aktion zum Erstellen eines neuen Artikels in einer Liste.  

Sie können die Region in der Browserregisterkarte ändern, mit der Sie in [!INCLUDE[prod_short](includes/prod_short.md)] arbeiten. Die Änderung bezieht sich nur auf Sie und die nicht die anderer Benutzer in Ihrem Unternehmen.  Die Auswahl der Region wird auf Ihre Einstellung in Ihrem Microsoft 365-Profil zurückgesetzt, wenn Ihr Administrator Benutzer von Microsoft 365 mit [!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert.

> [!IMPORTANT]  
> Wenn Sie die Region ändern, wird eine eine lange Liste von Sprachen und Regionen angezeigt. Die Sprache wird jedoch nicht von der Auswahl der Region beeinflusst.  

Wechseln Sie zur Seite **Meine Einstellungen**, um die Region zu ändern. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).  

## <a name="changing-the-region-setting-for-customers-contacts-and-vendors"></a>Festlegen der Region für Kunden, Kontakte und Kreditor
Einige Unternehmen verwenden einen externen Dienst, der die Adressdaten in ihrem Land oder ihrer Region validiert. Wenn Sie jedoch Adressdaten aktualisieren müssen, ist der strukturierte Ansatz, den diese Dienste verwenden, für manche Szenarien nicht immer das Richtige. Business Central bietet eine flexiblere Möglichkeit zur Eingabe von Adressdaten.

Wenn Sie auf der Seite **Hauptbuchhaltungs-Einrichtung** den Schalter **Länder-/Regionscode in Adresse erforderlich** aktivieren, werden bei Änderungen im Feld **Länder-/Regionscode** bei Adressen für Kunden, Kontakte oder Kreditor die Werte in anderen Adressfeldern zurückgesetzt.

## <a name="application-version"></a>Anwendungsversionen

Auf der Seite **Hilfe und Support** sehen Sie die Version von [!INCLUDE[prod_short](includes/prod_short.md)], auf der Ihr Unternehmen basiert. Wenn Sie ein Unternehmen auf einer anderen Version aufbauen möchten, kann Ihr Administrator eine neue Produktionsumgebung anlegen. Weitere Informationen finden Sie unter [Erstellen einer neuen Produktionsumgebung](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) im Entwickler- und IT Pro-Inhalt.  

## <a name="languages-of-the-prod_short-help"></a>Sprachen der [!INCLUDE[prod_short](includes/prod_short.md)]-Hilfe

Der Hilfeinhalt für die Kernfunktionalität in [!INCLUDE[prod_short](includes/prod_short.md)] wird auf der Microsoft Dokumentenseite veröffentlicht und ist in unterschiedlichen Sprachen verfügbar. Wenn Sie die Dokumente in [!INCLUDE[prod_short](includes/prod_short.md)] öffnen, wird der Inhalt in Ihrer Sprache angezeigt. Wenn eine bestimmte Seite noch nicht in der Sprache verfügbar ist, wird sie in Englisch angezeigt.

### <a name="how-do-i-change-the-language-of-the-microsoft-docs-site"></a>Wie ändere ich die Sprache der Microsoft Dokumentenseite?

Ganz einfach - einen Bildlauf zum unteren Rand der Browserseite ausführen und das Kugelsymbol in der unteren linken Ecke auswählen.

> [!NOTE]  
> Die Liste zeigt alle Sprachen an, die von der Microsoft Dokumentenseite unterstützt werden. [!INCLUDE[prod_short](includes/prod_short.md)] ist in einer begrenzten Anzahl von Ländern/Regionen verfügbar, und die [!INCLUDE [prod_short](includes/prod_short.md)]-Hilfeinhalte sind nicht in allen Sprachen verfügbar, die von der Microsoft Dokumentenseite unterstützt werden.

## <a name="see-also"></a>Siehe auch

[Ressourcen für Hilfe und Support](product-help-and-support.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]