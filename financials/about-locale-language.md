---
title: Mehrsprachig und Lokalisierung| Microsoft Docs
description: "Erhalten von Informationen, wie Sprache und Gebietsschema die Benutzeroberfläche in Dynamics 365 beeinflussen."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 94a7a3e1da9f2ac3145f18102f86386cfc980ea5
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="language-and-locale"></a>Sprache und  Gebiet
[!INCLUDE[d365fin](includes/d365fin_md.md)] wird in mehreren Märkten unterstützt und ist in den Sprachen verfügbar, die diese Märkte benötigen. Dieses ist ein Ergebnis für Supportleistungen für mehrere Sprachen zu Laufzeit mit Unterstützung für rechtliche Anforderungen in den unterstützten Märkten. Das bedeutet, das [!INCLUDE[d365fin](includes/d365fin_md.md)] in verschiedenen Sprachen angezeigt werden kann. Sie können die Sprache ändern, die verwendet wird, um Texte anzuzeigen und die Änderung tritt sofort in Kraft, sobald Sie automatisch exportiert und wieder unterzeichnet wurde. Die Einstellung trifft auf Sie zu und nicht auf alle in Ihrer Unternehmung.  

Wenn Sie kanadisch sind, können Sie die Benutzeroberfläche in Englisch und auf französisch sehen, aber es ist immer noch die kanadische Version [!INCLUDE[d365fin](includes/d365fin_md.md)] in allen anderen Aspekten. Es ist nicht gleich wie sagen wir [!INCLUDE[d365fin](includes/d365fin_md.md)] in Großbritannien.  

> [!NOTE]  
>  Das Ändern der Sprache wird nur in [!INCLUDE[d365fin](includes/d365fin_md.md)] nicht unterstützt.

Die Änderung der Texte in den Daten der Anwendung ist kein Bestandteil der Multilanguagefunktionalität. Dies ist durch das Design der Anwendung bedingt. Beispiele für solche Texte sind die Namen der Artikel oder Bemerkungen für einen Debitor. D. h. diese Textarten werden nicht übersetzt.  

> [!NOTE]  
>  Da  [!INCLUDE[d365fin](includes/d365fin_md.md)] nur einen Zeichensatz für Daten unterstützt. Beim Abrufen von Daten, die unter Verwendung eines anderen Zeichensatzes eingegeben wurden, können daher Fehler auftreten. Wenn Ihr Tenant zum Beispiel nur englische und russische Zeichen unterstützt und Sie Daten in einer anderen Sprache eingegeben, werden diese möglicherweise nicht ordnungsgemäß gespeichert. Wenden Sie sich an den zuständigen Systemadministrator, und erkundigen Sie sich nach den Sprachen, die von Ihrer Installation für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt werden.  

## <a name="changing-the-locale"></a>Ändern des Gebietsschemas
Ist für Gebietsschema Sprache und gesetzlichen Anforderungen in den lokalen Märkten abweichen. Gebietsschema bestimmt, wie die Daten in Bezug auf das trennzeichen Komma angezeigt werden, von nach links oder rechts, bestimmte und andere Einstellungen. Das Gebietsschema bestimmt auch einige der Systemelemente im Browser, wie der Aktion, einen neuen Artikel in einer Liste zum Erstellen, beispielsweise.  

Sie können das Gebietsschema in der Browserregisterkarte ändern, die Sie verwenden, um Daten zu arbeiten [!INCLUDE[d365fin](includes/d365fin_md.md)]. die Änderung bezieht sich nur auf Sie  und die nicht die anderer Benutzer in Ihrem Unternehmen.  

> [!IMPORTANT]  
>  Wenn Sie das Gebietsschema ändern, sehen Sie auch eine lange Liste von Sprachen und von Gebietsschemen. Jedoch nur die Gebietsschemaeinstellung wird in der aktuellen Version von verwendet [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Um das Gebietsschema zu ändern, gehen Sie zum Fenster **Meine Einstellungen**. Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).  

## <a name="see-also"></a>Siehe auch  
[Sprachen der Dokumente](about-languages.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

