---
title: Erstellen von Sachkontenbudgets
description: 'Beschreibt, wie Sie Sachkontenbudgets erstellen, um verschiedene finanzielle Aktivitäten zu planen und Dimensionen für Business Intelligence-Zwecke zuzuordnen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Sachkontenbudgets erstellen

Sie können für dieselbe Periode mehrere Budgets verwalten, indem Sie Budgets mit verschiedenen Namen einrichten. Zuerst richten Sie den Budgetnamen ein und geben die Budgetzahlen ein. Der Budgetname wird dann allen Budgetposten zugewiesen, die Sie erstellen.  

Wenn Sie ein Budget erstellen, können Sie dafür vier budgetspezifische Dimensionen, die so genannten Budgetdimensionen, definieren. Sie können Budgetdimensionen verwenden, um Filter für ein Budget festzulegen und Dimensionsinformationen für Budgeteinträge hinzuzufügen. Erfahren Sie mehr unter [Arbeiten mit Dimensionen](finance-dimensions.md).

Budgets spielen eine wichtige Rolle bei Business Intelligence. Zum Beispiel in einer Bilanz, die auf Finanzberichten basiert, die Budgetbuchungen enthalten, oder bei der Analyse von budgetierten gegenüber tatsächlichen Beträgen im Kontenplan. Erfahren Sie mehr unter [Business Intelligence](bi.md).

In der Kostenrechnung arbeiten Sie mit Kostenbudgets auf ähnliche Weise. Erfahren Sie mehr unter [Erstellen von Kalkulationsbudgets](finance-create-cost-budgets.md).  

## Einrichten eines neuen Sachkonten-Budgets

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Sachkontenbudgets** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Liste bearbeiten** und füllen Sie dann die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
4. Auf der Seite oben von **Budget** füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.  

   Auf der Seiten werden nur Einträge angezeigt, die den Budgetnamen enthalten, den Sie im Feld **Budgetname** eingegeben haben. Da Sie gerade den Budgetnamen erstellt haben, gibt es keine Einträge, die dem Filter entsprechen. Daher ist die Seite leer.  
5. Wählen Sie zum Eingeben eines Betrags die entsprechende Zelle in der Matrix. Die Seite **Finanzbudgetposten** wird geöffnet.  
6. Erstellen Sie eine neue Zeile, und füllen Sie das Feld **Betrag** aus. Schließen Sie die Seite **Finanzbudgetposten**.  
7. Wiederholen Sie die Schritte 5 und 6 für alle Beträge im Budget.  

> [!NOTE]  
> Auf dem Inforegister **Filter** können Sie die Budgetinformationen nach den Dimensionen filtern, die Sie unter dem Budgetnamen festgelegt haben.

## Sachkontenbudgets mit Excel exportieren und importieren

Wie bei praktisch allen anderen Seiten auch, können Sie die Daten auf den Budgetseiten zur weiteren Verarbeitung oder Analyse nach Microsoft Excel exportieren. Erfahren Sie mehr unter [Exportieren Ihrer Geschäftsdaten nach Excel](about-export-data.md).

> [!NOTE]
> Der Kontenplan, auf dem die Sachkontenbudgets basieren, verfügt über Zeilen des Kontotyps „Überschrift“. Diese Zeilen enthalten die Summe der darunterliegenden Zeilen. Wenn Sie ein Sachkontenbudget exportieren, exportieren Sie Daten in allen Zeilen ungeachtet des Kontotyps. Sie können jedoch nur Daten aus Zeilen des Kontotyps „Buchung“ importieren.

Wenn Sie also ein Sachkontenbudget importieren, werden alle Werte in den Zeilen der Überschrift gelöscht. Sie werden gelöscht, um falsche Summen zu vermeiden, nachdem Sie Daten importiert haben, die in Excel erstellt oder bearbeitet wurden.

### Szenario

Sie wissen, dass die neuen kalkulierten Gehaltskosten in Mandantenwährung (MW) 1.200.000 betragen werden. Sie möchten der Abteilung Gehälter ermöglichen, die drei spezifischen Zeilen (der Kontoart Buchung) für Vollzeitmitarbeiter, Teilzeitmitarbeiter und Aushilfen zu budgetieren. Die drei Zeilen werden unter einer Gehaltsüberschrift gruppiert.

Sie geben in der Zeile „Überschrift“ 1.200.000 ein, exportieren das Budget nach Excel und senden es dann an die Abteilung Gehälter, um sie anzuweisen, die MW 1.200.000 zu verteilen.

Die Gehaltsabteilung verteilt den Betrag in drei Sachkonten. Wenn Sie dann das Finanzbudget wieder importieren, werden diese drei Konten mit den neuen Excel-Daten ausgefüllt und summieren zu MW 1.200.000, und die "Überschrift" ist leer.

## Siehe auch

[Geschäftsdaten nach Excel exportieren](about-export-data.md)  
[Finanzen](finance.md)  
[Business Intelligence](bi.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
