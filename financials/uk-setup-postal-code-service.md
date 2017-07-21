---
title: Einrichten der britischen Postleitzahlerweiterung GetAddress.io| Microsoft Docs
description: "Beschreibt die allgemeine Funktionen, die Sie verwenden, um die Daten in den Finanzverhältnissen für Aktivitäten, wie Eingabe von Werten, Sortieren von Daten und Ändern von Ansichten auszuführen."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a>Vorgehensweise: Einrichten der britischen Postleitzahlerweiterung für Postleitzahlen, GetAddress.io
Diese Erweiterung macht es einfach Adressen in Großbritannien für Entitäten beispielsweise Kunden, Kontakten, Mitarbeiter, Kreditoren, Bankkonten einzugeben, usw. 

Die britische Postleitzahlerweiterung GetAddress.io verwendet die getAddress API Adressen, um Postleitzahlen in Großbritannien zu finden. Um die Erweiterung zu verwenden, müssen Sie einen Plan und einen API Schlüssel für getAddress API haben. Das ist einfach und wir Ihnen helfen das tun, wenn Sie die britische Postleitzahlerweiterung GetAddress.io einrichten. Pläne basieren auf der Nutzung, manchmal auch als Aufrufe bezeichnet. Ein Aufruf ist in diesem Fall, wenn [!INCLUDE[d365fin](includes/d365fin_md.md)] eine Übersicht der Adressen für eine Postleitzahl anzeigt. Abhängig davon, wie oft Sie Adressen hinzufügen, wählen Sie den Plan aus, der für Sie sinnvoll ist. Wenn Sie einfach auf der Seite **Abrufen von API Schlüsseln** auswählen, verwenden Sie den **Kostenlosen** Plan, mit dem Sie 20 Adressen pro hinzufügen können und der für 30 Tage gültig ist. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Einrichten der britischen Postleitzahlerweiterung für Postleitzahlen, GetAddress.io 
1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Erweiterung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Im Fenster **Dienstverbindungen** wählen Sie **Britischer Postleitzahl-Dienst** aus.
3. Auf der Seite **Postleitzahlanbieterkonfiguration** wählen Sie **Deaktiviert** aus.
4. Im Fenster **Postleitzahldienst-Auswahl** wählen Sie **GetAddress.io** aus.
5. Im Fenster **GetAddress.io-Config** wählen Sie **API Schlüssel abrufen**, um die Seite **Pläne** auf der Website getAddress API zu öffnen.  

    > [!NOTE]  
>   Sie müssen möglicherweise Popups in Ihrem Browser ermöglichen.
6. Kaufen einen Plan oder wählen Sie einfach **API Schlüssel abrufen** aus und erstellen Sie dann Ihre E-Mail-Adresse bereit.
7. Öffnen Sie die E-Mail aus getAddress.io und kopieren Sie den API-Schlüssel. Der Schlüssel ist unter der Überschrift **Ihr API Schlüssel**.
8. Im Fenster **GetAddress.io-Config** geben Sie den API-Schlüssel im Feld **API Schlüssel** ein, und wählen Sie dann **OK** aus.
9. Auf der Seite **Dienstverbindungen** prüfen Sie, dass das Feld **Adressen-Anbieter** Feld **GetAddress.io** anzeigt. Wenn dies so ist, ist der Dienst aktiviert.

## <a name="see-also"></a>Siehe auch
[" GetAddress.io Großbritannien](ui-extensions-getaddressio.md)
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Mittels der Erweiterungen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
