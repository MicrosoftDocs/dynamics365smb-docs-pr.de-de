---
title: 'Anhänge, Links und Notizen zu Datensätzen hinzufügen'
description: 'Fügen Sie einen Hyperlink zu einem Beleg oder eine Website zu einem bestimmten Datensatz hinzu, z. B. zu einem Debitor oder einem Dokument.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/15/2023
ms.custom: bap-template
ms-service: dynamics-365-business-central
ms.service: dynamics-365-business-central
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten

Auf den meisten Listenseinten, karten und Belegen können Sie auf der Registerkarte **Anhänge** im Bereich **Infobox** Dateien anhängen, Links hinzufügen und Notizen schreiben. Die Zahl im Titel der Registerkarte gibt an, wie viele angehängte Dateien, Links oder Notizen für die Karte oder der Beleg vorhanden sind.

Auf dem Inforegister **Zeilen** können Sie auch die Aktion **Anhänge** verwenden, um Belege an eine bestimmte Zeile anzuhängen. Beispielsweise möchten Sie möglicherweise Designspezifikationen an einen Artikel auf einer Einkaufsrechnung anhängen.

Anhänge, Links und Notizen bleiben an die Karte oder den Beleg angehängt, während sie/er in andere Status umgewandelt wird. Beispielsweise von einem laufenden Verkaufsauftrag zu einer gebuchten Verkaufsrechnung. Allerdings wird keiner der Anhangstypen vom System ausgegeben, z. B. beim Drucken oder beim Speichern in einer Datei.

Sie können den E-Mails, die Sie von [!INCLUDE [prod_short](includes/prod_short.md)] senden, auch Anhänge hinzufügen. Wenn Sie eine E-Mail direkt aus einem Beleg, z. B. einem Verkaufsangebot, senden, können Sie mit der Aktion **Datei aus Herkunftsbeleg hinzufügen** angehängte Dateien auswählen. Sie können nur Dateien auswählen, die an den Beleg angehängt sind. Sie können keine Dateien auswählen, die an Zeilen angehängt sind.

> [!NOTE]
> Wenn Sie einen Verkaufsauftrag oder eine Einkaufsbestellung teilweise versenden und in Rechnung stellen, wird der Anhang nur der endgültigen Rechnung dieser Bestellung beigefügt. Wenn Sie Abgrenzungen in Rechnung stellen, wird der Anhang entsprechend an die Sachkontenbucheinträge für den Beleg angehängt, nicht jedoch an die Abgrenzungseinträge.
>
> Wenn Sie eine Bestellung löschen, bevor sie in Rechnung gestellt wird, wird auch der Anhang entfernt.
>
> Wenn Sie die Aktion **Belegzeilen abrufen** auf einer Kaufrechnung verwenden, wird der Anhang zu der dazugehörigen Bestellung zur Kaufrechnung hinzugefügt.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>So hängen Sie eine Datei an eine Eikaufsrechnung an

Sie können jede Art von Datei, z. B. Text-, Bild- oder Videodateien, an eine Karte, einen Beleg oder die Zeile eines Belegs anhängen. Dies ist beispielsweise nützlich, wenn Sie eine Lieferantenrechnung als PDF-Datei auf der zugehörigen Einkaufsrechnung in [!INCLUDE[prod_short](includes/prod_short.md)] speichern möchten.

> [!NOTE]
> Dateien, die mit der Funktion Eingehende Belege angehängt sind, werden auf der Registerkarte **Anhänge** nicht eingeschlossen. Weitere Informationen finden Sie unter [Eingehende Belege](across-income-documents.md). Dasselbe gilt für Dateien, die an Zeilen von Belegen angehängt sind.

Das folgende Verfahren basiert auf einer Einkaufsrechnung. Die Schritte sind für alle anderen unterstützten Dokumente und Karten ähnlich.

> [!TIP]
> Wenn Ihr Anhang spezifisch für eine Zeile in einem Beleg ist, können Sie ihn an die Zeile anhängen. Wählen Sie die Zeile und dann die Aktion **Anhänge** aus.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Einkaufsrechnung, die Sie einer Datei zuordnen möchten.
3. Wählen Sie im Bereich **Infobox** die Registerkarte **Anhänge**.
4. Wählen Sie den Wert hinter dem Feld **Belege** z. B. "0".
5. Wählen Sie auf der Seite **Angefügte Belege** das Feld **Anhang** aus.
6. Führen Sie im Dialogfeld **Beleg anhängen** einen der folgenden Schritte aus, um eine Datei anzuhängen:

   [!INCLUDE[file-upload](includes/file-upload.md)]

