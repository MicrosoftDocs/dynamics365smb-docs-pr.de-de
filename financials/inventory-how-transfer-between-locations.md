---
title: "So geht's: Lagerbestand zwischen Lagerplätzen umlagern| Microsoft Docs"
description: "Beschreibt, wie vom Bestand von einem Bereich oder von einem Lager an einen anderen Ort umgebucht wird, entweder mit dem Umlagerungs Buch.-Blatt mit oder den Umlagerungsaufträgen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d54b75240cb0a2dddcfabc488a18e0bf9635f82c
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-transfer-inventory-between-locations"></a>So geht's: Lagerbestand zwischen Lagerplätzen umlagern
Sie können Bestandsartikel zwischen Lagerplätzen umlagern, indem Sie Umlagerungsaufträge erstellen. Sie können auch das Einkaufs-Buch.-Blatt verwenden.

Bei Umlagerungsaufträgen senden Sie die ausgehende Umlagerung von einem Lagerplatz und empfangen die eingehende Umlagerung am anderen Lagerplatz. Dies ermöglicht es Ihnen, die einbezogenen Lageraktivitäten zu verwalten und bietet mehr Sicherheit, dass Lagerbestandsmengen korrekt aktualisiert werden.

Mit dem Umlagerungs Buch.-Blatt füllen Sie einfach die Felder **Lagerortcode** und **Neuer Lagerortcode** aus. Wenn Sie das Buch.-Blatt buchen, werden die Artikelposten an den fraglichen Lagerplätzen reguliert. Mit dieser Methode werden Lageraktivitäten nicht verwaltet.

> [!NOTE]  
>   Wenn Sie Artikel haben, die in Ihrem Lager ohne Lagerortcode erfasst sind, wie beispielsweise aus einer Zeit, als Sie nur ein Lager hatten, dann können Sie diejenigen Artikel nicht mithilfe von Umlagerungsaufträgen übertragen. Stattdessen müssen Sie das Umlagerungs Buch.-Blatt verwenden, um die Artikel aus einem leeren Lagerortcode zu einem tatsächlichen Lagerortcode umzubuchen.  Weitere Informationen finden Sie Schritt 3 im "Artikel mit Abschnitt des Artikel Umlag. Buch.-Blattes übertragen".

Um Artikel umzulagern, müssen Lagerplätze und Umlagerungsrouten eingerichtet werden. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lagerplätzen](inventory-how-setup-locations.md).

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.

## <a name="to-transfer-items-with-a-transfer-order"></a>So lagern Sie Artikel mit einem Umlagerungsauftrag um
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen ")aus und geben Sie **Umlagerungsaufträge** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie im Fenster **Umlagerungsauftrag** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Wenn Sie die Felder **In Transit Code**, **Zustellercode** und **Zustellertransportart** im Fenster **Umlagerungsroutenspezifikation** ausgefüllt haben, wenn Sie die Umlagerungsroute einrichten, werden die entsprechenden Felder im Umlagerungsauftrag automatisch ausgefüllt.

    Wenn Sie das Feld **Zustellertransportarten** ausfüllen, wird das Zugangsdatum am Ziellagerplatz berechnet, indem Sie die Transportzeit der Zustellertransportart zum Lieferdatum hinzuaddieren.

    Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel auszuliefern.
3. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Warenausgang**, und wählen Sie dann die Schaltfläche **OK** aus.

    Die Artikel befinden sich jetzt in der Umlagerung zwischen den angegebenen Lagerplätzen, entsprechend der angegebenen Umlagerungsroute.

    Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel zu empfangen
4. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Eingang**, und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>So lagern Sie Artikel mit dem Artikel Umlag. Buch.-Blatt um
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Artikel Buchblatt neu klassieren** ein und wählen den zugehörenden Link aus.
2. Füllen Sie im Fenster **Umlagerungs Buch.-Blatt** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Geben Sie im Feld **Lagerortcode** den Lagerplatz ein, an dem die Artikel aktuell gelagert sind.

    > [!NOTE]  
>   Um Artikel umzulagern die keinen Lagerortcode haben, belassen Sie das Feld **Lagerortcode** leer.
4. Im Feld **Neuer Lagerortcode** geben Sie den Lagerplatz ein, an den Sie die Artikel umlagern möchten.
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="see-also"></a>Siehe auch
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[So wird's gemacht: Standorte einrichten](inventory-how-setup-locations.md)  
[Lieferkette](madeira-supply-chain.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassen der[!INCLUDE[d365fin](includes/d365fin_md.md)]Erfahrung](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
