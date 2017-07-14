---
title: 'So gehts: Neue Kreditoren registrieren | Microsoft Docs'
description: "Erfahren Sie, wie Sie Kreditoren Ihrem Financials hinzufügen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 3420a91200b64ea0672d5757a0104c6806fc607f
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Vorgehensweise: Einen neuen Kreditor registrieren
<a id="how-to-register-new-vendors" class="xliff"></a>
Kreditoren stellen die Produkte bereit, die Sie verkaufen. Jeder Kreditor, von dem Sie kaufen, muss als Kreditorenkarte erfasst werden.

Bevor Sie neue Kreditoren erfassen können, müssen Sie verschiedene Einkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Kreditorenkarten ausfüllen. Nach der Erstellung aller erforderlichen Masterdaten können weitere Konfigurationsschritte für den Mandanten – wie Priorisieren des Kreditors zu Zahlungszwecken oder Aufführen von Artikeln, die von diesem und anderen Kreditoren geliefert werden – ausgeführt werden. Eine weitere Gruppe von Einrichtungsaufgaben bildet die Erfassung von Vereinbarungen zu Rabatten, Preisen und Zahlungsmethoden. Weitere Informationen finden Sie unter [Einrichten des Einkaufs](purchasing-setup-purchasing.md).

Kreditorenkarten verwahren die Informationen, die benötigt werden, um Produkte vom Kreditor einzukaufen. Weitere Informationen finden Sie unter [Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md) und [Vorgehensweise: Neue Produkte erfassen](inventory-how-register-new-items.md).

**Hinweis**: Wenn es Kreditorenvorlagen für verschiedene Kreditorenarten gibt, dann erscheint ein Fenster automatisch, wenn Sie eine neue Kreditorenkarte erstellen, von der aus Sie eine entsprechende Kreditorenvorlage auswählen können. Wenn nur eine Kreditorenvorlage vorhanden ist, verwenden neue Kreditorenkarten immer diese Vorlage.

## Erstellen einer neue Kreditorenkarte
<a id="to-create-a-new-vendor-card" class="xliff"></a>
1. Auf der Startseite wählen Sie **Kreditoren**, um die Liste der Bestandskreditoren zu öffnen.  
2. Im **Kreditoren**-Fenster wählen Sie **Neu**.

    Wenn mehr als eine Kreditorenvorlage vorhanden ist, dann öffnet sich ein Fenster mit verfügbaren Kreditorenvorlagen automatisch. In diesem Fall, folgen Sie den nächsten zwei Schritten.
3. Wählen Sie im Fenster **Vorlage für neuen Kreditor auswählen** die Vorlage, die Sie für die neue Kreditorenkarte verwenden möchten.
4. Wählen Sie die Schaltfläche **OK** aus. Eine neue Kreditorenkarte wird geöffnet mit einigen Feldern, die mit Daten aus der Vorlage ausgefüllt werden.
5. Wenn nötig, fahren Sie mit dem Ausfüllen oder Ändern der Felder auf der Kreditorenkarte fort. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Der Kreditor ist nun erfasst und die Kreditorenkarte ist bereit, in Einkaufsbeleg verwendet zu werden, in denen Sie mit dem Kreditor handeln.

Wenn Sie diese Kreditorenkarte als Vorlage verwenden möchten, wenn Sie neue Kreditorenkarten erstellen, dann fahren sie fort, um sie als Kreditorenvorlage zu speichern. Weitere Informationen finden Sie im folgenden Abschnitt.

## So speichern Sie die Kreditorenkarte als Vorlage
<a id="to-save-the-vendor-card-as-a-template" class="xliff"></a>
1. Wählen Sie im Fenster **Kreditorenkarte** die Aktion **Als Vorlage speichern** aus. Das Fenster **Kreditorenvorlage** wird geöffnet und zeigt die Kreditorenkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Das Fenster **Dimensionen Vorlagenübersicht** wird geöffnet und zeigt alle Dimensionscodes, die für den Kreditor eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Kreditorenkarten gelten, die mit der Vorlage erstellt wurden.
5. Wenn Sie die neue Kreditorvorlage abgeschlossen haben, klicken Sie auf die Schaltfläche **OK**.  
   Die Kreditorvorlage wird der Liste von Kreditorvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Kreditorenkarten zu erstellen.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Einkauf](purchasing-manage-purchasing.md)  
[Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md)   
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

