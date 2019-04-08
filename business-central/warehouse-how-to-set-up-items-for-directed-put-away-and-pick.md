---
title: So richten Sie einen Artikel für die gesteuerte Einlagerung und Kommissionierung ein | Microsoft Docs
description: Wenn Sie einen Lagerort für die gesteuerte Einlagerung und Kommissionierung einrichten, steht Ihnen eine neue Funktionalität zur Verfügung, die Ihnen hilft, das Lager so effizient wie möglich zu betreiben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 0f69cfc3257de42aacf01c26090230350f83dfba
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799029"
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick"></a>Einrichten von Artikeln und Standorten für die gesteuerte Einlagerung und Kommissionierung
Wenn Sie einen Lagerort für die gesteuerte Einlagerung und Kommissionierung einrichten, steht Ihnen eine neue Funktionalität zur Verfügung, die Ihnen hilft, das Lager so effizient wie möglich zu betreiben. Um diese Funktionalität voll auszuschöpfen, liefern Sie der Anwendung zusätzliche Informationen zu den Artikeln, wodurch die Anwendung ihrerseits dabei unterstützt wird, die erforderlichen Berechnungen anzustellen, um die effizientesten und effektivsten Möglichkeiten zur Durchführung der Lageraktivitäten vorzuschlagen. Weitere Informationen finden Sie unter [Designdetails: Lagerhaus einrichten](design-details-warehouse-setup.md).

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>So richten Sie einen Artikel für die gesteuerte Einlagerung und Kommissionierung ein:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.  
2.  Öffnen Sie die Karte für den Artikel, den Sie für gesteuerte Einlagerung und Kommissionierung einrichten möchten.
3. Füllen Sie im Inforegister **Logistik** der Artikelkarte die Felder aus, um festzulegen, wie der Artikel im Lager verarbeitet werden soll.  
4.  Wählen Sie die **Einheiten** Aktion aus.
5. Fülle Sie auf der Seite **Artikeleinheiten** die Felder zum Definieren der Einheiten aus, in denen der Artikel verarbeitet werden kann, einschließlich Höhe, Breite, Länge, das Volumen und das Gewicht der Einheit.
6. Wählen Sie die **Lagerplatzinhalte** Aktion aus.
7. Auf der Seite **Lagerplatzinhalte** können Sie den Lagerort und den Lagerplatz festlegen, mit denen der Artikel verknüpft sein soll. Das Feld **Vorgabewert** wird nicht verwendet, wenn der Lagerort für die gesteuerte Einlagerung und Kommissionierung eingerichtet wurde.  

## <a name="to-activate-directed-put-away-and-pick-functionality"></a>So aktivieren Sie die Funktionalität gesteuerte Einlagerung und Kommissionierung  
Die gesteuerte Einlagerung und Kommissionierung verschafft Ihnen Zugang zu erweiterten Lagerkonfigurationsfunktionalitäten, die Ihre Effizienz und Datenzuverlässigkeit stark erhöhen können. Um diese Funktionalität nutzen zu können, müssen Sie zuerst eine Reihe von Parametern in Ihrem Lagerort einrichten.  

Um die gesteuerte Einlagerung und Kommissionierung zu nutzen, müssen Sie die Funktionalität auf der Lagerortkarte aktivieren.    
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Lagerort, bei dem Sie die gesteuerte Einlagerung und Kommissionierung nutzen möchten, wählen Sie dann die Aktion**Bearbeiten** aus.  
3.  Wählen Sie im Inforegister **Lager** das Kontrollkästchen **Gesteuerte Einlag. u. Kommiss.**.  

Sie brauchen zu diesem Zeitpunkt der Einrichtung keine weiteren Felder auf der Lagerortkarte auszufüllen.  

> [!NOTE]  
>  Sie können ein Lager nicht so einrichten, dass er Lagerplätze verwendet, wenn dieser Lagerort offene Artikelposten hat.  

Der nächste Schritt ist die Definition der Arten von Lagerplätzen, die Sie betreiben möchten. Weitere Informationen finden Sie unter [Einrichten von Lagerplatzarten](warehouse-how-to-set-up-bin-types.md). Die Lagerplatzart legt fest, wie ein bestimmter Lagerplatz im Warenfluss verwendet wird. Sie können sowohl einer Zone als auch einem Lagerplatz eine Lagerplatzart zuordnen.  

Sie können auch Lagerklassen definieren, wenn im Lager Artikel geführt werden, die unterschiedliche Lagerbedingungen benötigen. Lagerklassen werden verwendet, wenn der Einlagerung von Artikeln an Lagerplätzen vorgeschlagen wird. Sie weisen den Produktgruppen die Lagerklassen zu, die dann Artikeln und Lagerhaltungsdaten zugeordnet werden, oder auch Zonen und Lagerplätzen, die Lagerbedingungen bieten können, die von der Lagerklasse gefordert werden.  

Sie können jetzt Zonen einrichten, wenn Sie in Ihrem Lager mit Zonen arbeiten möchten. Die Verwendung von Zonen reduziert die Anzahl der Felder, die Sie ausfüllen müssen, wenn Sie Ihre Lagerplätze einrichten, da Lagerplätze, die innerhalb einer Zone angelegt werden, einige Eigenschaften der Zone übernehmen. Zonen können es darüber hinaus neuen Mitarbeitern oder nur vorübergehend tätigen Mitarbeitern erleichtern, sich in Ihrem Lager zu orientieren. Beachten Sie, dass der Fluss nach Lagerplätzen gesteuert wird. Daher ist es möglich, mit Lagerplätzen und nur einer Zone zu arbeiten.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a>So richten Sie eine Zone in Ihrem Lager ein:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Lagerort aus, in dem Sie die Zone einrichten möchten, öffnen Sie die Lagerortkarte, und wählen Sie dann die Aktion **Zonen** aus.  
3.  Füllen Sie auf der Seite **Zonen** die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Wenn Sie einen Zonenparameter ändern, werden alle Lagerplätze, die von diesem Zeitpunkt an angelegt werden, die neuen Eigenschaften aufweisen.  

> [!NOTE]  
>  Wenn Sie ohne Zonen arbeiten möchten, müssen Sie dennoch eine Zone erstellen, die außer für den Code undefiniert ist.  

Der nächste Schritt beim Einrichten des Lagers ist die Definition von Lagerplätzen. Weitere Informationen finden Sie unter [Vorgehensweise: Lagerorte für die Verwendung von Lagerplätzen einrichten](warehouse-how-to-set-up-locations-to-use-bins.md).  

Darüber hinaus müssen Sie Einlagerungsvorlagen und Inventurhäufigkeiten erstellen. Weitere Informationen finden Sie unter [Einrichten von Aktivitätvorlagen](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
