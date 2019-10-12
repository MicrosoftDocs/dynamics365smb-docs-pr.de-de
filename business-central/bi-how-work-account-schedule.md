---
title: Finanzberichte mithilfe von Kontenschemata bauen
description: Beschreibt, wie Filter verwendet werden, um unterschiedliche Ansichten und Berichte zum Analysieren von Finanzverhältnisleistungsdaten zu erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 23027c809571512c99d75860c108aa4a23ca5477
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307564"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor
Verwenden von Kontenplan, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden. Verwenden von Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten. Die Ergebnisse werden in den Diagrammen in Ihrem Rollencenter angezeigt, wie der Cashflowplan und Berichten, wie den GuV und den Bilanzberichten.

Sie rufen diese beiden Berichte beispielsweise mit der Aktion **Finanzverhältnis-Abrechnungen** im Business Manager und Buchhalter Rollen-Centers ab.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält mehrere Beispielkontenschemata, die Sie verwenden können , oder Sie können eigene Zeilen und Spalten einrichten, um die Werte anzugeben und zu vergleichen. So können beispielsweise Kontenschemata zur Berechnung von Gewinnmargen für Dimensionen wie beispielsweise Abteilungen oder Debitorengruppen erstellen. Das bedeutet, dass Sie so viele maßgeschneiderte Finanzaufstellungen erstellen können, wie Sie möchten.  

Das Einrichten von Kontenschemata erfordert ein Verständnis für die Finanzdaten im Kontenplan. Sie können beispielsweise die Sachposten als prozentualen Anteil der Budgetposten sehen. Dazu ist es erforderlich, dass Budgets erstellt werden. Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Kontenschemata
Kontenschemata dienen dazu, die Konten aus dem Kontenplan auf informative Weise anzuordnen. Durch die Möglichkeit zum Einrichten mehrerer Layouts können Sie die Informationen definieren, die Sie dem Kontenplan entnehmen möchten. Eine der Hauptfunktionen eines Kontenschemas besteht in der Bereitstellung eines Orts für Berechnungen, die nicht direkt im Kontenplan vorgenommen werden können – beispielsweise zur Erstellung von Zwischensummen für Kontengruppen, die in neue Summen einbezogen und anschließend in anderen Summen verwendet werden können. So können Benutzer beispielsweise Kontenschemata zur Berechnung von Gewinnmargen für Dimensionen (beispielsweise Abteilungen oder Debitorengruppen) erstellen. Darüber hinaus besteht die Möglichkeit zum Filtern von Sachposten und Finanzbudgetposten – beispielsweise nach Bewegung oder Sollbetrag.

Auch können mehrere Kontenschemata und Spaltenlayouts mithilfe von Formeln verglichen werden. Diese Art des Vergleichs ermöglicht Folgendes:

* Erstellen benutzerdefinierter Finanzberichte
* Erstellen einer beliebigen Anzahl von Kontenschemata, jeweils mit eindeutigem Namen
* Einrichten unterschiedlicher Berichtslayouts und Drucken der Berichte mit den aktuellen Werten

