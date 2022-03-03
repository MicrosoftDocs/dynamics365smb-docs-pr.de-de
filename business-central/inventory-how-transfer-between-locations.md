---
title: Artikel zwischen Lagerorten transferieren
description: Beschreibt, wie vom Bestand von einem Bereich oder von einem Lager an einen anderen Ort umgebucht wird, entweder mit dem Umlagerungs Buch.-Blatt mit oder den Umlagerungsaufträgen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.search.forms: 5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b51bd44099c85ae16498e2f40abc86db7134cb1b
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148498"
---
# <a name="transfer-inventory-between-locations"></a>Lagerbestand zwischen Lagerplätzen umlagern
Sie können Bestandsartikel zwischen Lagerplätzen umlagern, indem Sie Umlagerungsaufträge erstellen. Sie können auch das Einkaufs-Buch.-Blatt verwenden.

Bei Umlagerungsaufträgen senden Sie die ausgehende Umlagerung von einem Lagerplatz und empfangen die eingehende Umlagerung am anderen Lagerplatz. Dies ermöglicht es Ihnen, die einbezogenen Lageraktivitäten zu verwalten und bietet mehr Sicherheit, dass Lagerbestandsmengen korrekt aktualisiert werden.

Mit dem Umlagerungs Buch.-Blatt füllen Sie einfach die Felder **Lagerortcode** und **Neuer Lagerortcode** aus. Wenn Sie das Buch.-Blatt buchen, werden die Artikelposten an den fraglichen Lagerplätzen reguliert. Mit dieser Methode werden Lageraktivitäten nicht verwaltet.

> [!NOTE]  
>   Wenn Sie Artikel haben, die in Ihrem Lager ohne Lagerortcode erfasst sind, wie beispielsweise aus einer Zeit, als Sie nur ein Lager hatten, dann können Sie diejenigen Artikel nicht mithilfe von Umlagerungsaufträgen übertragen. Stattdessen müssen Sie das Umlagerungs Buch.-Blatt verwenden, um die Artikel aus einem leeren Lagerortcode zu einem tatsächlichen Lagerortcode umzubuchen.  Weitere Informationen finden Sie in Schritt 3 unter [So lagern Sie Artikel mit dem Artikel Umlag. Buch.-Blatt um](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Um Artikel umzulagern, müssen Lagerplätze und Umlagerungsrouten eingerichtet werden. Weitere Informationen finden Sie unter [Einrichten von Lagerorten](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>So lagern Sie Artikel mit einem Umlagerungsauftrag um
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Umlagerungsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie auf der Seite **Umlagerungsauftrag** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Wenn Sie die Felder **Umlag. in Code**, **Zustellercode** und **Zustellertransportartencode** auf der Seite **Umlagerungsroutenspezifikation** ausgefüllt haben, als Sie die Umlagerungsrouten zwischen diesen Lagerorten eingerichtet haben, werden die entsprechenden Felder im Umlagerungsauftrag automatisch ausgefüllt.

    Wenn Sie das Feld **Zustellertransportarten** ausfüllen, wird das Zugangsdatum am Ziellagerplatz berechnet, indem Sie die Transportzeit der Zustellertransportart zum Lieferdatum hinzuaddieren.

3. Um die Zeilen auszufüllen, geben Sie sie entweder manuell ein oder wählen Sie eine der folgenden Optionen unter der Aktion **Funktionen** aus:
    - Wählen Sie die Aktion **Bin-Inhalt abrufen** aus, um vorhandene Elemente aus einem bestimmten Fach am Standort auszuwählen.
    - Wählen Sie **Belegzeilen abrufen** aus, um Elemente auszuwählen, die gerade am Transfer-von-Standort angekommen sind.   

    Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel auszuliefern.
4. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Warenausgang**, und wählen Sie dann die Schaltfläche **OK** aus.

    Die Artikel befinden sich jetzt in der Umlagerung zwischen den angegebenen Lagerplätzen, entsprechend der angegebenen Umlagerungsroute.

    Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel zu empfangen Die Überweisungsauftragspositionen sind dieselben wie im Auslieferungszustand und können nicht bearbeitet werden.
5. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Eingang**, und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>So lagern Sie Artikel mit dem Artikel Umlag. Buch.-Blatt um
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element Reclass. Erfassungen** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie auf der Seite **Umlagerungs Buch.-Blatt** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Geben Sie im Feld **Lagerortcode** den Lagerplatz ein, an dem die Artikel aktuell gelagert sind.

    > [!NOTE]  
    >   Um Artikel umzulagern die keinen Lagerortcode haben, belassen Sie das Feld **Lagerortcode** leer.
4. Im Feld **Neuer Lagerortcode** geben Sie den Lagerplatz ein, an den Sie die Artikel umlagern möchten.
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="see-also"></a>Siehe auch
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Einrichten von Lagerorten](inventory-how-setup-locations.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Merkmale angezeigt werden](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]