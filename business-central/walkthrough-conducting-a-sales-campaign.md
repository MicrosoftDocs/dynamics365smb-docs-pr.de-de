---
title: 'Exemplarische Vorgehensweise: Durchführen einer Verkaufskampagne'
description: 'Diese exemplarische Vorgehensweise gibt einen detaillierten Überblick über alle Aufgaben, die bei der Durchführung einer Verkaufskampagne in Business Central anfallen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 01/31/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Exemplarische Vorgehensweise: Durchführen einer Verkaufskampagne

Eine Kampagne ist eine Aktivität, die mehrere Kontakte umfasst. Ein wichtiger Schritt beim Einrichten einer Kampagne ist die Auswahl der Zielgruppe. Zu diesem Zweck erstellen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe von Filtern ein Segment bzw. eine Gruppe von Kontakten.  

 Mit den entsprechenden Funktionen in "Verkauf und Marketing" können Sie Ihre Marketingaktivitäten sorgfältig planen und die Aktivitäten mit Kontakten und Debitoren verwalten. Sie können Kampagnen erstellen und Segmente Ihrer Kontakte für Verteiler und andere Formen der Interaktion mit Debitoren und Interessenten einrichten.  

 Die Kampagnen- und Segmentfunktionen enthalten automatisierte Prozesse zum Planen, Organisieren und Verfolgen der Marketingaktivitäten. Mit diesen Funktionen verbessern Sie Ihre Chancen, neue Debitoren zu gewinnen und bestehende Debitoren zu halten.  

## Informationen zu dieser exemplarischen Vorgehensweise

 In dieser exemplarischen Vorgehensweise wird die Nachbereitung einer Messe und die Ausrichtung einer Folgekampagne auf Interessenten (Kontakte) erläutert.  

 Die Kampagnen- und Segmentverwaltungsfunktionen der Abteilung "Verkauf und Marketing" werden in der exemplarischen Vorgehensweise vorgestellt. In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

- Vorbereiten der Daten
- Einrichten einer Kampagne  
- Auswählen der Zielgruppe  
- Data Mining  
- Senden von Briefen an Kontakte  
- Erfassen von Kampagnenreaktionen  

## Rollen

 Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:  

- Marketingmanager oder Vertriebsmanager  
- Marketingmitarbeiter  

## Voraussetzungen

 Bevor Sie die Aufgaben in dieser Demonstration ausführen, müssen Sie [!INCLUDE[prod_short](includes/prod_short.md)] installieren.  

## Hintergrund

 Der Marketingmanager in der Verkaufsabteilung der CRONUS ist für die Planung und Durchführung von Kampagnen verantwortlich. Der Marketingmanager entscheidet auch, an welchen Messen das Unternehmen teilnimmt, und bewertet den Fortschritt von Kampagnen.  

 Der Marketingmitarbeiter in der Marketingabteilung ist für die Herstellung, Verteilung und Platzierung von Marketingmaterial zuständig.  

 Das Unternehmen hat ein neues Produkt namens Rome Guest Chair auf den Markt gebracht. Das Produkt wurde kürzlich auf einer Messe vorgestellt, der Office Futurus. Viele Debitoren haben großes Interesse am Produkt beDebitort, und im Rahmen der Werbeinitiative wurde Debitoren, die Rome Guest Chair während des Kampagnenzeitraums erworben haben, ein spezieller Kampagnenpreis angeboten.  

 Eine der Aufgaben des Marketingmitarbeiters nach der Messe ist die Erfassung aller Interessenten als Kontakte im System.  

 Der Marketingmanager richtet eine Kampagne ein, erstellt ein Segment, das alle neuen Kontakte enthält, und wählt dann mittels Data-Mining aus den Kontaktdaten die Zielgruppe für die Kampagne aus.  

 Der Marketingmitarbeiter sendet Dankschreiben an alle Kontakte, die ihre Geschäftskarten am Stand hinterlassen haben, und zum Schluss erfasst der Marketingmanager alle Reaktionen, die sie von Interessenten erhalten.  

## Einrichten einer Kampagne

 Sobald der Marketingmitarbeiter die Geschäftskarten von der Messe erfasst hat, richtet der Marketingmanager eine Kampagnenkarte zum Verwalten der Kampagnenaktivitäten ein.  

