---
title: Yodlee Bank Feeds einrichten| Microsoft Docs'
description: "Sie können Zahlungsinformationen in ein beliebiges Datenformat umwandeln, die die Bank benötigt und den Export oder den Import von Bankdateien aktivieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 5f4b675db86bc6fef19a587454e1e513fe6fa83d
ms.contentlocale: de-de
ms.lasthandoff: 10/17/2017

---
# <a name="how-to-set-up-the-envestnet-yodlee-bank-feeds-service"></a>Gewusst wie: Einrichten des Envestnet Yodlee Bank-Feed-Service
Sie können elektronische Bankauszüge von Ihrer Bank importieren, um das Fenster **Zahlungsabstimmungsbuch.-Blatt** schnell auszufüllen und so Zahlungen zu begleichen und das Bankkonto auszugleichen. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Der Bankfeeddienst Envestnet Yodlee wird als eine Erweiterung zum [!INCLUDE[d365fin](includes/d365fin_md.md)] eingerichtet und steht zur Aktivierung bereit. Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-extensions.md) mithilfe der Erweiterungen .

> [!NOTE]
> Der Bank-Feeddienst Envestnet Yodlee wird nur in den USA, in das Kanada und in Großbritannien unterstützt.

Wenn Sie den Bankfeeddienst aktiviert haben, müssen Sie das beteiligte Bankkonto mit dem Onlinebankkonto verknüpfen, von dem der Feed stammt. In den folgenden unterschiedlichen Szenarios verknüpfen Sie Bankkonten mit Onlinebankkonten:

* Im [!INCLUDE[d365fin](includes/d365fin_md.md)] ist kein Bankkonto für Ihr Onlinebankkonto vorhanden. Daher erstellen Sie das Bankkonto über eine Verknüpfung mit dem Onlinebankkonto.
* Im [!INCLUDE[d365fin](includes/d365fin_md.md)] ist bereits ein Bankkonto vorhanden, das Sie mit einem Onlinebankkonto verknüpfen möchten.
* Bei einem verknüpften Bankkonto muss die Verknüpfung entfernt werden, da Sie den Bankfeeddienst für dieses Konto beenden möchten.
* Die Onlinebankkonten haben geändert und Sie möchten die Informationen zu den Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktualisieren.

Wenn der Bankfeeddienst aktiviert ist, können Sie ein Bankkonto so einrichten, dass automatisch alle zwei Stunden neue Bankauszüge in das Fenster **Zahlungsabstimmungsbuch.-Blatt** importiert werden. Transaktionen für Zahlungen, die bereits als ausgeführt und/oder abgestimmt im Fenster **Zahlungsabstimmungsbuch.-Blatt** gebucht wurden, werden nicht importiert. Weitere Informationen finden Sie im Abschnitt “So aktivieren Sie das automatische Importieren von Bankauszügen”.

> [!NOTE]  
>   Wenn Sie die unterstützte Einrichtung über "Unternehmen einrichten" verwenden, werden einige der folgenden Schritte automatisch beim Einrichten von Unternehmensbankkonten ausgeführt. Weitere Informationen finden Sie unter [Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)

## <a name="to-enable-the-bank-feed-service"></a>So aktivieren Sie den Bankfeeddienst
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie das Bankkonto, das Sie für den Bankfeeddienst verwenden werden.
3. Wählen Sie im Fenster **Bankkonto** im Feld **Format Bankauszugimport** YODLEEBANKFEED aus.  

Der Bankfeeddienst wird aktiviert, wenn Sie ein Bankkonto mit den dazugehörigen Onlinebankkonto verknüpfen. Siehe das folgende Verfahren.  

## <a name="to-create-a-new-linked-bank-account"></a>So erstellen Sie ein neues verknüpftes Bankkonto
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie das entsprechende Bankkonto aus, und wählen Sie dann **Neues verknüpftes Bankkonto erstellen**. Das Fenster **Bankkontenverknüpfung** wird nach wenigen Augenblicken geöffnet.

    > [!NOTE]  
