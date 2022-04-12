---
title: Finanzberichte mithilfe von Kontenschemata bauen
description: Beschreibt, wie Filter verwendet werden, um unterschiedliche Ansichten und Berichte zum Analysieren von Finanzverhältnisleistungsdaten zu erstellen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 32ca89daf15485057cf9ef8b86ff9090bb12d037
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512360"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor

Verwenden von Kontenplan, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden. Verwenden von Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten. Die Ergebnisse werden in den Diagrammen in Ihrem Rollencenter angezeigt, wie der Cashflowplan und Berichten, wie den GuV und den Bilanzberichten.

Sie rufen diese beiden Berichte beispielsweise mit der Aktion **Finanzverhältnis-Abrechnungen** im Business Manager und Buchhalter Rollen-Centers ab.  

[!INCLUDE[prod_short](includes/prod_short.md)] enthält mehrere Beispielkontenschemata, die Sie verwenden können , oder Sie können eigene Zeilen und Spalten einrichten, um die Werte anzugeben und zu vergleichen. So können beispielsweise Kontenschemata zur Berechnung von Gewinnmargen für Dimensionen wie beispielsweise Abteilungen oder Debitorengruppen erstellen. Das bedeutet, dass Sie so viele maßgeschneiderte Finanzaufstellungen erstellen können, wie Sie möchten.  

Das Einrichten von Kontenschemata erfordert ein Verständnis für die Finanzdaten im Kontenplan. Sie können beispielsweise die Sachposten als prozentualen Anteil der Budgetposten sehen. Dazu ist es erforderlich, dass Budgets erstellt werden. Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Kontenschemata

Kontenschemata dienen dazu, die Konten aus dem Kontenplan auf informative Weise anzuordnen. Durch die Möglichkeit zum Einrichten mehrerer Layouts können Sie die Informationen definieren, die Sie dem Kontenplan entnehmen möchten. Eine der Hauptfunktionen eines Kontenschemas besteht in der Bereitstellung eines Orts für Berechnungen, die nicht direkt im Kontenplan vorgenommen werden können – beispielsweise zur Erstellung von Zwischensummen für Kontengruppen, die in neue Summen einbezogen und anschließend in anderen Summen verwendet werden können. So können Benutzer beispielsweise Kontenschemata zur Berechnung von Gewinnmargen für Dimensionen (beispielsweise Abteilungen oder Debitorengruppen) erstellen. Darüber hinaus besteht die Möglichkeit zum Filtern von Sachposten und Finanzbudgetposten – beispielsweise nach Bewegung oder Sollbetrag.

Auch können mehrere Kontenschemata und Spaltenlayouts mithilfe von Formeln verglichen werden. Diese Art des Vergleichs ermöglicht Folgendes:

* Erstellen benutzerdefinierter Finanzberichte
* Erstellen einer beliebigen Anzahl von Kontenschemata, jeweils mit eindeutigem Namen
* Einrichten unterschiedlicher Berichtslayouts und Drucken der Berichte mit den aktuellen Werten

## <a name="gl-account-categories"></a>Sachkontokategorien

Sie können Sachkontokategorien dazu verwenden, das Layout Ihrer Finanzberichte zu ändern. Wenn Sie Ihre Kontengruppen auf der Seite **Sachkontokategorien** eingerichtet haben und die Aktion **Kontenschemata generieren** auswählen, werden die zugrunde liegenden Kontenschemata für die Kernfinanzberichte aktualisiert. Wenn Sie das nächste Mal einen dieser Berichte wie die **Saldoabrechnung** ausführen, werden neue Summen und Untereinträge basierend auf Ihren Änderungen hinzugefügt.

> [!NOTE]
> Die Kontokategorien der obersten Ebene wie beispielsweise der **Verbindlichkeiten**-Knoten sind fest, und Sie können keine eigenen hinzufügen. Sie können jedoch Kontokategorien auf niedrigeren Ebenen löschen und hinzufügen und ihre Struktur ändern, um zu definieren, wie der zugehörige Kontoplan in Berichten angezeigt wird.
>
> Es wird empfohlen, eigene Sachkontokategorien auf einer niedrigeren Ebene von Grund auf neu, bei Bedarf in einer Hierarchie, zu erstellen, anstatt die vorhandenen neu anzuordnen. Sie können beispielsweise den Knoten **Verbindlichkeiten** neu strukturieren, sodass er den neuen Knoten **Eigenkapital** gefolgt von den Knoten **Kurzfristige Verbindlichkeiten** und **Langfristige Verbindlichkeiten** enthalten.

