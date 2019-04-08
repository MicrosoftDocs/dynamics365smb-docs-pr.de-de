---
title: Eine Kreditorenkarte erstellen, um einen neuen Kreditor zu erfassen | Microsoft Docs
description: Erfahren Sie, wie Sie eine Kreditorenkarte erstellt, um einen neuen Kreditor oder einem Lieferanten zu erfassen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: c8f8620d21b9e2187e968d4015fd0f12446d30c9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799093"
---
# <a name="register-new-vendors"></a>Registriert einen neuen Kreditor
Kreditoren stellen die Produkte bereit, die Sie verkaufen. Jeder Kreditor, von dem Sie kaufen, muss als Kreditorenkarte erfasst werden.

Bevor Sie neue Kreditoren erfassen können, müssen Sie verschiedene Einkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Kreditorenkarten ausfüllen. Nach der Erstellung aller erforderlichen Masterdaten können weitere Konfigurationsschritte für den Mandanten – wie Priorisieren des Kreditors zu Zahlungszwecken oder Aufführen von Artikeln, die von diesem und anderen Kreditoren geliefert werden – ausgeführt werden. Eine weitere Gruppe von Einrichtungsaufgaben bildet die Erfassung von Vereinbarungen zu Rabatten, Preisen und Zahlungsformen. Weitere Informationen finden Sie unter [Einrichten des Einkaufs](purchasing-setup-purchasing.md).

Kreditorenkarten verwahren die Informationen, die benötigt werden, um Produkte vom Kreditor einzukaufen. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md) und [Neue Artikel registrieren](inventory-how-register-new-items.md).

> [!NOTE]  
>   Wenn es Kreditorenvorlagen für verschiedene Kreditorenarten gibt, dann erscheint eine Seite automatisch, wenn Sie eine neue Kreditorenkarte erstellen, von der aus Sie eine entsprechende Kreditorenvorlage auswählen können. Wenn nur eine Kreditorenvorlage vorhanden ist, verwenden neue Kreditorenkarten immer diese Vorlage.

## <a name="to-create-a-new-vendor-card"></a>Erstellen einer neue Kreditorenkarte
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kreditoren** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Kreditoren** **Neu** aus.

    Wenn mehr als eine Kreditorenvorlage vorhanden ist, dann öffnet sich eine Seite mit verfügbaren Kreditorenvorlagen automatisch. In diesem Fall, folgen Sie den nächsten zwei Schritten.
3. Wählen Sie auf der Seite **Vorlage für neuen Kreditor auswählen** die Vorlage, die Sie für die neue Kreditorenkarte verwenden möchten.
4. Wählen Sie die Schaltfläche **OK** aus. Eine neue Kreditorenkarte wird geöffnet mit einigen Feldern, die mit Daten aus der Vorlage ausgefüllt werden.
5. Wenn nötig, fahren Sie mit dem Ausfüllen oder Ändern der Felder auf der Kreditorenkarte fort. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Falls Sie nicht im Voraus wissen, ob eine bestimmte Rechnungsadresse für jede Rechnung eines Kreditoren verwendet wird, füllen Sie das Feld **Zahlung an Kred.-Nr.** auf der Kreditorenkarte nicht aus. Geben Sie stattdessen die Zahlung-an Kred.-Nr. später ein, wenn Sie eine Einkaufsanfrage, -bestellung oder -rechnung erstellen.

Der Kreditor ist nun erfasst und die Kreditorenkarte ist bereit, in Einkaufsbeleg verwendet zu werden, in denen Sie mit dem Kreditor handeln.

Wenn Sie diese Kreditorenkarte als Vorlage verwenden möchten, wenn Sie neue Kreditorenkarten erstellen, dann fahren sie fort, um sie als Kreditorenvorlage zu speichern. Weitere Informationen finden Sie im folgenden Abschnitt.

## <a name="to-save-the-vendor-card-as-a-template"></a>So speichern Sie die Kreditorenkarte als Vorlage
1. Wählen Sie auf der Seite **Kreditorenkarte** die Aktion **Als Vorlage speichern** aus. Die Seite **Kreditorenvorlage** wird geöffnet und zeigt die Kreditorenkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Die Seite **Dimensionen Vorlagen** wird geöffnet und zeigt alle Dimensionscodes, die für den Kreditor eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Kreditorenkarten gelten, die mit der Vorlage erstellt wurden.
5. Wenn Sie die neue Kreditorvorlage abgeschlossen haben, klicken Sie auf die Schaltfläche **OK**.  
   Die Kreditorvorlage wird der Liste von Kreditorvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Kreditorenkarten zu erstellen.

## <a name="see-also"></a>Siehe auch
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)   
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
