---
title: 'Gewusst wie: Einrichten eine Belegaustauschdienstes | Microsoft Docs'
description: Sie verwenden einen externen Anbieter zum Austausch elektronischer Belege mit Ihren Handelspartnern.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="set-up-a-document-exchange-service" />So richten Sie einen Belegaustauschdienst ein

Als Teil des Data Exchange Frameworks können Sie Einkaufs- und Verkaufsbelege mit Ihren Handelspartnern ohne zusätzliche Schritte austauschen, z. B. indem Sie die Belege als PDF-Dateien an E-Mail-Nachrichten anhängen. Wenn Sie z.B. bereit sind, einem Kunden eine Rechnung zu stellen, können Sie diese zur Zahlung als Datei versenden, die Ihr Kunde in seiner Business Management-Anwendung empfangen kann. Weitere Informationen finden Sie unter [Daten elektronisch austauschen](across-data-exchange.md).

> [!NOTE]
> Das Einrichten eines Document Exchange Service für Business Central On-Premises erfordert einige zusätzliche Schritte zur Autorisierung. Weitere Informationen finden Sie unter [Einstellungen für Business Central On-Premises](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners" />Verbindung mit Handelspartnern herstellen

Der Austausch von elektronischen Belegen erfordert eine Verbindung zu Ihren Handelspartnern. Um das Erstellen einer sicheren Verbindung zu erleichtern, ist [!INCLUDE[prod_short](includes/prod_short.md)] Online für die Verwendung der Business Central Integration-App konfiguriert. Die App ist im Tradeshift App Store erhältlich. Sie und Ihre Geschäftspartner müssen lediglich ein Tradeshift-Konto erstellen und dann die App aktivieren. Die Business Central Integration-App gibt es in einer Produktions- und einer Sandbox-Version. Die Sandbox-Version eignet sich zum Beispiel gut, um den Austausch von Belegen zu testen. Sie können zwischen der Produktions- und der Sandbox-Version wechseln, indem Sie den Schalter **Sandbox** auf der Seite **Doc. Exch. Service Einrichtung** einschalten. Wenn Sie dies tun, werden die Informationen auf dem Inforegister **Service** für Sie aktualisiert.

Wenn Sie einen anderen Dienst verwenden möchten, müssen Sie alternativ Informationen für die Verbindung bereitstellen. Weitere Informationen finden Sie unter [So stellen Sie eine Verbindung zu einem Document Exchange Service her](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift" />So verbinden Sie sich mit der Business Central Integration-App auf Tradeshift

Sie können schnell ein Tradeshift-Konto erstellen und mit der Business Central Integration-App über die **Doc. Exch. Service Einrichtung** Seite. Wählen Sie entweder den Link **App aktivieren** in der Benachrichtigung oder das Feld **App URL**, um die App im Tradeshift App Store aufzurufen. Auf der Login-Seite für Tradeshift melden Sie sich entweder an oder registrieren sich.

> [!NOTE]
> Nachdem Sie sich bei Ihrem Tradeshift-Konto angemeldet haben, werden Sie möglicherweise nicht zu der Seite weitergeleitet, auf der Sie die App aktivieren. Um dies zu tun, können Sie auf den Link auf der Seite **Doc. Exch. Service Einrichtung** in Business Central erneut klicken, um direkt zur App zu gelangen.

Wenn Sie sich entscheiden, die Business Central Integration-App nicht mehr zu verwenden, sollten Sie sie im Tradeshift-App-Store deaktivieren. 

## <a name="to-connect-to-a-document-exchange-service" />So stellen Sie eine Verbindung zu einem Document Exchange Service her

Wenn Sie es vorziehen, einen anderen Document Exchange Service zu verwenden, müssen Sie einige Informationen angeben, um sich mit dem Service zu verbinden.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Document Exchange Service Einrichtung** ein, und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Benutzeragent**|Geben Sie einen Text ein, der zur Identifizierung Ihrer Firma in den Prozessen des Belegaustauschs verwendet werden kann.|  
    |**Aktiviert**|Geben Sie an, ob die Verbindung zum Dienst aktiviert ist.<br><br> **Hinweis:** Wenn Sie den Dienst aktivieren, werden mindestens zwei Einträge für die Auftragswarteschlange erstellt, um elektronische Belege zu senden und zu empfangen. Wenn Sie den Service deaktivieren, werden die Projektwarteschlangenposten gelöscht.|  
    |**Sandbox**|Geben Sie an, ob Sie eine Verbindung zu einer Sandbox-Version des Document Exchange Service herstellen.|
    |**Anmelde-URL**|Geben Sie die Webseite an, auf der Sie sich für den Belegaustauschdienst anmelden.|  
    |**App URL**|Wählen Sie den Link, um den App-Store zu öffnen und die Business Central Integration-App zu aktivieren oder zu deaktivieren.|
    |**Dienste-URL**|Geben Sie die Adresse des Belegaustauschdienst an, die aufgerufen wird, wenn Sie elektronische Belege versenden und erhalten.|  
    |**Anmelde-URL**|Geben Sie die URL für die Seite an, mit der Sie sich beim Document Exchange Service anmelden. Dies ist die Seite, auf der Sie den Benutzernamen und das Kennwort Ihrer Firma eingeben.|  
    
    > [!NOTE]  
    > Ihre Anmeldeinformationen werden automatisch verschlüsselt. Sie können die Verschlüsselung nicht abschalten.

    > [!NOTE]
    > Wenn Sie aufgrund eines Berechtigungsproblems keine Verbindung zum Document Exchange Service herstellen können, liegt das möglicherweise daran, dass [!INCLUDE[prod_short](includes/prod_short.md)] den Zugriffstoken nicht automatisch erneuern kann. Dies kann z.B. der Fall sein, wenn Sie den Dienst seit einiger Zeit nicht mehr genutzt haben. Sie können das Token manuell erneuern, indem Sie die Aktion **Token erneuern** verwenden.

## <a name="settings-for-business-central-on-premises" />Einstellungen für Business Central On-Premises

Um Business Central on-premises zu verbinden, müssen Sie eine App im Tradeshift App Store erstellen. Verwenden Sie dazu die Weiterleitungs-URL aus dem Feld **Weiterleitungs-URL** auf der Seite **Document Exchange Service Einrichtung**. Nachdem Sie Ihre App registriert haben, stellt Tradeshift eine Client ID und ein Client Geheimnis zur Verfügung. In [!INCLUDE[prod_short](includes/prod_short.md)] geben Sie diese Werte auf der Seite **Document Exchange Service Einrichtung** im Inforegister **Autorisierung** ein.

Wenn Sie die App-ID und den geheimen Schlüssel lieber an einem anderen Ort speichern möchten, können Sie die Felder „Client-ID“ und „Geheimer Clientschlüssel“ leer lassen und eine Erweiterung schreiben, um die ID und den geheimen Schlüssel von diesem Speicherort abzurufen. Sie können das Geheimnis zur Laufzeit bereitstellen, indem Sie die Ereignisse OnGetClientId und OnGetClientSecret in der Codeunit 1410 „Doc. Exch. Service Mgt.“

## <a name="see-related-microsoft-trainingtrainingmoduleselectronic-documents-dynamics--business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/electronic-documents-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Datenaustausch einrichten](across-set-up-data-exchange.md)  
[Daten elektronisch austauschen](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