## <a name="to-create-a-new-account-schedule"></a>So erstellen Sie neue Kontenschemata

Sie benutzen Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten. Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.

Die Kontenschemata in der Standardeinstellung sind [!INCLUDE[prod_short](includes/prod_short.md)] die Basis der Standardfinanzberichte, die möglicherweise nicht den Anforderungen Ihres Unternehmens entsprechen. Um Ihre eigenen Finanzberichte schnell erstellen zu können, beginnen Sie, indem Sie ein vorhandenes Kontenschema kopieren. Siehe dazu auch Schritt 3 unten.

Die Seite **Kontenschema. Planen Überblick** ist jene, auf der Sie Finanzbericht in der Vorschau sehen, die das Kontenschema definiert. Im Weiteren ist es wichtig zu verstehen, dass, was Sie einrichten, während Kontenschemazeilen und Spalten auf der Seite **Kontenschema. "Kontenschemamatrix** angezeigt werden und überprüft werden können, das Sie von einem Fenster öffnen, indem Sie die Aktion **Matrix** auswählen. Die Seite **Kontenschema** selbst ist nur ein Aufsetzbereich.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten"). Symbol. Geben Sie **Kontenschemata** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Fenster **Kontoschema** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Kontenschemanamen zu erstellen.
3. Im Fenster **Kontenplan kopieren** geben Sie die zwei Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.
4. Füllen Sie die Felder nach Bedarf aus. Wählen Sie im Feld **Standard Spaltenlayout** ein vorhandenes Layout aus. Sie können diese bei Bedarf später bearbeiten.

    Sie nutzen Spaltenlayouts, um Spalten für verschiedene Parameter festzulegen, durch die die Finanzdaten in den Zeilen angezeigt werden. Zum Beispiel können Sie ein Spalten-Layout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres mit vier Spalten vergleicht. Weitere Informationen finden Sie im Abschnitt [So erstellen Sie ein Spaltenlayout](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.
6. Erstellen Sie eine Zeile für jedes Finanzelement, dass im Bericht, wie eine Zeile für Umlaufvermögen und eine weitere Zeile für Anlagen erscheinen sollen. Für Inspiration finden Sie im CRONUS-Demounternehmen vorhandene Kontenschemata.
7. Wählen Sie die **Übersicht** Aktion aus, um den resultierenden Finanzbericht anzuzeigen.
8. Auf der Seite **Kontenschema-Überblick** im Feld **Spaltenlayoutname** wählen Sie ein anderes Spaltenlayout aus, um die Finanzdaten durch andere Einstellungen anzuzeigen.
9. Wählen Sie die Schaltfläche **OK** aus.

Sie haben jetzt die Grundlage des Kontenschemas, die Zeilen von Finanzdaten, die angezeigt werden sollen und ein bestehendes Layout der Spalten definiert, um die Daten in den Zeilen für verschiedene Einstellungen anzuzeigen. Wenn Standard-Spaltenlayout, das Sie in Schritt 4 ausgewählt haben, nicht Ihrem Zweck entspricht, gehen Sie folgendermaßen vor.

### <a name="to-edit-a-column-layout"></a>Um ein Spaltenlayout zu bearbeiten

Sie verwenden Spaltenlayouts, um festzulegen, welche Spalten in dem Bericht erscheinen sollen. Zum Beispiel können Sie ein Layout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres vergleicht. Sie können bis zu 15 Spalten verwenden. Dies ist beispielsweise hilfreich, wenn Sie Budgets für 12 Monate anzeigen und eine Spalte mit der Gesamtsumme einfügen möchten.

> [!NOTE]
> Beachten Sie, dass in einer gedruckten Version eines Kontenschemas höchstens fünf Spalten angezeigt werden können. Wenn das Kontenschema ausschließlich zur Analyse der Seite **Kontenschema. Planen Überblick** dient, können Sie so viele Spalten erstellen, wie Sie möchten.

1. Auf der Seite **Kontenschemata** wählen Sie das relevante Kontenschema, und wählen die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.
2. Auf der Seite **Spaltenlayouts** erstellen Sie eine Zeile für jede Spalte, für die Finanzdaten in dem Finanzbericht angezeigt werden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die Schaltfläche **OK** aus.
4. Öffnen Sie die Seite **Kontenschema. Planen Überblick** gelegentlich, um sicherzustellen, dass das neue Spaltenlayouts wie vorgesehen arbeitet.

> [!NOTE]
> Die Spalten, die Sie in jeder Zeile definieren, zeigt drei Spalten auf der Seite **Kontenschema. Planen Überblick**. Die ersten beiden Spalten, **Zeilennr.** und **Beschreibung**, sind fest.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Eine Spalte zur Berechnung von Prozentsätzen erstellen:

Manchmal möchten Sie möglicherweise eine Spalte in ein Kontenschema einfügen, in der Prozentsätze einer Summe berechnet werden. Wenn beispielsweise mehrere Zeilen vorhanden sind, in denen die Verkäufe nach Dimension aufgeschlüsselt sind, empfiehlt sich die Einrichtung einer Spalte, in der für jede Zeile der prozentuale Anteil an den Gesamtverkäufen angegeben ist.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontenschemata** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Klicken Sie auf der Registerkarte **Kontoschema bearbeiten** in der Gruppe Prozess auf Kontenschema bearbeiten, um eine Kontenschemazeile einzurichten, um die Gesamtsumme zu berechnen, auf denen die Prozentsätze basieren.  
4. Fügen Sie eine Zeile unmittelbar über der ersten Zeile ein, für die Sie einen Prozentsatz anzeigen möchten.  
5. Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein. Geben Sie im Feld **Zusammenzählung** eine Formel für die Summe ein, auf die der Prozentsatz basiert. Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.  
6. Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.  
7. Füllen Sie die Felder in der Zeile wie folgt aus: Wählen Sie im Feld **Spaltenart** **Formel** aus. Geben Sie im Feld **Formel** eine Formel für den Betrag ein, für den ein Prozentsatz berechnet werden soll, gefolgt von %. Wenn beispielsweise Spalte N die Bewegung enthält, geben Sie **N%** ein.  
8. Wiederholen Sie Schritt 4 bis 7 für jede Zeilengruppe, die nach Prozentsätzen aufgeschlüsselt werden soll.

## <a name="to-set-up-account-schedules-with-overviews"></a>Kontenschemata mit Matrizen einrichten:

Sie können eine Kontenschema zum Erstellen eines Vergleichs der in der Finanzbuchhaltung gebuchten Werte mit den Finanzbudgetwerten benutzen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontenschemata** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.  
4. Auf der Seite **Kontenplan** im Feld **Name** wählen Sie den Standard-Kontenplan aus.
5. Wählen Sie die Aktion **Sachkonten einfügen** aus.  
6. Wählen Sie die Konten, die Sie in Ihrer Aufstellung berücksichtigen möchten, und wählen Sie dann **OK**.

    Die Konten sind damit in Ihr Kontenschema eingefügt. Wenn Sie möchten, können Sie auch das Spaltenlayout ändern.  
7. Wählen Sie die Aktion **Übersicht** aus.  
8. Auf der Seite **Kontoschema-Übersicht** im Inforegister **Dimensionenfilter** legen Sie den gewünschten Budgetfilter fest.  
9. Wählen Sie die Schaltfläche **OK** aus.  

Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Vergleichen von Buchhaltungsperioden mithilfe der Periodenformulare

Ihr Kontenschema kann sich die Ergebnisse von verschiedenen Buchhaltungsperioden, wie diesen Monat mit jenem des Vorjahresmonat vergleichen. Öffnen Sie dazu die Seite **Spaltenlayout** und personalisieren Sie sie, indem Sie das Feld **Vergleichsperiodenformel** als Spalte hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md). Sie können dieses Feld dann auf eine Periodenformel setzen.  

