---
title: Verarbeiten von Verkaufschancen in Verkaufsprozessen
description: 'Dieses Thema beschreibt die verschiedenen Möglichkeiten, wie Sie Verkaufschancen in Verkaufszyklen verarbeiten und eine Verkaufschance durch die Phasen eines Verkaufszyklus bewegen können.'
author: jswymer
ms.author: jswymer
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'relationship, prospect'
ms.date: 12/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Verarbeiten von Verkaufschancen

Nachdem Sie eine Verkaufschance erstellen haben, gibt es einige Funktionen für die Verwaltung der Verkaufschance und deren Abschluss.

## Verkaufschancen anzeigen

Vorhandene Verkaufsverkaufschancen stehen auf der Seite **Verkaufschancenübersicht** zur Verfügung. In der folgenden Tabelle werden Möglichkeiten für den Zugriff auf die Seite beschrieben, um Verkaufschancen zu bearbeiten.

| Verkaufschancen anzeigen für | Dann |
| --- | --- |
| Alle Verkäufer und Kontakte |Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Verkaufschancenübersicht** ein und wählen Sie dann den zugehörigen Link. |
| Ein bestimmter Verkäufer |Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkäufer** ein und wählen Sie dann den zugehörigen Link. Wählen Sie den Verkäufer, wählen sie die Aktion **Verkaufschancen** und dann die Aktion **Übersicht**. |
| Ein bestimmter Kontakt |Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontakte** ein, und wählen Sie dann den zugehörigen Link. Wählen Sie den Kontakt aus der Liste, und wählen sie die Aktion **Verkaufschancen**. |

Jede dieser Aufgaben öffnet die Seite **Verkaufschancenübersicht**.

## Verkaufschancen abschließen

Sie können Verkaufschancen abschließen, wenn die Verhandlungen abgeschlossen sind. Wenn Sie eine Verkaufschance schließen, können Sie angeben, ob sie gewonnen oder verloren wurde, und die Gründe für das Schließen eingeben. Um einen Grund anzugeben, müssen Sie Verkaufschancenabschlusscodes einrichten.

1. Auf der Seite **Verkaufschancenübersicht** wählen Sie die Verkaufschance und die **Abschluss**-Aktion aus. Die Seite **Verkaufschance abschließen** wird geöffnet.
2. Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.

   Die Felder **Verkaufschancenabschlusscode** und **Abschlussdatum** sind erforderlich und müssen ausgefüllt werden, bevor Sie auf die Schaltfläche **Ok** klicken können.

   Geben Sie im **Verkaufschancenabschlusscode**-Feld einen der vorhandenen Verkaufschancenabschlusscodes aus oder fügen Sie einen neuen Code hinzu. Um einen neuen Code hinzuzufügen, wählen Sie in der Dropdownliste **Aus vollständiger Liste auswählen** aus in wählen Sie dann **Neu**. Füllen Sie in der neuen leeren Zeile die Felder **Code**, **Art** und **Beschreibung** aus, und wählen Sie dann die **OK**-Schaltfläche.

## Angebote für Verkaufschancen erstellen

> [!NOTE]
> Sie können nur Verkaufsangebote aus Verkaufschancen erstellen, bei denen der Kontakttyp Firma ist.

1. Auf der Seite **Verkaufschancenübersicht** wählen Sie die Verkaufschance und dann die **Verkaufsangebot zuweisen**-Aktion aus. Die Seite **Verkaufsangebot** wird geöffnet.
2. Füllen Sie die entsprechenden Felder aus.

## Verkaufsaufträge für Verkaufschancen erstellen

Sie können Verkaufsaufträge aus Verkaufsangeboten erstellen, die Sie für Ihre Verkaufschancen erfasst haben. Bevor Sie Verkaufsaufträge für Ihre Kontakte erstellen können, müssen Sie den Kontakt als Debitor erstellen. Weitere Informationen finden Sie unter [Kontakte erstellen](marketing-create-contact-companies.md).

1. Suchen Sie auf der Seite **Verkaufschancenübersicht** die Verkaufschance, für die Sie ein Verkaufsangebot erstellt haben.
2. Wählen Sie die Aktion **Verkaufsangebot zuweisen** aus. Die Seite **Verkaufsangebot** wird geöffnet. Es enthält das Verkaufsangebot, das der Verkaufschance zugewiesen wurde.
3. Füllen Sie die weiteren Felder aus, und wählen Sie dann die Aktion **Auftrag erstellen** aus.

Bei der Bearbeitung von Verkaufschancen können Sie ein Angebot für den Kontakt erstellen, mit dem die Verkaufschance verknüpft ist.

## Verkaufschancen löschen

Sie können Verkaufschancen z. B. löschen, wenn Sie ein Geschäft abgeschlossen haben. Es können jedoch nur abgeschlossene Verkaufschancen gelöscht werden. Es gibt zwei Möglichkeiten, um abgeschlossene Verkaufschancen zu löschen. Sie können einzelnen abgeschlossene Verkaufschancen über die Seite **Verkaufschancenübersicht** löschen, oder Sie können die Stapelverarbeitung **Verkaufschancen löschen** ausführen, um mehrere Verkaufschancen auf Grundlage von Kriterien zu löschen.

Um abgeschlossene Verkaufschancen aus der Seite **Verkaufschancenübersicht** zu löschen, wählen Sie die Verkaufschance, und wählen Sie dann die Aktion **Löschen** aus.

Um abgeschlossene Verkaufschancen über die Stapelverarbeitung **Verkaufschancen löschen** zu löschen verwenden, gehen Sie folgendermaßen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Datenadministration** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie unter der Aktion **Verkaufschancen löschen** die Filter ein, die die zu löschenden abgeschlossenen Verkaufschancen definieren.
3. Wählen Sie die Schaltfläche **OK**.

Nachdem Sie eine Verkaufschance gelöscht haben, wird sie aus der Seite **Verkaufschancenübersicht** entfernt.

## Eine Verkaufschance über Verkaufsprozessstufen verschieben

Wenn eine Verkaufschance einem Verkaufsprozess folgt, können Sie sie auf die nächste oder vorhergehende Stufe verschieben und sogar eine Stufe überspringen.

1. Wählen Sie auf der Seite **Verkaufschancenübersicht** die Aktion **Aktualisieren**. Der Assistent **Verkaufschance aktualisieren** wird geöffnet.
2. Verwenden Sie das **Aktionsart**-Feld, um die Verkaufschance durch die Verkaufsprozessstufen zu verschieben:
   * **Nächste** verschiebt die Verkaufschance eine Stufe weiter.
   * **Überspringen** verschiebt die Verkaufschance eine oder mehrere Stufen im Verkaufsprozess weiter, die Sie im Feld **Präsentation** angeben. Sie können nur Stufen überspringen, die eingerichtet wurden, um das Überspringen zu ermöglichen.
   * **Vorherige** verschiebt die Verkaufschance eine Stufe zurück.
   * **Überspringen** verschiebt die Verkaufschance eine oder mehrere Stufen im Verkaufsprozess zurück, die Sie im Feld **Präsentation** angeben.
   * **Aktualisieren** ermöglicht das Ändern von Informationen (z. B. Ihre Einschätzung zu den Erfolgschancen und den erwarteten Zahlen), ohne die Verkaufschance auf eine andere anderen Stufe zu verschieben.
3. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.

## Siehe auch

[Verkauf](sales-manage-sales.md)  
[Erstellen und Verwalten von Kontakten](marketing-contacts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]