---
title: Fehlerbehandlung in Ihrem Unternehmens-Hub
description: 'Erfahren Sie, wie Sie Probleme umgehen können, wenn Sie sich im Unternehmenshub in Dynamics 365 Business Central befinden, um die Arbeit über mehrere Unternehmen hinweg zu verwalten.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accountant, accounting, troubleshoot'
ms.search.form: 1151
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="troubleshooting-your-company-hub"></a><a name="troubleshooting-your-company-hub"></a><a name="troubleshooting-your-company-hub"></a>Fehlerbehandlung in Ihrem Unternehmens-Hub

Das Hinzufügen von Unternehmen zum Dashboard des Unternehmens-Hubs ist äußerst einfach, aber in diesem Artikel werden Probleme behandelt, die dabei auftreten können.  

## <a name="check-errors"></a><a name="check-errors"></a><a name="check-errors"></a>Fehler prüfen

Verwenden Sie die Aktion **Fehler prüfen** zum Anzeigen einer Liste aktueller Fehler. Sie können zusätzliche Details für jeden Fehler anzeigen, und Sie können das Protokoll bereinigen, indem Sie ältere Posten löschen.  

## <a name="connection-failed"></a><a name="connection-failed"></a><a name="connection-failed"></a>Verbindung fehlgeschlagen

Es kann verschiedene Gründe geben, warum Sie keine Verbindung zu einem Unternehmen herstellen können, darunter die folgenden:

- Die URL im Feld **Umgebungslink** ist ungültig  

  Wechseln Sie zur Seite **Umgebungslinks**, öffnen Sie die Umgebung, mit der Sie keine Verbindung herstellen können, und wählen Sie dann die Aktion **Die Verbindung testen** aus.  
- Das Unternehmen des Kundens ist derzeit offline, beispielsweise bei einem Upgrade

  Wählen Sie in Ihrem Dashboard das Menüelement **Werkzeuge** aus, und wählen Sie dann **Fehler prüfen**. Dadurch wird eine Liste mit technischen Details geöffnet, daher sollten Sie sich an Ihren Administrator wenden, wenn Sie Fehler finden. Zum Beispiel weist die Fehlermeldung „*Der Server hat die Anmeldeinformationen des Kunden abgelehnt*“ darauf hin, dass Sie keinen Zugriff haben.  
- Sie haben nicht Zugriff auf alle Unternehmen in der Umgebung, zu der Sie eine Verbindung herstellen möchten

  In [!INCLUDE [prod_short](includes/prod_short.md)] kann eine Organisation mehrere Konzernmandanten haben, die als Unternehmen bezeichnet werden, und Sie haben möglicherweise nicht Zugriff auf alle Unternehmen. Arbeiten Sie mit Ihrem Administrator oder Client, um sicherzustellen, dass Sie Zugriff auf die Unternehmen haben, in denen Sie arbeiten müssen.  

## <a name="data-does-not-refresh"></a><a name="data-does-not-refresh"></a><a name="data-does-not-refresh"></a>Daten werden nicht aktualisiert

Wenn Sie ein Unternehmen hinzufügen oder eine Aktualisierung der Daten anfordern, ruft [!INCLUDE [prod_short](includes/prod_short.md)] die Daten ab. Sie müssen die Seite allerdings selbst aktualisieren, z. B. durch Auswählen der Aktion **Alle Unternehmen neu laden**, die Browser-Seite aktualisieren, vom Dashboard hinweg und wieder dorthin zurück navigieren oder etwas Ähnliches.  

Wenn Sie ein Unternehmen hinzugefügt haben, dieses jedoch nicht in der Liste angezeigt wird, können Sie auch die Aktion **Alle Unternehmen neu laden** zum Aktualisieren der Liste verwenden.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten](company-hub.md)  
[Fügen Sie Unternehmen zu Ihrem Unternehmens-Hub hinzu](company-hub-add-company.md)  
[Buchhaltungs-Erfahrung in Business Central](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
