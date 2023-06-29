---
title: Die Erweiterung zur Problembehebung bei Anlagenposten
description: 'Es ist einfacher, mit ganzen Zahlen zu arbeiten. Verwenden Sie diese Erweiterung, um Beträge für Anlagen im Anlagenposten zu runden.'
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'machinery, buildings'
ms.date: 10/01/2021
ms.author: bholtorf
---
# <a name="the-troubleshooting-fa-ledger-entries-extension"></a><a name="the-troubleshooting-fa-ledger-entries-extension"></a>Die Erweiterung zur Problembehebung bei Anlagenposten
Verwenden Sie die Erweiterung zur Problembehebung bei Anlagenposten, um Abschreibungs- und Anschaffungsbeträge in Anlagenposten auf ganze Zahlen zu runden. Beispielsweise zum Runden eines Betrags von 30.000,44 auf 30.000. Typische Ursachen für Rundungsprobleme sind Datenmigration, plötzliche Buchungen von Beträgen im Sachposten oder Anpassungen, die Sie an Ihrem [!INCLUDE[prod_short](includes/prod_short.md)] vorgenommen haben.

Die Erweiterung zur Problembehebung bei Anlagenposten ist vorinstalliert und kann verwendet werden. Wenn Sie die Erweiterung entfernen, sie jedoch erneut installieren möchten, finden Sie sie unter AppSource.

## <a name="troubleshooting-fixed-asset-ledger-entries"></a><a name="troubleshooting-fixed-asset-ledger-entries"></a>Problembehebung bei Anlagenposten
Wenn Sie die Seite **Anlagenkarte** zum ersten Mal öffnen, wird die Aufgabenwarteschlange **Anlagenpostenüberprüfung** so geplant, dass die Beträge jeden Sonntag überwacht werden. Wenn Beträge gefunden werden, die Sie möglicherweise runden möchten, wird beim nächsten Öffnen der Seite „Anlagenkarte“ eine Benachrichtigung angezeigt. Die Benachrichtigung stellt die Option **Weitere Informationen** zum Öffnen der Seite **Anlagenposten mit Rundungsproblemen** bereit, auf der die Posten aufgelistet sind, die Sie möglicherweise runden möchten. Wählen Sie zum Runden der Beträge die entsprechenden Posten und dann die Aktion **Auswahl akzeptieren** aus. Mit der Aktion **Posten mit Problemen suchen** können Sie die Liste mit neuen Problemen aktualisieren, die aufgetreten sind, nachdem der Aufgabenwarteschlangenposten am vorherigen Sonntag ausgeführt wurde.

## <a name="see-also"></a><a name="see-also"></a>Weitere Informationen
[Anlagen](fa-manage.md)  
[Verwaltung von Anlagen](fa-manage.md)  
[Anlagen verwalten](fa-how-maintain.md)  
[Anpassen von Business Central Online mithilfe der Erweiterungen](ui-extensions.md)  
[Finanzen](finance.md)  
[Vorbereiten auf die Geschäftsabwicklung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



