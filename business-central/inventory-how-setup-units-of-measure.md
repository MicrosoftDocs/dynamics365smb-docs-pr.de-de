---
title: "So geht's: Artikeleinheiten einrichten| Microsoft Docs"
description: Sie können mehrere Einheiten für einen Artikel einrichten, sodass Sie für Einheiten den Artikeln zuweisen können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e6a9465f13e272d653ec9a0544618b243928af03
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923720"
---
# <a name="set-up-units-of-measure"></a>Einheiten einrichten

Im Rahmen der Einrichtung von [!INCLUDE [prodshort](includes/prodshort.md)] legen Sie allgemeine Einheiten auf der Seite **Enheit** fest. Wenn Sie dann neue Elemente registrieren, legen Sie die Basiseinheit auf der **Artikelkarte** fest. Sie können Einheiten jedoch auch später hinzufügen.  

Sie können mehrere Einheiten für einen Artikel einrichten, sodass Sie für folgende Zwecke Einheiten den Artikeln zuweisen können:

- Weisen Sie eine Basiseinheit auf der Artikelkarte des Artikels aus, um festzulegen, wie sie im Lagerbestand gespeichert wird und um als die Konvertierungsbasis für alternative Einheiten zu dienen.
- Ordnen Sie alternative Einheiten dem Einkauf, der Produktion oder Verkaufsbelegen zu, um anzugeben, wie viele Einheiten der Basiseinheit Sie gleichzeitig in diesen Prozessen verarbeiten. Beispielsweise kaufen Sie möglicherweise den Artikel auf Paletten und benutzen nur einzelne Stücke in Ihrer Produktion.