### So richten Sie eine Kampagne ein  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kampagnen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die **Neu** Aktion aus, um eine neue Kampagne zu erstellen. Klicken Sie auf die Kampagnenkarte, wählen Sie die <kbd>Eingabetaste</kbd>, um eine Kampagnennummer automatisch einfügen zu lassen.  
3. Geben Sie im Feld **Beschreibung** eine Beschreibung für die Kampagne ein, z. B. **Office Futurus-Messe**.  
4. Wählen Sie das Feld **Statuscode** und den Statuscode „1-PLAN“ aus. 
5. Füllen Sie die Felder **Startdatum** und **Enddatum** der Kampagne aus.  

## Auswählen der Zielgruppe

 Der Marketingmanager erstellt ein Segment, um die Kontakte auszuwählen, mit denen er interagieren möchte.  
 
 Wenn Sie ein Segment erstellen, können Sie verschiedene Kriterien verwenden, um die Kontakte auszuwählen, die Ziele für das Segment sein müssen. Sie können beispielsweise Kontakte auswählen, die an einem (potenziellen) Kundenstandort arbeiten und für den Einkauf in ihrem Unternehmen verantwortlich sind. Sie verwenden Filter, um Kontakte nach den Kriterien hinzuzufügen, die für Ihre Zwecke am besten geeignet sind. Mithilfe von Filtern können Sie Kontakte z. B. nach der Verantwortlichkeit der Kontaktperson oder der Geschäftsbeziehung oder Branche des Unternehmens hinzufügen. In dieser Demonstration verwenden Sie den Filter **Verantwortlichkeit** zum Auswählen von Kontakten.

### So erstellen Sie ein Segment mit den relevanten Kontakten  

1. Wählen Sie die Aktion **Navigieren** und dann **Segmente** aus.  
2. Wählen Sie die **Neu** Aktion aus, um ein neues Segment zu erstellen. Klicken Sie auf die Segmentkarte, und wählen Sie **Eingabe** aus, um eine Segmentnummer automatisch einfügen zu lassen.  
3. Geben Sie im Inforegister **Allgemein** im Feld **Beschreibung** z. B. *Besucher bei der Office Futurus-Messe* ein.
4. Wählen Sie die Aktion **Kontakte hinzufügen** aus, um den Filter **Kontakte hinzufügen** zu öffnen.  
5. Führen Sie einen Bildlauf zum Inforegister **Kontakt Verantwortlichkeit** weiter unten durch, wählen Sie den Filter **Einkauf** als **Verantwortlichkeitscode** und dann die Schaltfläche **OK** aus.  

Die Seite **Segment** enthält jetzt eine auf dem eingegebenen Filter beruhende Liste von Kontakten. Im Inforegister **Allgemein** im Feld **Anzahl Zeilen** können Sie auf einen Blick die Anzahl der Kontakte sehen, die diesen Kriterien entsprechen.  

> [!NOTE]  
> Sie können die Segmentierungskriterien zur Wiederverwendung speichern.

### So speichern Sie Ihre Segmentierungskriterien

1. Wählen Sie auf der Seite **Segment** die Option **Aktionen** aus.
2. Wählen Sie **Funktionen**, dann **Segment** und anschließend die Aktion **Kriterien speichern** aus.  
3. Geben Sie auf der Seite **Segmentkriterien speichern** einen Code für das Segment ein. Geben Sie im Feld **Beschreibung** eines der Segmentkriterien ein.
4. Wählen Sie die Schaltfläche **OK** aus.  

## Data Mining

 Der Marketingmanager untersucht die segmentierte Kontaktliste genauer und stellt fest, dass die Liste viel zu groß ist. Der Manager entscheidet, die Liste basierend auf tatsächlichen Interessenten einzuschränken, um sicherzustellen, dass er sich auf die richtige Zielgruppe konzentriert. Dieser Prozess der Neudefinition und Reduktion der Daten wird als Data Mining bezeichnet.  

### So entfernen Sie Kontakte aus dem Segment  

1. Wählen Sie auf der Seite **Segment** die Option **Aktionen** aus.
2. Wählen Sie in der Menüleiste unten **Funktionen**, **Kontakte** und dann **Kontakte reduzieren** aus.  

  Daraufhin wird das Dialogfeld **Kontakte entfernen – Reduzieren** geöffnet.  
