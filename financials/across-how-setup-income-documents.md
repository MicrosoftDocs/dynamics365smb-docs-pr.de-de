---
title: Einrichten von eingehenden Belegen| Microsoft Docs
description: Verwenden Sie die Funktion der eingehenden Belege, um elektronische Belege zu erstellen, verwalten Sie OCRaufgaben, importieren Sie Rechnungen und wandeln Sie Bilddateien um.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 69cb1037da2f3873ecb9a3f498ce5fadfeabac1d
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-incoming-documents"></a>Gewusst wie: Eingehende Dokumente einrichten
Wenn Sie Fibu Buch.-Blattzeilen für eingehende Belegdatensätze erstellen, müssen Sie im Fenster **Einrichtung für eingehende Dokumente** angeben, welche Buch.-Blattvorlage und welches Buch.-Blatt verwendet werden sollen.

Wenn Sie nicht möchten, dass Benutzer Rechnungen oder Fibu Buch.-Blattzeilen anhand von eingehende Belegdatensätzen erstellen können, ausser, wenn diese genehmigt sind, müssen Sie Genehmiger im Fenster **Genehmiger für eingehendes Dokument** einrichten.

Um PDF und Bilddateien in elektronische Dokumente umzuwandeln, die in Dokumentdatensätze in Project [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden, müssen Sie die OCR-Funktion einrichten und den Dienst aktivieren.

Wenn die Funktion für Eingangsbelege eingerichtet ist, können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren von Eingangsbelegen, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden. Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten. Weitere Informationen finden Sie unter [Eingehende Dokumente verarbeiten](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>So richten Sie die Funktion für Eingangsbelege ein
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png " Nach Seite oder Bericht suchen")und geben **Einrichtung für eingehende Dokumente** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>So richten Sie Genehmiger für Eingangsbelege ein
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png " Nach Seite oder Bericht suchen")und geben **Einrichtung für eingehende Dokumente** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Einrichtung für eingehende Dokumente** die Aktion **Genehmiger** aus.

    Im Fenster **Genehmiger für eingehendes Dokument** werden alle Benutzer, die in Ihrem Project [!INCLUDE[d365fin](includes/d365fin_md.md)] eingerichtet sind, angezeigt.  
3. Wählen Sie mindestens einen Benutzer aus, der einen eingehenden Beleg genehmigen kann, bevor eine zugehörige Beleg- oder Buch.-Blattzeile erstellt werden kann.

Nachdem Sie Genehmiger im Fenster **Genehmiger für eingehendes Dokument** eingerichtet haben, können nur diese Benutzer ein eingehendes Dokument genehmigen, wenn im Fenster **Einrichtung für eingehende Dokumente** das Kontrollkästchen **Genehmigung zum Erstellen anfordern** aktiviert ist.

> [!NOTE]  
>   Diese Genehmigungseinrichtung ist nicht mit den Genehmigungsworkflows verknüpft. Weitere Informationen erhalten Sie unter [So gehts: Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>So richten Sie einen OCR-Service ein
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **OCR-Dienst einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a>So verschlüsseln Sie Ihre Anmeldeinformationen
Es wird empfohlen, dass Sie die Anmeldeinformationen, die Sie im Fenster **OCR-Dienst einrichten** eingeben, schützen. Sie können Daten auf dem Server verschlüsseln, indem Sie neue Verschlüsselungsschlüssel erstellen oder vorhandene importieren, die Sie auf der Serverinstanz aktivieren, die mit der Datenbank verknüpft ist.

1. Wählen Sie im Fenster **OCR-Dienst einrichten** die Aktion **Verschlüsselungsverwaltung**.
2. Aktivieren Sie im Fenster **Datenverschlüsselungsverwaltung** die Verschlüsselung der Daten.

## <a name="see-also"></a>Siehe auch
[Eingehende Dokumente verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

