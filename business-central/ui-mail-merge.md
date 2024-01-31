---
title: Verwenden von Word-Vorlagen für die Massen-Kommunikation
description: 'Mit Word-Vorlagen können Sie auf einfache Weise Dokumente in großen Mengen erstellen, die für bestimmte Entitäten personalisiert sind.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
ms.service: dynamics-365-business-central
---

# Word-Vorlagen für die Massenkommunikation verwenden

Microsoft Word-Vorlagen können die Massenkommunikation in Druckform oder per E-Mail mit Entitäten wie Kontakten, Kunden und Kreditoren erleichtern. Sie können beispielsweise Folgendes erstellen:

* Broschüren, um Kunden auf eine Verkaufsaktion aufmerksam zu machen
* Briefe, um Lieferanten über eine neue Einkaufspolitik zu informieren
* Einladungen, um Kontakte zu einer bevorstehenden Veranstaltung zu gewinnen

> [!NOTE]
> Wenn Sie Word-Vorlagen erstellen, müssen Sie ein Gerät mit Microsoft Word 2019 oder neuer haben und das Windows-Betriebssystem installiert haben.

## Einrichten der Datenquelle

Sie können Entitäten in [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle für die Vorlage verwenden und fügen die Zusammenführungsfelder hinzufügen, um Dokumente für jede Entität zu personalisieren. Die Zusammenführungsfelder stammen von der Entität in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn Sie eine Word-Vorlage auf eine Entität anwenden, werden die Daten aus den Seriendruckfeldern in den Beleg eingefügt.

Wenn Sie auf der Seite **Word-Vorlagen** eine neue Vorlage erstellen, hilft Ihnen eine unterstützte Einrichtungsanleitung durch die folgenden Schritte:

1. Wählen Sie eine oder mehrere Entitäten aus, die als Datenquelle verwendet werden sollen. Wenn Sie beispielsweise eine Broschüre für eine Verkaufskampagne erstellen möchten, würden Sie wahrscheinlich die Kundenentität als Quelle auswählen.
2. Wählen Sie andere Entitäten als zusätzliche Datenquellen aus. Weitere Informationen finden Sie unter [Einträge hinzufügen, die mit der Quellentität zusammenhängen oder nicht zusammenhängen](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Eine leere Vorlage herunterladen. Sie können die Vorlage sofort in Word einrichten oder die leere Vorlage hochladen und den Leitfaden fertig stellen. Wenn Ihre Vorlage fertig ist, verwenden Sie die Aktion **Hochladen** auf der Seite **Word-Vorlagen**, um die leere Vorlage durch Ihre fertige Vorlage zu ersetzen Vorlage. Weitere Informationen finden Sie unter [Vorlage in Word einrichten](#set-up-the-template-in-word).
4. Laden Sie die vorbereitete Vorlage hoch.
5. Geben Sie einen Code und einen Namen ein, der die Vorlage identifiziert.

Wenn Sie eine Vorlage herunterladen, erhalten Sie eine ZIP-Datei, die zwei Dateien enthält.

|Datei  |Beschreibung  |
|---------|---------|
|DataSource.xlsx     | Die Datenquellendatei enthält die Felder, die Sie in der Vorlage verwenden können. Bearbeiten Sie die Datenquellendatei nicht. Sie können nur die Word-Vorlage und die Datenquellendateien verwenden, die Sie heruntergeladen haben und Sie müssen die Dateien am selben Speicherort speichern.     |
|Word-Vorlage     | Eine .docx-Datei, die als Vorlage verwendet werden soll.        |

Informationen zum Einrichten einer Vorlage in Word finden Sie unter [Einrichten der Vorlage in Word](#set-up-the-template-in-word).

## Einträge hinzufügen, die mit der Quellentität zusammenhängen oder nicht zusammenhängen

Sie können auch Daten von anderen Entitäten zusammenführen. Um andere Entitäten als Datenquellen hinzuzufügen, verwenden Sie eine der folgenden Aktionen auf der Seite **Word-Vorlagen** oder wenn Sie die unterstützte Einrichtung verwenden:

|Aktion  |Beschreibung  |
|---------|---------|
|**Verbundene Entität hinzufügen**  | Verwenden Sie Daten von Entitäten, die mit der Quellentität in Beziehung stehen. Beispielsweise können Sie für die Kundenentität auch Daten aus der Kontaktentität zusammenführen. Entitäten sind verwandt, wenn ein Feld einer Entität auf eine andere verweist. Ein Feld in der Entität „Kunde“ verweist auf ein Feld in der Entität „Kontakt“, also sind sie verwandt. Das gemeinsam genutzte Feld ist häufig eine Kennung wie ein Name, ein Code oder eine ID.        |
|**Nicht verbundene Entität hinzufügen**| Verwenden von Daten von Entitäten, die nicht mit der Quellentität in Beziehung stehen. Beispielsweise erstellen Sie eine Vorlage für die Kundenentität. Sie können die Entität Unternehmensinformationen hinzufügen, damit Sie Ihre Kontaktdaten einfügen können. Ein wesentlicher Vorteil besteht darin, dass Ihre Kontaktinformationen automatisch in Ihrer Vorlage aktualisiert werden, wenn Sie sie ändern. Nachdem Sie eine nicht verwandte Entität hinzugefügt haben, können Sie damit verwandte Entitäten hinzufügen.         |

Für nicht zusammenhängende Einträge wählen Sie einen bestimmten Datensatz aus. Da Sie eine Entität nur einmal hinzufügen können, müssen Sie zur Verwendung eines anderen Datensatzes die Entität löschen und sie mit dem neuen Datensatz erneut hinzufügen.

Sie können eine Hierarchie von verwandten und nicht verknüpften Entitäten erstellen. Die Relation wird als Baumstruktur dargestellt. Das Feld **Entitätsbeziehung** zeigt auch Informationen über die Beziehung an. Bei nicht verbundenen Entitäten zeigt das Feld den Datensatz an, der die Beziehung erstellt.

Verwenden Sie beim Hinzufügen von Entitäten das Feld **Feldpräfix**, um ein Präfix für die Feldnamen anzugeben. Wenn Sie dann der Vorlage Felder hinzufügen, kann das Präfix die Unterscheidung zwischen Feldern der Ursprungsentität und Feldern von anderen Entitäten erleichtern.

### Wählen Sie die einzuschließenden Felder aus

Sie können für jede Entität die Felder angeben, die für die Vorlage verfügbar sein sollen. Wählen Sie die Zahl in der Spalte **Anzahl der ausgewählten Felder** aus, um auf eine Liste der verfügbaren Felder zuzugreifen. Verwenden Sie auf der Seite **Feldauswahl** das Kontrollkästchen **Einschließen**, um die Felder anzugeben. Bei einigen Entitäten sind Felder, die Unternehmen normalerweise verwenden, standardmäßig enthalten. Sie können die Liste beispielsweise bearbeiten, um die Standardfelder zu entfernen. Ihre Änderungen gelten nur für die Vorlage, an der Sie gerade arbeiten.

> [!NOTE]
> Die Gesamtzahl der Felder, die Sie aus allen Entitäten hinzufügen können, beträgt 250.

> [!NOTE]
> Sie oder Ihr Microsoft-Partner können Entitäten benutzerdefinierte Felder hinzufügen. Dabei stellen wir den Namen der Felder **CALC** voran und geben ihnen den Feldtyp **Berechnet**. Der Feldtyp wird als berechnet bezeichnet, um anzugeben, dass das Feld verschiedene Arten von Werten anzeigen kann, z. B. Text, Zahlen, Datumsangaben usw.

## So erstellen Sie eine Word-Vorlage in Business Central

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Word-Vorlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, dann **Vorlage erstellen** und folgen Sie dann den Schritten in der Anleitung zur unterstützten Einrichtung. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Sie können eine Vorlage auch direkt von der Seite für eine Entität erstellen, indem Sie die Aktion **Word-Vorlage anwenden** wählen, um die Anleitung für die unterstützte Einrichtung zu öffnen, und dann **Neue Vorlage**. Wenn Sie dies tun, wird die Datenquelle auf der Grundlage der Art der Entität für Sie ausgewählt.

## Einrichten der Vorlage in Word

Wenn Sie eine Vorlage in Word einrichten, können Sie auf der Registerkarte **E-Mails** über die Option **Zusammenführungsfeld einfügen** Seriendruckfelder hinzufügen. Die verfügbaren Seriendruckfelder stammen aus der Datenquellendatei, die Sie für die Entität heruntergeladen haben. Sie dienen als Platzhalter, die Word mitteilen, wo im Beleg die Informationen über die Entität eingefügt werden sollen.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Hinzufügen von Platzhalterfeldern in Microsoft Word":::

## Eine Vorlage anwenden

Wenn Ihre Word-Vorlage fertig ist, können Sie auf der Seite **Word-Vorlagen** **Anwenden** auswählen, um die Dokumente zu generieren. Wenn Sie eine Word-Vorlage auf eine Entität anwenden, werden die Daten aus den Seriendruckfeldern in den Beleg eingefügt. Sie können entweder einen Beleg erstellen, der Abschnitte für jede Entität enthält, oder Sie wählen **Split**, um für jede Entität einen neuen Beleg zu erstellen.

Sie können die Aktion **Word-Vorlagen anwenden** auf eine oder mehrere Vorlagen desselben Entitätstyps, z.B. einen Kontakt, direkt im Kontext dieser Seite für die Entität anwenden. Zum Beispiel die Seiten **Debitor** oder **Kreditor**.

## Word-Vorlagen mit E-Mail verwenden

Sie können Word-Vorlagen verwenden, um E-Mail-Nachrichten mit Inhalten zu versehen. Wenn Sie eine E-Mail verfassen, können Sie die Aktion **Word-Vorlage verwenden** wählen, um den Inhalt einer Vorlage auf die Nachricht anzuwenden. Sie müssen Vorlagen für die Entität erstellt haben. Sie können jeweils eine Vorlage verwenden. Wenn Sie zwischen den Vorlagen wechseln, ändert sich die Nachricht so, dass sie den Inhalt der gewählten Vorlage wiedergibt.

Zusätzlich können Sie die Aktion **Datei aus Word-Vorlage hinzufügen** verwenden, um den Inhalt der Vorlage als Datei an die E-Mail anzuhängen. Die Datei wird das Format verwenden, das Sie für die Ausgabe der Vorlage angegeben haben.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Optionen für die Verwendung von Inhalten aus einer Word-Vorlage in einer E-Mail":::

## Eine Word-Vorlage bearbeiten

Sie können die folgenden Änderungen an Ihren Word-Vorlagen vornehmen:

* Verwenden Sie zum Bearbeiten des Textkörpers oder der Platzhalterfelder in der Vorlage die Aktion **Herunterladen**, nehmen Sie Ihre Änderungen vor und verwenden Sie dann die Aktion **Hochladen**
* Um die Datenquellen zu ändern, verwenden Sie die Aktion **Zugehörige Entitäten bearbeiten**
* Um die Word-Vorlage durch eine neue Vorlage zu ersetzen, verwenden Sie die Aktion **Hochladen**
* Ausgewählte Vorlage löschen

## Weitere Informationen

[Verwaltung von Berichts- und Dokumentlayouts](ui-manage-report-layouts.md)  
[E-Mail einrichten](admin-how-setup-email.md)  
