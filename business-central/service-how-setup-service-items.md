---
title: Übersicht und Einrichten von Serviceartikel und Serviceartikelkomponenten | Microsoft Docs
description: Erhalten von Informationen über die Elemente, die Sie einrichten müssen, bevor Sie Serviceartikel, einschließlich Vorgabewerte wie Reaktionszeit, Vertragsrabatt, und Servicepreisgruppen verwenden können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 196f3d73827f03ce03e4990039779d8f814295ff
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877399"
---
# <a name="set-up-service-items-and-service-item-components"></a>Richten Sie Serviceartikel und Serviceartikelkomponenten ein.
Um mit Serviceartikeln arbeiten können, müssen Sie Folgendes einrichten

* Serviceartikelgruppen
* Optional

## <a name="to-set-up-service-item-groups"></a>Um Serviceartikelgruppen einzurichten:
Sie können Artikelgruppen einrichten, die bezüglich Reparatur und Wartung miteinander in Verbindung stehen. Sie können für Serviceartikel in einer Serviceartikelgruppe Vorgabewerte wie Reaktionszeit, Vertragsrabatt und Servicepreisgruppe festlegen. Für Artikel in einer Serviceartikelgruppe können Sie auswählen, ob sie beim Verkauf automatisch als Serviceartikel erfasst werden sollen.  

Sie verbinden die Serviceartikelgruppen mit **Artikeln** auf der Artikelkarte und mit Serviceartikeln auf der **Serviceartikel**-Karte.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceartikelgruppen** ein und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie eine neue Serviceartikelgruppe.  
3. Füllen Sie die Felder **Code** und **Beschreibung** aus.  
4. Im Feld **Vorg.-Vertragsrabatt %** geben Sie den Vertragsrabattprozentsatz ein, der als Standardwert für Serviceartikel in dieser Gruppe angewendet werden soll.  
5. Im Feld **Vorg.-Servicepreisgrp.-Code** geben Sie den Servicepreisgruppencode ein, der als Standardwert für Serviceartikel in dieser Gruppe angewendet werden soll.  
6. Im Feld **Vorg.-Reaktionszeit (Std.)** geben Sie die Reaktionszeit in Stunden ein, die als Standardwert auf Serviceartikel in dieser Gruppe angewendet werden soll.  
7. Wenn die Artikel in der Gruppe beim Verkauf als Serviceartikel erfasst werden sollen, aktivieren Sie das Feld **Serviceartikel erstellen**.  

## <a name="to-set-up-service-item-components"></a>So richten Sie Serviceartikelkomponenten ein
Ein Serviceartikel kann aus mehreren Komponenten bestehen, die mit Ersatzteilen ersetzt werden können, wenn ein Service durchgeführt wird. Diese Komponenten werden in dem Fenster **Serviceartikelkomponenten** eingerichtet. Wenn Sie Komponenten für Serviceartikel einrichten wollen, die Stücklisten sind, können die Stücklistenartikel als Serviceartikelkomponenten angelegt werden.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceartikel** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie den Serviceartikel, für den Sie Komponenten einrichten möchten.  
3. Wählen Sie die Aktion **Komponenten** aus. Die Seite **Serviceartikelkomponenten** wird geöffnet.  
4. Fügen Sie eine neue Komponente hinzu.  
5. Wählen Sie im Feld **Art** den Eintrag **Serviceartikel**, falls die Komponente selbst ein Serviceartikel ist. Oder wählen Sie **Artikel** aus.  
6. Geben Sie im Feld **Nr.** Wählen Sie im Feld Nr. den Artikel oder Serviceartikel aus, der eine Komponente des Serviceartikels ist.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>So richten Sie Serviceartikelkomponenten aus Stücklisten ein
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceartikel** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den Serviceartikel, für den Sie Komponenten aus Stücklisten einrichten möchten.  
3. Wählen Sie die Aktion **Komponenten** aus. Die Seite **Serviceartikelkomponenten** wird geöffnet.  
4. Wählen Sie im Fenster **Kopiere von Stückliste**  

    Ist der mit dem Serviceartikel verbundene Artikel eine Stückliste, werden für alle Artikel in der Stückliste automatisch Komponenten erstellt.  

## <a name="to-set-up-a-service-shelf"></a>So richten Sie ein Servicelagerfach ein
Sie können Servicelagerfächer einrichten, die identifizieren, wo Sie Serviceartikel speichern. Servicelagerfächer werden im Fenster **Serviceauftrag** und im Fenster **Servicearbeitsschein** mit Serviceartikeln verbunden.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Servicelagerfächer** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="see-also"></a>Siehe auch
[Einrichten von Codes für Standardservices](service-how-setup-service-coding.md)   
[Lösungsanleitung Einrichtung](service-how-setup-troubleshooting.md)
