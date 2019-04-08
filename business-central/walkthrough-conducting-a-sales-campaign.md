---
title: 'Exemplarische Vorgehensweise: Durchführen einer Verkaufskampagne | Microsoft Docs'
description: Eine Kampagne ist eine Aktivität, die mehrere Kontakte umfasst. Ein wichtiger Schritt beim Einrichten einer Kampagne ist die Auswahl der Zielgruppe. Zu diesem Zweck erstellen Sie in Business Central mithilfe von Filtern ein Segment bzw. eine Gruppe von Kontakten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 1922c9c2112006b302851301224818f803d9f4e2
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798845"
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Exemplarische Vorgehensweise: Durchführen einer Verkaufskampagne
Eine Kampagne ist eine Aktivität, die mehrere Kontakte umfasst. Ein wichtiger Schritt beim Einrichten einer Kampagne ist die Auswahl der Zielgruppe. Zu diesem Zweck erstellen Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] mithilfe von Filtern ein Segment bzw. eine Gruppe von Kontakten.  

 Mit den entsprechenden Funktionen in "Verkauf und Marketing" können Sie Ihre Marketingaktivitäten sorgfältig planen und die Aktivitäten mit Kontakten und Debitoren verwalten. Sie können Kampagnen erstellen und Segmente Ihrer Kontakte für Verteiler und andere Formen der Interaktion mit Debitoren und Interessenten einrichten.  

 Die Kampagnen- und Segmentfunktionen enthalten automatisierte Prozesse zum Planen, Organisieren und Verfolgen der Marketingaktivitäten. Mit diesen Funktionen verbessern Sie Ihre Chancen, neue Debitoren zu gewinnen und bestehende Debitoren zu halten.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
 In dieser exemplarischen Vorgehensweise wird die Nachbereitung einer Messe und die Ausrichtung einer Folgekampagne auf Interessenten (Kontakte) erläutert.  

 Die Kampagnen- und Segmentverwaltungsfunktionen der Abteilung "Verkauf und Marketing" werden in der exemplarischen Vorgehensweise vorgestellt. In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

-   Einrichten einer Kampagne  
-   Auswählen der Zielgruppe  
-   Data Mining  
-   Senden von Briefen an Kontakte  
-   Erfassen von Kampagnenreaktionen  

## <a name="roles"></a>Rollen  
 Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:  

-   Marketingmanager oder Vertriebsmanager  
-   Marketingmitarbeiter  

## <a name="prerequisites"></a>Voraussetzungen  
 Bevor Sie die Aufgaben in dieser Demonstration ausführen, müssen Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] installieren.  

## <a name="story"></a>Hintergrund  
 Der Marketingmanager in der Verkaufsabteilung der CRONUS ist für die Planung und Durchführung von Kampagnen verantwortlich. Er entscheidet auch, an welchen Messen das Unternehmen teilnimmt, und bewertet den Fortschritt von Kampagnen.  

 Der Marketingmitarbeiter in der Marketingabteilung ist für die Herstellung, Verteilung und Platzierung von Marketingmaterial zuständig.  

 Das Unternehmen hat gerade ein neues Produkt namens Millennium Server auf den Markt gebracht. Das Produkt wurde kürzlich auf einer Messe vorgestellt, der Computer Futurus. Viele Debitoren haben großes Interesse am Produkt beDebitort, und im Rahmen der Werbeinitiative wurde Debitoren, die Millennium Server während des Kampagnenzeitraums erworben haben, ein spezieller Kampagnenpreis angeboten.  

 Eine der Aufgaben des Marketingmitarbeiters nach der Messe ist die Erfassung aller Interessenten als Kontakte im System.  

 Der Marketingmanager richtet eine Kampagne ein, erstellt ein Segment, das alle neuen Kontakte enthält, und wählt dann mittels Data-Mining aus den Kontaktdaten die Zielgruppe für die Kampagne aus.  

 Der Marketingmitarbeiter sendet Dankschreiben an alle Kontakte, die ihre Geschäftskarten am Stand hinterlassen haben, und zum Schluss erfasst der Marketingmanager alle Reaktionen, die sie von Interessenten erhalten.  

## <a name="setting-up-a-campaign"></a>Einrichten einer Kampagne  
 Sobald der Marketingmitarbeiter die Geschäftskarten von der Messe erfasst hat, richtet der Marketingmanager eine Kampagnenkarte zum Verwalten der Kampagnenaktivitäten ein.  

