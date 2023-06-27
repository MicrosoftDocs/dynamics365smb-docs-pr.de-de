---
title: Doppelte Debitoren- oder Kreditorendatensätze zusammenführen
description: 'Beschreibt, wie Informationen zu Kunden oder Lieferanten konsolidiert werden, wenn Sie doppelte Einträge zu einigen von ihnen haben.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="merge-duplicate-records" />Doppelt Datensätze zusammenführen

Wenn unterschiedliche Benutzer im Laufe der Zeit neue Debitoren-, Kreditoren- oder Kontaktkarten erstellen, oder die neuen Datensätze automatisch während der Migration erstellt werden, wird ein Debitor, ein Kreditor oder ein Kontakt im System mit mehr als einem Datensatz dargestellt. In diesem Fall können Sie die Seite **Doppelte Datensätze zusammenführen** aus der Karte des Datensatzes verwenden, den Sie erfassen möchten. Die Seite zeigt Ihnen eine Übersicht der duplizierten Feldwerte und bietet Funktionen, um auszuwählen, welche Werte behalten oder verworfen werden, wenn zwei Datensätze zusammengeführt werden.

> [!NOTE]
> Nur Benutzer mit dem Berechtigungssatz DOPPELTE DATENSÄTZE ZUSAMMENFÜHREN können diese Funktion verwenden.

> [!TIP]
> Auf der Seite **Doppelte Datensätze zusammenführen** werden alle Felder angezeigt, deren Werte für die zwei verglichenen Datensätze abweichen. Daher wird ein Duplikat von der Seite angezeigt, indem sehr wenige Felder eingeblendet werden. Wenn die Seite hingegen viele Felder anzeigt, dann ist der betreffende Datensatz wahrscheinlich kein Duplikat.

Das folgende Verfahren basiert auf einer Debitorenkarte. Die Schritte sind für Debitor- und Kontaktkarten ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Debitor, von dem Sie wissen oder vermuten, dass ein doppelter Datensatz für ihn existiert, und wählen Sie die dann die Aktion **Bearbeiten** aus.
3. Wählen Sie auf der Seite **Debitorenkarte** die Aktion **Zusammenführen mit** aus.
4. Wählen Sie auf der Seite **Doppelte Datensätze zusammenführen** im Feld **Zusammenführen mit** den Kunden aus, von dem Sie der Meinung sind, dass dies ein Duplikat des von Ihnen geöffneten Datensatzes ist, der im Feld **Aktuell** angezeigt wird.

    Die Inforegisterliste **Felder** zeigt auf, in dem die Werte für die zwei Debitoren abweichen. Das bedeutet, wenn der ausgewählte Debitor tatsächlich ein Duplikat ist, dann können nur sehr wenige Felder aufgeführt werden, wie Eingabefehler und andere Dateneingabefehler.

    Die Inforegisterliste **Zugehörige Tabellen** zeigt Tabellen auf, in denen es Felder mit einer Verbindung zu beiden Debitoren gibt. Die Felder **Aktuelle Anzahl** und **Doppelte Anzahl** zeigen die Anzahl der Felder in den verknüpften Tabellen, bei denen der Wert **Nr.** sowohl des aktuellen als auch des doppelten Kunden verwendet wird. Auf der Seite **Doppelte Datensätze zusammenführen** dient der entsprechende Abschnitt nur der Information. Wenn jedoch Zusammenführungskonflikte vorhanden sind, lösen Sie sie auf der Seite **Doppelte Konflikte zusammenführen**. Siehe Schritte 8 bis 12.   

5. Für jedes Feld, in dem Sie einen anderen Wert als den aktuellen verwenden möchten, wählen Sie das Kontrollkästchen **Außer Kraft setzen** aus. Der Wert im Feld **Alternativer Wert** wird dann in den aktuellen Datensatz übertragen, wenn Sie diesen Vorgang abschließen.
6. Wenn Sie die Auswahl abgeschlossen haben, welche Werte behalten oder überschrieben werden sollen, wählen Sie die Aktion **Zusammenführen** aus.

    Das System prüft, ob die Zusammenführung von Werten für den doppelten Debitor in den aktuellen Debitor Konflikte verursacht. Es gibt Konflikte, wenn ein Wert in mindestens einem Primärschlüsselfeld für beide Debitoren übereinstimmt, während der Wert im Feld **Nr.** für die zwei Debitoren übereinstimmt.

7. Wenn Konflikte nicht gefunden werden, wählen Sie die Schaltfläche **Ja** im Bestätigungsmeldungsfeld aus.

    Der doppelte Debitor wird umbenannt, damit die gesamte Nutzung des Werts **Nr.** in allen Felder mit Beziehungen zur Debitortabelle durch den Wert **Nr.** des aktuellen Debitors ersetzt.
8. Wenn Konflikte vorliegen, wählen Sie die Aktion **(xx) Konflikte vor dem Zusammenführen beheben** im Inforegister **Konflikte** aus, das angezeigt wird, wenn Konflikte vorhanden sind.
9. Wählen Sie auf der Seite **Doppelte Konflikte zusammenführen** die Zeile für eine zugehörige Tabelle mit einem Konflikt aus, und wählen Sie die Aktion **Details anzeigen** aus.

    Auf der Seite **Doppelte Datensätze zusammenführen** werden jetzt die Felder in der ausgewählten Tabelle angezeigt, die einen Zusammenführungskonflikt zwischen den beiden Debitorendatensätzen verursachen. Beachten Sie bei beiden zusammengefassten Werten in den Feldern **Aktuell** und **Steht im Konflikt mit** und in den Zeilen, bei denen mindestens ein Primärschlüsselfeld für beide Debitoren übereinstimmt und der Wert des Felds **Nr.** sich für die beiden Debitoren unterscheidet.   
10. Wenn Sie den doppelten Debitorendatensatz nicht behalten möchten, wählen Sie die Aktion **Dublette entfernen** und dann die Schaltfläche **Schließen** aus.

    Identische Feldwerte werden im Gegensatz zu dem Wert im Feld **Nr.** aus dem doppelten Datensatz entfernt und in den aktuellen Datensatz eingefügt.
11. Wenn Sie den doppelten Debitorendatensatz nach der Zusammenführung behalten möchten, wählen Sie **Dublette umbenennen** aus.
12. Ändern Sie in den Zeilen, nicht für das Feld **Nr.**, in dem das Feld den gleichen Wert bei beiden Datensätzen hat, den Wert im Feld **Alternativer Wert**, und wählen Sie dann die Schaltfläche **Schließen** aus.

    Der in Konflikt stehende Feldwert wird im doppelten Datensatz aktualisiert, sodass er mit dem aktuellen Datensatz zusammengeführt werden kann. Der doppelte Datensatz existiert auch weiterhin nach der Zusammenführung.
13. Wiederholen Sie die Schritte 8 bis 12, bis alle Konflikte gelöst sind. Das Inforegister **Konflikte** wird nicht mehr angezeigt.
14. Wählen Sie auf der Seite **Doppelt Datensätze zusammenführen** wieder die Aktion **Zusammenführen** und dann im Feld mit der Bestätigungsmeldung die Schaltfläche **Ja** aus.

> [!NOTE]
> Für Kontakte können Sie Funktionen zum Auffinden von doppelten Kontakten nutzen, bevor Sie die Seite **Doppelt Datensätze zusammenführen** verwenden. Weitere Informationen finden Sie unter [Suchen nach doppelten Kontakten](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Verkauf](sales-manage-sales.md)  
[Kontakte einrichten](marketing-setup-contacts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
