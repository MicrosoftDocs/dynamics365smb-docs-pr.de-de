---
title: Erstellen von Sachkontenbudgets
description: 'Beschreibt, wie Sie Sachkontenbudgets erstellen, um verschiedene finanzielle Aktivitäten zu planen und Dimensionen für Business Intelligence-Zwecke zuzuordnen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="create-gl-budgets"></a>Sachkontenbudgets erstellen

Sie können für dieselbe Periode mehrere Budgets verwalten, indem Sie Budgets mit verschiedenen Namen einrichten. Zuerst richten Sie den Budgetnamen ein und geben die Budgetzahlen ein. Der Budgetname wird dann allen Budgetposten zugewiesen, die Sie erstellen.  

Wenn Sie ein Budget erstellen, können Sie für jedes Budget vier budgetspezifische Dimensionen, die so genannten Budgetdimensionen, definieren. Sie wählen die Dimensionen für jedes Budget aus den Dimensionen aus, die Sie bereits festgelegt haben. Budgetdimensionen können Budgetposten hinzugefügt werden und als Filter für ein Budget verwendet werden. Erfahren Sie mehr unter [Arbeiten mit Dimensionen](finance-dimensions.md).

Budgets spielen eine wichtige Rolle bei Business Intelligence. Zum Beispiel in einer Bilanz, die auf Finanzberichten basiert, die Budgetbuchungen enthalten, oder bei der Analyse von budgetierten gegenüber tatsächlichen Beträgen im Kontenplan. Erfahren Sie mehr unter [Business Intelligence](bi.md).

In der Kostenrechnung arbeiten Sie mit Kostenbudgets auf ähnliche Weise. Erfahren Sie mehr unter [Erstellen von Kalkulationsbudgets](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Einrichten eines neuen Sachkonten-Budgets

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Sachkontenbudgets** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Liste bearbeiten** und füllen Sie dann die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
4. Auf der Seite oben von **Budget** füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.  

    Es werden nur Einträge angezeigt, die den Budgetnamen enthalten, den Sie in das Feld **Budgetname** eingegeben haben. Da Sie gerade den Budgetnamen erstellt haben, gibt es keine Einträge, die dem Filter entsprechen. Daher ist die Seite leer.  
5. Wählen Sie zum Eingeben eines Betrags die entsprechende Zelle in der Matrix. Die Seite **Finanzbudgetposten** wird geöffnet.  
6. Erstellen Sie eine neue Zeile, und füllen Sie das Feld **Betrag** aus. Schließen Sie die Seite **Finanzbudgetposten**.  
7. Wiederholen Sie die Schritte 5 und 6, bis Sie alle Budgetbeträge eingegeben haben.  

> [!NOTE]  
> Auf dem Inforegister **Filter** können Sie die Budgetinformationen nach den Dimensionen filtern, die Sie unter dem Budgetnamen festgelegt haben.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Sachkontenbudgets mit Excel exportieren und importieren

Wie bei praktisch allen anderen Seiten auch, können Sie die Daten auf den Budgetseiten zur weiteren Verarbeitung oder Analyse nach Microsoft Excel exportieren. Erfahren Sie mehr unter [Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md).

> [!NOTE]
> Der Kontenplan, auf dem die Sachkontenbudgets basieren, enthält Zeilen der Kontenart Überschrift, die die Summe der darunter liegenden Zeilen enthalten. Wenn Sie ein Budget exportieren, werden Daten in allen Zeilen ungeachtet der Kontoart exportiert. Es können jedoch nur Daten aus Zeilen der Kontenart Buchung wieder importiert werden. 

Wenn Sie also ein Sachkontenbudget importieren, werden alle Werte in den Zeilen der Überschrift gelöscht. Dadurch werden falsche Summen vermieden, nachdem die Daten, die in Excel erstellt oder bearbetet wurden, importiert wurden.

### <a name="scenario"></a>Szenario

Sie wissen, dass die neuen kalkulierten Gehaltskosten in Mandantenwährung (MW) 1.200.000 betragen werden. Sie möchten der Abteilung Gehälter ermöglichen, die drei spezifischen Zeilen (der Kontoart Buchung) für Vollzeitmitarbeiter, Teilzeitmitarbeiter und Aushilfen zu budgetieren. Die drei Zeilen werden unter einer Gehaltsüberschrift gruppiert.

Sie geben in der Zeile Überschrift 1.200.000 ein, exportieren das Budget nach Excel und senden es dann an die Abteilung Gehälter, um sie anzuweisen, die MW 1.200.000 zu verteilen.

Die Gehaltsabteilung verteilt den Betrag in drei Sachkonten. Wenn Sie dann das Finanzbudget wieder importieren, werden diese drei Konten mit den neuen Excel-Daten ausgefüllt und summieren zu MW 1.200.000, und die "Überschrift" ist leer.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md)  
[Finanzen](finance.md)  
[Business Intelligence](bi.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
