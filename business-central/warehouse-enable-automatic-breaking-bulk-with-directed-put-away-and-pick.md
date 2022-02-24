---
title: 'Vorgehensweise: Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung | Microsoft Docs'
description: Bei Lagerorten, die die gesteuerte Einlagerung und Kommissionierung verwenden, können Sie eine größere Einheit in kleinere Einheiten aufteilen, wenn Logistikanweisungen erstellt werden, die die Anforderungen von Herkunftsbelegen, Fertigungsaufträgen oder internen Einlagerungs- und Kommissionierungsanforderungen erfüllen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9d2e0c1b065cfb96c27bc7f76ab3168e927e3705
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193323"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung aktivieren
Bei Lagerorten, die die gesteuerte Einlagerung und Kommissionierung verwenden, kann die [!INCLUDE[d365fin](includes/d365fin_md.md)] in verschiedenen Situationen einen automatischen Gebindeanbruch durchführen, d. h. eine größere Einheit in kleinere Einheiten aufteilen, wenn Logistikanweisungen erstellt werden, die die Anforderungen von Herkunftsbelegen, Fertigungsaufträgen oder internen Einlagerungs- und Kommissionierungsanforderungen erfüllen. Einen Gebindeanbruch durchzuführen, bedeutet manchmal auch, kleinere Einheiten zusammenzufassen, falls dies notwendig ist, um ausgehende (das Lager verlassende) Anforderungen zu erfüllen: Als Ergebnis wird die größere Einheit im Herkunftsbeleg oder Fertigungsauftrag in kleinere Einheiten unterteilt, die im Lager verfügbar sind.   

## <a name="breakbulking-in-picks"></a>Gebindeanbruch beim Kommissionieren  
Wenn Sie Artikel in unterschiedlichen Einheiten lagern möchten und der Anwendung erlauben, diese beim Kommissionieren zu kombinieren, wählen Sie das Feld **Gebindeanbruch zulassen** der Lagerortkarte.  

Um eine Aufgabe auszuführen, sucht die Anwendung automatisch nach einem Artikel in der gleichen Einheit. Wenn sie jedoch den Artikel nicht in dieser Form findet und Sie dieses Feld ausgewählt haben, schlägt die Anwendung vor, dass Sie eine größere Einheit in die Einheit aufbrechen, die erforderlich ist.  

Wenn das System nur kleinere Einheiten findet, schlägt sie vor, dass Sie Artikel zusammenfassen, um die Menge im Warenausgang oder Fertigungsauftrag zu erfüllen. Das Ergebnis ist, dass sie größere Einheiten im Herkunftsbeleg für die Kommissionierung in kleinere Einheiten aufbricht.  

## <a name="breakbulking-in-put-aways"></a>Gebindeanbruch beim Einlagern  
Bei der Einlagerung in der Logistik schlägt die Anwendung dann automatisch Zeilen mit der Aktionsart "Einlagerung" in der Einlagerungseinheit (z. B. Stück) vor, obwohl die Artikel in einer abweichenden Einheit ankommen.  

## <a name="breakbulking-in-movements"></a>Gebindeanbruch bei Lagerplatzumlagerungen  
Die Anwendung führt einen automatischen Gebindeanbruch auch bei Lagerplatzumlagerungen zum Wiederauffüllen durch, wenn das Feld **Gebindeanbruch zulassen** im Inforegister unter **Option** auf der Seite **Lagerplatzauffüllung berechnen** ausgewählt ist.  

Sie können sich das Ergebnis der Konvertierung von einer Einheit in eine andere als vorläufige Gebindeanbruchszeilen in den Einlagerungs-, Kommissionierungs- oder Lagerplatzumlagerungsanweisungen anzeigen lassen.  

> [!NOTE]  
>  Wenn das Feld **Gebindeanbruchsfilter** des Kopfes der Logistikanweisung gewählt wird, blendet die Anwendung die Gebindeanbruchszeilen aus, solange die größere Einheit vollständig verwendet wird. Wenn z. B. eine Palette aus 12 Stück besteht, und Sie alle 12 Stück auch verwenden, erhalten Sie von der Kommissionierung die Anweisung, eine Palette zu kommissionieren und 12 Stück einzulagern. Wenn Sie jedoch nur 9 Stück kommissionieren müssen, werden die Gebindeanbruchszeilen nicht versteckt, selbst wenn Sie das Feld **Gebindeanbruchsfilter** ausgewählt haben, da Sie die drei überzähligen Stück an beliebiger Stelle im Lager einlagern müssen.  

> [!NOTE]  
>  Wenn Sie möchten, dass sich eine Einheit in der Logistik optimal verhält, auch im Zusammenhang mit der Gebindeanbruchsfunktionalität, sollten Sie – falls möglich – Folgendes versuchen:  
>   
> - Richten Sie die Einheit eines Artikels als die kleinste Einheit ein, von der Sie erwarten, dass Sie sie in Ihren Logistikprozessen verarbeiten müssen.  
> - Richten Sie Ihre alternativen Einheiten für diesen Artikel als Vielfache der Basiseinheit ein.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
