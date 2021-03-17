---
title: Debitoren oder Kreditoren spezielle Beleglayouts zuweisen | Microsoft Docs
description: Wenn benutzerdefinierte Berichtslayouts definiert sind, können Sie diese aus Debitoren- und Kreditorenkarten auswählen, um anzugeben, dass die ausgewählten Layouts für Belege verwendet werden, die Sie für den betreffenden Debitoren oder Kreditoren erstellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 493a801b381ef21a2f8265e3a59615fa21618fc1
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385899"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Beleglayouts für Debitoren und Kreditoren definieren
Wenn benutzerdefinierte Berichtslayouts definiert sind, können Sie diese aus Debitoren- und Kreditorenkarten auswählen, um anzugeben, welche Layouts für verschiedene Arten von Belegen verwendet werden, die Sie für den betreffenden Debitoren oder Kreditoren erstellen. Der Wert im Feld **Verwendung** definiert, für welchen Prozess das Beleglayout verwendet wird, z. B. **Erinnerung**, **Lieferung** und **Bestätigung**.

Sie können nicht nur festlegen, welche Layouts für welchen Beleg verwendet werden sollen, sondern auch Zeit sparen, wenn Sie Belege an verschiedene Debitoren- oder Kreditorenkontakte senden, indem Sie die E-Mail-Adressen bestimmter Kontakte für die Verwendung mit bestimmten Belegen einrichten. Beispielsweise werden Kontoauszüge an Buchhalterkontakte gesendet, Verkaufsaufträge an die Käufer Ihrer Debitoren und Einkaufsbestellungen an Verkäufer oder Kundenbetreuer der Kreditoren.

Wenn Sie ein Beleglayout für einen Debitoren oder Kreditoren definieren, können Sie auch die E-Mail-Adresse der Kontaktperson angeben, die den Beleg erhalten muss. Dies können Sie schnell mit der Funktion **E-Mail von Kontakten auswählen** erledigen, die automatisch nach Kontakt-E-Mail-Adressen filtert, die für den betreffenden Debitor oder Kreditor registriert sind.

Bevor Sie festlegen können, welches Beleglayout für welche Prozesse verwendet werden soll und an welchen Kontakt der Beleg gesendet werden soll, müssen Sie alle verfügbaren Berichte (Belege) von der Seite **Berichtsauswahl** laden. Dies können Sie schnell mit der Funktion **Aus Berichtsauswahl kopieren** erledigen.

Im Folgenden wird beschrieben, wie Sie Verkaufsbeleglayouts aus einer Debitorenkarte definieren. Die Schritte sind dieselben für Einkaufsbeleglayouts aus einer Kreditorenkarte.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>So aktivieren Sie alle verfügbaren Verkaufsbelege für einen Debitor
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte des Debitoren, für den Sie Beleglayouts pro Geschäftsprozess definieren möchten.
3. Wählen Sie auf der Seite **Debitorenkarte** die Seite **Belegvorlagen** aus.
4. Auf der Seite **Beleglayouts** wählen Sie die Aktion **Aus Berichtsauswahl kopieren** aus.

Die Seite **Beleglayouts** für den betreffenden Debitor wird mit allen Berichtslayouts für Verkäufe gefüllt, die im System vorhanden sind. Weitere Informationen über ihre Erstellung finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

Sie können nun damit fortfahren, die Liste mit sämtlichen benutzerdefinierten Berichtslayouts oder E-Mail-Adressen für die Kontakte anzupassen, zu denen die Belege gesendet werden müssen.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>So wählen Sie ein benutzerdefiniertes Berichtslayout aus, das für das Verkaufsbeleglayout verwendet werden soll
Wenn für eines oder mehrere der Berichtslayouts, die auf der Seite **Beleglayouts** für den Debitor definiert sind, kein benutzerdefiniertes Berichtslayout definiert ist, können Sie dies schnell tun.

1. Auf der Seite **Beleglayouts** in der Zeile für ein Berichtslayout, für das Sie ein benutzerdefiniertes Layout verwenden möchten, wählen Sie das Feld **Benutzerdefinierte Layoutbeschreibung** aus. Das Feld wird entweder gefüllt, wenn das Debitorenlayout bereits ausgewählt ist oder leer ist.
2. Auf der Seite **Benutzerdefinierte Berichtslayouts** wählen Sie das spezielle Beleglayout aus, das Sie für die betreffende Verkaufsbelegart verwenden möchten. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>So legen Sie fest, welcher Kontakt welches Beleglayout für einen Debitor erhält
Sie können Zeit sparen, wenn Sie Belege an verschiedene Debitoren- oder Kreditorenkontakte senden, indem Sie Kontakt-E-Mail-Adressen in den verschiedenen Zeilen auf der Seite **Beleglayouts** angeben. Beispielsweise können Kontoauszüge an Buchhalterkontakte gesendet werden, Verkaufsaufträge an die Käufer Ihrer Debitoren und Einkaufsbestellungen an Verkäufer oder Kundenbetreuer der Kreditoren.

1. Auf der Seite **Beleglayouts** in der Zeile für ein Berichtslayout, das Sie an einen bestimmten Kontakt für den Debitor senden möchten, wählen Sie die Aktion **E-Mail aus Kontakten auswählen** aus.
2. Auf der Seite **Kontakte** wählen Sie die Zeile für den relevanten Kontakt aus, und wählen Sie dann die Schaltfläche **OK** aus.

Die E-Mail-Adresse des Kontakts wird nun in die Beleglayoutzeile eingefügt, sodass der betreffende Verkaufsbeleg, z. B. Erinnerungen, immer an diesen Kontakt im Unternehmen des Debitors gesendet wird.

## <a name="see-also"></a>Siehe auch  
[Benutzerdefinierte Berichtslayouts aktualisieren](ui-update-report-layouts.md)  
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Importieren und Exportieren von einem benutzerdefinierten Berichts- oder Beleglayout](ui-how-import-and-export-report-layout.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]