---
title: Breaking Bulk mit gerichteter Einlagerung und Kommissionierung
description: 'Erfahren Sie, wie Sie das automatische Teilen von Gebindeeinheiten mit gerichteter Einlagerung und Kommissionierung sowie den Gebindeanbruch beim Kommissionieren, Einlagern, Lagerplatzumlagern und mehr aktivieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Automatisches Teilen von Gebindeeinheiten mit gesteuerter Einlagerung und Kommissionierung aktivieren

Bei Lagerorten, die die gesteuerte Einlagerung und Kommissionierung verwenden, kann [!INCLUDE[prod_short](includes/prod_short.md)] größere Einheiten in kleinere Einheiten aufteilen, wenn es Logistikanweisungen für Herkunftsbelege, Fertigungsaufträge oder interne Einlagerungen und Kommissionierungen erstellt. Einen Gebindeanbruch durchzuführen, kann auch bedeuten, Artikel in kleineren Einheiten zu sammeln, um der Menge einer größeren Einheit in einem Herkunftsbeleg oder Fertigungsauftrag zu entsprechen.

## <a name="breakbulk-in-picks"></a>Gebindeanbruch beim Kommissionieren

Wenn Sie Artikel in mehreren unterschiedlichen Einheiten an einem Lagerort lagern möchten und erlauben, diese beim Kommissionieren automatisch zu kombinieren, aktivieren Sie den Umschalter **Gebindeanbruch zulassen** auf der Lagerortseite. Danach, um eine Aufgabe auszuführen, sucht [!INCLUDE [prod_short](includes/prod_short.md)] nach einem Artikel in der gleichen Einheit. Wenn es keinen findet, wird [!INCLUDE [prod_short](includes/prod_short.md)] vorschlagen, dass Sie eine größere Einheit in die benötigte Einheit zerlegen.  

Wenn nur kleinere Einheiten verfügbar sind, schlägt [!INCLUDE [prod_short](includes/prod_short.md)] vor, dass Sie Artikel zusammenfassen, um die Menge im Warenausgang oder Fertigungsauftrag zu erfüllen. Das Ergebnis ist, dass sie größere Einheiten im Herkunftsbeleg für die Kommissionierung in kleinere Einheiten aufbricht.  

## <a name="breakbulk-in-put-aways"></a>Gebindeanbruch beim Einlagern

Bei Lagereinlagerungen schlägt [!INCLUDE [prod_short](includes/prod_short.md)] Zeilen mit der Aktionsart „Einlagerung“ in der Einlagerungseinheit vor. Beispielsweise kann es Stücke vorschlagen, obwohl die Artikel in einer anderen Einheit ankommen.  

## <a name="breakbulk-in-movements"></a>Gebindeanbruch bei Lagerplatzumlagerungen

[!INCLUDE [prod_short](includes/prod_short.md)] kann auch einen Gebindeanbruch in Auffüllumlagerungen durchführen, wenn der Umschalter **Gebindeanbruch zulassen** auf der Seite **Lagerplatzauffüllung berechnen** eingeschaltet ist.  

Sie können sich das Ergebnis der Konvertierung von einer Einheit in eine andere als vorläufige Gebindeanbruchszeilen in den Einlagerungs-, Kommissionierungs- oder Lagerplatzumlagerungsanweisungen anzeigen lassen.  

> [!NOTE]  
> Wenn das Feld **Gebindeanbruchsfilter** des Kopfes der Logistikanweisung gewählt wird, blendet die Anwendung die Gebindeanbruchszeilen aus, solange die größere Einheit vollständig verwendet wird. Wenn z. B. eine Palette aus 12 Stück besteht und Sie alle 12 Stück verwenden, erhalten Sie von der Kommissionierung die Anweisung, eine Palette zu kommissionieren und 12 Stück einzulagern. Wenn Sie jedoch nur 9 Stück kommissionieren müssen, werden die Gebindeanbruchszeilen nicht ausgeblendet, auch wenn Sie das Feld **Gebindeanbruchsfilter** ausgewählt haben. Die Zeilen werden nicht ausgeblendet, da Sie die restlichen drei Stücke irgendwo im Lager ablegen müssen.  

> [!NOTE]  
> Wenn Sie möchten, dass sich Ihre Einheiten im Lager optimal verhalten, auch im Zusammenhang mit dem Gebindeanbruch, sollten Sie Folgendes versuchen:  
>
> - Richten Sie die Einheit eines Artikels als die kleinste Einheit ein, von der Sie erwarten, dass Sie sie in Ihren Logistikprozessen verarbeiten müssen.  
> - Richten Sie Ihre alternativen Einheiten für diesen Artikel als Vielfache der Basiseinheit ein.  

## <a name="see-also"></a>Weitere Informationen

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten der Lagerverwaltung](warehouse-setup-warehouse.md) 
[Montageverwaltung](assembly-assemble-items.md)
[Arbeiten Sie mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
