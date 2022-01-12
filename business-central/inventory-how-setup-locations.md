---
title: Eine Standortkarte festlegen und Umlagerungsrouten definieren (enthält ein Video)
description: Wenn Sie Artikel an mehreren Orten oder Lagern kaufen, lagern oder verkaufen, müssen Sie für jeden Lagerort eine Standortkarte festlegen und Umlagerungsrouten definieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 1d65213d81c2a615481e753adb380675ff2ee691
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940726"
---
# <a name="set-up-locations"></a>Einrichten von Lagerorten

Wenn Sie Artikel an mehreren Orten oder Lagern kaufen, lagern oder verkaufen, müssen Sie für jeden Lagerort eine Standortkarte festlegen und Umlagerungsrouten definieren. [!INCLUDE [prod_short](includes/prod_short.md)] verwendet Lagerorte, um den Bestand sowohl in einfacheren Fällen als auch in komplexeren Lagerprozessen zu verfolgen.

Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern. Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lagerortkarten

Die Lagerortkarte enthält Informationen zu einem Lagerort, z. B. ein Lager oder eine Vertriebsstelle. Sie vergeben für jeden Lagerort einen Namen und einen Code, der den Lagerort darstellt. Sie können dann den Lagerortcode auch in anderen Bereichen des Programms angeben, wenn Sie die Transaktionen für einen bestimmten Lagerort speichern möchten.  

Sie können Informationen zu Lagerplätzen und Lagerrichtlinien für jeden Lagerort eingeben. Basierend auf den von Ihnen ausgewählten Lagerrichtlinien können Sie die Optionen des Inforegisters **Lagerplätze** verwenden, um die Lagerplätze zu definieren, die bei bestimmten Transaktionen als Standardlagerplätze verwendet werden. Wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, verwenden Sie die meisten Optionen im Inforegister **Lagerplatzprüfung**, um festzulegen, wie Sie die zahlreichen erweiterten Logistikfunktionen verwenden möchten.  

Einige Optionsfelder werden durch andere Einstellungen auf der Seite **Lagerortkarte** abgeblendet dargestellt und deaktiviert, um nicht unterstützte Einrichtungskombinationen zu begrenzen.  

Wählen Sie die Aktion **Zonen** oder **Lagerplätze** aus, um Informationen über Zonen und Lagerplätze anzuzeigen, die ggf. für den Lagerplatz festgelegt sind.

### <a name="to-create-a-location-card"></a>So erstellen Sie eine Lagerortkarte

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.

> [!NOTE]  
> Viele Felder auf der Lagerortkarte beziehen sich auf Auftragsabwicklung von Artikel in eingehenden und ausgehenden Lagerprozessen. Für Unternehmen, die die komplexeren Lagerfunktionen nicht benötigen, sind die Felder nicht relevant. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

Sie können die Konfiguration eines Lagerorts später ändern, die Einrichtung von Lagerorten mit Artikel-Ledger-Einträgen jedoch nicht bearbeiten.  

Wenn Sie über mehrere Lagerorte verfügen, können Sie als Nächstes Umlagerungsrouten zwischen Lagerorten definieren.  

### <a name="to-create-a-transfer-route"></a>So erstellen Sie eine Umlagerungsroute

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Umlagerungsrouten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie von jedem beliebigen Fenster **Standortkarten** die Aktion **Umlagerungsrouten** aus.
3. Wählen Sie die Aktion **Neu** aus.
4. Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern. Weitere Informationen finden Sie unter [Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Lagerplätze

Lagerplätze stellen die grundlegende Lagerstruktur dar und werden verwendet, um Vorschläge zur Einlagerung von Artikeln zu erstellen. Wenn Sie Ihre Lagerplätze erzeugt haben, können Sie präzise festlegen, welche Inhalte in jeden Lagerplatz eingelagert werden soll, oder der Lagerplatz kann als freier Lagerplatz fungieren, dem kein bestimmter Inhalt zugewiesen wurde. Lagerplätze werden überwiegend in grundlegenden und erweiterten Lagervorgängen eingesetzt. Wenn Sie das Lager in einer einfacheren Einrichtung verwalten, benötigen Sie wahrscheinlich keine Lagerplätze.

Um die Lagerplatzfunktionen an einem Lagerort zu verwenden, aktivieren Sie zuerst die Funktion auf der Karte **Lagerort**, indem Sie das Feld **Lagerplatz notwendig** im Inforegister **Lager** auswählen. Dann entwerfen Sie den Warenfluss am Lagerort, indem Sie Lagerplatzcodes in den Einrichtungsfeldern angeben, die für die verschiedenen Ströme stehen.

> [!NOTE]
> Bevor Sie Lagerplatzcodes auf der Lagerortkarte festlegen können, müssen die Lagerplatzcodes erstellt werden.

Weitere Informationen finden Sie unter [Erstellen von Lagerplätzen](warehouse-how-to-create-individual-bins.md) und [Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zonen

Wenn Sie Ihre Lagerplätze nach Zonen strukturieren möchten, haben Sie auf der Seite **Zonen** dazu die Möglichkeit.

[!INCLUDE [prod_short](includes/prod_short.md)] kopiert die Felder, die Sie für jede Zone einrichten, in alle zugehörigen Lagerplätze. Auf diese Weise können Sie eine Zone einem Lagerplatz oder einer Lagerplatzvorlage zuweisen (Filter für Lagerplatzerstellung), und verschiedene andere Felder werden dann automatisch gefüllt.

Sie können jedoch auch nur eine Zone einrichten und Ihr Lager einfach auf Lagerplatzebene verwalten. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

## <a name="see-also"></a>Siehe auch

[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)  
[Lagerplätze erstellen](warehouse-how-to-create-individual-bins.md)  
[Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]