### <a name="to-set-up-a-campaign"></a>So richten Sie eine Kampagne ein  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kampagnen** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die **Neu** Aktion aus, um eine neue Kampagne zu erstellen. Klicken Sie auf die Kampagnenkarte, drücken Sie die Eingabetaste, um eine Kampagnennummer automatisch einfügen zu lassen.  
3.  Geben Sie im Feld **Beschreibung** eine Beschreibung für die Kampagne ein, z. B. **FUTURUS-Messe**.  
4.  Wählen Sie das Feld **Statuscode** und wählen Sie auf der Seite **Kampagnenstatus** einen Statuscode aus der List aus, die sich öffnet, aus.  
5.  Füllen Sie die Felder **Startdatum** und **Enddatum** der Kampagne aus.  

## <a name="selecting-the-target-audience"></a>Auswählen der Zielgruppe  
 Der Marketingmanager erstellt ein Segment, um die Kontakte auszuwählen, mit denen er interagieren möchte.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>So erstellen Sie ein Segment mit den relevanten Kontakten  

1.  Wählen Sie die Aktion **Segmente** aus.  
2.  Wählen Sie die **Neu** Aktion aus, um ein neues Segment zu erstellen. Klicken Sie auf die Segmentkarte, drücken Sie die Eingabetaste, um eine Segmentnummer automatisch einfügen zu lassen.  
3.  Geben Sie auf dem Inforegister **Allgemein** im Feld **Beschreibung** z. B. **Besucher bei der FUTURUS-Messe** ein.  

     Nach der Eingabe der allgemeinen Informationen zum Segment wählen Sie die gewünschten Kontakte für das Segment aus.  

     Sie können zum Auswählen der Kontakte verschiedene Kriterien verwenden, z. B. Kontaktpersonen an einem (potenziellen) Debitorenstandort, die im Unternehmen für den Einkauf zuständig sind.  

     Sie verwenden Filter, um Kontakte nach den Kriterien hinzuzufügen, die für Ihre Zwecke am besten geeignet sind. Mithilfe von Filtern können Sie Kontakte z. B. nach der Verantwortlichkeit der Kontaktperson oder der Geschäftsbeziehung oder Branche des Unternehmens hinzufügen. In dieser Demonstration verwenden Sie den Filter **Verantwortlichkeit** zum Auswählen von Kontakten.  

4.  Auf der Seite **Segment** wählen Sie die **Kontakte hinzufügen** Aktion aus, den Filter **Kontakte hinzufügen** zu öffnen.  
5.  Wählen Sie auf dem Inforegister **Verantwortlichkeit** den Filter **Einkauf** als **Verantwortlichkeitscode** aus, und wählen Sie dann die Schaltfläche **OK**.  

     Die Seite **Segment** enthält jetzt eine auf dem eingegebenen Filter beruhende Liste von Kontakten. Im Inforegister **Allgemein** im Feld **Anzahl Zeilen** können Sie auf einen Blick die Anzahl der Kontakte sehen, die diesen Kriterien entsprechen.  

    > [!NOTE]  
    >  Sie können die Segmentierungskriterien zur Wiederverwendung speichern.

    1.  Auf der Seite **Segment** wählen Sie die **Segment** Aktion aus, und wählen Sie die **Speicherkriterien** Aktion aus.  
    2.  Geben Sie auf der Seite **Segmentkriterien speichern** einen Code für das Segment ein. Geben Sie im Feld **Beschreibung** eine  der Segmentkriterien ein.
    3.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="mining-the-data"></a>Data Mining  
 Der Marketingmanager untersucht die segmentierte Kontaktliste genauer und stellt fest, dass die Liste viel zu umfangreich ist. Er entscheidet, die Liste basierend auf tatsächlichen Interessenten einzuschränken, um sicherzustellen, dass er sich auf die richtige Zielgruppe konzentriert. Dieser Prozess der Neudefinition und Reduktion der Daten wird als Data Mining bezeichnet.  

### <a name="to-remove-contacts-from-the-segment"></a>So entfernen Sie Kontakte aus dem Segment  

1.  Klicken Sie auf der Seite **Segment** auf Aktionen, zeigen Sie auf Funktionen, klicken Sie auf **Kontakte** und klicken Sie dann auf **Kontakte ausblenden**, um die Seite **Kontakte entfernen - Ausblenden** zu öffnen.  
2.  Wählen Sie auf dem Inforegister **Geschäftsbeziehung** den Filter **INTERESS** als **Geschäftsbeziehungscode** aus, und wählen Sie dann die Schaltfläche **OK**.  

     Die Seite **Segment** enthält jetzt eine eingeschränkte Liste von Kontakten, und im Feld **Anzahl Zeilen** wird angezeigt, wie viele Kontakte diesen neuen Kriterien entsprechen.  

    > [!NOTE]  
    >  Wenn Sie das Entfernen einer Gruppe von Kontakten rückgängig machen müssen, können Sie dazu die Funktion **Ein Kriterium zurück** verwenden. Anders gesagt, Sie können die letzte Segmentierung rückgängig machen.  
    >   
    >  Auf der Seite **Segment** wählen Sie die **Segment** Aktion aus, und wählen Sie die **Zurück** Aktion aus.  
    >   
    >  Die Kontakte, die Sie soeben entfernt haben, werden wieder in die Liste der Kontakte eingefügt.  

