---
title: Breaking Bulk mit gerichteter Einlagerung und Kommissionierung
description: Erfahren Sie, wie Sie das automatische Breaking Bulk mit gerichteter Einlagerung und Kommissionierung sowie das Breaking Bulk in Kommissionierungen, Einlagerungen, Lagerplatzumlagerungen und mehr aktivieren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 5703, 7352
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 86ad8c18c58eaf24665310f3455ae801ebe611a2
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518679"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung aktivieren
Bei Lagerorten, die die gesteuerte Einlagerung und Kommissionierung verwenden, kann die [!INCLUDE[prod_short](includes/prod_short.md)] in verschiedenen Situationen einen automatischen Gebindeanbruch durchführen, d. h. eine größere Einheit in kleinere Einheiten aufteilen, wenn Logistikanweisungen erstellt werden, die die Anforderungen von Herkunftsbelegen, Fertigungsaufträgen oder internen Einlagerungs- und Kommissionierungsanforderungen erfüllen. Einen Gebindeanbruch durchzuführen, bedeutet manchmal auch, kleinere Einheiten zusammenzufassen, falls dies notwendig ist, um ausgehende (das Lager verlassende) Anforderungen zu erfüllen: Als Ergebnis wird die größere Einheit im Herkunftsbeleg oder Fertigungsauftrag in kleinere Einheiten unterteilt, die im Lager verfügbar sind.   

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
[Warehouse Management einrichten](warehouse-setup-warehouse.md) 
[Montageverwaltung](assembly-assemble-items.md)
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]