---
title: 'So geht''s: Einrichten des Bankfeeddienstes Envestnet Yodlee| Microsoft Docs'
description: 'Gewusst wie: Einrichten des Envestnet Yodlee Bank-Feed-Service'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 62c314958700257f5889b69c8724a4348929765f
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Gewusst wie: Einrichten des Envestnet Yodlee Bank-Feed-Service
<a id="how-to-set-up-the-envestnet-yodlee-bank-feeds-service" class="xliff"></a>
Sie können elektronische Bankauszüge von Ihrer Bank importieren, um das Fenster **Zahlungsabstimmungsbuch.-Blatt** schnell auszufüllen und so Zahlungen zu begleichen und das Bankkonto auszugleichen. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Der Bankfeeddienst Envestnet Yodlee wird als eine Erweiterung zum [!INCLUDE[d365fin](includes/d365fin_md.md)] eingerichtet und steht zur Aktivierung bereit. Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)] mithilfe von Erweiterungen](ui-extensions.md).

Wenn Sie den Bankfeeddienst aktiviert haben, müssen Sie das beteiligte Bankkonto mit dem Onlinebankkonto verknüpfen, von dem der Feed stammt. In den folgenden unterschiedlichen Szenarios verknüpfen Sie Bankkonten mit Onlinebankkonten:

* Im [!INCLUDE[d365fin](includes/d365fin_md.md)] ist kein Bankkonto für Ihr Onlinebankkonto vorhanden. Daher erstellen Sie das Bankkonto über eine Verknüpfung mit dem Onlinebankkonto.
* Im [!INCLUDE[d365fin](includes/d365fin_md.md)] ist bereits ein Bankkonto vorhanden, das Sie mit einem Onlinebankkonto verknüpfen möchten.
* Bei einem verknüpften Bankkonto muss die Verknüpfung entfernt werden, da Sie den Bankfeeddienst für dieses Konto beenden möchten.
* Die Onlinebankkonten haben geändert und Sie möchten die Informationen zu den Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktualisieren.

Wenn der Bankfeeddienst aktiviert ist, können Sie ein Bankkonto so einrichten, dass automatisch alle zwei Stunden neue Bankauszüge in das Fenster **Zahlungsabstimmungsbuch.-Blatt** importiert werden. Transaktionen für Zahlungen, die bereits als ausgeführt und/oder abgestimmt im Fenster **Zahlungsabstimmungsbuch.-Blatt** gebucht wurden, werden nicht importiert. Weitere Informationen finden Sie im Abschnitt “So aktivieren Sie das automatische Importieren von Bankauszügen”.

**Hinweis**: Wenn Sie die unterstützte Einrichtung über "Unternehmen einrichten" verwenden, werden einige der folgenden Schritte automatisch beim Einrichten von Unternehmensbankkonten ausgeführt. Weitere Informationen finden Sie unter [Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).

## So aktivieren Sie den Bankfeeddienst
<a id="to-enable-the-bank-feed-service" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie das Bankkonto, das Sie für den Bankfeeddienst verwenden werden.
3. Wählen Sie im Fenster **Bankkonto** im Feld **Format Bankauszugimport** YODLEEBANKFEED aus.  

Der Bankfeeddienst wird aktiviert, wenn Sie ein Bankkonto mit den dazugehörigen Onlinebankkonto verknüpfen. Siehe das folgende Verfahren.  

## So erstellen Sie ein neues verknüpftes Bankkonto
<a id="to-create-a-new-linked-bank-account" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie das entsprechende Bankkonto aus, und wählen Sie dann **Neues verknüpftes Bankkonto erstellen**. Das Fenster **Bankkontenverknüpfung** wird nach wenigen Augenblicken geöffnet.

    **Hinweis:** Dieses Fenster zeigt die tatsächliche Webseite des Bankfeeddienstes Envestnet Yodlee an. Die Terminologie und die Funktionen im Fenster weichen möglicherweise von den Anweisungen ab, die in diesem Thema bereitgestellt werden.  
3. Verwenden Sie die Suchfunktion im Fenster **Onlinebankkonto-Verknüpfung** im Bereich **Konto verknüpfen**, um die Bank zu suchen, bei der Sie ein oder mehrere Onlinebankkonten haben.
4. Wählen Sie den Banknamen aus. Der Bereich **Anmeldung** wird geöffnet.
5. Geben Sie den Benutzernamen und das Kennwort, das Sie für die Ameldung bei der Onlinebank verwenden, an, und wählen Sie dann die Schaltfläche **Weiter** .  
6. Der Bankfeeddienst bereitet die Verknüpfung des ersten Onlinebankkontos der angegebenen Bank mit einem neuen Bankkonto in [!INCLUDE[d365fin](includes/d365fin_md.md)] vor.

    **Hinweis:** Wenn Sie mehr als ein Onlinebankkonto bei der Bank haben, müssen Sie für alle zusätzlichen Onlinebankkonten weitere Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen. Siehe Schritte 8 bis 10.  

    Wenn der Prozess erfolgreich abgeschlossen ist, erscheint der Bankname im Bereich **Meine Konten** der Registerkarte **Verknüpft** . Die Nummer in Klammern gibt an, wie viele Onlinebankkonten verknüpft wurden.  
7. Wählen Sie die Schaltfläche **OK** aus.

    Wenn Sie nur Online ein Bankkonto verknüpfen, wird das Fenster **Bankkontokarte** geöffnet und zeigt den Namen des Online Bankkontos an. In diesem Fall ist die Bankkontoverknüpfung abgeschlossen. Jetzt müssen Sie nur noch das Bankkonto einrichten. Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-how-setup-bank-accounts.md).

    Wenn mehr als ein Onlinebankkonto verknüpft wurde, öffnet sich das Fenster **Bankkontenverknüpfung** und die zusätzlichen Onlinebankkonten, die nicht mit den Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] verknüpft sind, werden aufgelistet. In diesem Fall, folgen Sie dem nächsten Schritt.  