## <a name="linking-a-segment-to-a-campaign"></a>Verknüpfen eines Segments mit einer Kampagne  
 Der Marketingmanager entscheidet, dass die reduzierte Liste als endgültige Kontaktliste für die Kampagne verwendet werden soll. Daher verknüpft er dieses Segment mit der Kampagne "FUTURUS-Messe".  

### <a name="to-link-a-segment-to-the-campaign"></a>So verknüpfen Sie ein Segment mit der Kampagne  

1.  Auf der Seite **Segment** im Inforegister **Kampagne**, **Kampagnennr.** Feld, um die Kampagne auszuwählen, zu der Sie das Segment zuordnen möchten **KP0001**.  
2.  Da dieses Segment die Zielgruppe der Kampagne darstellt, aktivieren Sie das Kästchen **Kampagnenziel**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Senden von Briefen und E-Mail-Nachrichten an Kontakte  
 Der Marketingmitarbeiter hilft dem Marketingmanager, Korrespondenz an Interessenten zu senden, in dem er ihnen für den Besuch auf der Messe dankt.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>So verwenden Sie ein Segment, um einen Brief an einen Kontakt zu senden  

1.  Öffnen Sie die Karte **Segment** für **Besucher bei der FUTURUS-Messe**.  
2.  Wählen Sie auf dem Inforegister **Interaktion** im Feld **Aktivitätenvorlagencode** die Vorlage für Geschäftsbriefe, mit dem Code **GESCHÄFT** aus.  
3.  Geben Sie im Feld **Betreff (Standard)** den folgenden Beispieltext ein: **Vielen Dank für Ihren Besuch auf der Messe**.  

    > [!NOTE]  
    >  Diese Vorlage besteht aus mehreren Anlagen, die alle in jeweils unterschiedlicher Sprache verfasst sind. Zu den Beispielsprachen gehören auch Englisch und Dänisch.  

4.  Wählen Sie das Feld **Sprachcode (Standard)**, um die Seite **Segmentaktivitätensprachen** zu öffnen. Wählen Sie einen Sprachcode aus, und wählen Sie dann die Schaltfläche **OK**.  
5.  Sie können das Dokument in der ausgewählten Sprache anzeigen. Wählen Sie die **Dateianhang** Aktion aus, und wählen Sie die **Öffnen** Aktion aus.  

     Um die Nachricht zu beantworten, die nach der Berechtigung zum Starten von Word fragt, wählen Sie die Option **Für diese Clientsitzung zulassen** aus.  

     Dadurch wird das angefügte Word-Dokument geöffnet, sodass Sie es prüfen können. Sie können auch die Gelegenheit nutzen und den Brief bearbeiten bzw. verändern. Schließen Sie anschließend Word.  

6.  Geben Sie den Betreff des Briefs in das Feld **Betreff** ein (in der ausgewählten Sprache für die Vorlage).  
7.  Wählen Sie die Aktion **Protokoll** aus.
8.  Wählen Sie das Feld **Dateianhänge senden**, um die Dateianhänge auszudrucken.  

    1. Wählen Sie das Kontrollkästchen **Anschluss-Segment erstellen**.  
    2. Wählen Sie die Schaltfläche **OK** um den Batchauftrag **Segment protokollieren** zu starten.  

9. Die Dateianhänge werden gesendet. Wenn der Vorgang abgeschlossen ist, wählen Sie die Schaltfläche **OK** für die Meldung aus, die angibt, dass das Segment protokolliert wurde.  

     Die Briefe werden automatisch gedruckt, und das Segment wird protokolliert. Da das Segment protokolliert wurde, ist es nicht mehr in der Liste der Segmente vorhanden, sondern wurde in die Liste der protokollierten Segmente verschoben. Wenn Sie diese Liste anzeigen möchten, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Protokollierte Segmente** ein, und wählen dann den zugehörigen Link aus.  

