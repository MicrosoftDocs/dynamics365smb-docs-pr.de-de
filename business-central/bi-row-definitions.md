---
title: Zeilendefinitionen in Finanzberichten
description: 'Beschreibt, wie Zeilendefinitionen in Finanzberichten funktionieren.'
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# <a name="row-definitions-in-financial-reporting"></a>Zeilendefinitionen in Finanzberichten

Zeilendefinitionen in Finanzberichten bieten einen Platz für Berechnungen, die nicht direkt im Kontenplan vorgenommen werden können. Sie können beispielsweise Zwischensummen für Gruppen von Konten erstellen und diese Summe dann in andere Summen aufnehmen. Dabei können auch Zwischenschritte berechnet werden, die im abschließenden Bericht nicht erscheinen.

## <a name="create-or-edit-a-row-definition"></a>Eine Zeilendefinition erstellen oder bearbeiten

Gehen Sie wie folgt vor, um eine Zeilendefinition zu erstellen oder zu bearbeiten:

1. Wählen Sie auf der Seite **Finanzberichte** den entsprechenden Finanzbericht und dann die Aktion **Zeilendefinition bearbeiten** aus.
1. Wählen Sie die Aktionen **Sachkonten einfügen**, **KF-Konten einfügen** und **Kostenarten einfügen**, um eine Zeile für jedes Finanzelement zu erstellen, das Sie analysieren möchten. Beispielsweise könnten Sie eine Zeile für Umlaufvermögen und eine andere für Anlagevermögen haben. Lassen Sie sich von den Finanzberichten im Demounternehmen CRONUS inspirieren.

    > [!NOTE]
    > Im Feld **Zeilennr.** Das Feld Kostenarten zeigt die ersten 10 Zeichen eines Bezeichners, z.B. einer Kontonummer. Wenn Sie Bezeichner hinzufügen, die mit denselben 10 Zeichen beginnen, enthält das Feld **Zeilennr.** Duplikate. Feld Bei Bedarf können Sie die Bezeichner manuell bearbeiten, nachdem Sie die Elemente eingefügt haben. Die vollständigen Bezeichner werden im Feld **Zusammenzählung** angezeigt.

> [!NOTE]
> Die Spalten, die Sie in jeder Zeile der Zeilendefinition festlegen, entsprechen den Spalten drei und höher auf der Seite **Finanzbericht**. Die ersten beiden Spalten, **Zeilennr.** und **Beschreibung**, sind fest.  

## <a name="built-in-row-definitions"></a>Integrierte Zeilendefinitionen

[!INCLUDE[prod_short](includes/prod_short.md)] bietet Beispielzeilendefinitionen, die Ihnen dabei helfen können, schnell mit der Einrichtung von Finanzberichten zu beginnen, die Ihren Anforderungen entsprechen.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> Die Beispielfinanzberichte in [!INCLUDE[prod_short](includes/prod_short.md)] sind nicht sofort einsatzbereit. Je nachdem, wie Sie Ihre Finanzbuchhaltungskonten, Dimensionen, Finanzbuchhaltungskontokategorien und Budgets einrichten, passen Sie die Beispielzeilen- und -spaltendefinitionen sowie die Finanzberichte, die sie verwenden, an Ihre Einrichtung an.

## <a name="use-gl-account-categories-to-change-the-layout-of-your-financial-statements"></a>Mithilfe von Finanzbuchhaltungskontokategorien das Layout Ihrer Finanzaufstellungen ändern

Sie können Sachkontokategorien dazu verwenden, das Layout Ihrer Finanzberichte zu ändern. Nachdem Sie beispielsweise Ihre Kontokategorien auf der Seite **Finanzbuchhaltungskontokategorien** festgelegt haben, können Sie die Aktion **Finanzberichte generieren** wählen und die zugrundeliegenden Finanzberichte für die Kernfinanzberichte aktualisieren. Wenn Sie dann das nächste Mal einen dieser Berichte ausführen, z. B. den Bericht **Bilanz**, werden neue Summen und Unterposten hinzugefügt.

Ein weiterer Vorteil der Verwendung von Finanzbuchhaltungskontokategorien anstatt reiner Finanzbuchhaltungskonten in Ihren Zeilendefinitionen besteht darin, dass sich eine Änderung der Struktur Ihres Kontenplans nicht auf Ihre Finanzberichte auswirkt.

