---
title: Erstellen von Sachkontenbudgets
description: Erstellen Sie Sachkonten-Budgets, um verschiedene Finanzaktivitäten zu prognostizieren und Dimensionen zu den einzelnen Intelligence-Zwecken zuzuordnen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: 113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66bd2ae0b30c8c13a6fb8285afd36f4a3495b609
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138596"
---
# <a name="create-gl-budgets"></a>Sachkontenbudgets erstellen

Sie können für dieselbe Periode mehrere Budgets verwalten, indem Sie Budgets mit verschiedenen Namen einrichten. Zuerst richten Sie den Budgetnamen ein und geben die Budgetzahlen ein. Der Budgetname wird dann allen Budgetposten zugewiesen, die Sie erstellen.  

Wenn Sie ein Budget erstellen, können Sie für jedes Budget vier Dimensionen festlegen. Diese bugetspezifischen Dimensionen werden Budgetdimensionen genannt. Sie wählen die Budgetdimensionen für jedes Budget aus den Dimensionen, die Sie bereits eingerichtet haben. Budgetdimensionen können Budgetposten hinzugefügt werden und als Filter für ein Budget verwendet werden. Weitere Informationen finden Sie unter [Arbeiten mit Dimensionen](finance-dimensions.md)

Budgets spielen eine wichtige Rolle in der Business Intelligence wie Finanzauswertung auf Basis von Kontenschemata, die erneut den Budgetposten enthalten, oder beim geplant Analysieren von tatsächlichen Beträgen im Kontenplan. Weitere Informationen finden Sie unter [Business Intelligence](bi.md).

In der Kostenrechnung arbeiten Sie mit Kostenbudgets auf ähnliche Weise. Weitere Informationen finden Sie unter [Budgets erstellen](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Einrichten eines neuen Sachkonten-Budgets

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Sachkontenbudgets** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Liste bearbeiten** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
4. Auf der Seite oben von **Budget** füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.  

    Nur Posten, die diesen Budgetnamen enthalten, der im Feld **Artikelbudgetname** angezeigt wird, werden nun angezeigt. Da der Budgetname gerade erstellt wurde, gibt es keine Posten, die dem Filter entsprechen. Daher ist die Seite leer.  
5. Wählen Sie zum Eingeben eines Betrags die entsprechende Zelle in der Matrix. Die Seite **Finanzbudgetposten** wird geöffnet.  
6. Erstellen Sie eine neue Zeile, und füllen Sie das Feld **Betrag** aus. Schließen Sie die Seite **Finanzbudgetposten**.  
7. Wiederholen Sie die Schritte 5 bis 6, bis alle Budgetbeträge eingegeben sind.  

> [!NOTE]  
> Im Inforegister **Filter** stehen zwischen vier und acht Filter zur Verfügung, abhängig davon, wie viele Budgetdimensionen für den Budgetnamen eingerichtet wurden.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Fibu-Budgets mit Excel exportieren und importieren

Wie bei anderen Seiten können Sie Daten in Budgetseiten in Excel zur weiteren Verarbeitung und Analyse exportieren. Weitere Informationen finden Sie unter [Geschäftsdaten nach Excel exportieren](about-export-data.md).

> [!NOTE]
> Der Kontenplan, auf dem dieses Finanzbudgets basiert, hat Zeilen der Kontoart Überschrift, die die Summe aller Zeilen unterhalb enthalten. Wenn Sie ein Budget exportieren, werden Daten in allen Zeilen ungeachtet der Kontoart exportiert. Sie können nur Daten auf Zeilen der Kontoart Konto zurück importieren. Entsprechend: <br /><br /> **Wenn Sie ein Budget importieren, werden jegliche Werte, die von den Überschriften vorhanden sind, gelöscht** <br /><br /> Dadurch werden falsche Summen vermieden, nachdem die Daten, die in Excel erstellt oder bearbetet wurden, importiert wurden.<br /><br /> **Szenario**: Sie wissen, dass die neuen geplanten Salärkostenr MW 1.200.000 sein werden. Sie möchten das Gehaltsabteilungsbudget für die drei bestimmten Zeilen (der Buchung nach Typ) für Vollzeitmitarbeiter, Teilzeitbeschäftigte und Temp-Hilfe lassen. Die drei Zeilen werden unter einer Gehaltsüberschrift gruppiert.<br /><br />Sie geben 1.200.000 in der Überschrift ein, exportieren das Budget in Excel und senden es dann in die Gehaltsabteilung und kommunizieren die Mandantenwährung 1.200.000.<br /><br /> Die Gehaltsabteilung verteilt den Betrag in drei Sachkonten. Wenn Sie dann das Finanzbudget wieder importieren, werden diese drei Konten mit den neuen Excel-Daten ausgefüllt und summieren zu MW 1.200.000, und die "Überschrift" ist leer.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)  
[Finanzen](finance.md)  
[Business Intelligence](bi.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]