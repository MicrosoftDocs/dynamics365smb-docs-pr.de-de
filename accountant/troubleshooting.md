---
title: Möglichkeit für die Problembehebung oder Umgehung von Problemen | Microsoft Docs
description: Erfahren Sie, wie Sie um jegliche Probleme im Accountant Hub for Dynamics 365 umgehen.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 8faba6940469265959d09f807d2d3c1afe6199af
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300401"
---
# <a name="troubleshooting-include-d365acc_longincludesd365acc_long_mdmd"></a>Problembehebung [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Die Anmeldung für [!INCLUDE [d365acc](includes/d365acc_md.md)] ist einfach und kann sehr schnell vorgenommen werden. Das Hinzufügen von Kundens zum Dashboard ist auch einfach, aber in diesem Artikel werden Probleme behandelt, die dabei auftreten können.

## <a name="what-email-address-can-i-use-with-include-d365accincludesd365acc_mdmd"></a>Welche E-Mail-Adresse kann ich mit [!INCLUDE [d365acc](includes/d365acc_md.md)] benutzen?
[!INCLUDE [d365acc](includes/d365acc_md.md)] erfordert eine Arbeits- oder Schul-E-Mail-Adresse, um sich anzumelden. [!INCLUDE [d365acc](includes/d365acc_md.md)] unterstützt keine E-Mail-Adressen, die von E-Mail-Diensten für Endverbraucher oder Telekommunikationsanbietern bereitgestellt werden. Dieses schließt outlook.com, hotmail.com, gmail.com und andere ein.  

Wenn Sie versuchen, sich mit einer persönlichen E-Mail-Adresse anzumelden, erhalten Sie eine Nachricht, in der Sie aufgefordert werden, eine Arbeits- oder Schul-E-Mail-Adresse zu verwenden.  

## <a name="why-cant-i-connect-to-my-clients-data"></a>Warum nicht kann ich keine Verbindung zu den Daten meines Kundens herstellen?
Es kann mehrere Gründe geben, unter anderem die Folgenden:

- Die URL im Feld **Kunden URL** ist ungültig  

  Wechseln zu **Manage Kundens**, öffnen Sie den Kunden, zu dem Sie keine Verbindung herstellen können, und wählen Sie dann **Test Kunden URL** aus.  
- Das Unternehmen des Kundens ist derzeit offline, beispielsweise bei einem Upgrade

  Wählen Sie in Ihrem Dashboard das Menüelement **Werkzeuge** aus, und wählen Sie dann **Fehler prüfen**. Dadurch wird eine Liste mit technischen Details geöffnet, daher sollten Sie sich an Ihren Administrator wenden, wenn Sie Fehler finden. Zum Beispiel weist die Fehlermeldung "Der Server hat die Anmeldeinformationen des Kundens abgelehnt" darauf hin, dass Sie keinen Zugriff haben.  
- Sie haben keine E-Mail von Ihrem Kunden erhalten, in der sie zu [!INCLUDE [d365fin](includes/d365fin_md.md)] eingeladen werden, oder Sie haben den Link in einer E-Mail nicht geöffnet, oder Sie haben die Einladung nicht angenommen

  Sie müssen den Link in der Einladung öffnen und die Schritte akzeptieren, mit denen Sie zum [!INCLUDE [d365fin](includes/d365fin_md.md)] Ihres Kundens hinzugefügt werden. Bis dahin haben Sie keinen Zugriff auf deren Daten.  
- Sie haben keinen Zugriff auf alle Unternehmen in [!INCLUDE [d365fin](includes/d365fin_md.md)] Ihres Kundens

  Ihr Kunden kann über mehrere Konzernmandanten oder Mandanten in [!INCLUDE [d365fin](includes/d365fin_md.md)] verfügen und Ihre Einladung berücksichtigt nicht immer alle Unternehmen. Arbeiten Sie mit Ihrem Kunden, um sicherzustellen, dass Sie Zugriff auf die Unternehmen haben, in denen der Kunden Sie arbeiten lassen möchte.  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a>Warum werden die Daten in meinem Dashboard nicht aktualisiert?
Wenn Sie einen Kunden hinzufügen oder eine Aktualisierung der Daten anfordern, ruft [!INCLUDE [d365acc](includes/d365acc_md.md)] die Daten ab. Sie müssen die Seite allerdings selbst aktualisieren, z. B. durch Auswählen der Aktion "Alle Unternehmen neu laden", der Browser-Seite aktualisieren, vom Dashboard fort und wieder dorthin zurück navigieren oder etwas Ähnliches durchführen. Dieses ist ein bekanntes Problem, an dessen Verbesserung in einem späteren Update wir arbeiten.  

## <a name="see-also"></a>Siehe auch
[Erste Schritte mit [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Fügen Sie Ihren Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md) Kunden hinzu  
