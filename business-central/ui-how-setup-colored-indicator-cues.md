---
title: "Geben Sie Farbindikatoren an, um visuelle Signale über eine Farbaktivität anzupassen | Microsoft Docs"
description: "Einrichten eines Farbindikator in einer Stapelkachel, um ein personalisiertes visuelles Signal der Farb-Aktivität zu erhalten."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e4ceaeae1a37a521d2d5bd22ab711757283e6321
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a>Einrichten eines farbigen Indikators auf Stapeln des Rollencenters
Sie können Stapel einrichten, die im Rollencenter mit einem Indikator angezeigt werden, dessen Farbe sich basierend auf den Datenwerten in den Stapeln ändert.

Der Indikator erscheint als farbige Leiste an der oberen Kante der Stapelfläche. Es wird ein optisches Signal zu dem Status der Aktivität des Stapels angezeigt, dss Bedingungen (vorteilhaft oder ungünstig) angeben kann, und den Benutzer auffordern kann, Maßnahmen zu ergreifen. Wenn beispielsweise ein Stapel laufende Verkaufsrechnungen angezeigt, können Sie die Markierung so einrichten, dass sie grün (vorteilhaft) angezeigt wird, wenn die Gesamtanzahl laufender Verkaufsrechnungen unter 10 ist, und in Rot (ungünstig), wenn die Anzahl größer als 20 ist.

Im Fenster **Stapel einrichten** können Sie Indikatoren für alle Stapel einrichten, die in der Unternehmensdatenbank verfügbar sind.

Um den Indikator einzurichten, geben Sie bis zu zwei Schwellenwerte an, die drei Bereiche von Datenwerten definieren (niedrig, mittel und hoch), die Sie jeweils mit einer anderen Farbe (oder einem anderen Format) anzeigen können.

## <a name="to-set-up-colored-indicators-on-cues"></a>So richten Sie farbige Indikatoren auf Stapeln ein.
1. Unter **Aktivitäten** auf Ihrer Rollencenter wählen Sie **Stapel einrichten** aus.  
   Das Fenster **Stapel einrichten** wird angezeigt. Das Fenster listet die Indikatoren auf, die derzeit in Stapeln für den Mandanten eingerichtet sind.
2. Um einen Indikator zu ändern, bearbeiten Sie die Felder und ändern Sie beispielsweise die Werte für die verschiedenen Schwellenwerte.  

Die folgende Tabelle enthält die Farben, die den Optionen der **Format des unteren Bereichs**, **Format des mittleren Bereichs** und **Format des oberen Bereichs** entsprechen.

| Option | Farbe |
| --- | --- |
| **Keine** |Keine Farbe (dieselbe Farbe wie die Stapelfläche)|
| **Vorteilhaft** |Grün |
| **Ungünstig** |Rot |
| **Mehrdeutig** |Gelb |
| **Untergeordnet** |Grau |

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

