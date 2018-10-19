---
title: "So richten Sie Lagerorte zur Verwendung von Lagerplätzen ein | Microsoft Docs"
description: "Lagerplätze stellen die grundlegende Lagerstruktur dar und werden verwendet, um Vorschläge zur Einlagerung von Artikeln zu erstellen. Wenn Sie Ihre Lagerplätze erzeugt haben, können Sie sehr genau festlegen, welche Inhalte in jeden Lagerplatz eingelagert werden soll, oder der Lagerplatz kann als freier Lagerplatz fungieren, dem kein bestimmter Inhalt zugewiesen wurde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 214de72b86e3d32e5161814a7f65079cbb4136b7
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-locations-to-use-bins"></a>Lagerorte für die Verwendung von Lagerplätzen einrichten
Lagerplätze stellen die grundlegende Lagerstruktur dar und werden verwendet, um Vorschläge zur Einlagerung von Artikeln zu erstellen. Wenn Sie Ihre Lagerplätze erzeugt haben, können Sie sehr genau festlegen, welche Inhalte in jeden Lagerplatz eingelagert werden soll, oder der Lagerplatz kann als freier Lagerplatz fungieren, dem kein bestimmter Inhalt zugewiesen wurde.  

Um die Funktionalität der Lagerplätze zu nutzen, müssen Sie diese auf der Karte **Lagerort** aktivieren. Dann entwerfen Sie den Warenfluss am Lagerort, indem Sie Lagerplatzcodes in den Einrichtungsfeldern angeben, die für die verschiedenen Ströme stehen.  

> [!NOTE]  
>  Bevor Sie Lagerplatzcodes auf der Lagerortkarte festlegen können, müssen die Lagerplatzcodes erstellt werden. Weitere Informationen finden Sie unter  [Lagerplätze erstellen](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Um einen Lagerort für die Verwendung von Lagerplätzen einzurichten  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie den Lagerort aus, an dem Sie Lagerplätze verwenden möchten.  
3.  Wählen Sie die Aktion **Bearbeiten** aus.  
4.  Aktivieren Sie im Inforegister **Lager** das Kontrollkästchen **Lagerplatz notwendig**.  
5.  Wenn Sie für den Lagerort die gesteuerte Einlagerung und Kommissionierung nicht nutzen, tragen Sie in das Feld **Vorg.-Lagerplatzauswahl** die Methode ein, die die Anwendung verwenden soll, wenn sie einem Artikel einen Standardlagerplatz zuweist.  
6.  Öffnen Sie  die Karte für den Lagerort, an dem Sie Lagerplätze einrichten möchten.
7.  Wählen Sie im Inforegister **Lagerplätze** die Lagerplätze, die Sie als Vorgabe Lagerplätze für Wareneingänge, Warenausgänge sowie zur Fertigungsbereitstellung, als Fertigungsausgangslager und für die offene Fertigungsbereitstellung nutzen möchten.  
8.  Die Lagerplatzcodes, die Sie hier eintragen, erscheinen automatisch im Kopf und danach in den Zeilen von verschiedenen Logistikbelegen. Die Vorgabe Lagerplätze legen alle Start- und Endeinlagerungen von Artikeln im Lager fest.  
9.  Wenn Sie die gesteuerte Einlagerung und Kommissionierung nutzen, wählen Sie einen Lagerplatz für den Ausgleich. Der Lagerplatzcode im Feld **Ausgleichslagerplatzcode** legt den virtuellen Lagerplatz fest, an dem Abweichungen im Lagerbestand erfasst werden, wenn Sie entweder beobachtete Abweichungen registrieren, die im Logistik Artikel Buch.-Blatt registriert wurden, oder Differenzen, die beim Registrieren einer Inventur im Logistikbereich berechnet werden.  
10. Füllen Sie die Felder im Inforegister **Lagerplatzprüfung** aus, wenn sie für Ihr Lager relevant sind. Die wichtigsten Felder sind **Lagerkapazitätsprüfung**, **Gebindeanbruch zulassen** und **Einlagerungsvorlagencode**.  
11. Tragen Sie im Inforegister **Logistik** die Felder **Ausgeh. Lagerdurchlaufzeit**, **Eingeh. Lagerdurchlaufzeit** und **Basiskalendercode** ein. Weitere Informationen finden Sie unter [Einrichten von Grundkalendern](across-how-to-assign-base-calendars.md).

## <a name="filling-the-consumption-bin"></a>Auffüllen des Verbrauchslagerplatzes
Dieses Flussdiagramm zeigt, wie das Feld **Lagerplatzcode** in FA-Komponentenzeilen entsprechend Ihrer Einrichtung ausgefüllt wird.

![Lagerplatz-Flussdiagramm](media/binflow.png "Lagerfluss")  

## <a name="see-also"></a>Siehe auch
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