8. Wählen Sie im Fenster **Bankkontenverknüpfung** die Zeile für ein Onlinebankkonto aus, und wählen Sie dann die Aktion **Mit neuem Onlinebankkonto verknüpfen**.  

    Das Fenster **Bankkontokarte** wird für ein neues Bankkonto geöffnet und der Name des Onlinebankkontos wird angezeigt.

    Wenn in [!INCLUDE[d365fin](includes/d365fin_md.md)] bereits ein Bankkonto vorhanden ist, mit dem Sie das zusätzliche Onlinebankkonto verknüpfen möchten, folgen Sie dem nächsten Schritt.  
9. Wählen Sie im Fenster **Bankkontenverknüpfung** die Zeile für ein Onlinebankkonto aus, und wählen Sie dann die Aktion **Mit vorhandenem Onlinebankkonto verknüpfen**.
10. Wählen Sie im Fenster **Bankkontenübersicht** das Bankkonto aus, mit dem Sie eine Verknüpfung erstellen möchten, und klicken Sie anschließend auf **OK**.

## So verknüpfen Sie ein Bankkonto mit einem Onlinebankkonto
<a id="to-link-a-bank-account-to-an-online-bank-account" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Zeile des Bankkontos aus, das nicht mit einem Onlinebankkonto verknüpft ist, und wählen Sie dann die Aktion **Verknüpfen mit Onlinebankkonto** . Das Fenster **Onlinebankkonto-Verknüpfung** wird für ein neues Bankkonto geöffnet und der Name des Onlinebankkontos ist bereits im Bereich **Konto verknüpfen** eingefügt.
3. Wählen Sie den Banknamen aus. Der Bereich **Anmeldung** wird geöffnet.
4. Geben Sie den Benutzernamen und das Kennwort, das Sie für die Ameldung bei der Onlinebank verwenden, an, und wählen Sie dann die Schaltfläche **Weiter** .  

    Der Bankfeeddienst bereitet die Verknüpfung Ihres Bankkontos in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit dem entsprechenden Onlinebankkonto vor.  

    Wenn der Prozess erfolgreich abgeschlossen ist, erscheint der Bankname im Bereich **Meine Konten** der Registerkarte **Verknüpft** . Wenn die Bank mehr als ein Bankkonto hat, wird nur das Bankkonto, das Sie in Schritt 2 ausgewählt haben, verknüpft.  
5. Wählen Sie die Schaltfläche **OK** aus.

Im Fenster **Bankkontenübersicht** ist das Kontrollkästchen **Verknüpft** aktiviert.

## So heben Sie die Verknüpfung mit dem Bankkonto auf
<a id="to-unlink-a-bank-account" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die Zeile des verknüpften Bankkontos aus, dessen Verknüpfung mit einem Onlinebankkonto aufgehoben werden soll, und wählen Sie dann die Aktion **Verknüpfung mit Onlinebankkonto aufheben**.

**Hinweis:** Wenn Sie **Ja** im Bestätigungsdialogfeld auswählen, wird die Verknüpfung mit dem Onlinebankkonto entfernt und die Anmeldedaten gelöscht. Um das Bankkonto wieder mit dem Onlinebankkonto zu verknüpfen, müssen Sie sich erneut bei der Bank anmelden. Weitere Informationen finden Sie im Abschnitt “So verknüpfen Sie ein Bankkonto mit einem Onlinebankkonto“.

## So aktualisieren Sie die Bankkontoverknüpfung
<a id="to-update-bank-account-linking" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie das entsprechende Bankkonto aus, und wählen Sie dann die Aktion **Bankkontoverknüpfung aktualisieren**.

Wenn Probleme für ein oder mehrere der verknüpften Bankkonten im Fenster **Bankkontenübersicht** vorhanden sind, wird das Fenster **Bankkontenverknüpfung** geöffnet und zeigt an, welche der Bankkonten Probleme haben. Probleme werden am besten gelöst, indem sie die Verknüpfung mit dem Onlinebankkonto entfernen und dann die Verknüpfung neu erstellen. Weitere Informationen finden Sie im Abschnitt “So verknüpfen Sie ein Bankkonto mit einem Onlinebankkonto“.

## So aktivieren Sie das automatische Importieren von Bankauszügen
<a id="to-enable-automatic-import-of-bank-statements" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Zeile für ein verknüpftes Bankkonto aus, und wählen Sie dann die Aktion **Setup für automatischen Bankauszugsimport** aus.
3. Geben Sie im Fenster **Setup für automatischen Bankauszugsimport** im Feld **Anzahl der inbegriffenen Tage** an, für wie weit zurück Sie neue Banktransaktionen erhalten.

    **Hinweis**: Es wird empfohlen diesen Wert auf 7 Tage oder mehr festzulegen.  
4. Aktivieren Sie das Kontrollkästchen **Aktiviert**.  

Jede Stunde wird das Fenster **Zahlungsabstimmungsbuch.-Blatt** mit allen neuen Zahlungen ausgefüllt, die auf dem Onlinebankkonto getätigt wurden.

**Hinweis:** Transaktionen für Zahlungen, die bereits als ausgeführt und/oder abgestimmt im Fenster **Zahlungsabstimmungsbuch.-Blatt** gebucht wurden, werden nicht importiert.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Einrichten von Banken](bank-setup-banking.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)] mithilfe der Erweiterungen] (ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