>   Dieses Fenster zeigt die tatsächliche Webseite des Bankfeeddienstes Envestnet Yodlee an. Die Terminologie und die Funktionen im Fenster weichen möglicherweise von den Anweisungen ab, die in diesem Thema bereitgestellt werden.  
3. Verwenden Sie die Suchfunktion im Fenster **Onlinebankkonto-Verknüpfung** im Bereich **Konto verknüpfen**, um die Bank zu suchen, bei der Sie ein oder mehrere Onlinebankkonten haben.
4. Wählen Sie den Banknamen aus. Der Bereich **Anmeldung** wird geöffnet.
5. Geben Sie den Benutzernamen und das Kennwort, das Sie für die Ameldung bei der Onlinebank verwenden, an, und wählen Sie dann die Schaltfläche **Weiter** .  
6. Der Bankfeeddienst bereitet die Verknüpfung des ersten Onlinebankkontos der angegebenen Bank mit einem neuen Bankkonto in [!INCLUDE[d365fin](includes/d365fin_md.md)] vor.

    > [!NOTE]  
>   Wenn Sie mehr als ein Onlinebankkonto bei der Bank haben, müssen Sie für alle zusätzlichen Onlinebankkonten weitere Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen. Siehe Schritte 8 bis 10.  

    Nachdem der Vorgang abgeschlossen ist, erscheint die Bankadresse im Bereich **Meine Konten** auf der Registerkarte **Verknüpft** . Die Nummer in Klammern gibt an, wie viele der Online Bankkonten verknüpft wurden.  
7. Wählen Sie die Schaltfläche **OK** aus.

    Wenn Sie nur Online ein Bankkonto verknüpfen, wird das Fenster **Bankkontokarte** geöffnet und zeigt den Namen des Online Bankkontos an. In diesem Fall ist die Bankkontoverknüpfung abgeschlossen. Jetzt müssen Sie nur noch das Bankkonto einrichten. Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-how-setup-bank-accounts.md).

    Wenn mehr als ein Onlinebankkonto verknüpft wurde, öffnet sich das Fenster **Bankkontenverknüpfung** und die zusätzlichen Onlinebankkonten, die nicht mit den Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] verknüpft sind, werden aufgelistet. In diesem Fall, folgen Sie dem nächsten Schritt.  
8. Wählen Sie im Fenster **Bankkontenverknüpfung** die Zeile für ein Onlinebankkonto aus, und wählen Sie dann die Aktion **Mit neuem Onlinebankkonto verknüpfen**.  

    Das Fenster **Bankkontokarte** wird für ein neues Bankkonto geöffnet und der Name des Onlinebankkontos wird angezeigt.

    Wenn in [!INCLUDE[d365fin](includes/d365fin_md.md)] bereits ein Bankkonto vorhanden ist, mit dem Sie das zusätzliche Onlinebankkonto verknüpfen möchten, folgen Sie dem nächsten Schritt.  
9. Wählen Sie im Fenster **Bankkontenverknüpfung** die Zeile für ein Onlinebankkonto aus, und wählen Sie dann die Aktion **Mit vorhandenem Onlinebankkonto verknüpfen**.
10. Wählen Sie im Fenster **Bankkontenübersicht** das Bankkonto aus, mit dem Sie eine Verknüpfung erstellen möchten, und klicken Sie anschließend auf **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>So verknüpfen Sie ein Bankkonto mit einem Onlinebankkonto
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Zeile des Bankkontos aus, das nicht mit einem Onlinebankkonto verknüpft ist, und wählen Sie dann die Aktion **Verknüpfen mit Onlinebankkonto** . Das Fenster **Onlinebankkonto-Verknüpfung** wird für ein neues Bankkonto geöffnet und der Name des Onlinebankkontos ist bereits im Bereich **Konto verknüpfen** eingefügt.
3. Wählen Sie den Banknamen aus. Der Bereich **Anmeldung** wird geöffnet.
4. Geben Sie den Benutzernamen und das Kennwort, das Sie für die Ameldung bei der Onlinebank verwenden, an, und wählen Sie dann die Schaltfläche **Weiter** .  

    Der Bankfeeddienst bereitet die Verknüpfung Ihres Bankkontos in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit dem entsprechenden Onlinebankkonto vor.  

    Wenn der Prozess erfolgreich abgeschlossen ist, erscheint die Bankadresse im Bereich **Meine Konten** auf der Registerkarte **Verknüpft** . Wenn die Bank mehr als ein Bankkonto hat, wird lediglich das Bankkonto, das Sie in Schritt 2 auswählten, verknüpft.  