Eine Buchhaltungsperiode muss nicht dem Kalender entsprechen, aber jedes Geschäftsjahr muss dieselbe Anzahl von Buchhaltungsperioden haben, selbst wenn jede Periode eine andere Länge haben kann.  

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet diese Periodenformel, um den Betrag der Vergleichsperiode in Bezug auf die Periode zu berechnen, die Sie im Datumsfilter des Anforderungsfensters im Bericht angegeben haben. Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters. Für Periodenspezifikationen stehen folgende Abkürzungen zur Verfügung:

| Abkürzung | Beschreibung                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode                                                                                |
| EP           | Endperiode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.                                   |
| LP           | Laufende Periode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres. Verwenden Sie CP in Formeln, um den Zeitraum festzulegen, in dem die Formel beginnt oder endet. Zum Beispiel FY \[1..CP\] bezeichnet die Zeit vom Beginn des laufenden Geschäftsjahres bis zur laufenden Periode.|
| GJ           | Geschäftsjahr. Zum Beispiel bezeichnet GJ \[1..3\] das erste Quartal des laufenden Geschäftsjahres |

Beispiele für Formeln:

| Formel         | Beschreibung                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Laufende Periode                                                                                  |
| \-1P            | Vorperiode                                                                                 |
| \-1GJ\[1..EP\]  | Das gesamte vorige Geschäftsjahr                                                                     |
| \-1GJ           | Laufende Periode des vorigen Geschäftsjahrs                                                          |
| \-1GJ\[1..3\]   | Das erste Quartal des vorigen Geschäftsjahres                                                           |
| \-1GJ\[1..LP\]  | Vom Anfang des vorigen Geschäftsjahres bis zur laufenden Periode des vorigen Geschäftsjahres einschließlich beider Perioden |
| \-1GJ\[LP..EP\] | Von der laufenden Periode im vorigen Geschäftsjahr bis zur letzten Periode des vorigen Geschäftsjahres, einschließlich beider Perioden   |

