---
title: Eingehende Dokumente aufzeichnen| Microsoft Docs
description: "Sie finden hier Datensätze aus eingehenden Belege, wie Erechnungen erstellen und verwalten OCRaufgaben, elektronische Geschäftsverkehr und Belegaustausch."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8642f4d904c9a1e7c46846d790fcb2d0837c4cc2
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-incoming-document-records"></a>Vorgehensweise: Erstellen von Eingangsbelegen
Im Fenster **Eingehende Dokumente** können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren eingehender Belege, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden. Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten.

Um einen externen Beleg in [!INCLUDE[d365fin](includes/d365fin_md.md)] aufzuzeichnen, müssen Sie zuerst einen Datensatz des Eingangsbeleges anlegen oder ausfüllen. Dies kann manuell erfolgen, oder Sie können ein Foto des externen Belegs machen und einen Eingangsbelegsdatensatz mit der angehängten Bilddatei erstellen.

Bevor Sie die Funktion für Eingangsbelege verwenden können, müssen Sie sie entsprechend einrichten. Weitere Informationen finden Sie unter [So gehts: Einrichten von eingehenden Belegen](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>So können Sie einen eingehenden Beleg genehmigen oder ablehnen
Wenn Sie wünschen, dass Benutzer Rechnungen oder Hauptjournalzeilen aus Eingangsbelegen nur dann erstellen dürfen, wenn diese genehmigt sind, können Sie Genehmiger einrichten, die alle Belege genehmigen müssen, bevor sie verarbeitet werden können.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Zeile mit dem Beleg, den Sie genehmigen oder ablehnen möchten, und wählen Sie dann die Aktion **Genehmigen** oder **Ablehnen** aus.

Das Kontrollkästchen **Freigegeben** in der Zeile für den Eingangsbeleg ist aktiviert, wenn dieser genehmigt wurde. Der jeweilige Benutzer, beispielsweise der für das Erstellen von Einkaufsrechnungen zuständige, kann dann fortfahren, den Datensatz zu verarbeiten.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>So erstellen Sie Eingangsbelegdatensätze indem Sie ein Foto machen
> [!NOTE]  
>   Der folgende Vorgang gilt nur für [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tablet- und Smartphone-Clients.

1. Wählen Sie auf der App-Leiste die Kachel **Erstellen von eingehendem Beleg von Kamera**, und wechseln Sie dann zu Schritt 4.
2. Wählen Sie alternativ in er Anwendungsleiste die Optionsschaltfläche aus, wählen Sie **Eingehende Belege** und wählen Sie dann **Alle** aus.
3. Verwenden Sie im Fenster **Eingehende Belege** die Auslassungspunkt-Schaltfläche, und wählen Sie dann **Von Kamera erstellen** aus. Die Kamera im Tablet oder dem Smartphone wird aktiviert.
4. Nehmen Sie ein Foto eines Belegs, wie einer Einkaufsquittung, die Sie als eingehender Beleg bearbeiten wollen, und wählen Sie dann die Schaltfläche **OK**.

    Ein neuer Datensatz für den eingehenden Beleg wird erstellt und das Bild wird angehängt.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>So hängen Sie ein Bild an ein Eingangsbelegdatensatz an, indem Sie ein Foto machen
> [!NOTE]  
>   Der folgende Vorgang gilt nur für [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tablet- und Smartphone-Clients.

1. Wählen Sie auf der App-Leiste die Optionsschaltfläche aus, wählen Sie **Eingehende Belege** und wählen Sie dann **Alle** aus.
2. Öffnen Sie die Karte eines vorhandenen eingehenden Belegsdatensatzes.
3. Verwenden Sie im Fenster **Eingehende Belege** die Auslassungspunkt-Schaltfläche, und wählen Sie dann **Bild von Kamera anhängen** aus. Die Kamera im Tablet oder dem Smartphone wird aktiviert.
4. Nehmen Sie ein Foto eines Belegs, wie einer Einkaufsquittung, die Sie als eingehender Beleg bearbeiten wollen, und wählen Sie dann die Schaltfläche **OK**.

    Das Bild wurde dem Datensatz des eingehenden Beleges angehängt.

## <a name="to-create-an-incoming-document-record-manually"></a>Eingangsbelege manuell erstellen
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Aus Datei erstellen** aus.  
3. Wählen Sie im Fenster **Datei einfügen** eine Datei aus und wählen Sie dann **Offen** aus. Die Datei wird automatisch angehängt.
4. Wählen Sie alternativ die Aktion **Neu** aus.
5. Um eine Datei hinzuzufügen, wählen Sie die Aktion **Datei anhängen**.
6. Im **Datei einfügen**-Fenster wählen Sie die Datei, die den jeweiligen Eingangsbeleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.
7. Füllen Sie im Fenster **Eingehende Belege** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Siehe auch
[Eingehende Dokumente verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

