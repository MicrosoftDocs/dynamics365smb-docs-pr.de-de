---
title: Mehrsprachig und Lokalisierung| Microsoft Docs
description: Erhalten von Informationen, wie Sprache und Gebietsschema die Benutzeroberfläche in Business Central. beeinflussen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 10/22/2019
ms.author: edupont
ms.openlocfilehash: 81377dfe391415c6922cf0dcf00a8c8567ee4c80
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692704"
---
# <a name="changing-language-and-locale"></a>Sprache und Gebiet ändern

[!INCLUDE[d365fin](includes/d365fin_md.md)] wird in mehreren Märkten unterstützt und ist in den Sprachen verfügbar, die diese Märkte benötigen. Dieses ist ein Ergebnis für Supportleistungen für mehrere Sprachen zu Laufzeit mit Unterstützung für rechtliche Anforderungen in den unterstützten Märkten. Das bedeutet, das [!INCLUDE[d365fin](includes/d365fin_md.md)] in verschiedenen Sprachen angezeigt werden kann. Sie können die Sprache ändern, die verwendet wird, um Texte anzuzeigen und die Änderung tritt sofort in Kraft, sobald Sie automatisch exportiert und wieder unterzeichnet wurde. Die Einstellung trifft auf Sie zu und nicht auf alle in Ihrer Unternehmung.  

Wenn Sie die kanadische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] nutzen, können Sie die Benutzeroberfläche in Englisch und auf französisch sehen, aber es ist immer noch die kanadische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] in allen anderen Aspekten. Es ist nicht gleich wie sagen wir [!INCLUDE[d365fin](includes/d365fin_md.md)] in Großbritannien.  

Um der Benutzeroberfläche die Sprache zu ändern, wechseln Sie zur Seite **Meine Einstellungen**. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md#language).  

Die Änderung der Texte in den Daten der Anwendung ist kein Bestandteil der Multilanguagefunktionalität. Dies ist durch das Design der Anwendung bedingt. Beispiele für solche Texte sind die Namen der Artikel oder Bemerkungen für einen Debitor. D. h. diese Textarten werden nicht übersetzt.  

> [!NOTE]  
> Da  [!INCLUDE[d365fin](includes/d365fin_md.md)] nur einen Zeichensatz für Daten unterstützt. Beim Abrufen von Daten, die unter Verwendung eines anderen Zeichensatzes eingegeben wurden, können daher Fehler auftreten. Wenn Ihr Tenant zum Beispiel nur englische und russische Zeichen unterstützt und Sie Daten in einer anderen Sprache eingegeben, werden diese möglicherweise nicht ordnungsgemäß gespeichert. Wenden Sie sich an den zuständigen Systemadministrator, und erkundigen Sie sich nach den Sprachen, die von Ihrer Installation für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt werden.  

## <a name="changing-the-locale"></a>Ändern des Gebietsschemas
Ist für Gebietsschema Sprache und gesetzlichen Anforderungen in den lokalen Märkten abweichen. Gebietsschema bestimmt, wie die Daten in Bezug auf das trennzeichen Komma angezeigt werden, von nach links oder rechts, bestimmte und andere Einstellungen. Das Gebietsschema bestimmt auch einige der Systemelemente im Browser, wie der Aktion, einen neuen Artikel in einer Liste zum Erstellen, beispielsweise.  

Sie können das Gebietsschema in der Browserregisterkarte ändern, die Sie verwenden, um Daten zu arbeiten [!INCLUDE[d365fin](includes/d365fin_md.md)]. die Änderung bezieht sich nur auf Sie und die nicht die anderer Benutzer in Ihrem Unternehmen.  

> [!IMPORTANT]  
>  Wenn Sie das Gebietsschema ändern, sehen Sie auch eine lange Liste von Sprachen und von Gebietsschemen. Jedoch nur die Gebietsschemaeinstellung wird in der aktuellen Version von verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Um das Gebietsschema zu ändern, gehen Sie auf die Seite **Meine Einstellungen**. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).  

## <a name="application-version"></a>Anwendungsversionen

Auf der Seite **Hilfe und Support** sehen Sie die Version von [!INCLUDE [prodshort](includes/prodshort.md)], auf der Ihr Unternehmen basiert. Wenn Sie ein Unternehmen auf einer anderen Version aufbauen möchten, kann Ihr Administrator eine neue Produktionsumgebung anlegen. Weitere Informationen finden Sie unter [Erstellen einer neuen Produktionsumgebung](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) im Entwickler- und IT Pro-Inhalt.  

## <a name="languages-of-the-d365fin-help"></a>Sprachen der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Hilfe
Der Hilfeinhalt für die Kernfunktionalität in [!INCLUDE[d365fin](includes/d365fin_md.md)] wird auf der Microsoft Dokumentenseite veröffentlicht und ist in unterschiedlichen Sprachen verfügbar. Wenn Sie die Dokumente in [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen, wird der Inhalt in Ihrer Sprache angezeigt. Wenn eine bestimmte Seite noch nicht in der Sprache verfügbar ist, wird sie in Englisch angezeigt.

### <a name="how-do-i-change-the-language"></a>Wie ändere ich die Sprache?
Ganz einfach - einen Bildlauf zum unteren Rand der Browserseite ausführen und das Kugelsymbol in der unteren linken Ecke auswählen.

> [!NOTE]  
> Die Liste zeigt alle Sprachen an, die von der Microsoft Dokumentenseite unterstützt werden. [!INCLUDE[d365fin](includes/d365fin_md.md)] ist in einer beschränkten Anzahl Länder/Regionen verfügbar, aber der Hilfeinhalts kann in mehr Sprachen bereitgestellt werden. Der Hilfeinhalt ist allerdings nicht in allen Sprachen verfügbar, die die Microsoft Dokumentenseite unterstützt.

## <a name="see-also"></a>Siehe auch

[Ressourcen für Hilfe und Support](product-help-and-support.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Erste Schritte](product-get-started.md)  
