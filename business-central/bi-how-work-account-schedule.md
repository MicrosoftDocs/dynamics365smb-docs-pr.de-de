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
ms.openlocfilehash: 8984d007f2082c6a21a3d2226a20f2ad585b131a
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129732"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor

Verwenden von Kontenplan, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden. Verwenden von Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten. Die Ergebnisse werden in Diagrammen und Berichten in Ihrem Rollencenter angezeigt, darunter der Cashflowplan sowie die GuV- und Bilanzberichte.

Sie rufen diese beiden Berichte beispielsweise mit der Aktion **Finanzverhältnis-Abrechnungen** im Business Manager und Buchhalter Rollen-Centers ab.  

[!INCLUDE[prod_short](includes/prod_short.md)] bietet Musterkontopläne, die Sie sofort verwenden können. Sie können auch Ihre eigenen Zeilen und Spalten einrichten, um die zu vergleichenden Zahlen anzugeben. Sie können beispielsweise Kontenschemata zur Berechnung von Gewinnmargen für Dimensionen, z. B. Abteilungen oder Debitorengruppen, erstellen. Die Anzahl der benutzerdefinierten Finanzaufstellungen, die Sie erstellen können, ist unbegrenzt.  

Das Einrichten von Kontenschemata erfordert ein Verständnis für die Finanzdaten im Kontenplan. Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten anzeigen. Dazu müssen Sie jedoch Budgets erstellt haben. Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Kontenschemata

Kontenschemata ordnen Konten aus Ihrem Kontenplan so an, dass Daten einfach dargestellt werden können. Durch die Möglichkeit zum Einrichten mehrerer Layouts können Sie die Informationen definieren, die Sie dem Kontenplan entnehmen möchten. Kontenschemata stellen einen Ort für Berechnungen bereit, die nicht direkt im Kontenplan vorgenommen werden können. Sie können beispielsweise Zwischensummen für Gruppen von Konten erstellen und diese Summe dann in andere Summen aufnehmen. Ein weiteres Beispiel ist die Berechnung von Gewinnmargen für Dimensionen wie Abteilungen oder Debitorengruppen. Darüber hinaus können Sie Sachposten und Finanzbudgetposten filtern, z. B. nach Bewegung oder Sollbetrag.

Auch können mehrere Kontenschemata und Spaltenlayouts mithilfe von Formeln verglichen werden, die Ihnen die Ausführung der folgenden Aktionen ermöglichen:

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

Die Kontenschemata in der Standardeinstellung sind [!INCLUDE[prod_short](includes/prod_short.md)] die Basis der Standardfinanzberichte, die möglicherweise nicht den Anforderungen Ihres Unternehmens entsprechen. Um Ihre eigenen Finanzberichte schnell erstellen zu können, beginnen Sie, indem Sie ein vorhandenes Kontenschema kopieren, wie in Schritt 3 beschrieben.

