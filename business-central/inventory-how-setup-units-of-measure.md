---
title: "So geht's: Artikeleinheiten einrichten| Microsoft Docs"
description: Sie können mehrere Einheiten für einen Artikel einrichten, sodass Sie für Einheiten den Artikeln zuweisen können.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2018
ms.author: SorenGP
ms.openlocfilehash: 376e34074c6ee216b7a9062a42404a8123758598
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799358"
---
# <a name="set-up-item-units-of-measure"></a>Artikeleinheiten einrichten
Sie können mehrere Einheiten für einen Artikel einrichten, sodass Sie für folgende Zwecke Einheiten den Artikeln zuweisen können:

- Weisen Sie eine Basiseinheit auf der Artikelkarte des Artikels aus, um festzulegen, wie sie im Lagerbestand gespeichert wird und um als die Konvertierungsbasis für alternative Einheiten zu dienen.
- Ordnen Sie alternative Einheiten dem Einkauf, der Produktion oder Verkaufsbelegen zu, um anzugeben, wie viele Einheiten der Basiseinheit Sie gleichzeitig in diesen Prozessen verarbeiten. Beispielsweise kaufen Sie möglicherweise den Artikel auf Paletten und benutzen nur einzelne Stücke in Ihrer Produktion.

Wenn ein Artikel in einer Einheit am Lager geführt, aber in einer anderen Einheit gefertigt wird, wird ein Fertigungsauftrag erstellt, für den eine Fertigungsloseinheit verwendet wird, um in der Stapelverarbeitung **Herstellungsantrag erneuern** die richtige Menge der Komponenten zu berechnen. Ein Beispiel für eine Berechnung über eine Fertigungsloseinheit ergibt sich, wenn ein Produktionsartikel am Lager in Einheiten geführt, aber in Tonnen gefertigt wird. Weitere Informationen finden Sie unter [Arbeiten mit Fertigungs-Batch-Einheiten](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>So richten Sie eine Maßeinheit ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Karte des Artikels, für die Sie alternative Einheiten einrichten möchten.
3. Wählen Sie die **Einheiten** Aktion aus. Die Seite **Artikeleinheiten** wird geöffnet.
4. Wenn das Feld **Basismaßeinheit** auf der Artikelkarte ausgefüllt wird, ist diese Maßeinheit bereits eingerichtet.
5. Wählen Sie die Aktion **Neu** aus. Eine neue leere Zeile wird eingefügt.
6. Geben Sie im Feld **Code** den Namen des Einheitencodes ein. Alternativ aktivieren Sie das Feld, um in den Einheitencodes auszuwählen, die in der Datenbank sind.
7. Geben Sie in das Feld **Menge per Basismaßeinheit** ein, wie viele der Einheiten der Basiseinheit die neue Maßeinheit enthält.
8. Wiederholen Sie die Schritte 5 und 7, um alle alternativen Einheiten einzurichten, die Sie in den verschiedenen Prozessen für diesen Artikel verwenden möchten.

Sie können die alternativen Einheiten von Einkauf, Produktion und Verkaufsbelegen jetzt verwenden. Weitere Informationen finden Sie unter Standardmaßeinheiten Einheitencodes für Einkaufstransaktionen und Verkaufstransaktionen eingeben oder Fertigungsloseinheit verwenden.

## <a name="to-set-up-unit-of-measure-translations"></a>Einheiten der Maßübersetzungen einrichten
Wenn Sie Artikel an ausländische Debitoren verkaufen, möchten Sie möglicherweise die Einheit in der Sprache des Debitors angeben. Dies können Sie tun, nachdem Sie die erforderlichen Einheitenübersetzungen eingerichtet haben.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Messeinheiten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den Code aus, für den Sie Übersetzungen einrichten möchten und klicken Sie auf **Übersetzungen**.
3. Wählen Sie im Feld **Sprachcode** auf den Dropdown-Pfeil, um eine Übersicht über die verfügbaren Sprachcodes anzuzeigen. Wählen Sie den Sprachcode, für den Sie eine Übersetzung eingeben möchten, und wählen Sie dann die Schaltfläche OK, um den Code in das Feld zu kopieren.
4. Geben Sie in dem Feld **Beschreibung** den entsprechenden Text ein.
5. Wiederholen Sie die Schritte 2 bis 4 für die Einheitencodes und die Sprachen, für die Sie Übersetzungen eingeben möchten.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Um einen Vorgabe-Einheitencode für Einkaufs- und Verkaufstransaktionen einzugeben
Wenn Sie normalerweise in Einheiten kaufen und verkaufen, die von der Basiseinheit abweichen, können Sie für Einkäufe und Verkäufe eigene Einheiten festlegen. Dazu müssen die  Einheiten auf der Seite **Artikeleinheiten** eingerichtet worden sein.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die entsprechende Artikelkarte, für die Sie einen Vorgabe-Einheitencode für Einkaufs- oder Verkaufsvorgänge festlegen möchten.
3. Öffnen Sie im Inforegister **Fakturierung** im Feld **Verkaufseinheitencode** die Seite **Artikeleinheiten**.
4. Öffnen Sie im Inforegister **Beschaffung** im Feld **Einkaufseinheitencode** die Seite **Artikeleinheiten**.
5. Wählen Sie den Code, den Sie als Standardeinheit für Verkäufe oder Einkäufe entsprechend einrichten möchten, und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Verwenden der Fertigungsloseinheit](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Käufe verwalten](purchasing-manage-purchasing.md)  
[Verkäufe verwalten](sales-manage-sales.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
