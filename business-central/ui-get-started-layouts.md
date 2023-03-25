---
title: Erste Schritte beim Erstellen von Layouts
description: 'Erfahren Sie, wie Sie Layouts erstellen, um das Erscheinungsbild eines Berichts beim Anzeigen, Drucken oder Speichern zu personalisieren.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
---
# Erste Schritte beim Erstellen von Berichtslayouts

Business Central enthält viele integrierte Layouts, die Sie für Ihre Berichte verwenden können. Andere Layouts wurden möglicherweise als Teil anderer Erweiterungen hinzugefügt. Es ist aber auch möglich, eigene Berichte entweder von Grund auf neu oder basierend auf einem bestehenden Layout zu erstellen.

> [!IMPORTANT]
> Sie können auchBerichtslayouts verwenden, um E-Mail-Nachrichten Inhalte hinzuzufügen. Berichtslayouts können beispielsweise Zeit sparen und zur Konsistenz beitragen, indem dieselben Inhalte wiederverwendet werden, wenn Sie mit Ihren Debitoren kommunizieren. Um benutzerdefinierte Berichtslayouts mit E-Mail verwenden zu können, muss der Dateityp für das Layout „Word“ sein. Der Dateityp „RDLC“ kann nicht verwendet werden. Weitere Informationen finden Sie unter [Wiederverwendbare E-Mail-Texte und -Layouts einrichten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## Übersicht

Beim Arbeiten mit Berichtslayouts ist es hilfreich, sich das Layout als eine Datei vorzustellen, die importiert und einem Bericht zugewiesen wird. Unabhängig vom Layouttyp ist die Verwaötung von Layouts in Business Central grundsätzlich gleich. Normalerweise arbeiten Sie auf der Seite **Berichtslayouts**. Der Hauptunterschied besteht darin, wie Sie das Layout entwerfen. Das erfolgt mit der Anwendungssoftware, auf der das Layout aufbaut, wie Word, Excel oder SQL Server Report Builder.

Mit diesem Konzept im Hinterkopf müssen im Wesentlichen drei oder vier Aufgaben erledigt werden, um ein Layout in einem Bericht einzurichten:

1. Entscheiden Sie sich für den Layouttyp.
2. Exportieren Sie eine Kopie eines vorhandenen Layouts, um es als Ausgangspunkt zu verwenden.
3. Nehmen Sie in der entsprechenden Anwendung Änderungen an der Layoutdatei vor.
4. Fügen Sie dem Bericht die neue Layoutdatei hinzu.

> [!IMPORTANT]
> Sie können ein Erweiterungslayout nicht ändern oder ersetzen, da es sich um ein Layout handelt, das aus einer Erweiterung stammt. Sie können nur benutzerdefinierte Layouts ändern oder entfernen. Auf der Seite **Berichtslayouts** können Sie anhand der Spalte **Erweiterung** erkennen, ob es sich um ein Erweiterungslayout oder ein benutzerdefiniertes Layout handelt. Ein Erweiterungslayout zeigt in der Spalte Informationen über die Quellerweiterung an. Die Spalte **Erweiterung** bleibt bei einem benutzerdefinierten Layout leer.
>
> Informationen zum Unterschied zwischen Erweiterungslayouts und benutzerdefinierten Layouts finden Sie unter [Layoutquelle](ui-manage-report-layouts.md#layout-sources).

## Erste Schritte

Je nach Ihrer Situation unterschieden sich die tatsächlichen Aufgaben. Verwenden Sie die folgende Tabelle, um Ihnen den Einstieg zu erleichtern.

|Was möchten Sie tun?|Siehe...|
|-----------------------|------|
|Herausfinden, welcher Layouttyp für meine Situation am besten geeignet ist|[Entscheiden Sie, welche Art von Layout Sie möchten](#decide)|
|Erstellen Sie ein neues Layout für einen Bericht, der auf einem vorhandenen Layout basiert, und behalten Sie das vorhandene Layout unverändert bei.|[Ein neues Layout erstellen](#create)|
|Änderungen an einem vorhandenen Layout vornehmen, das in einem Bericht verwendet wird|[Ändern eines Layouts](#modify)|
|Ich habe eine neue Version einer Layoutdatei für einen Bericht. Ich möchte die vorhandene Layoutdatei ersetzen.|[Ein Layout ersetzen](#replace)|
|Vom aktuellen Layout, das von einem Bericht verwendet wird, zu einem anderen Layout wechseln|[Festlegen des von einem Bericht verwendeten Layouts](ui-set-report-layout.md)|
|Den Namen und die Beschreibung eines Layouts ändern|[Ein Layout umbennen](#rename)|

## <a name="decide"></a>Entscheiden Sie, welche Art von Layout Sie möchten

Als erstes müssen Sie beim Erstellen eines Layouts entscheiden, welchen [Layouttyp](ui-manage-report-layouts.md#layout-types) Sie wollen. Sie können entweder Word, Excel oder RDLC auswählen. Der Layouttyp hängt davon ab, wie der generierte Bericht aussehen soll. Außerdem hängt er von Ihren Kenntnissen der Anwendungssoftware zum Erstellen der Layouts ab, z. B. Word, Excel und SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Excel-Layouts sind im Allgemeinen am einfachsten zu erstellen und zu ändern, da die Funktionen zum Zusammenfassen von Daten, Hinzufügen von Grafiken und Formatieren gängige Excel-Funktionen sind.

* Nicht alle Berichte und Dokumente verfügen über einen Datensatz, der für die Verwendung mit einem Excel-Layout optimiert ist. Beispielsweise funktionieren Aggregationen und komplexe Berechnungen am besten mit RDLC- oder Word-Layouts. Gleiches gilt für Dokumente.

* Wenn Sie nur Stiländerungen wie Schriftart, Größe und Farben vornehmen, ist ein Word-Layout ebenfalls eine gute Wahl.

* Das Hinzufügen von Datenfeldern oder das Neuanordnen von Datenfeldern in Word oder RDLC ist fortgeschrittener als in Excel.

* Word- und RDLC-Layouts eignen sich gut für Berichte, die schließlich gedruckt werden.  

* Die allgemeinen Entwurfskonzepte für Word- und RDLC-Layouts sind ähnlich. Jedoch hat jede Art bestimmte Design-Funktionalitäten, die beeinflussen, wie der generierte Bericht im [!INCLUDE[prod_short](includes/prod_short.md)]erscheint. Derselbe Bericht sieht möglicherweise bei Verwendung eines Word-Layout anders aus als bei einem RDLC-Berichtslayout.

## <a name="create"></a>Ein neues Layout erstellen

Es gibt zwei Möglichkeiten, ein neues Layout aus einem bestehenden Layout zu erstellen. Eine Möglichkeit besteht darin, das vorhandene Layout in einer Kopie zu speichern. Die andere Möglichkeit besteht darin, das vorhandene Layout zu exportieren.

## [Kopieren](#tab/copy)

Kopieren ist eine schnelle Möglichkeit, ein neues Layout zu erstellen, das mit einem vorhandenen Layout identisch ist. Sobald Sie die Kopie haben, nehmen Sie Änderungen vor, indem Sie das Layout exportieren. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Wählen Sie das Layout aus, das Sie für Ihr neues Layout kopieren möchten, und wählen Sie dann die Aktion **Informationen bearbeiten** aus.

    Wenn Sie ein Erweiterungslayout ausgewählt haben, werden Sie gefragt, ob Sie eine Kopie bearbeiten möchten. Wählen Sie **Ya** aus, um fortzufahren.

    > [!TIP]
    > Um Ihnen das Auffinden des Layouts zu erleichtern, verwenden Sie das Feld **Suchen**, den Bereich **Filtern** und die Spaltensortierung.
3. Ändern Sie den **Layout-Namen**.
4. Schalten Sie den Schalter **Änderungen zum Kopieren speichern** auf **Ein** und wählen Sie **OK** aus

   Das neue Layout wird auf der Seite **Berichtslayouts** angezeigt.
5. Informationen zum Vornehmen von Änderungen am neuen Layout finden Sie unter [Ändern eines vorhandenen Layouts](#modify).

### [Exportieren/Importieren](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Wählen Sie das Layout aus, das Sie für Ihr neues Layout kopieren möchten, und wählen Sie dann die Aktion **Layout exportieren** aus.

   Die Layoutdatei wird auf Ihr Gerät heruntergeladen. 

    > [!TIP]
    > Um Ihnen das Auffinden des Layouts zu erleichtern, verwenden Sie das Feld **Suchen**, den Bereich **Filtern** und die Spaltensortierung.

3. Öffnen Sie die Layoutdatei in der entsprechenden Anwendung, wie Word (für eine .docx-Datei) oder Excel (für eine .xlsx-Datei).

   Weitere Informationen finden Sie unter:

   * [Arbeiten mit Word-Layouts](ui-how-add-fields-word-report-layout.md)
   * [Mit Excel-Layouts arbeiten](ui-excel-report-layouts.md)
   * [Mit RDLC-Layouts arbeiten](ui-rdlc-report-layouts.md)

   Nehmen Sie Änderungen an der Datei vor und speichern Sie sie.

4. Zurück bei den **Berichtslayouts** wählen Sie die Aktion **Neues Layout** aus.
5. Füllen Sie die folgenden Felder aus:

   |Feld|Beschreibung|Notwendig|
   |-----|-----------|---------|
   |Berichts-ID|Auf die ID festlegen, die dem Bericht zugewiesen ist|ja|
   |Layoutname| Geben Sie einen kurzen Beschreibungsnamen für das Layout ein, damit Sie es leichter identifizieren können.|ja|
   |Beschreibung| Geben Sie detailliertere Informationen zum Layout ein. |keine|
   |Format-Optionen|Legen Sie dieses Feld so fest, dass es dem Typ des Layouts entspricht, z. B. Word, Excel oder RDLC.|ja|

6. Wählen Sie **OK** > **Auswählen** fest, um den Datei-Explorer auf Ihrem Gerät zu öffnen.
7. Suchen Sie die Excel-Datei und wählen Sie sie aus. Wählen Sie dann **Öffnen** aus.

   Die ausgewählte Datei wird in das Layout hochgeladen und Sie kehren zur **Berichtslayouts**-Seite zurück.

Wenn Sie sehen möchten, wie der Bericht mit dem neuen Layout aussieht, wählen Sie das Layout in der Liste und dann **Bericht ausführen** aus.

---

## <a name="modify"></a>Ändern eines Layouts

Führen Sie diese Schritte aus, um ein vorhandenes benutzerdefiniertes Layout zu ändern.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Wählen Sie das Layout aus, das Sie ändern möchten, und wählen Sie die Aktion **Layout exportieren** aus.

   Die Layoutdatei wird auf Ihr Gerät heruntergeladen. 

   > [!TIP]
   > Um Ihnen das Auffinden des Layouts zu erleichtern, verwenden Sie das Feld **Suchen**, den Bereich **Filtern** und die Spaltensortierung.

3. Öffnen Sie die Layoutdatei in der entsprechenden Anwendung, wie Word (für eine .docx-Datei) oder Excel (für eine .xlsx-Datei).

   Weitere Informationen finden Sie unter:

   * [Arbeiten mit Word-Layouts](ui-how-add-fields-word-report-layout.md)
   * [Mit Excel-Layouts arbeiten](ui-excel-report-layouts.md)
   * [Mit RDLC-Layouts arbeiten](ui-rdlc-report-layouts.md)

   Nehmen Sie Änderungen an der Datei vor und speichern Sie sie.

4. Zurück auf der Seite **Berichtslayouts** wählen Sie das vorhandene Layout und dann die **Layout ersetzen**-Aktion aus.
5. Wählen Sie **OK** > **Auswählen** fest, um den Datei-Explorer auf Ihrem Gerät zu öffnen.
6. Suchen Sie die Excel-Datei und wählen Sie sie aus. Wählen Sie dann **Öffnen** aus.

   Die ausgewählte Datei wird in das Layout hochgeladen und Sie kehren zur **Berichtslayouts**-Seite zurück.
7. Wenn Sie sehen möchten, wie der Bericht mit dem neuen Layout aussieht, wählen Sie das Layout in der Liste und dann **Bericht ausführen** aus.

## <a name="replace"></a>Ein Layout ersetzen

Führen Sie diese Schritte aus, um die vorhandene benutzerdefinierte Layoutdatei durch eine neue Datei zu ersetzen.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Wählen Sie das vorhandene Layout und dann die **Layout ersetzen**-Aktion aus.
3. Wählen Sie **OK** > **Auswählen** fest, um den Datei-Explorer auf Ihrem Gerät zu öffnen.
4. Suchen Sie die Excel-Datei und wählen Sie sie aus. Wählen Sie dann **Öffnen** aus.

   Die ausgewählte Datei wird in das Layout hochgeladen und Sie kehren zur **Berichtslayouts**-Seite zurück.
5. Wenn Sie sehen möchten, wie der Bericht mit dem neuen Layout aussieht, wählen Sie das Layout in der Liste und dann **Bericht ausführen** aus.

## <a name="rename"></a>Ein Layout umbennen

Befolgen Sie diese Schritte, wenn Sie den Namen und die Beschreibung eines benutzerdefinierten Layouts ändern möchten.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Wählen Sie das Layout aus, das Sie umbenennen möchten, und wählen Sie dann die Aktion **Informationen bearbeiten** aus.

    > [!TIP]
    > Um Ihnen das Auffinden des Layouts zu erleichtern, verwenden Sie das Feld **Suchen**, den Bereich **Filtern** und die Spaltensortierung.
3. Ändern Sie den **Layout-Namen** und wählen Sie dann **OK** aus.

## Siehe verwandte [Microsoft Schulungen](/training/modules/change-documents-dynamics-365-business-central/index)

## Siehe auch

[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Arbeiten mit Word Layouts](ui-how-add-fields-word-report-layout.md)  
[Arbeiten mit Excel-Layouts](ui-excel-report-layouts.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