5. Wählen Sie die Schaltfläche **OK** aus.

Im Fenster **Bankkontenübersicht** ist das Kontrollkästchen **Verknüpft** aktiviert.

## <a name="to-unlink-a-bank-account"></a>So heben Sie die Verknüpfung mit dem Bankkonto auf
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Zeile des verknüpften Bankkontos aus, dessen Verknüpfung mit einem Onlinebankkonto aufgehoben werden soll, und wählen Sie dann die Aktion **Verknüpfung mit Onlinebankkonto aufheben**.

> [!NOTE]  
>   Wenn Sie **Ja** im Bestätigungsdialogfeld auswählen, wird die Verknüpfung mit dem Onlinebankkonto entfernt und die Anmeldedaten gelöscht. Um das Bankkonto wieder mit dem Onlinebankkonto zu verknüpfen, müssen Sie sich erneut bei der Bank anmelden. Weitere Informationen finden Sie im Abschnitt “So verknüpfen Sie ein Bankkonto mit einem Onlinebankkonto“.

## <a name="to-update-bank-account-linking"></a>So aktualisieren Sie die Bankkontoverknüpfung
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie das entsprechende Bankkonto aus, und wählen Sie dann die Aktion **Bankkontoverknüpfung aktualisieren**.

Wenn Probleme für ein oder mehrere der verknüpften Bankkonten im Fenster **Bankkontenübersicht** vorhanden sind, wird das Fenster **Bankkontenverknüpfung** geöffnet und zeigt an, welche der Bankkonten Probleme haben. Probleme werden am besten gelöst, indem sie die Verknüpfung mit dem Onlinebankkonto entfernen und dann die Verknüpfung neu erstellen. Weitere Informationen finden Sie im Abschnitt “So verknüpfen Sie ein Bankkonto mit einem Onlinebankkonto“.

## <a name="to-enable-automatic-import-of-bank-statements"></a>So aktivieren Sie das automatische Importieren von Bankauszügen
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Zeile für ein verknüpftes Bankkonto aus, und wählen Sie dann die Aktion **Setup für automatischen Bankauszugsimport** aus.
3. Geben Sie im Fenster **Setup für automatischen Bankauszugsimport** im Feld **Anzahl der inbegriffenen Tage** an, für wie weit zurück Sie neue Banktransaktionen erhalten.

    > [!NOTE]  
>   Es wird empfohlen diesen Wert auf 7 Tage oder mehr festzulegen.  
4. Aktivieren Sie das Kontrollkästchen **Aktiviert**.  

Jede Stunde wird das Fenster **Zahlungsabstimmungsbuch.-Blatt** mit allen neuen Zahlungen ausgefüllt, die auf dem Onlinebankkonto getätigt wurden.

> [!NOTE]  
>   Transaktionen für Zahlungen, die bereits als ausgeführt und/oder abgestimmt im Fenster **Zahlungsabstimmungsbuch.-Blatt** gebucht wurden, werden nicht importiert.

## <a name="see-also"></a>Siehe auch
[Einrichten von Banken](bank-setup-banking.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