Wenn ein Artikel in einer Einheit am Lager geführt, aber in einer anderen Einheit gefertigt wird, wird ein Fertigungsauftrag erstellt, für den eine Fertigungsloseinheit verwendet wird, um in der Stapelverarbeitung **Herstellungsantrag erneuern** die richtige Menge der Komponenten zu berechnen. Ein Beispiel für eine Berechnung über eine Fertigungsloseinheit ergibt sich, wenn ein Produktionsartikel am Lager in Einheiten geführt, aber in Tonnen gefertigt wird. Weitere Informationen finden Sie unter [Arbeiten mit Fertigungs-Batch-Einheiten](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

## <a name="to-set-up-units-of-measure"></a>So richten Sie Einheiten ein

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Maßeinheiten** ein, und wählen Sie dann die entsprechende Verknüpfung.  
2. Wählen Sie die Aktion **Neu**. Eine neue leere Zeile wird eingefügt.  
3. Füllen Sie die Felder aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Wenn Sie wissen, dass Ihre Organisation Artikel mit dieser Einheit an Kunden in anderen Ländern verkauft, können Sie Übersetzungen hinzufügen.  
    1. Wählen Sie den Code aus, für den Sie Übersetzungen einrichten möchten und klicken Sie auf **Übersetzungen**.
    2. Wählen Sie im Feld **Sprachcode** auf den Dropdown-Pfeil, um eine Übersicht über die verfügbaren Sprachcodes anzuzeigen. Wählen Sie den Sprachcode, für den Sie eine Übersetzung eingeben möchten, und wählen Sie dann die Schaltfläche OK, um den Code in das Feld zu kopieren.
    3. Geben Sie in dem Feld **Beschreibung** den entsprechenden Text ein.
5. Wiederholen Sie die vorherigen Schritte für alle zusätzlichen Einheiten, die Sie hinzufügen möchten.  

Wenn Sie einen neuen Artikel registrieren, können Sie die Einheit aus der Liste der Einheiten auswählen, die Sie jetzt eingerichtet haben. Sie können auch mehrere Einheiten für einen Artikel einrichten.  

## <a name="to-set-up-multiple-item-units-of-measure"></a>So richten Sie mehrere Einheiten für Artikel ein

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte des Artikels, für die Sie alternative Einheiten einrichten möchten.
3. Wählen Sie die **Einheiten** Aktion aus. Die Seite **Artikeleinheiten** wird geöffnet.
4. Wenn das Feld **Basismaßeinheit** auf der Artikelkarte ausgefüllt wird, ist diese Maßeinheit bereits eingerichtet.
5. Wählen Sie die Aktion **Neu** aus. Eine neue leere Zeile wird eingefügt.
6. Geben Sie im Feld **Code** den Namen des Einheitencodes ein. Alternativ aktivieren Sie das Feld, um in den Einheitencodes auszuwählen, die in der Datenbank sind.
7. Geben Sie in das Feld **Menge per Basismaßeinheit** ein, wie viele der Einheiten der Basiseinheit die neue Maßeinheit enthält.
8. Geben Sie in den Feldern **Höhe**, **Breite**, **Länge** und **Gewicht** optional detaillierte Informationen zur Größe einer Einheit ein, sodass [!INCLUDE [prodshort](includes/prodshort.md)] berechnen kann, wie viele Artikeleinheiten in bestimmte Lagerplätze eingelagert werden können. Das Feld **Volumen** wird automatisch basierend auf **Höhe**, **Breite** und **Länge** berechnet.

    Wenn eines dieser Felder einen anderen Wert als 0 enthält, wird diese Abmessung bei allen Prozessen verwendet, die die Einlagerung von Artikeln in Lagerplätzen betreffen: Einlagerung, Umlagerungen, Zugänge, Lieferungen, Kommissionierungen und Regulierungen. [!INCLUDE [prodshort](includes/prodshort.md)] überprüft die Summe jeder physischen Abmessung der einzulagernden und der bereits am Lagerplatz befindlichen Artikel anhand der maximalen Größe oder einer anderen Abmessung, die an einem Lagerplatz eingelagert werden kann, gemäß der Lagerplatzkapazitätsrichtlinie auf der Lagerortkarte für diesen Artikel. Somit müssen Sie für jede Dimension über alle Artikeleinheiten hinweg dieselbe Einheit verwenden, z. B. Kilogramm oder Pfund für Gewicht, und dies jedoch konsistent.
9. Wiederholen Sie die Schritte 5 und 7, um alle alternativen Einheiten einzurichten, die Sie in den verschiedenen Prozessen für diesen Artikel verwenden möchten.

    Im Feld **Basiseinheit** am unteren Rand des Fensters, können Sie die Basiseinheit des Artikels anzeigen oder ändern. Sie können auch die Basiseinheit im Feld **Basiseinheit** auf der Artikelkarte ändern. Auf der Seite **Artikeleinheiten** muss die Basiseinheit den Wert **1** im Feld **Menge pro Einheit** aufweisen.

Sie können jetzt die alternativen Einheiten für Einkaufs-, Produktions- und Verkaufsbelege verwenden, wie im Abschnitt [So geben Sie einen Standardeinheitencode für Verkaufs- und Einkaufstransaktionen ein](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions) beschrieben.  

## <a name="to-set-up-unit-of-measure-translations"></a>Einheiten der Maßübersetzungen einrichten

Wenn Sie Artikel an ausländische Debitoren verkaufen, können Sie die Einheit in der Sprache des Debitors angeben. Dies können Sie tun, nachdem Sie die erforderlichen Einheitenübersetzungen eingerichtet haben.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Maßeinheiten** ein, und wählen Sie dann die entsprechende Verknüpfung.
2. Wählen Sie den Code aus, für den Sie Übersetzungen einrichten möchten und klicken Sie auf **Übersetzungen**.
3. Wählen Sie im Feld **Sprachcode** auf den Dropdown-Pfeil, um eine Übersicht über die verfügbaren Sprachcodes anzuzeigen. Wählen Sie den Sprachcode, für den Sie eine Übersetzung eingeben möchten, und wählen Sie dann die Schaltfläche OK, um den Code in das Feld zu kopieren.
4. Geben Sie in dem Feld **Beschreibung** den entsprechenden Text ein.
5. Wiederholen Sie die Schritte 2 bis 4 für die Einheitencodes und die Sprachen, für die Sie Übersetzungen eingeben möchten.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Um einen Vorgabe-Einheitencode für Einkaufs- und Verkaufstransaktionen einzugeben

Wenn Sie normalerweise in Einheiten kaufen und verkaufen, die von der Basiseinheit abweichen, können Sie für Einkäufe und Verkäufe eigene Einheiten festlegen. Dazu müssen die  Einheiten auf der Seite **Artikeleinheiten** eingerichtet worden sein.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Artikel** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die entsprechende Artikelkarte, für die Sie einen Vorgabe-Einheitencode für Einkaufs- oder Verkaufsvorgänge festlegen möchten.
3. Öffnen Sie im Inforegister **Fakturierung** im Feld **Verkaufseinheitencode** die Seite **Artikeleinheiten**.
4. Öffnen Sie im Inforegister **Beschaffung** im Feld **Einkaufseinheitencode** die Seite **Artikeleinheiten**.
5. Wählen Sie den Code, den Sie als Standardeinheit für Verkäufe oder Einkäufe entsprechend einrichten möchten, und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch

[Verwenden der Fertigungsloseinheit](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Käufe verwalten](purchasing-manage-purchasing.md)  
[Verkäufe verwalten](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