4. Wählen Sie im Inforegister **Kontakt Geschäftsbeziehung** den Filter **CUST** als **Geschäftsbeziehungscode** und dann die Schaltfläche **OK** aus.

 Die Seite **Segment** enthält jetzt eine eingeschränkte Liste von Kontakten, und im Feld **Anzahl Zeilen** wird angezeigt, wie viele Kontakte diesen neuen Kriterien entsprechen.  

 > [!NOTE]  
 > Wenn Sie das Entfernen einer Gruppe von Kontakten rückgängig machen müssen, können Sie dazu die Funktion **Ein Kriterium zurück** verwenden. Anders gesagt, Sie können die letzte Segmentierung rückgängig machen.  

### So stellen Sie die entfernten Kontakte wieder her

1. Wählen Sie auf der Seite **Segment** die Aktion **Protokoll** aus.
2. Wählen Sie die Aktion **Zurück** aus.

Die Kontakte, die Sie entfernt haben, werden wieder in die Liste der Kontakte eingefügt.

## Verknüpfen eines Segments mit einer Kampagne

Der Marketingmanager entscheidet, dass die reduzierte Liste als endgültige Kontaktliste für die Kampagne verwendet werden soll. Daher verknüpft er dieses Segment mit der Kampagne „FUTURUS-Messe“.  

### So verknüpfen Sie ein Segment mit der Kampagne  

1. Auf der Seite **Segment** im Inforegister **Kampagne**, **Kampagnennr.** Feld, um die Kampagne auszuwählen, zu der Sie das Segment zuordnen möchten **KP0001**.
2. Klicken Sie auf **Ja**.  
3. Da dieses Segment die Zielgruppe der Kampagne darstellt, aktivieren Sie das Kontrollkästchen **Kampagnenziel**, und wählen Sie **Ja** aus.  

## Senden von Briefen und E-Mail-Nachrichten an Kontakte

 Der Marketingmitarbeiter hilft dem Marketingmanager, Korrespondenz an Interessenten zu senden, in dem er ihnen für den Besuch auf der Messe dankt.

### So verwenden Sie ein Segment, um einen Brief an einen Kontakt zu senden  

> [!NOTE]  
> Bei diesem Verfahren müssen Sie ein Word-Dokument anhängen. Sie können Anhänge in jeder Sprache hinzufügen.

> [!NOTE]  
> Klicken Sie bei Bedarf auf das Symbol **Bleistift bearbeiten**, um die Seite im Bearbeitungsmodus zu öffnen.

1. Öffnen Sie die Karte **Segment** für **Besucher bei der FUTURUS-Messe**.  
2. Wählen Sie im Inforegister **Interaktion** im Feld **Aktivitätenvorlagencode** die Vorlage für Geschäftsbriefe mit dem Code **GESCHÄFT** und dann **Ja** aus.
3. Wählen Sie das Feld **Sprachcode (Standard)**, um die Seite **Segmentaktivitätensprachen** zu öffnen. Wählen Sie einen **Sprachcode** und dann die Schaltfläche **OK** aus.
4. Stellen Sie sicher, dass **Korrespondenzart (Standard)** auf **Brief** festgelegt ist.
5. Aktivieren Sie im Feld **Anhang** das Kontrollkästchen **Auslassungspunkte**. Daraufhin wird das Dialogfeld „Anhang importieren“ geöffnet.
    1. Wählen Sie die Schaltfläche **Auswählen** aus, um Ihre Datei auszuwählen.
    1. Suchen Sie die Datei, und wählen Sie die Schaltfläche **Öffnen** aus, um sie anzuhängen.
6. Geben Sie im Feld **Betreff (Standard)** den folgenden Beispieltext ein: **Vielen Dank für Ihren Besuch auf der Messe**. Wählen Sie die <kbd>Tab</kbd>-Taste, um das Feld zu verlassen, und wählen Sie die Schaltfläche **Ja** aus.
7. Aktivieren Sie die Option **Word-Dokumente als Anh. senden** über die Schiebeschaltfläche, und wählen Sie die Schaltfläche **Ja** aus.
8. Wählen Sie die Aktion **Protokoll** aus. Aktivieren Sie im Popupfenster „Segment protokollieren“ die Option **Anschluss-Segment erstellen**.
9. Wählen Sie die Schaltfläche **OK** aus, um den Batchauftrag **Segment protokollieren** zu starten.  