10. Nachdem das Segment protokolliert ist, wird jeder Brief, der versendet wurde, als Aktivität gespeichert, die Sie im Protokoll einsehen können.  

     Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aktivitätenprotokollposten** ein, und wählen dann den zugehörigen Link aus. Es gibt jeweils einen Posten für jeden gesendeten Brief.  

### <a name="to-send-an-email-message-to-a-contact"></a>So senden Sie eine E-Mail-Nachricht an einen Kontakt  

1.  Wählen Sie auf dem Inforegister **Interaktion** im Feld **Aktivitätenvorlagencode** die Vorlage für Geschäftsbriefe, mit dem Code **GESCHÄFT** aus.  
2.  Geben Sie im Feld **Betreff (Standard)** den folgenden Beispieltext ein: **Vielen Dank für Ihren Besuch auf der Messe**.  
3.  Wählen Sie im Feld **Korrespondenzart** **E-Mail** aus.  
4.  Geben Sie Spracheneinstellungen, wie im vorhergegangenen Verfahren, an.  
5.  Wählen Sie die Aktion **Protokoll** aus. Die Seite **Segment protokollieren** wird geöffnet.  
6.  Wählen Sie das Feld **Dateianhänge senden**, um die Dateianhänge per E-Mail zu versenden.  
7.  Wählen Sie das Kontrollkästchen **Anschluss-Segment erstellen**.  
8.  Wählen Sie die Schaltfläche **OK** aus.  

     Die Briefe werden automatisch per E-Mail gesendet, und das Segment wird protokolliert. Da das Segment protokolliert wurde, ist es nicht mehr in der Liste der Segmente vorhanden, sondern wurde in der Liste der protokollierten Segmente gespeichert. Wenn Sie diese Liste anzeigen möchten, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Protokollierte Segmente** ein, und wählen dann den zugehörigen Link aus.  

## <a name="registering-campaign-responses"></a>Erfassen von Kampagnenreaktionen  
 Im Laufe der nächsten Wochen antworten die Interessenten auf den Brief. Der Marketingmanager möchte die Reaktionen verfolgen und diese Interaktionen erfassen.  

 Zu diesem Zweck richten Sie ein Segment für die Kontakte ein, die auf den Brief reagiert haben.  

### <a name="to-register-campaign-responses"></a>So erfassen Sie Kampagnenreaktionen  

1.  Erweitern Sie auf der Seite **Segment** das Inforegister **Interaktion**.  
2.  Wählen Sie das Feld **Aktivitätenvorlagencode** aus.  

     Da keine Interaktionsvorlage für die Erfassung von Kampagnenreaktionen verfügbar ist, erstellen Sie eine neue Vorlage. Hierfür erstellen Sie eine neue Word-Dokumentvorlage.  

3.  Wählen Sie auf der Seite **Interaktionsvorlagen** **Neu**.  
4.  Geben Sie im Feld **Code** den Code **REAKT** und im Feld **Beschreibung** den Text **Kampagnenreaktionen** ein.  
5.  Wählen Sie die Schaltfläche **OK** aus.  
6.  Wählen Sie diese Aktivitätenvorlage im Feld **Aktivitätenvorlagencode** aus, und bestätigen Sie die Meldung, in der Sie gefragt werden, ob die Segmentszeilen mit diesem Aktivitätenvorlagencode aktualisiert werden sollen.  

     Geben Sie nun an, dass diese Kontakte auf die Kampagne reagiert haben:  
7.  Geben Sie auf im Inforegister **Beschaffung** im **Arbeitsplannr.** Feld, wählen Sie Ihre Kampagne aus.  
8.  Lassen Sie **Kampagnen.Nr.** Verlassen Sie das Feld Kampagnennr. und bestätigen Sie die Meldung, in der Sie gefragt werden, ob die Segmentszeilen mit diesem Aktivitätenvorlagencode aktualisiert werden sollen.  
9. Wählen Sie das Feld **Kampagnenreaktion** aus, und bestätigen Sie die nachfolgende Meldung.  

     Protokollieren Sie das Segment, um sicherzustellen, dass die Interaktionen erfasst werden.  
10. Wählen Sie auf der Seite **Segment** **Protokoll** aus.  
11. Deaktivieren Sie auf der Seite **Segment protokollieren** das Kontrollkästchen **Dateianhänge senden**, und wählen Sie dann die Schaltfläche **OK**, und bestätigen Sie die Meldung, die angezeigt wird.  

     Nachdem das Segment protokolliert wurde, wird automatisch ein Eintrag für die Kampagne erstellt, um diese Aktion auf der Seite **Kampagnenposten** zu erfassen.  

## <a name="see-also"></a>Siehe auch  
[Marketing & Vertrieb](marketing-relationship-management.md)  
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
