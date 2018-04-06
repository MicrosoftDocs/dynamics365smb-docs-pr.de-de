---
title: 'Vorgehensweise: Umlagerung von Artikeln in erweiterten Basis-Lagerkonfigurationen | Microsoft Docs'
description: "In erweiterten Lagerkonfigurationen, die Lagerorte mit gesteuerter Einlagerung und Kommissionierung verwenden, werden die Umlagerungen zwischen Lagerplätzen von einem erfahrenen Mitarbeiter durchgeführt, der die Umlagerungen im Lagerplatzumlagerungsvorschlag vorbereitet und von dort aus Lagerplatzumlagerungen erstellt, die die Mitarbeiter ausführen sollen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/232017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4caa041c6b3acef5d0cbf6c037f0ec535cd3176e
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Umlagerung von Artikeln in erweiterten Lagerkonfigurationen
In erweiterten Lagerkonfigurationen, die Lagerorte mit gesteuerter Einlagerung und Kommissionierung verwenden, werden die Umlagerungen zwischen Lagerplätzen von einem erfahrenen Mitarbeiter durchgeführt, der die Umlagerungen im Lagerplatzumlagerungsvorschlag vorbereitet und von dort aus Lagerplatzumlagerungen erstellt, die die Mitarbeiter ausführen sollen.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Um Artikel mit dem Lagerplatzumlagerungsvorschlag umzulagern
Das Fenster **Lagerplatzumlagerungsvorschlag** beinhaltet zwei Funktionen, die Sie dabei unterstützen, die Zeilen automatisch auszufüllen. Die erste Funktion ist die Funktion **Lagerplatzauffüllung berechnen**. Diese Funktion verwendet die Lagerplatzprioritäten, um eine Auffüllung der Lagerplätze aus denen mit niedrigeren Prioritäten vorzuschlagen. Die zweite Funktion ist die Funktion **Lagerplatzinhalt holen**, die die Vorschlagszeilen mit dem gesamten Inhalt des Lagerplatzes oder der Lagerplätze füllt, die Sie angeben.

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplatzumlagerungsvorschlag** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Geben Sie die entsprechenden Lagerplatzumlagerungs-Informationen in die Vorschlagszeilen ein.  
3. Wählen Sie die Aktion **Lagerplatzumlagerung erstellen**aus, um einen Umlagerungsbeleg zu erstellen, der registriert werden kann, wenn die Lagerplatzumlagerung abgeschlossen ist.  

### <a name="to-register-the-warehouse-movement"></a>So registrieren Sie die Lagerplatzumlagerung:  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Lagerplatzumlagerungen** ein. Wählen Sie dann den zugehörigen Link aus.  
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

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Logistik Umlag. Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Füllen Sie die Felder **Artikelnr.**, **Von Zonencode**, **Von Lagerplatzcode**, **Nach Zonencode** und **Nach Lagerplatzcode** aus.  
3.  Wählen Sie die Aktion **Registrieren** aus.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

