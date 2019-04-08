---
title: Definieren, welche eingehenden Dokumente Sie sehen möchten| Microsoft Docs
description: Regulieren der Standardansicht aus eingehenden Belege, wie Erechnungen, um die Übersicht verarbeiteten und nicht verarbeiteten Datensätzen zu verbessern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 97ca5aab24b04f6c2d0677c6fd9626b93fcd8ca8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799008"
---
# <a name="manage-many-incoming-document-records"></a>Mehrere eingehende Belegdatensätze verwalten
Wenn Sie eingehende Belegdatensätze verarbeiten, erhöht sich die Anzahl der Zeilen auf der Seite **Eingehende Dokumente** möglicherweise so, dass Sie die Übersicht verlieren. Daher können Sie eingehende Belegdatensätze auf "Verarbeitet" festlegen, um sie aus der Standardansicht zu entfernen. Wenn Sie die Aktion **Alle anzeigen** auswählen, können Sie sowohl verarbeitete als auch nicht verarbeitete Datensätze anzeigen.

> [!NOTE]  
>   Sie können in eingehenden Belegdatensätzen, die auf "Verarbeitet" gesetzt wurden, keine Informationen bearbeiten, Dateien hinzufügen oder andere Prozesse ausführen. Sie müssen sie zuerst auf "Nicht verarbeitet" festlegen.

Das Kontrollkästchen **Verarbeitet** ist automatisch bei eingehenden Belegdatensätzen aktiviert, die verarbeitet wurden, aber Sie können das Kontrollkästchen auch manuell aktivieren oder deaktivieren. Abhängig von Ihrem Geschäftsprozess wird ein Datensatz möglicherweise verarbeitet, wenn ein zugehöriger Beleg dafür erstellt oder eine Datei angehängt wurde.

> [!NOTE]  
>   Wenn Sie die Seite **Eingehende Dokumente** innerhalb der Aktion **Meine eingehenden Dokumente** im Rollencenter öffnen, werden nur nicht verarbeitete Belege standardmäßig angezeigt. Dies wird in diesem Thema als "Standardansicht" bezeichnet.

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>So entfernen Sie eingehende Belegdatensätze aus der Standardansicht
1. Auf der Seite **Eingehende Dokumente** wählen Sie eine oder mehrere Zeilen für eingehende Datensätze, die Sie von der Standardansicht entfernen möchten.
2. Wählen Sie die Aktion **Auf "Verarbeitet" setzen** aus.

    Die eingehenden Belegdatensätze werden aus der Standardansicht entfernt, und das Kontrollkästchen **Verarbeitet** wird in den Zeilen aktiviert.

> [!NOTE]  
>   Sie können diese Aktion für einzelne Datensätze auf der Seite **Eingehende Belegkarte** durchführen.

## <a name="to-view-all-incoming-document-records"></a>So zeigen Sie alle eingehende Belegdatensätze an
1. Wählen Sie auf der Seite **Eingehende Dokumente** die Aktion **Alle anzeigen** aus.

Alle eingehenden Belegdatensätze einschließlich derer, bei denen das Kontrollkästchen **Verarbeitet** nicht aktiviert ist, werden angezeigt.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>So fügen Sie eingehende Belegdatensätze der Standardansicht hinzu
1. Wählen Sie auf der Seite **Eingehende Dokumente** die Aktion **Alle anzeigen** aus.
2. Wählen Sie eine oder mehrere Zeilen für eingehende Belegdatensätzeaus, die in der Standardansicht angezeigt werden sollen.
3. Wählen Sie die Aktion **Auf "Nicht verarbeitet" setzen** aus.  

> [!NOTE]  
>   Sie können diese Aktion für einzelne Datensätze auf der Seite **Eingehende Belegkarte** durchführen.

## <a name="see-also"></a>Siehe auch
[Eingehende Belege verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