Die Dateianhänge werden gesendet. Wenn der Vorgang abgeschlossen ist, wählen Sie die Schaltfläche **OK** für die Meldung aus, die angibt, dass das Segment protokolliert wurde.  

 Die Briefe werden automatisch gedruckt, und das Segment wird protokolliert. Da das Segment protokolliert wurde, ist es nicht mehr in der Liste der Segmente vorhanden, sondern wurde in die Liste der protokollierten Segmente verschoben. Um diese Liste zu sehen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Protokollierte Segmente** ein und wählen Sie dann den zugehörigen Link.  

Nachdem das Segment protokolliert ist, wird jeder Brief, der versendet wurde, als Aktivität gespeichert, die Sie im Protokoll einsehen können.  

Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Interaktionsprotokollposten** ein und wählen Sie dann den zugehörigen Link. Es gibt jeweils einen Posten für jeden gesendeten Brief.  

### So senden Sie eine E-Mail-Nachricht an einen Kontakt  

1. Wählen Sie auf dem Inforegister **Interaktion** im Feld **Aktivitätenvorlagencode** die Vorlage für Geschäftsbriefe, mit dem Code **GESCHÄFT** aus.  
2. Geben Sie im Feld **Betreff (Standard)** den folgenden Beispieltext ein: **Vielen Dank für Ihren Besuch auf der Messe**.  
3. Wählen Sie im Feld **Korrespondenzart** **E-Mail** aus.  
4. Legen Sie Spracheinstellungen fest, und hängen Sie ein Word-Dokument an, wie im vorherigen Verfahren beschrieben.  
5. Wählen Sie die Aktion **Protokoll** aus. Die Seite **Segment protokollieren** wird geöffnet.  
6. Wählen Sie das Feld **Dateianhänge senden**, um die Dateianhänge per E-Mail zu versenden.  
7. Wählen Sie das Kontrollkästchen **Anschluss-Segment erstellen**.  
8. Wählen Sie die Schaltfläche **OK** aus.  

 Die Briefe werden automatisch per E-Mail gesendet, und das Segment wird protokolliert. Da das Segment protokolliert wurde, ist es nicht mehr in der Liste der Segmente vorhanden, sondern wurde in der Liste der protokollierten Segmente gespeichert. Um diese Liste zu sehen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Protokollierte Segmente** ein und wählen Sie dann den zugehörigen Link.  

## Kampagnenreaktionen erfassen

 Im Laufe der nächsten Wochen antworten die Interessenten auf den Brief. Der Marketingmanager möchte die Reaktionen verfolgen und diese Interaktionen erfassen.  

 Zu diesem Zweck richten Sie ein Segment für die Kontakte ein, die auf den Brief reagiert haben.  

### So erfassen Sie Kampagnenreaktionen  

1. Wählen Sie auf der Seite **Segment** im Inforegister **Interaktion** das Feld **Aktivitätenvorlagencode** aus.  

 Da keine Interaktionsvorlage für die Erfassung von Kampagnenreaktionen verfügbar ist, erstellen Sie eine neue Vorlage. Hierfür erstellen Sie eine neue Word-Dokumentvorlage.  

2. Wählen Sie im Dropdownmenü **Interaktionsvorlagen** die Aktion **Neu** aus.  
3. Geben Sie im Feld **Code** den Code **REAKT** und im Feld **Beschreibung** den Text **Kampagnenreaktionen** ein.  
4. Wählen Sie die Schaltfläche **OK**.
5. Wählen Sie **Ja** aus, um zu bestätigen, dass Sie diesen Aktivitätenvorlagencode auf alle Segmentzeilen anwenden möchten.
6. Wählen Sie im Inforegister **Kampagne** das Feld **Kampagnenreaktion** aus. Wählen Sie **Ja** aus, um die Nachricht *Sie haben die Kampagnenreaktion geändert* zu bestätigen.  
7. Wählen Sie auf der Seite **Segment** **Protokoll** aus.  
8. Deaktivieren Sie auf der Seite **Segment protokollieren** das Kontrollkästchen **Anhänge senden**. Wählen Sie dann die Schaltfläche **OK** aus, um die Meldung, dass das Segment protokolliert wurde, zu bestätigen.  
  
## Siehe auch  
[Marketing und Vertrieb](marketing-relationship-management.md)  
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