Wenn die Berechnung gemäß regulärer Zeitperioden erfolgen soll, muss eine Formel in das Feld **Vergleichsdatumsformel** eingegeben werden. Wenn das Feld zum Beispiel auf -1J festgelegt wird, wird [!INCLUDE [prod_short](includes/prod_short.md)] mit derselben Periode 1 Jahr zuvor verglichen.

> [!NOTE]
> Es ist jedoch nicht immer transparent, welche Perioden Sie vergleichen, da Sie einen Datumsfilter in einem Bericht festlegen können, die verschiedene Daten als die Buchhaltungsperioden umfasst, die Daten im Kontenplan angezeigt werden. Beispielsweise können Sie ein Kontenschema erstellen, in dem Sie diese Periode mit derselben Periode des Vorjahrs vergleichen möchten, damit Sie den **Vergleichs-Datums-Formel** im Feld *1GJ* festlegen. Dann führen Sie den Bericht am 28. Februar aus und legen die Datumsfilter des Januar und Februar fest. Deshalb vergleicht das Kontenschema Januar und Februar dieses Jahr mit dem Januar des Vorjahrs, die die einzige abgeschlossene Buchhaltungsperiode der zwei für das Vorjahr ist.  

Weitere Informationen zu Datumsformeln finden Sie unter [Arbeiten mit Kalenderdaten und -zeiten](ui-enter-date-ranges.md).  

## <a name="import-or-export-account-schedules"></a>Import- oder Exportkontenpläne
Sie können Kontenschemata als RapidStart-Konfigurationspakete importieren und exportieren. Dies ist beispielsweise hilfreich, um sie für andere Unternehmen freizugeben. Das Paket wird in einer .rapidstart-Datei erstellt werden, die Paketinhalte in einem komprimierten Format bereitstellt.

### <a name="to-import-and-export-account-schedules"></a>Kontenschemata importieren und exportieren
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontenschemata** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Kontoplan und dann die Aktionen **Kontenplan importieren** oder **Kontenplan exportieren** aus, je nachdem, was Sie tun möchten. 

> [!NOTE]
> Beim Importieren von Kontenplänen werden vorhandene Datensätze mit demselben Namen wie die importierten Datensätze gelöscht.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index).

## <a name="see-also"></a>Weitere Informationen

[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]