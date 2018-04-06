---
title: Verarbeiten von Verkaufschancen in Verkaufszyklen | Microsoft Docs
description: "Sie können Verkaufschancen anzeigen, schließen oder löschen, und Sie können auch Angebote und Aufträge für Verkaufschancen einrichten und eine Verkaufschance über die einzelnen Phasen des Verkaufsprozesses verschieben."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c7c7dca1d59b407f119347345cbbdef3f730acbc
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="process-sales-opportunities"></a>Verarbeiten von Verkaufschancen
Nachdem Sie eine Verkaufschance erstellen haben, gibt es einige Funktionen für die Verwaltung der Verkaufschance und deren Abschluss.

## <a name="to-view-opportunities"></a>Anzeigen von Verkaufschancen
Vorhandene Verkaufsverkaufschancen sind im Fenster **Verkaufschancenübersicht** verfügbar. Es gibt unterschiedliche Arten, um auf dieses Fenster für die Verarbeitung von Verkaufschancen zuzugreifen:

| Verkaufschancen anzeigen für | Dann |
| --- | --- |
| Alle Verkäufer und Kontakte |Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Chancenliste** ein. Wählen Sie dann den zugehörigen Link aus. |
| Ein bestimmter Verkäufer |Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkäufer** ein. Wählen Sie dann den zugehörigen Link aus. Wählen Sie den Verkäufer, wählen sie die Aktion **Verkaufschancen** und dann die Aktion **Übersicht**. |
| Ein bestimmter Kontakt |Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Kontakte** ein. Wählen Sie dann den zugehörigen Link aus. Wählen Sie den Kontakt aus der Liste, und wählen sie die Aktion **Verkaufschancen**. |

Jede dieser Aufgaben öffnet das Fenster **Verkaufschancenübersicht**.

## <a name="to-close-opportunities"></a>Um Verkaufschancen abzuschließen
Sie können Verkaufschancen abschließen, wenn die Verhandlungen abgeschlossen sind. Wenn Sie eine Verkaufschance schließen, können Sie angeben, ob sie gewonnen oder verloren wurde und dafür die Gründe festlegen. Um einen Grund anzugeben, müssen Sie Verkaufschancenabschlusscodes einrichten.

1. Im **Verkaufschancenübersicht**-Fenster wählen Sie die Verkaufschance und die **Abschluss**-Aktion aus. Der Fenster **Verkaufschance abschließen** wird geöffnet.
2. Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.

   Die Felder **Verkaufschancenabschlusscode** und **Abschlussdatum** sind erforderlich und müssen ausgefüllt werden, bevor Sie auf die Schaltfläche **Ok** klicken können.

   Geben Sie im **Verkaufschancenabschlusscode**-Feld einen der vorhandenen Verkaufschancenabschlusscodes aus oder fügen Sie einen neuen Code hinzu. Um einen neuen Code hinzuzufügen, wählen Sie in der Dropdownliste **Aus vollständiger Liste auswählen** aus in wählen Sie dann **Neu**. Füllen Sie in der neuen leeren Zeile die Felder **Code**, **Art** und **Beschreibung** aus, und wählen Sie dann die **OK**-Schaltfläche.

## <a name="to-create-quotes-for-opportunities"></a>Um Angebote für Verkaufschancen zu erstellen
Sie können Verkaufsangebote für Kontakte erstellen, die nicht als Debitoren erfasst werden.

1. Im **Verkaufschancenübersicht**-Fenster wählen Sie die Verkaufschance und dann die **Verkaufsangebot zuweisen**-Aktion aus. Das Fenster **Verkaufsangebot** wird geöffnet.
2. Füllen Sie die entsprechenden Felder aus.