> [!TIP]
> Nachdem Sie einen Kontenplan erstellt haben, können Sie die Seite **Kontenschemamatrix** verwenden, um eine Vorschau des Finanzberichts anzuzeigen und zu validieren, den der Kontenplan definiert. Wählen Sie zum Öffnen der Seite die Aktion **Übersicht** aus.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten"). Symbol. Geben Sie **Kontenschemata** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Fenster **Kontoschema** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Kontenschemanamen zu erstellen.
3. Wenn Sie alternativ Einstellungen aus einem vorhandenen Kontoplan wiederverwenden möchten, wählen Sie die Aktion **Kontoplan kopieren** aus.
4. Füllen Sie die Felder nach Bedarf aus. Wählen Sie im Feld **Standard Spaltenlayout** ein vorhandenes Layout aus. Sie können diese bei Bedarf später bearbeiten.

    Spaltenlayouts definieren Spalten für die Parameter, nach denen die Finanzdaten in den Zeilen angezeigt werden. Ein Spaltenlayout kann beispielsweise vier Spalten enthalten, anhand derer Sie Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres vergleichen können. Weitere Informationen finden Sie im Abschnitt [So erstellen Sie ein Spaltenlayout](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.
6. Wählen Sie je nachdem, was Sie analysieren möchten, die Aktionen **Sachkonten einfügen**, **CF-Konten einfügen** und **Kostenarten einfügen** aus, um eine Zeile für jedes Finanzelement zu erstellen. Beispielsweise könnten Sie eine Zeile für Umlaufvermögen und eine andere für Anlagevermögen haben. Lassen Sie sich von den Kontenplänen des Demonstrationsunternehmens CRONUS inspirieren.

    > [!NOTE]
    > Im Feld **Zeilennr.** werden die ersten 10 Zeichen eines Bezeichners angezeigt, beispielsweise eine Kontonummer. Wenn Sie Bezeichner hinzufügen, die mit denselben 10 Zeichen beginnen, enthält das Feld **Zeilennr.** Duplikate . Bei Bedarf können Sie die Bezeichner nach dem Einfügen der Elemente manuell bearbeiten. Die vollständigen Bezeichner werden im Feld **Zusammenzählung** angezeigt.

7. Wählen Sie die **Übersicht** Aktion aus, um den resultierenden Finanzbericht anzuzeigen.
8. Auf der Seite **Kontenschema-Überblick** im Feld **Spaltenlayoutname** wählen Sie ein anderes Spaltenlayout aus, um die Finanzdaten durch andere Einstellungen anzuzeigen.
9. Wählen Sie die Schaltfläche **OK**.

Sie haben jetzt die Grundlage des Kontenschemas, die Zeilen von Finanzdaten, die angezeigt werden sollen und ein bestehendes Layout der Spalten definiert, um die Daten in den Zeilen für verschiedene Einstellungen anzuzeigen. Wenn Standard-Spaltenlayout, das Sie in Schritt 4 ausgewählt haben, nicht Ihrem Zweck entspricht, gehen Sie folgendermaßen vor.

### <a name="to-edit-a-column-layout"></a>Um ein Spaltenlayout zu bearbeiten

Sie verwenden Spaltenlayouts, um festzulegen, welche Spalten in dem Bericht erscheinen sollen. Zum Beispiel können Sie ein Layout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres vergleicht. Sie können bis zu 15 Spalten haben, was beispielsweise hilfreich ist, um Budgets für 12 Monate mit einer Spalte anzuzeigen, die die Gesamtsumme anzeigt.

> [!NOTE]
> Beachten Sie, dass in einer gedruckten Version eines Kontenschemas höchstens fünf Spalten angezeigt werden können. Wenn das Kontenschema ausschließlich zur Analyse der Seite **Kontenschema. Planen Überblick** dient, können Sie so viele Spalten erstellen, wie Sie möchten.

1. Auf der Seite **Kontenschemata** wählen Sie das relevante Kontenschema, und wählen die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.
2. Auf der Seite **Spaltenlayouts** erstellen Sie eine Zeile für jede Spalte, für die Finanzdaten in dem Finanzbericht angezeigt werden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die Schaltfläche **OK** aus.
4. Öffnen Sie die Seite **Kontenschema. Planen Überblick** gelegentlich, um sicherzustellen, dass das neue Spaltenlayouts wie vorgesehen arbeitet.

> [!NOTE]
> Die Spalten, die Sie in jeder Zeile definieren, zeigt drei Spalten auf der Seite **Kontenschema. Planen Überblick**. Die ersten beiden Spalten, **Zeilennr.** und **Beschreibung**, sind fest.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Eine Spalte zur Berechnung von Prozentsätzen erstellen:

Manchmal möchten Sie möglicherweise eine Spalte in ein Kontenschema einfügen, in der Prozentsätze einer Summe berechnet werden. Wenn beispielsweise Zeilen vorhanden sind, die den Umsatz nach Dimensionen aufschlüsseln, empfiehlt sich die Einrichtung einer Spalte, die den prozentualen Anteil an den Gesamtverkäufen in jeder Zeile angibt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontenschemata** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Klicken Sie auf der Registerkarte **Kontoschema bearbeiten** in der Gruppe Prozess auf Kontenschema bearbeiten, um eine Kontenschemazeile einzurichten, um die Gesamtsumme zu berechnen, auf denen die Prozentsätze basieren.  
4. Fügen Sie eine Zeile unmittelbar über der ersten Zeile ein, für die Sie einen Prozentsatz anzeigen möchten.  
5. Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein. Geben Sie im Feld **Zusammenzählung** eine Formel für die Summe ein, auf die der Prozentsatz basiert. Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.  
6. Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.  
7. Füllen Sie die Felder in der Zeile wie folgt aus: Wählen Sie im Feld **Spaltenart** **Formel** aus. Geben Sie im Feld **Formel** eine Formel für den Betrag ein, für den ein Prozentsatz berechnet werden soll, gefolgt von %. Wenn beispielsweise Spalte N die Bewegung enthält, geben Sie **N%** ein.  
8. Wiederholen Sie Schritt 4 bis 7 für jede Zeilengruppe, die nach Prozentsätzen aufgeschlüsselt werden soll.

## <a name="to-set-up-account-schedules-with-overviews"></a>Kontenschemata mit Matrizen einrichten:

Sie können eine Kontenschema verwenden, um einen Vergleichs der Finanzbudgetbeträge mit den Sachkonto-Budgetbeträgen zu erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontenschemata** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.  
4. Auf der Seite **Kontenplan** im Feld **Name** wählen Sie den Standard-Kontenplan aus.
5. Wählen Sie die Aktion **Sachkonten einfügen** aus.  
6. Wählen Sie die Konten, die Sie in Ihrer Aufstellung berücksichtigen möchten, und wählen Sie dann **OK**.

    Die Konten sind damit in Ihr Kontenschema eingefügt. Wenn Sie möchten, können Sie auch das Spaltenlayout ändern.  
7. Wählen Sie die Aktion **Übersicht** aus.  
8. Auf der Seite **Kontoschema-Übersicht** im Inforegister **Dimensionenfilter** legen Sie den Budgetfilter fest, den Sie verwenden möchten.  
9. Wählen Sie die Schaltfläche **OK**.  

Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Vergleichen von Buchhaltungsperioden mithilfe der Periodenformulare

Ihr Kontenschema kann sich die Ergebnisse von verschiedenen Buchhaltungsperioden, wie diesen Monat mit jenem des Vorjahresmonat vergleichen. Öffnen Sie dazu die Seite **Spaltenlayout** und personalisieren Sie sie, indem Sie das Feld **Vergleichsperiodenformel** als Spalte hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md). Sie können dieses Feld dann auf eine Periodenformel setzen.  

Eine Buchhaltungsperiode muss nicht mit dem Kalender übereinstimmen. Jedes Geschäftsjahr muss jedoch dieselbe Anzahl von Buchhaltungsperioden aufweisen, selbst wenn jede Periode eine andere Länge haben kann.  

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet die Periodenformel, um den Betrag aus der Vergleichsperiode im Verhältnis zu der durch den Datumsfilter im Bericht dargestellten Periode zu berechnen. Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters. Für Periodenspezifikationen stehen folgende Abkürzungen zur Verfügung:

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
Sie können Kontenschemata als RapidStart-Konfigurationspakete importieren und exportieren. Konfigurationspakete sind beispielsweise hilfreich, um sie für andere Unternehmen freizugeben. Das Paket wird in einer .rapidstart-Datei erstellt werden, die Paketinhalte in einem komprimierten Format bereitstellt.

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