Die Datei wird nun der Einkaufsrechnung zugeordnet.

## <a name="to-view-an-attached-file"></a>So zeigen Sie eine angehängte Datei an

1. Öffnen Sie in der Infobox die Registerkarte **Anhänge**.
2. Wählen Sie den Wert hinter dem Feld **Belege** z. B. "1".
3. Wählen Sie auf der Seite **Angefügte Dokumente** die Aktion **Vorschau** aus.
4. Öffnen Sie die heruntergeladene Datei.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>So speichern Sie ein Dokument als PDF-Anhang

Wann immer Sie ein Dokument als Datei speichern müssen, können Sie die Aktion **Anhängen als PDF** verwenden, um den aktuellen Dokumentinhalt als PDF-Datei zu erfassen, die an die FactBox des Dokuments angehängt wird. Dies ist z.B. nützlich, wenn Dokumente mehreren Schritten in einem Prozess folgen, wie z.B. einem Verkaufsprozess oder einem Genehmigungs-Workflow, und Sie sich auf einen Ausdruck des vorherigen Schritts beziehen möchten.

Das folgende Verfahren basiert auf einer Auftragsabwicklung. Die Schritte sind für alle unterstützten Dokumente ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Markieren Sie einen Debitorenauftrag, und wählen Sie dann die Aktion **Anhängen als PDF**.

Eine PDF-Datei mit dem aktuellen Inhalt des Kundenauftrags wird der Registerkarte **Anlagen** im Infoboxbereich hinzugefügt.

## <a name="to-add-a-link-from-an-item-card"></a>Um einen Link von einer Artikelkarte hinzuzufügen

Sie können einen Link von einer Karte oder einem Beleg zu einer beliebigen URL hinzufügen. Dies ist beispielsweise hilfreich, wenn Sie eine Artikelkarte mit dem Artikelkatalog des Lieferanten verknüpfen möchten.

Das folgende Verfahren basiert auf einer Elementkarte. Die Schritte sind für alle anderen unterstützten Belege und Karten gleich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Element aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.
3. In dem **Link**, wählen Sie das **+** Symbol.
4. Geben Sie im Feld **Link Adresse** den Link ein.

    Der Link muss eine gültige Internet- oder Intranet-URL sein.

5. Geben Sie im Feld **Beschreibung** die Informationen zu dem Link ein.  
6. Wählen Sie die Schaltfläche **OK** aus.

Der Link ist jetzt an die Artikel-Karte angehängt.  

## <a name="to-write-a-note-on-a-sales-order"></a>So schreiben Sie eine Notiz zu einem Verkaufsauftrag

Sie können eine Notiz auf ein Dokument oder eine Karte schreiben, um beispielsweise anderen Benutzern des Dokuments oder der Karte spezielle Anweisungen zu übermitteln. Sie können Dateilinks und URLs in Notizen einfügen.

> [!NOTE]
> Hinweise auf der Registerkarte **Anhänge** haben nichts mit der internen Notizfunktion zu tun, die hauptsächlich für die Kommunikation zwischen Workflowbenutzern verwendet wird. Weitere Informationen finden Sie unter [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md).

Das folgende Verfahren basiert auf einer Auftragsabwicklung. Die Schritte sind für alle anderen unterstützten Belege und Karten ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Verkaufsauftrag aus, zu dem Sie einen Link hinzufügen möchten, und wählen Sie dann die Registerkarte **Anhänge** in der Infobox.
3. In dem Abschnitt **Notizen** wählen Sie das **+** Symbol.
4. In dem Feld **Hinweis** geben Sie in das Feld einen beliebigen Text ein, z. B. "Dies ist eine dringende Bestellung.".
5. Wählen Sie die Schaltfläche **OK**.

Der Hinweis ist jetzt dem Verkaufsauftrag beigefügt.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eingehende Belege](across-income-documents.md)  
[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
