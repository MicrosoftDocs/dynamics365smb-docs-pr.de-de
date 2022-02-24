---
title: Gebuchte Einkaufs- und Verkaufsbelege bearbeiten | Microsoft Docs
description: Erfahren Sie mehr über die verschiedenen Buchungsfunktionen zum Buchen von Einkaufsbelegen und wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1041dda83552af3c2c805c08518600d89f0467fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188732"
---
# <a name="edit-posted-documents"></a>Gebuchte Belege bearbeiten
Manchmal müssen Sie einen gebuchten Beleg aktualisieren, da sich die für das Dokument relevanten Informationen geändert haben. Bei einem gebuchten Verkaufsbeleg kann dies beispielsweise die Paketverfolgungsnummer des Zustellers sein. Bei einem gebuchten Einkaufsbeleg kann es sich um einen Zahlungsreferenztext handeln.

Sie führen die Änderung an einer bearbeitbaren Version des Originaldokuments durch, was durch „**- Update**“ im Seitentitel angegeben wird. Die Seite enthält eine Teilmenge der Felder im Originaldokument, von denen einige nicht bearbeitbare Felder sind, die nur zu Informationszwecken angezeigt werden.

Die Funktionalität ist für folgende Dokumente in allen Länderversionen verfügbar:
- Geb. Verkaufslieferung
- Geb. Einkaufsrechnung
- Gebuchte Rücklieferung
- Gebuchte Rücksendung

Die folgenden zusätzlichen Dokumente können in ausgewählten Länderversionen bearbeitet werden:
- ES: Gebuchte Verkaufsrechnung, Geb. Verkaufsgutschrift, Gebuchte Einkaufsgutschrift
- APAC: Geb. Verkaufsgutschrift, Gebuchte Einkaufsgutschrift
- RU: Geb. Verkaufsgutschrift
- IT: Geb. Umlag.-Ausgang, Gebuchte Servicelieferung

## <a name="to-edit-a-posted-sales-shipment"></a>So bearbeiten Sie eine gebuchte Verkaufslieferung
Im Folgenden wird erläutert, wie Sie eine gebuchte Verkaufslieferung bearbeiten. Die Schritte sind für die anderen unterstützten Dokumente ähnlich.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Gebuchte Verkaufslieferungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das zu bearbeitende Dokument aus, und wählen Sie anschließend die Aktion **Beleg aktualisieren** aus. Alternativ können Sie das Dokument öffnen und dann die Aktion auswählen.
3. Auf der Seite **Gebuchte Verkaufslieferungen - Update** bearbeiten Sie das Feld **Paketverfolgungsnr.** zum Beispiel.
4. Wählen Sie die Schaltfläche **OK** aus.

Die gebuchte Verkaufslieferung wird aktualisiert.

## <a name="see-also"></a>Siehe auch
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Journale und Dokumente buchen](ui-post-documents-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
