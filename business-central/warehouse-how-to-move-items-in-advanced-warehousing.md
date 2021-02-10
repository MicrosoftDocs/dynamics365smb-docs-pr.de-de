---
title: 'Vorgehensweise: Umlagerung von Artikeln in erweiterten Basis-Lagerkonfigurationen | Microsoft Docs'
description: In erweiterten Lagerkonfigurationen, die Lagerorte mit gesteuerter Einlagerung und Kommissionierung verwenden, werden die Umlagerungen zwischen Lagerplätzen von einem erfahrenen Mitarbeiter durchgeführt, der die Umlagerungen im Lagerplatzumlagerungsvorschlag vorbereitet und von dort aus Lagerplatzumlagerungen erstellt, die die Mitarbeiter ausführen sollen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 976ea1b26ec9a765bf38d38eadf77429d1ade61e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759817"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Umlagerung von Artikeln in erweiterten Lagerkonfigurationen
In erweiterten Lagerkonfigurationen, die Lagerorte mit gesteuerter Einlagerung und Kommissionierung verwenden, werden die Umlagerungen zwischen Lagerplätzen von einem erfahrenen Mitarbeiter durchgeführt, der die Umlagerungen im Lagerplatzumlagerungsvorschlag vorbereitet und von dort aus Lagerplatzumlagerungen erstellt, die die Mitarbeiter ausführen sollen.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Um Artikel mit dem Lagerplatzumlagerungsvorschlag umzulagern
Die Seite **Lagerplatzumlagerungsvorschlag** beinhaltet zwei Funktionen, die Sie dabei unterstützen, die Zeilen automatisch auszufüllen. Die erste Funktion ist die Funktion **Lagerplatzauffüllung berechnen**. Diese Funktion verwendet die Lagerplatzprioritäten, um eine Auffüllung der Lagerplätze aus denen mit niedrigeren Prioritäten vorzuschlagen. Die zweite Funktion ist die Funktion **Lagerplatzinhalt holen**, die die Vorschlagszeilen mit dem gesamten Inhalt des Lagerplatzes oder der Lagerplätze füllt, die Sie angeben.

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerplatzumlagerungsvorschlag** ein, und wählen Sie dann den zugehörigen Link.  
2.  Geben Sie die entsprechenden Lagerplatzumlagerungs-Informationen in die Vorschlagszeilen ein.  
3. Wählen Sie die Aktion **Lagerplatzumlagerung erstellen** aus, um einen Umlagerungsbeleg zu erstellen, der registriert werden kann, wenn die Lagerplatzumlagerung abgeschlossen ist.  

### <a name="to-register-the-warehouse-movement"></a>So registrieren Sie die Lagerplatzumlagerung:  
1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Bewegungen** ein, und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie die Lagerumlagerung, die Sie verarbeiten möchten.  
3.  Geben Sie in Zeilen der Aktionsart **Bereich** an, wo, welche und wann der fragliche Artikel umgelagert wird, indem Sie die Felder **Zonencode**, **Lagerplatzcode**, **Bewegungsmenge** oder **Fälligkeitsdatum** bearbeiten.  

    Wenn Ihr Lager so eingerichtet wurde, dass die Lagerplatzcodes der physischen Struktur des Lagers entsprechen, können Sie Mengen mehrerer Artikel aus aufeinander folgenden Gebindelagerplätzen (Palettenlagerplätzen) entnehmen und sie dann in Kommissionierlagerplätze (mit hoher Priorität) einlagern, die ebenfalls dicht nebeneinander liegen können.  
4.  Geben Sie in Zeilen der Aktionsart **Lagerentnahme** im Feld **Bewegungsmenge** eine Teilmenge des Lagerplatzinhalts ein, die Sie umlagern möchten. Alle anderen Felder in Zeilen der Aktionsart **Lagerentnahme** sind schreibgeschützt.  
5.  Um alle vorgeschlagenen Mengen zu verschieben, die im Feld **Menge** angegeben sind, wählen Sie die Aktion **Bewegungsmenge autom. ausfüllen** aus.  
6. Wählen Sie die Aktion **Registrieren** aus.  

> [!NOTE]  
>  Wenn der Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet, können Sie keine Artikel manuell in einen Lagerplatz der Lagerplatzart EING hinein oder aus diesem heraus umlagern, da Artikel in einem solchen Lagerplatz als eingelagert registriert werden müssen, bevor sie Teil des verfügbaren Lagerbestands werden.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>So registrieren Sie eine Lagerplatzumlagerung eines Artikels, die bereits stattgefunden hat:  
Wenn Ihr Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet und Sie Artikel ohne eine bereits bestehende Einlagerung, Kommissionierung oder Lagerplatzumlagerung in andere Lagerplätze umlagern müssen, können Sie die richtige Platzierung der Artikel im Lager mithilfe des **Logistik Umlag. Buch.-Blatts** registrieren.

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), und geben Sie **Logistik Umlag. Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie die Felder **Artikelnr.**, **Von Zonencode**, **Von Lagerplatzcode**, **Nach Zonencode** und **Nach Lagerplatzcode** aus.  
3.  Wählen Sie die Aktion **Registrieren** aus.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
