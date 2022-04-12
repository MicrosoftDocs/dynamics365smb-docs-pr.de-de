---
title: Eine Standortkarte festlegen und Umlagerungsrouten definieren (enthält ein Video)
description: Wenn Sie Artikel an mehreren Orten oder Lagern kaufen, lagern oder verkaufen, müssen Sie für jeden Lagerort eine Standortkarte festlegen und Umlagerungsrouten definieren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9de6580971f25d092de474c0720b86fab420bbf8
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515511"
---
# <a name="set-up-locations"></a>Einrichten von Lagerorten

Standorte sind Orte wie z.B. Lager, an denen Sie Artikel kaufen, lagern oder verkaufen. [!INCLUDE [prod_short](includes/prod_short.md)] verwendet Standorte, um den Bestand sowohl in einfachen als auch in komplexen Lagerprozessen im Auge zu behalten.

Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern. Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lagerortkarten
Auf der Seite **Standortkarte** geben Sie Informationen über einen Standort an, z.B. ein Lager oder ein Vertriebszentrum. Sie vergeben für jeden Lagerort einen Namen und einen Code, der den Lagerort darstellt. Sie können dann den Lagerortcode auch in anderen Bereichen des Programms angeben, wenn Sie die Transaktionen für einen bestimmten Lagerort speichern möchten.  

Sie können Informationen zu Lagerplätzen und Lagerrichtlinien für jeden Lagerort eingeben. Basierend auf den von Ihnen ausgewählten Lagerrichtlinien können Sie die Optionen des Inforegisters **Lagerplätze** verwenden, um die Lagerplätze zu definieren, die bei bestimmten Transaktionen als Standardlagerplätze verwendet werden. Wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, verwenden Sie die meisten Optionen im Inforegister **Lagerplatzprüfung**, um festzulegen, wie Sie die zahlreichen erweiterten Logistikfunktionen verwenden möchten.  

Einige Optionsfelder hängen von den Einstellungen auf der Seite **Standortkarte** ab, um nicht unterstützte Einrichtungskombinationen einzuschränken.  

Wählen Sie die Aktionen **Zonen** oder **Lagerplätze**, um Informationen über Zonen und Lagerplätze anzuzeigen, die für den Standort definiert sind.

### <a name="to-set-up-a-location"></a>So legen Sie einen Ort fest

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.

> [!NOTE]  
> Viele Felder auf der Seite Standortkarte stehen im Zusammenhang mit der Verarbeitung von Artikeln in eingehenden und ausgehenden Lagerprozessen. Diese Felder sind für Firmen, die keine komplexen Lagerfunktionen benötigen, nicht relevant. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

Sie können die Konfiguration eines Lagerorts später ändern, die Einrichtung von Lagerorten mit Artikel-Ledger-Einträgen jedoch nicht bearbeiten.  

Wenn Sie mehrere Standorte haben, können Sie Umlagerungsrouten zwischen den Standorten definieren. Weitere Informationen finden Sie unter [Sie erstellen eine Umlagerungsroute](inventory-how-setup-locations.md#to-create-a-transfer-route). 

### <a name="to-create-a-transfer-route"></a>So erstellen Sie eine Umlagerungsroute

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Umlagerungsrouten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie von jedem beliebigen Fenster **Standortkarten** die Aktion **Umlagerungsrouten** aus.
3. Wählen Sie die Aktion **Neu** aus.
4. Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern. Weitere Informationen finden Sie unter [Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Lagerplätze

Lagerplätze stellen die grundlegende Lagerstruktur dar und werden verwendet, um Vorschläge zur Einlagerung von Artikeln zu erstellen. Wenn Sie Ihre Lagerplätze erstellt haben, können Sie deren Inhalt definieren, oder sie können als schwebende Lagerplätze ohne festgelegten Inhalt fungieren. Lagerplätze werden überwiegend in grundlegenden und erweiterten Lagervorgängen eingesetzt. Wenn Sie das Lager in einer einfacheren Einrichtung verwalten, benötigen Sie wahrscheinlich keine Lagerplätze.

Um die Lagerplatz-Funktionalität an einem Standort zu nutzen, aktivieren Sie die Funktionalität zunächst auf der Seite **Standortkarte**, indem Sie das Feld **Lagerplätze obligatorisch** auf dem Inforegister **Lager** auswählen. Dann entwerfen Sie den Warenfluss am Lagerort, indem Sie Lagerplatzcodes in den Einrichtungsfeldern angeben, die für die verschiedenen Ströme stehen.

> [!NOTE]
> Bevor Sie Lagerplätze auf einem Platz angeben können, müssen Sie Lagerplatzcodes erstellen. Weitere Informationen finden Sie unter [Erstellen von Lagerplätzen](warehouse-how-to-create-individual-bins.md) und [Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zonen

Wenn Sie Ihre Lagerplätze nach Zonen strukturieren möchten, haben Sie auf der Seite **Zonen** dazu die Möglichkeit.

[!INCLUDE [prod_short](includes/prod_short.md)] kopiert die Felder, die Sie für jede Zone einrichten, in alle zugehörigen Lagerplätze. Auf diese Weise können Sie eine Zone einem Lagerplatz oder einer Lagerplatzvorlage zuweisen (Filter für Lagerplatzerstellung), und verschiedene andere Felder werden dann automatisch gefüllt.

Sie können jedoch auch nur eine Zone einrichten und Ihr Lager einfach auf Lagerplatzebene verwalten. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Standarddimensionen für Standorte
Sie legen Standarddimensionen für einen Standort auf der **Standortkarte**-Seite festlegen, indem Sie **Standort** und dann **Dimensionen** auswählen. Die Standarddimensionen des Standorts werden in Journale und Dokumente kopiert, wenn Sie den Standort in einer Zeile angeben, aber Sie können die Dimension in der Zeile bei Bedarf löschen oder ändern. Sie können verlangen, dass Personen Dimensionen für bestimmte Standorte angeben, bevor sie einen Eintrag veröffentlichen können. Sie können auch Standortdimensionswerte in **Standarddimensionsprioritäten** und **Dimensionskombinationen** für Kombinationen aus Prioritäts- und Dimensionsregeln einbeziehen.

## <a name="see-also"></a>Weitere Informationen

[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)  
[Lagerplätze erstellen](warehouse-how-to-create-individual-bins.md)  
[Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md)  
[Warehouse Management einrichten](warehouse-setup-warehouse.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]