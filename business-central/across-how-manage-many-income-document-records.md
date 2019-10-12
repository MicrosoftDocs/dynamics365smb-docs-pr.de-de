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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5401b8049e13d594f3429c97cfff915fc944c733
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305572"
---
# <a name="manage-many-incoming-document-records"></a>Mehrere eingehende Belege verwalten
Wenn Sie eingehende Belege verarbeiten, erhöht sich die Anzahl der Zeilen auf der Seite **Eingehende Belege** möglicherweise so, dass Sie die Übersicht verlieren. Daher können Sie eingehende Belege auf "Verarbeitet" festlegen, um sie aus der Standardansicht zu entfernen. Wenn Sie die Aktion **Alle anzeigen** auswählen, können Sie sowohl verarbeitete als auch nicht verarbeitete Datensätze anzeigen.

> [!NOTE]  
>   Sie können in eingehenden Belegen, die auf "Verarbeitet" gesetzt wurden, keine Informationen bearbeiten, Dateien hinzufügen oder andere Prozesse ausführen. Sie müssen sie zuerst auf "Nicht verarbeitet" festlegen.

Das Kontrollkästchen **Verarbeitet** ist automatisch bei eingehenden Belegen aktiviert, die verarbeitet wurden, aber Sie können das Kontrollkästchen auch manuell aktivieren oder deaktivieren. Abhängig von Ihrem Geschäftsprozess wird ein eingehender Beleg möglicherweise verarbeitet, wenn ein zugehöriger Beleg dafür erstellt oder eine Datei angehängt wurde.

> [!NOTE]  
>   Wenn Sie die Seite **Eingehende Belege** innerhalb der Aktion **Meine eingehenden Belege** im Rollencenter öffnen, werden nur nicht verarbeitete Belege standardmäßig angezeigt. Dies wird in diesem Thema als "Standardansicht" bezeichnet.

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>So entfernen Sie eingehende Belege aus der Standardansicht
1. Auf der Seite **Eingehende Belege** wählen Sie eine oder mehrere Zeilen für eingehende Belege, die Sie von der Standardansicht entfernen möchten.
2. Wählen Sie die Aktion **Auf "Verarbeitet" setzen** aus.

    Die eingehenden Belegdatensätze werden aus der Standardansicht entfernt, und das Kontrollkästchen **Verarbeitet** wird in den Zeilen aktiviert.

> [!NOTE]  
>   Sie können diese Aktion für einzelne Datensätze auf der Seite **Eingehende Belege** durchführen.

## <a name="to-view-all-incoming-document-records"></a>So zeigen Sie alle eingehende Belege an
1. Wählen Sie auf der Seite **Eingehende Belege** die Aktion **Alle anzeigen** aus.

Alle eingehenden Belegdatensätze einschließlich derer, bei denen das Kontrollkästchen **Verarbeitet** nicht aktiviert ist, werden angezeigt.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>So fügen Sie eingehende Belege der Standardansicht hinzu
1. Wählen Sie auf der Seite **Eingehende Belege** die Aktion **Alle anzeigen** aus.
2. Wählen Sie eine oder mehrere Zeilen für eingehende Belegeaus, die in der Standardansicht angezeigt werden sollen.
3. Wählen Sie die Aktion **Auf "Nicht verarbeitet" setzen** aus.  

> [!NOTE]  
>   Sie können diese Aktion für einzelne Datensätze auf der Seite **Eingehende Belege** durchführen.

## <a name="see-also"></a>Siehe auch
[Eingehende Belege verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
