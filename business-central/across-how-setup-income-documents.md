---
title: Einrichten von eingehenden Belegen| Microsoft Docs
description: Verwenden Sie die Funktion der eingehenden Belege, um elektronische Belege zu erstellen, verwalten Sie OCRaufgaben, importieren Sie Rechnungen und wandeln Sie Bilddateien um.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0a33652ac230e63607957916308ee960d14a2b47
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188468"
---
# <a name="set-up-incoming-documents"></a>Einrichten von eingehenden Belegen
Wenn Sie Fibu Buch.-Blattzeilen für eingehende Belege erstellen, müssen Sie auf der Seite **Einrichtung für eingehende Belege** angeben, welche Buch.-Blattvorlage und welches Buch.-Blatt verwendet werden sollen.

Wenn Sie möchten, dass Benutzer Rechnungen oder Journalzeilen anhand von Eingangsbelegen nur dann erstellen können, wenn diese genehmigt sind, müssen Sie Workflow-Genehmiger einrichten.

Um PDF und Bilddateien in elektronische Dokumente umzuwandeln, die in Dokumentdatensätze in Project [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden, müssen Sie die OCR-Funktion einrichten und den Dienst aktivieren.

Wenn die Funktion für eingehende Belege eingerichtet ist, können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren von eingehenden Belegen, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden. Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten. Weitere Informationen finden Sie unter [Eingehende Belege verarbeiten](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>So richten Sie die Funktion für eingehende Belege ein
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Eingehenden Beleg einrichten** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder bei Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>So richten Sie Genehmiger für eingehende Belege ein
Genehmiger von eingehenden Belegen müssen als Genehmigungsworkflow-Benutzer eingerichtet werden.

Bevor Sie Workflows erstellen können, die Genehmigungsschritte betreffen, müssen Sie die Workflowbenutzer einrichten, die von den Genehmigungsprozessen betroffen sind. Auf der Seite **Genehmigungsbenutzereinrichtung** müssen Sie zusätzlich Grenzbeträge für bestimmte Arten von Anforderungen festlegen und Ersatzgenehmiger definieren, an die Genehmigungsanforderungen delegiert werden, wenn der ursprüngliche Genehmiger abwesend ist. Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern.](across-how-to-set-up-approval-users.md)

## <a name="to-set-up-an-ocr-service"></a>So richten Sie einen OCR-Service ein
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **OCR-Serviceeinrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Sie informieren Daten werden verschlüsselt automatisch an.

## <a name="see-also"></a>Siehe auch
[Eingehende Belege verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