## <a name="to-create-sales-orders-for-opportunities"></a>Verkaufsaufträge für Verkaufschancen erstellen
Sie können Verkaufsaufträge aus Verkaufsangeboten erstellen, die Sie für Ihre Verkaufschancen erfasst haben. Bevor Sie Verkaufsaufträge für Ihre Kontakte erstellen können, müssen Sie den Kontakt als Debitor erstellen. Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. Suchen Sie im Fenster **Verkaufschancenübersicht** die Verkaufschance, für die Sie ein Verkaufsangebot erstellt haben.
2. Wählen Sie die Aktion **Verkaufsangebot zuweisen** aus. Das Fenster **Verkaufsangebot** wird geöffnet. Es enthält das Verkaufsangebot, das der Verkaufschance zugewiesen wurde.
3. Füllen Sie die weiteren Felder aus, und wählen Sie dann die Aktion **Auftrag erstellen** aus.

Bei der Bearbeitung von Verkaufschancen können Sie ein Angebot für den Kontakt erstellen, mit dem die Verkaufschance verknüpft ist.

## <a name="to-delete-opportunities"></a>Um Verkaufchancen zu löschen
Sie können Verkaufschancen z. B. löschen, wenn Sie ein Geschäft abgeschlossen haben. Es können jedoch nur abgeschlossene Verkaufschancen gelöscht werden. Es gibt zwei Möglichkeiten, um abgeschlossene Verkaufschancen zu löschen. Sie können einzelnen abgeschlossene Verkaufschancen über das **Verkaufschancenübersicht**-Fenster löschen, oder Sie können die Stapelverarbeitung **Geschlossene Verkaufschancen löschen...** ausführen, um mehrere Verkaufschancen auf Grundlage von Kriterien zu löschen.

Um abgeschlossene Verkaufschancen aus dem Fenster **Verkaufschancenübersicht** zu löschen, wählen Sie die Verkaufschance, und wählen Sie dann die Aktion **Löschen** aus.

Um abgeschlossene Verkaufschancen über die Stapelverarbeitung **Geschlossene Verkaufschancen löschen...** zu löschen verwenden, gehen Sie folgendermaßen vor:

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Chancenliste löschen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Im **Verkaufschance**-Abschnitt richten Sie die Filter ein, die die zu löschenden abgeschlossenen Verkaufschancen definieren.
3. Wählen Sie die Schaltfläche **OK** aus.

Nachdem Sie eine Verkaufschance gelöscht haben, wird sie aus dem Fenster **Verkaufschancenübersicht** entfernt.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Verschieben einer Verkaufschance über Verkaufsprozessstufen
Wenn eine Verkaufschance einem Verkaufsprozess folgt, können Sie sie vorwärts oder rückwärts durch die verschiedenen Stufen verschieben oder eine Stufe überspringen.

1. Wählen Sie im Fenster **Verkaufschancenübersicht** die Aktion **Aktualisieren**. Der Assistent **Verkaufschance aktualisieren** wird geöffnet.
2. Verwenden Sie das **Aktionsart**-Feld, um die Verkaufschance durch die Verkaufsprozessstufen zu verschieben:
   * **Nächste** verschiebt die Verkaufschance eine Stufe weiter.
   * **Überspringen** verschiebt die Verkaufschance eine oder mehrere Stufen im Verkaufsprozess weiter, die Sie im Feld **Präsentation** angeben. Sie können nur Stufen überspringen, die eingerichtet wurden, um das Überspringen zu ermöglichen.
   * **Vorherige** verschiebt die Verkaufschance eine Stufe zurück.
   * **Überspringen** verschiebt die Verkaufschance eine oder mehrere Stufen im Verkaufsprozess zurück, die Sie im Feld **Präsentation** angeben.
   * **Aktualisieren** ermöglicht das Ändern von Informationen (z. B. Ihre Einschätzung zu den Erfolgschancen und den erwarteten Zahlen), ohne die Verkaufschance auf eine andere anderen Stufe zu verschieben.
3. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Erstellen und Verwalten von Kontakten](marketing-contacts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

