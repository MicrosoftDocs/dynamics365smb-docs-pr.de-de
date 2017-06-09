---
title: Verwaltung von Verkaufschancen  | Microsoft Docs
description: Beschreibt die Verarbeitung von Verkaufschancen in Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 889ef028b34ddad52c978373a5dab4329d96c91f
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="processing-sales-opportunities"></a>Verarbeiten von Verkaufschancen
Nachdem Sie eine Verkaufschance erstellen haben, gibt es einige Funktionen für die Verwaltung der Verkaufschance und deren Abschluss.

## <a name="view-opportunities"></a>Anzeigen von Verkaufschancen
Vorhandene Verkaufsverkaufschancen sind im Fenster **Verkaufschancenübersicht** verfügbar. Es gibt unterschiedliche Arten, um auf dieses Fenster für die Verarbeitung von Verkaufschancen zuzugreifen:

| Verkaufschancen anzeigen für | Dann |
| --- | --- |
| Alle Verkäufer und Kontakte |In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus **![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Chancenlisten** ein und wählen Sie dann den entsprechenden Link aus. |
| Ein bestimmter Verkäufer |In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus **![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Verkäufer** ein und wählen Sie dann den entsprechenden Link aus. Wählen Sie den Verkäufer, wählen sie die Aktion **Verkaufschancen** und dann die Aktion **Übersicht**. |
| Ein bestimmter Kontakt |In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus **![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Kontakte** ein und wählen Sie dann den entsprechenden Link aus. Wählen Sie den Kontakt aus der Liste, und wählen sie die Aktion **Verkaufschancen**. |

Jede dieser Aufgaben öffnet das Fenster **Verkaufschancenübersicht**.

## <a name="close-opportunities"></a>Abschließen von Verkaufschancen
Sie können Verkaufschancen abschließen, wenn die Verhandlungen abgeschlossen sind. Wenn Sie eine Verkaufschance schließen, können Sie angeben, ob sie gewonnen oder verloren wurde und dafür die Gründe festlegen. Um einen Grund anzugeben, müssen Sie Verkaufschancenabschlusscodes einrichten.

1. Im **Verkaufschancenübersicht**-Fenster wählen Sie die Verkaufschance und die **Abschluss**-Aktion aus. Der Fenster **Verkaufschance abschließen** wird geöffnet.
2. Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.

   Die Felder **Verkaufschancenabschlusscode** und **Abschlussdatum** sind erforderlich und müssen ausgefüllt werden, bevor Sie auf die Schaltfläche **Ok** klicken können.

   Geben Sie im **Verkaufschancenabschlusscode**-Feld einen der vorhandenen Verkaufschancenabschlusscodes aus oder fügen Sie einen neuen Code hinzu. Um einen neuen Code hinzuzufügen, wählen Sie in der Dropdownliste **Aus vollständiger Liste auswählen** aus in wählen Sie dann **Neu**. Füllen Sie in der neuen leeren Zeile die Felder **Code**, **Art** und **Beschreibung** aus, und wählen Sie dann die **OK**-Schaltfläche.

## <a name="create-quotes-for-opportunities"></a>Angebote für Verkaufschancen erstellen
Sie können Verkaufsangebote für Kontakte erstellen, die nicht als Debitoren erfasst werden.

1. Im **Verkaufschancenübersicht**-Fenster wählen Sie die Verkaufschance und dann die **Verkaufsangebot zuweisen**-Aktion aus. Das Fenster **Verkaufsangebot** wird geöffnet.
2. Füllen Sie die entsprechenden Felder aus.

## <a name="create-sales-orders-for-opportunities"></a>Verkaufsaufträge für Verkaufschancen erstellen
Sie können Verkaufsaufträge aus Verkaufsangeboten erstellen, die Sie für Ihre Verkaufschancen erfasst haben. Bevor Sie Verkaufsaufträge für Ihre Kontakte erstellen können, müssen Sie den Kontakt als Debitor erstellen. Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. Suchen Sie im Fenster **Verkaufschancenübersicht** die Verkaufschance, für die Sie ein Verkaufsangebot erstellt haben.
2. Wählen Sie die Aktion **Verkaufsangebot zuweisen** aus. Das Fenster **Verkaufsangebot** wird geöffnet. Es enthält das Verkaufsangebot, das der Verkaufschance zugewiesen wurde.
3. Füllen Sie die weiteren Felder aus, und wählen Sie dann die Aktion **Auftrag erstellen** aus.

Bei der Bearbeitung von Verkaufschancen können Sie ein Angebot für den Kontakt erstellen, mit dem die Verkaufschance verknüpft ist.

## <a name="delete-opportunities"></a>Verkaufschancen löschen
Sie können Verkaufschancen z. B. löschen, wenn Sie ein Geschäft abgeschlossen haben. Es können jedoch nur abgeschlossene Verkaufschancen gelöscht werden. Es gibt zwei Möglichkeiten, um abgeschlossene Verkaufschancen zu löschen. Sie können einzelnen abgeschlossene Verkaufschancen über das **Verkaufschancenübersicht**-Fenster löschen, oder Sie können die Stapelverarbeitung **Geschlossene Verkaufschancen löschen...** ausführen, um mehrere Verkaufschancen auf Grundlage von Kriterien zu löschen.

Um abgeschlossene Verkaufschancen aus dem Fenster **Verkaufschancenübersicht** zu löschen, wählen Sie die Verkaufschance, und wählen Sie dann die Aktion **Löschen** aus.

Um abgeschlossene Verkaufschancen über die Stapelverarbeitung **Geschlossene Verkaufschancen löschen...** zu löschen verwenden, gehen Sie folgendermaßen vor:

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus **![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Chancen löschen** ein und wählen Sie dann den entsprechenden Link aus.
2. Im **Verkaufschance**-Abschnitt richten Sie die Filter ein, die die zu löschenden abgeschlossenen Verkaufschancen definieren.
3. Wählen Sie die Schaltfläche **OK** aus.

Nachdem Sie eine Verkaufschance gelöscht haben, wird sie aus dem Fenster **Verkaufschancenübersicht** entfernt.

## <a name="move-an-opportunity-through-sales-cycle-stages"></a>Verschieben einer Verkaufschance über Verkaufsprozessstufen
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
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

