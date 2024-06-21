---
title: Buchhaltungsperioden festlegen
description: 'Sie legen Buchungsperioden (Buchungsstart- und -enddatum) fest, um zu bestimmen, wann Benutzer im Hauptbuch buchen können.'
author: brentholtorf
editor: ''
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: user setup
ms.search.form: 118
ms.date: 12/05/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="specify-posting-periods"></a>Buchhaltungsperioden festlegen

Verwenden Sie Buchungsperioden, um anzugeben, wann Benutzer in der Finanzbuchhaltung buchen können.  

## <a name="to-specify-posting-periods"></a>Buchhaltungsperioden festlegen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Aauf der Seite **Finanzbuchhaltungs-Einrichtung:** legen Sie die Periode fest, indem Sie Daten in den Feldern **Buchungen zugel. ab** und **Buchungen zugel. bis** eingeben.  

> [!NOTE]  
> Diese Buchungszeiträume gelten für den Mandanten und alle Anwender. Wenn Sie für verschiedene Benutzer verschiedene Buchungszeiträume definieren möchten, können Sie diese auf der Seite **Benutzer einrichten** Diese Buchungszeiträume haben Vorrang vor jenen, die auf der Seite **Finanzbuchhaltung einrichten** angegeben werden. Weitere Informationen finden Sie unter [Zeiteinschränkungen für Benutzende einrichten](ui-define-granular-permissions.md#set-up-time-constraints-for-users).

## <a name="video-guidance"></a>Videoanleitung

Wenn Sie eine Buchhaltungsperiode abschließen, möchten Sie möglicherweise verhindern, dass neue Beiträge eingehen, oder nur bestimmten Personen erlauben, Transaktionen zu buchen. Das folgende Video zeigt, wie Sie steuern, wer wann Transaktionen in Ihrem Hauptbuch buchen kann.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fAB8]

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Abschließen von Periodenabschlüssen](year-how-complete-period-end-processes.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
