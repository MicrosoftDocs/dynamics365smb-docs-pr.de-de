---
title: Verwalten der Datenbank-Zugriffsabsicht in Business Central | Microsoft Docs
description: Ändern Sie die Datenbank-Zugriffsabsicht für Berichte, API-Seiten und Abfragen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/30/2020
ms.author: jswymer
ms.openlocfilehash: b46786b60d7c5799b056c49188785bd595db57ff
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333908"
---
# <a name="managing-database-access-intent"></a>Verwaltung der Datenbank-Zugriffsabsicht 

Als Superuser oder Administrator können Sie die Datenbankzugriffsabsicht auf Berichte, Seiten vom Typ API und Abfragen ändern, um die Leistung des Dienstes zu verbessern.

## <a name="overview"></a>Matrix

[!INCLUDE[d365fin](includes/d365fin_md.md)] kann so eingerichtet werden, dass schreibgeschützte Replikate der primären Datenbank (Lesen und Schreiben) verwendet werden. Die Verwendung der Datenbankreplik reduziert die Belastung der primären Datenbank. In einigen Fällen wird dadurch auch die Leistung beim Anzeigen von Daten im Client verbessert. Replikate sind vorteilhaft für Objekte wie Berichte, Abfragen und API-Seiten, die nur zur Anzeige von Daten, nicht zur Änderung von Daten verwendet werden.

Wenn Objekte ausgeführt werden, bestimmt die Datenbank-Zugriffsabsicht, ob eine schreibgeschützte Replik, falls vorhanden, oder die primäre Datenbank verwendet werden soll. Berichte, API-Seiten und Abfragen werden mit einer vordefinierten Datenbank-Zugriffsabsicht entwickelt (siehe [DatabaseAccessIntent-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

Auf der Seite **Datenbank-Zugriffsabsichtsliste** können Sie die vordefinierte Datenbank-Zugriffsabsicht für Objekte außer Kraft setzen, wenn sie ausgeführt werden.

In Bezug auf die Datenbank wird diese Funktion allgemein als *Lesen Scale-out* bezeichnet. Weitere Informationen über die Ausleseskalierung und die Datenzugriffsabsicht in [!INCLUDE[prodshort](includes/prodshort.md)] finden Sie unter [Ausnutzung der Ausleseskalierung für eine bessere Leistung](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in der Hilfe für Entwickler und die Verwaltung unter [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="to-change-the-database-access-intent"></a>So ändern Sie die Datenbank-Zugriffsabsicht

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Datenbankzugriffsabsichtsliste** ein, und wählen Sie dann den entsprechenden Link.

    Die Seite listet alle Berichte, Seiten und Abfragen auf. Die Spalte **Zugriffsabsicht** enthält einen der folgenden Werte:

    |**Einstellung**|**Beschreibung**|  
    |------------|-------------|  
    |**Standard**|Zeigt an, dass das Objekt die vordefinierte Datenbankzugriffsabsicht verwendet.|
    |**Schreiben erlauben**|Legt das Objekt so fest, dass es die primäre Datenbank verwendet, was bedeutet, dass der Benutzer Daten ändern kann.|
    |**Nur lesen**|Legen Sie das Objekt so fest, dass die Datenbankreplik verwendet wird, d.h. der Benutzer kann die Daten nur anzeigen und nicht ändern.|

2. Wählen Sie die Aktion **Liste bearbeiten** aus.

3. Ändern Sie auf der Seite **Bearbeiten - Datenbank-Zugriffsabsichtsliste** das Feld **Zugriffsabsicht** für die Objekte.

    > [!NOTE]
    > Wenn ein editierbares Objekt, wie die Debitorenkarte, auf **Nur lesen** gesetzt ist, wird die primäre Datenbank unabhängig von der Zugriffsabsicht weiterhin verwendet, so dass die Benutzer wie gewohnt Änderungen vornehmen können.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch
[Geschäftsfunktionen](across-business-functionality.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Erste Schritte](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
