---
title: Verwenden von Word-Vorlagen für die Massenkommunikation | Microsoft Docs
description: 'Mit Word-Vorlagen können Sie auf einfache Weise Dokumente in großen Mengen erstellen, die für bestimmte Entitäten personalisiert sind.'
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'document, mail, merge, Word, template, email'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Word-Vorlagen für die Massenkommunikation verwenden
Microsoft Word-Vorlagen können die Massenkommunikation in Druckform oder per E-Mail mit Entitäten wie Kontakten, Kunden und Kreditoren erleichtern. Sie können beispielsweise Broschüren erstellen, um Debitoren über eine Verkaufskampagne zu informieren, Briefe, um Kreditoren über eine neue Einkaufsrichtlinie zu informieren, oder Einladungen, um Kontakte zu einer bevorstehenden Veranstaltung zu gewinnen.

> [!NOTE]
> Sie können Word-Vorlagen nur auf Geräten mit Microsoft Word 2019 und installiertem Windows-Betriebssystem verwenden.

Sie können Entitäten in [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle für die Vorlage verwenden und fügen die Zusammenführungsfelder hinzufügen, um Dokumente für jede Entität zu personalisieren. Die Zusammenführungsfelder stammen von der Entität in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn Sie eine Word-Vorlage auf eine Entität anwenden, werden Daten aus den Zusammenführungsfeldern in das Dokument eingefügt.

Wenn Sie auf der Seite **Word-Vorlagen** eine neue Vorlage erstellen, laden Sie mit Hilfe einer Anleitung zur unterstützten Einrichtung eine ZIP-Datei herunter, die eine DataSource.xlsx und eine Word-Vorlagendatei für die Entität enthält. Die Datenquellendatei enthält die Felder, die Sie in der Vorlage verwenden können. Bearbeiten Sie die Datenquellendatei nicht. Sie können nur die Word-Vorlage und die Datenquellendateien verwenden, von denen Sie [!INCLUDE[prod_short](includes/prod_short.md)] herunterladen, und Sie müssen die Dateien am selben Speicherort speichern.

Nachdem Sie die Vorlage eingerichtet und Zusammenführungsfelder hinzugefügt haben, verwenden Sie dieselbe Anleitung zum Hochladen der Vorlage.

## Einrichten der Vorlage in Word
Wenn Sie eine Vorlage in Word einrichten, können Sie auf der Registerkarte **E-Mails** über die Option **Zusammenführungsfeld einfügen** Seriendruckfelder hinzufügen. Die verfügbaren Seriendruckfelder stammen aus der Datenquellendatei, die Sie für die Entität heruntergeladen haben. Sie dienen als Platzhalter, die Word mitteilen, wo im Beleg die Informationen über die Entität eingefügt werden sollen. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Hinzufügen von Platzhalterfeldern in Microsoft Word":::

## Hinzufügen von verwandten Entitäten
Zusätzlich zum Hinzufügen von Daten für die Quell-Entität, d.h. die Entität, für die Sie die Vorlage erstellen, können Sie auch Daten aus Entitäten zusammenführen, die mit ihr in Beziehung stehen. Wenn die Quelle beispielsweise die Entität Debitor ist, können Sie auch Daten aus Feldern der Entität Kunde/Einkäufer zusammenführen, da beide Entitäten ein Feld gemeinsam haben.

Verwandte Entitäten teilen sich ein Feld, bei dem es sich oft um einen Bezeichner wie einen Namen, einen Code oder eine ID handelt, mit der Entität der Quelle. Wenn Sie eine Vorlage festlegen, gibt es einfache und erweiterte Optionen für die Auswahl verwandter Entitäten:

* Einfach – Fügen Sie bekannte Beziehungen hinzu, die mit [!INCLUDE[prod_short](includes/prod_short.md)] standardmäßig zur Verfügung stehen.
* Erweitert – Fügen Sie Nicht-Standard-Beziehungen hinzu, z.B. solche, die durch Erweiterungen oder Anpassungen hinzugefügt wurden. Dies setzt voraus, dass Sie die Felder kennen, die die Entitäten gemeinsam haben.

Wenn Sie eine verwandte Entität hinzufügen, müssen Sie ein Präfix für den Feldnamen angeben. Wenn Sie der Vorlage Felder hinzufügen, kann das Präfix die Unterscheidung zwischen Feldern der Ursprungsentität und Feldern von verwandten Entitäten erleichtern.

## So erstellen Sie eine Word-Vorlage in Business Central
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Word-Vorlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, dann **Vorlage erstellen** und folgen Sie dann den Schritten in der Anleitung zur unterstützten Einrichtung. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Sie können eine Vorlage auch direkt von der Seite für eine Entität erstellen, indem Sie die Aktion **Word-Vorlage anwenden** wählen, um die Anleitung für die unterstützte Einrichtung zu öffnen, und dann **Neue Vorlage**. Wenn Sie dies tun, wird die Datenquelle auf der Grundlage der Art der Entität für Sie ausgewählt.

## Anwenden einer Vorlage
Wenn Ihre Word-Vorlage fertig ist, können Sie auf der Seite **Word-Vorlagen** **Anwenden** auswählen, um die Dokumente zu generieren. Wenn Sie eine Word-Vorlage auf eine Entität anwenden, werden die Daten aus den Seriendruckfeldern in den Beleg eingefügt. Sie können entweder einen Beleg erstellen, der Abschnitte für jede Entität enthält, oder Sie wählen **Split**, um für jede Entität einen neuen Beleg zu erstellen.

Sie können Vorlagen auf eine oder mehrere Entitäten desselben Typs, z.B. einen Kontakt, direkt im Kontext dieser Seite anwenden oder über die Seite Word-Vorlagen, um die Vorlage auf alle Entitäten dieses Typs anzuwenden.

## Word-Vorlagen mit E-Mail verwenden
Sie können Word-Vorlagen verwenden, um E-Mail-Nachrichten mit Inhalten zu versehen. Wenn Sie eine E-Mail verfassen, können Sie die Aktion **Word-Vorlage verwenden** wählen, um den Inhalt einer Vorlage auf die Nachricht anzuwenden. Dies setzt voraus, dass Sie eine oder mehrere Vorlagen für die Entität erstellt haben. Sie können jeweils eine Vorlage verwenden. Wenn Sie zwischen den Vorlagen wechseln, ändert sich die Nachricht so, dass sie den Inhalt der gewählten Vorlage wiedergibt.

Zusätzlich können Sie die Aktion **Datei aus Word-Vorlage hinzufügen** verwenden, um den Inhalt der Vorlage als Datei an die E-Mail anzuhängen. Die Datei wird das Format verwenden, das Sie für die Ausgabe der Vorlage angegeben haben.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Optionen für die Verwendung von Inhalten aus einer Word-Vorlage in einer E-Mail":::

## Weitere Informationen
[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