## <a name="account-categories"></a>Kontokategorien
Sie können Kontengruppen dazu verwenden, das Layout Ihrer Finanzberichte zu ändern. Wenn Sie Ihre Kontengruppen auf der Seite **Sachkontokategorien** eingerichtet haben und die Aktion **Kontenschemata generieren** auswählen, werden die zugrunde liegenden Kontenschemata für die Kernfinanzberichte aktualisiert. Wenn Sie das nächste Mal einen dieser Berichte wie die Saldoabrechnung ausführen, werden neue Summen und Untereinträge basierend auf Ihren Änderungen hinzugefügt. Weitere Informationen finden Sie unter [Kontokategorien](finance-general-ledger.md#account-categories).  

## <a name="to-create-a-new-account-schedule"></a>So erstellen Sie neue Kontenschemata  
Sie benutzen Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten. Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.

Die Kontenschemata in der Standardeinstellung sind [!INCLUDE[d365fin](includes/d365fin_md.md)] die Basis der Standardfinanzberichte, die möglicherweise nicht den Anforderungen Ihres Unternehmens entsprechen. Um Ihre eigenen Finanzberichte schnell erstellen zu können, beginnen Sie, indem Sie ein vorhandenes Kontenschema kopieren. Siehe dazu auch Schritt 3 unten.

Die Seite **Kontenschema. Planen Überblick** ist jene, auf der Sie Finanzbericht in der Vorschau sehen, die das Kontenschema definiert. Im Weiteren ist es wichtig zu verstehen, dass, was Sie einrichten, während Kontenschemazeilen und Spalten auf der Seite **Kontenschema. "Kontenschemamatrix** angezeigt werden und überprüft werden können, das Sie von einem Fenster öffnen, indem Sie die Aktion **Matrix** auswählen. Die Seite **Kontenschema** selbst ist nur ein Aufsetzbereich.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Kontoschema** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Kontenschemanamen zu erstellen.
3. Im Fenster **Kontenplan kopieren** geben Sie die zwei Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.
4. Füllen Sie die Felder je nach Bedarf aus. Im **Standard Spaltenlayout** Feld wählen Sie ein existierendes Layout aus. Sie können diese bei Bedarf später bearbeiten.

    Sie nutzen Spaltenlayouts, um Spalten für verschiedene Parameter festzulegen, durch die die Finanzdaten in den Zeilen angezeigt werden. Zum Beispiel können Sie ein Spalten-Layout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres mit vier Spalten vergleicht. Weitere Informationen finden Sie im Abschnitt [So erstellen Sie ein Spaltenlayout](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.
6. Erstellen Sie eine Zeile für jedes Finanzelement, dass im Bericht, wie eine Zeile für Umlaufvermögen und eine weitere Zeile für Anlagen erscheinen sollen. Für Inspiration finden Sie im CRONUS-Demounternehmen vorhandene Kontenschemata.
7. Wählen Sie die **Übersicht** Aktion aus, um den resultierenden Finanzbericht anzuzeigen.
8. Auf der Seite **Kontenschema-Überblick** im Feld **Spaltenlayoutname** wählen Sie ein anderes Spaltenlayout aus, um die Finanzdaten durch andere Einstellungen anzuzeigen.
9. Wählen Sie die Schaltfläche **OK** aus.

Sie haben jetzt die Grundlage des Kontenschemas, die Zeilen von Finanzdaten, die angezeigt werden sollen und ein bestehendes Layout der Spalten definiert, um die Daten in den Zeilen für verschiedene Einstellungen anzuzeigen. Wenn Standard-Spaltenlayout, das Sie in Schritt 4 ausgewählt haben, nicht Ihrem Zweck entspricht, gehen Sie folgendermaßen vor.

### <a name="to-edit-a-column-layout"></a>Um ein Spaltenlayout zu bearbeiten
Sie verwenden Spaltenlayouts, um festzulegen, welche Spalten in dem Bericht erscheinen sollen. Zum Beispiel können Sie ein Layout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres vergleicht.

> [!NOTE]
> Beachten Sie, dass in einer gedruckten Version eines Kontenschemas höchstens fünf Spalten angezeigt werden können. Wenn das Kontenschema ausschließlich zur Analyse der Seite **Kontenschema. Planen Überblick** dient, können Sie so viele Spalten erstellen, wie Sie möchten.

1. Auf der Seite **Kontenschemata** wählen Sie das relevante Kontenschema, und wählen die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.
2. Auf der Seite **Spaltenlayouts** erstellen Sie eine Zeile für jede Spalte, für die Finanzdaten in dem Finanzbericht angezeigt werden. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die Schaltfläche **OK** aus.
4. Öffnen Sie die Seite **Kontenschema. Planen Überblick** gelegentlich, um sicherzustellen, dass das neue Spaltenlayouts wie vorgesehen arbeitet.

> [!NOTE]
> Die Spalten, die Sie in jeder Zeile definieren, zeigt drei Spalten auf der Seite **Kontenschema. Planen Überblick**. Die ersten beiden Spalten, **Zeilennr.** und **Beschreibung**, sind fest.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Eine Spalte zur Berechnung von Prozentsätzen erstellen:  
Manchmal möchten Sie möglicherweise eine Spalte in ein Kontenschema einfügen, in der Prozentsätze einer Summe berechnet werden. Wenn beispielsweise mehrere Zeilen vorhanden sind, in denen die Verkäufe nach Dimension aufgeschlüsselt sind, empfiehlt sich die Einrichtung einer Spalte, in der für jede Zeile der prozentuale Anteil an den Gesamtverkäufen angegeben ist.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Klicken Sie auf der Registerkarte **Kontoschema bearbeiten** in der Gruppe Prozess auf Kontenschema bearbeiten, um eine Kontenschemazeile einzurichten, um die Gesamtsumme zu berechnen, auf denen die Prozentsätze basieren.  
4. Fügen Sie eine Zeile unmittelbar über der ersten Zeile ein, für die Sie einen Prozentsatz anzeigen möchten.  
5. Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein. Geben Sie im Feld **Zusammenzählung** eine Formel für die Summe ein, auf die der Prozentsatz basiert. Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.  
6. Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.  
7. Füllen Sie die Felder in der Zeile wie folgt aus: Wählen Sie im Feld **Spaltenart** **Formel** aus. Geben Sie im Feld **Formel** eine Formel für den Betrag ein, für den ein Prozentsatz berechnet werden soll, gefolgt von %. Wenn beispielsweise Spalte N die Bewegung enthält, geben Sie **N%** ein.  
8. Wiederholen Sie Schritt 4 bis 7 für jede Zeilengruppe, die nach Prozentsätzen aufgeschlüsselt werden soll.

## <a name="to-set-up-account-schedules-with-overviews"></a>Kontenschemata mit Matrizen einrichten:  
Sie können eine Kontenschema zum Erstellen eines Vergleichs der in der Finanzbuchhaltung gebuchten Werte mit den Finanzbudgetwerten benutzen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.  
4. Auf der Seite **Kontenplan** im Feld **Name** wählen Sie den Standard-Kontenplan aus.
5. Wählen Sie die **Konten einfügen** Aktion aus.  
6. Wählen Sie die Konten, die Sie in Ihrer Aufstellung berücksichtigen möchten, und wählen Sie dann **OK**.

    Die Konten sind damit in Ihr Kontenschema eingefügt. Wenn Sie möchten, können Sie auch das Spaltenlayout ändern.  
7. Wählen Sie die Aktion **Übersicht** aus.  
8. Auf der Seite **Kontoschema-Übersicht** im Inforegister **Dimensionenfilter** legen Sie den gewünschten Budgetfilter fest.  
9. Wählen Sie die Schaltfläche **OK** aus.  

Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Vergleichen von Buchhaltungsperioden mithilfe der Periodenformulare
Ihr Kontenschema kann sich die Ergebnisse von verschiedenen Buchhaltungsperioden, wie diesen Monat mit jenem des Vorjahresmonat vergleichen. Um das zu tun, fügen Sie eine Spalte mit dem Feld **Vergleichsperiodendatumsformel** hinzu und legen Sie dann dieses Feld auf eine Periodenformel fest.  

Eine Buchhaltungsperiode muss nicht dem Kalender entsprechen, aber jedes Geschäftsjahr muss dieselbe Anzahl von Buchhaltungsperioden haben, selbst wenn jede Periode eine andere Länge haben kann.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet diese Periodenformel, um den Betrag der Vergleichsperiode in Bezug auf die Periode zu berechnen, die Sie im Datumsfilter des Anforderungsfensters im Bericht angegeben haben. Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters. Für Periodenspezifikationen stehen folgende Abkürzungen zur Verfügung:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Abkürzung</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Periode</p></td>
</tr>
<tr class="even">
<td><p>EP</p></td>
<td><p>Endperiode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.</p></td>
</tr>
<tr class="odd">
<td><p>LP</p></td>
<td><p>Laufende Periode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.</p></td>
</tr>
<tr class="even">
<td><p>GJ</p></td>
<td><p>Geschäftsjahr. GJ[1..3] bezeichnet beispielsweise das erste Quartal des laufenden Geschäftsjahres.</p></td>
</tr>
</tbody>
</table>

Beispiele für Formeln:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Formel</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;"Leer"&gt;</p></td>
<td><p>Laufende Periode</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Vorperiode</p></td>
</tr>
<tr class="odd">
<td><p>-1GJ[1..EP]</p></td>
<td><p>Das gesamte vorige Geschäftsjahr</p></td>
</tr>
<tr class="even">
<td><p>-1GJ</p></td>
<td><p>Laufende Periode des vorigen Geschäftsjahrs</p></td>
</tr>
<tr class="odd">
<td><p>-1GJ[1..3]</p></td>
<td><p>Das erste Quartal des vorigen Geschäftsjahres</p></td>
</tr>
<tr class="even">
<td><p>-1GJ[1..LP]</p></td>
<td><p>Vom Anfang des vorigen Geschäftsjahres bis zur laufenden Periode des vorigen Geschäftsjahres einschließlich.</p></td>
</tr>
<tr class="odd">
<td><p>-1GJ[LP..EP]</p></td>
<td><p>Von der laufenden Periode des vorigen Geschäftsjahres bis zur Endperiode des vorigen Geschäftsjahres einschließlich.</p></td>
</tr>
</tbody>
</table>

Wenn die Berechnung gemäß regulärer Zeitperioden erfolgen soll, muss eine Formel in das Feld **Vergleichsdatumsformel** eingegeben werden.

> [!NOTE]
> Es ist jedoch nicht immer transparent, welche Perioden Sie vergleichen, da Sie einen Datumsfilter in einem Bericht festlegen können, die verschiedene Daten als die Buchhaltungsperioden umfasst, die Daten im Kontenplan angezeigt werden. Beispielsweise können Sie ein Kontenschema erstellen, in dem Sie diese Periode mit derselben Periode des Vorjahrs vergleichen möchten, damit Sie den **Vergleichs-Datums-Perioden-Filter** im Feld *1GJ* festlegen. Dann führen Sie den Bericht am 28. Februar aus und legen die Datumsfilter des Januar und Februar fest. Deshalb vergleicht das Kontenschema Januar und Februar dieses Jahr mit dem Januar des Vorjahrs, die die einzige abgeschlossene Buchhaltungsperiode der zwei für das Vorjahr ist.  


## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
