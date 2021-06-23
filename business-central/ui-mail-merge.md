---
title: Verwenden von Word-Vorlagen für die Massenkommunikation | Microsoft Docs
description: Mit Word-Vorlagen können Sie auf einfache Weise Dokumente in großen Mengen erstellen, die für bestimmte Entitäten personalisiert sind.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110954"
---
# <a name="using-word-templates-for-bulk-communication"></a>Verwenden von Word-Vorlagen für die Kommunikation
Microsoft Word-Vorlagen können die Massenkommunikation mit Entitäten wie Debitoren und Kreditoren vereinfachen. Sie können beispielsweise Broschüren erstellen, um Debitoren über eine Verkaufskampagne zu informieren, Briefe, um Kreditoren über eine neue Einkaufsrichtlinie zu informieren, oder Einladungen, um Kontakte zu einer bevorstehenden Veranstaltung zu gewinnen.

> [!NOTE]
> Sie können Word-Vorlagen nur auf Geräten mit Microsoft Word 2019 und installiertem Windows-Betriebssystem verwenden.

Sie können Entitäten in [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle für die Vorlage verwenden und fügen die Zusammenführungsfelder hinzufügen, um Dokumente für jede Entität zu personalisieren. Die Zusammenführungsfelder stammen von der Entität in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn Sie eine Word-Vorlage auf eine Entität anwenden, werden Daten aus den Zusammenführungsfeldern in das Dokument eingefügt.

Auf der Seite **Word-Vorlagen** können Sie mithilfe eines unterstützten Einrichtungshandbuchs eine ZIP-Datei herunterladen, die eine DataSource.txt‑ und eine Word-Vorlagendatei für eine Entität enthält. Nachdem Sie die Vorlage eingerichtet und Zusammenführungsfelder hinzugefügt haben, verwenden Sie dieselbe Anleitung zum Hochladen der Vorlage. Sie können nur die Word-Vorlage und die Datenquellendateien verwenden, von denen Sie [!INCLUDE[prod_short](includes/prod_short.md)] herunterladen, und Sie müssen die Dateien am selben Speicherort speichern.

> [!NOTE]
> Wenn Sie eine Entität auswählen, für die eine Vorlage erstellt werden soll, werden in der Liste alle Entitäten in [!INCLUDE[prod_short](includes/prod_short.md)] angezeigt. Sie können jedoch nicht für alle Entitäten Vorlagen erstellen. Wenn der Name einer Entität Sonderzeichen enthält, z. B. **/**, **.**, **_**, oder **-** können Sie keine Vorlage dafür erstellen. Der Name der Entität wird in der Spalte **Objektbeschriftung** angezeigt.

Wenn Sie die Vorlage in Word einrichten, können Sie auf der Registerkarte **Mailings** die Zusammenführungsfelder hinzufügen, indem Sie **Seriendruckfeld einfügen** auswählen.

> [!NOTE]
> Sie können Zusammenführungsfelder nicht verwenden, wenn der Name des Felds 40 Zeichen oder mehr enthält. Beispielsweise können Sie das Feld „Company__Information_Customs_Permit_Date“ nicht verwenden, da es 40 Zeichen enthält. 

Wenn Ihre Word-Vorlage fertig ist, können Sie auf der Seite **Word-Vorlagen** **Anwenden** auswählen, um die Dokumente zu generieren. Sie können entweder ein Dokument erstellen, das Abschnitte für jede Entität enthält, oder den Vorgang aufteilen, um ein neues Dokument für jede Entität zu erstellen.

## <a name="to-create-a-word-template"></a>Eine Word-Vorlage erstellen
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Word-Vorlagen** ein, und wählen Sie dann den zugehörigen Link aus.
2. Folgen Sie diesen Schritten im unterstützten Setup. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Siehe auch
[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