> [!NOTE]
> Die Kontokategorien der obersten Ebene, wie z. B. der Knoten **Verbindlichkeiten**, sind fest vorgegeben, und Sie können keine eigenen hinzufügen. Sie können jedoch Kontenkategorien auf niedrigeren Ebenen löschen und hinzufügen und festlegen, wie der zugehörige Finanzbericht in Berichten erscheint.
>
> Sie sollten Ihre eigenen Sachkonto-Kategorien auf unterer Ebene von Grund auf erstellen und strukturieren, ggf. in einer Hierarchie, anstatt zu versuchen, die vorhandenen Kategorien neu anzuordnen. Sie können beispielsweise den Knoten **Verbindlichkeiten** neu strukturieren, sodass er den neuen Knoten **Eigenkapital** gefolgt von den Knoten **Kurzfristige Verbindlichkeiten** und **Langfristige Verbindlichkeiten** enthalten. Weitere Informationen finden Sie unter [Finanzbuchhaltungskonten Kontokategorien zuordnen](finance-general-ledger.md#account-categories).

## <a name="best-practices-for-working-with-row-definitions"></a>Bewährte Methoden für die Arbeit mit Zeilendefinitionen

Zeilendefinitionen sind nicht versioniert. Wenn Sie eine Zeilendefinition ändern, wird die alte Version ersetzt, wenn Ihre Änderung in der Datenbank gespeichert wird. Die folgende Liste enthält einige bewährte Vorgehensweisen für die Arbeit mit Zeilendefinitionen:

- Wenn Sie Zeilendefinition hinzufügen, wählen Sie einen guten Code und geben Sie im Beschreibungsfeld einen aussagekräftigen Text ein, solange Sie noch wissen, wofür Sie die Zeilendefinition verwenden. Diese Informationen helfen Ihren Mitarbeitenden (und Ihnen selbst in der Zukunft) bei der Arbeit mit Finanzberichten und falls notwendig beim Ändern der Zeilendefinition.
- Bevor Sie eine Zeilendefinition ändern, sollten Sie eine Sicherungskopie davon erstellen, für den Fall, dass die Änderung nicht wie erwartet funktioniert. Sie können die Definition entweder einfach kopieren (geben Sie ihr einen guten Namen) oder exportieren. Mehr erfahren Sie unter [Zeilendefinitionen importieren oder exportieren](#import-or-export-financial-reporting-row-definitions).
- Wenn Sie eine neue Kopie einer Definition benötigen, die [!INCLUDE[prod_short](includes/prod_short.md)] bereitstellt, erhalten Sie diese ganz einfach, indem Sie ein neues Unternehmen erstellen, das nur die Einrichtungsdaten enthält. Exportieren Sie dann die Definition und importieren Sie sie in das Unternehmen, wo die Definition aktualisiert werden muss.

## <a name="import-or-export-financial-reporting-row-definitions"></a>Finanzberichtszeilendefinitionen importieren oder exportieren

Sie können Finanzberichtszeilendefinitionen als RapidStart-Konfigurationspakete importieren und exportieren. Konfigurationspakete sind beispielsweise hilfreich, um Informationen für andere Unternehmen freizugeben. Das Paket wird in einer .rapidstart-Datei erstellt, die den Inhalt komprimiert.

> [!NOTE]
> Wenn Sie Finanzberichtszeilendefinitionen importieren, werden bestehende Datensätze mit dem gleichen Namen wie die zu importierenden durch die neuen Definitionen ersetzt. Das Konfigurationspaket für eine Berichtsdefinition überschreibt keine vorhandenen Zeilen- oder Spaltendefinitionen, die in der Berichtsdefinition verwendet werden.

Um Finanzberichtszeilendefinitionen zu importieren oder zu exportieren, gehen Sie wie folgt vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") öffnet. aus, geben Sie **Zeilendefinitionen** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie die Zeilendefinition und dann die Aktion **Zeilendefinition importieren** oder **Zeilendefinition exportieren** aus, je nachdem, was Sie tun möchten.

## <a name="see-also"></a>Siehe auch

[Spaltendefinitionen in Finanzberichten](bi-column-definitions.md)  
[Finanzberichte erstellen](bi-how-work-account-schedule.md)  
[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
