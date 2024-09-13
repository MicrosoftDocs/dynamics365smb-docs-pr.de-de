---
title: Nachhaltigkeit Finanzberichterstellung
description: 'Beschreibt, wie Sie mithilfe von Finanzberichten verschiedene Ansichten und Berichte zur Analyse von Nachhaltigkeitsleistungsdaten erstellen.'
author: altotovi
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: '104, 108, 490'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="analyzing-sustainability-entries-with-financial-reports"></a>Nachhaltigkeitseinträge mit Finanzberichten analysieren

Die Funktion  *Finanzberichte*  bietet Ihnen Einblick in die Finanzdaten, die in Ihrem Kontenplan angezeigt werden. Sie können Finanzberichte einrichten, um die Zahlen in den Sachkonten zu analysieren und Sachposten mit Budgetposten zu vergleichen. Sie können mit derselben Funktion aber auch statistische und Nachhaltigkeitsdaten analysieren und sogar alle drei Datentypen kombinieren.  

## <a name="prerequisites-for-financial-reporting"></a>Voraussetzungen für Finanzberichte

Zum Erstellen von Finanzberichten müssen Sie die Struktur der Daten verstehen, die Sie analysieren möchten. Es gibt einige Schlüsselkonzepte, die Sie wahrscheinlich beachten sollten, bevor Sie Ihre Finanzberichte entwerfen: 

1. Bezogen auf den Kontenplan: 
   1. Ordnen Sie Sachbuchungen den Finanzbuchkontokategorien zu. 
   2. Legen Sie fest, wie Sie Dimensionen verwenden wollen.
   3. Legen Sie Finanzbuchhaltungsbudgets fest.  
2. Im Zusammenhang mit der Nachhaltigkeit:   
   1. Richten Sie Ihre Nachhaltigkeitskonten ein. 
   2. Richten Sie Ihre CO2-Gebühren und CO2e in den  **Emissionsgebühren ein**.
   3. Legen Sie fest, wie Sie Dimensionen verwenden wollen.  
3. Im Zusammenhang mit der statistischen Kontenführung: 
   1. Richten Sie Ihre statistischen Konten ein. 
   2. Legen Sie fest, wie Sie Dimensionen verwenden wollen.  

> [!NOTE]
> Finanzberichte arbeiten nicht direkt mit CO2-, CH4- oder N2O-Emissionen. Stattdessen wird das CO2-Äquivalentmodell verwendet. Das bedeutet, dass Sie zunächst auf der Seite  **Emissionsgebühren**  **CO2e**  (Kohlendioxidäquivalent) konfigurieren müssen.  

> [!NOTE]
> Weitere Einzelheiten zur Verwendung von Finanzberichten mit Finanzdaten und Kontenplänen finden Sie hier  [Finanzberichte mit Finanzdaten und Kontokategorien erstellen](bi-how-work-account-schedule.md).   

## <a name="create-a-new-financial-report"></a>Erstellen Sie einen neuen Finanzbericht

Um schnell eigene Finanzberichte zu erstellen, beginnen Sie mit dem Kopieren eines bestehenden Berichts, wie in Schritt 3 unten beschrieben. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Finanzberichte** wählen Sie die Aktion **Neu**, um einen neuen Finanzbericht zu erstellen.  
3. Geben Sie den Kurznamen des Berichts in das Feld  **Name**  ein (Sie können den Namen später nicht mehr ändern) und geben Sie die  **Beschreibung** ein.  
4. Wählen Sie eine Zeilendefinition und eine Spaltendefinition aus.   
5. Wählen Sie die Aktion  **Bearbeiten Berichtsdefinition**, um auf weitere Eigenschaften des Finanzberichts zuzugreifen.  
6. Auf dem Inforegister **Optionen** können Sie die Berichtsbeschreibung bearbeiten, die Zeilen- und Spaltendefinitionen ändern und festlegen, wie Datumsangaben angezeigt werden. Datumsangaben können in der Hierarchie Tag/Woche/Monat/Quartal/Jahr angegeben sein oder Sie können Buchhaltungsperiode verwenden. Mehr erfahren Sie unter [Vergleich von Buchhaltungsperioden mit Hilfe von Periodenformeln](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas) 
7. Auf dem Inforegister **Dimensionen** können Sie Dimensionsfilter für den Bericht festlegen.  
8. Sie können eine Vorschau des Berichts im Bereich unterhalb des Inforegisters **Dimensionen** anzeigen lassen.   

Wenn Sie Ihre Nachhaltigkeits- oder Statistikdaten analysieren möchten, können Sie dies durch die Einrichtung des  **Zeilendefinition** erreichen.  

So erstellen oder bearbeiten Sie ein Zeilendefinition, folgen:

1. Wählen Sie auf der Seite **Finanzberichte** den entsprechenden Finanzbericht und dann die Aktion **Zeilendefinition bearbeiten** aus. 
2. Richten Sie Zeilen wie in den folgenden Schritten ein.  

> [!NOTE]
> Im Feld **Zeilennr.** Das Feld Kostenarten zeigt die ersten 10 Zeichen eines Bezeichners, z.B. einer Kontonummer. Wenn Sie Bezeichner hinzufügen, die mit denselben 10 Zeichen beginnen, enthält das Feld **Zeilennr.** Duplikate. Feld Bei Bedarf können Sie die Bezeichner manuell bearbeiten, nachdem Sie die Elemente eingefügt haben. Die vollständigen Bezeichner werden im Feld **Zusammenzählung** angezeigt.

> [!NOTE]
> Sie können alle  **Summierungsarten** kombinieren, also Buchungskonten, Sust. Konten, Statistisches Konto.

> [!NOTE]
> Zeilendefinitionen sind nicht versioniert. Wenn Sie ein Zeilendefinition ändern, wird die alte Version ersetzt und Ihre Änderungen werden in der Datenbank gespeichert. 

### <a name="analyzing-sustainability-data"></a>Nachhaltigkeitsdaten analysieren

1. Geben Sie die  **Zeilennummer ein.** Um Ihr Rohmaterial zu identifizieren und eine  **Beschreibung**  als Text hinzuzufügen, der in der Zeile des Finanzberichts angezeigt wird. 
2. Wählen Sie in der Spalte „Summierungsart“ die Option  **Summierungskonten** .   
3. Wählen Sie im Feld „Summierung“ ein oder mehrere Nachhaltigkeitskonten aus. Verwenden Sie dazu alle anwendbaren Filter. 
4. Wählen Sie unter  **Betragsart** eine der folgenden Optionen aus:   
   1. **CO2e**, wenn Sie den CO2-Äquivalentwert aus dem Feld  **CO2e-Emission**  in den  **Nachhaltigkeitshauptbucheinträgen** melden möchten. 
   2. **CO2-Abgabe**, wenn Sie den finanziellen Gegenwert (CO2-Abgabe) aus dem Feld  **CO2-Abgabe**  in den  **Nachhaltigkeitshauptbucheinträgen** melden möchten. 
5. Wenn Sie als  **Summentyp** die Option  **Formel**  wählen, können Sie in der Spalte  **Summen**  mathematische Formeln verwenden.  

### <a name="analyzing-statistical-data"></a>Statistische Daten analysieren

1. Geben Sie die  **Zeilennummer ein.** , um Ihre Zeile zu identifizieren und eine  **Beschreibung**  als Text hinzuzufügen, der in der Zeile des Finanzberichts angezeigt wird. 
2. Wählen Sie in der Spalte  **Summierungsart**  die Option  **Statistische Konten** .   
3. Wählen Sie im Feld  **Summierung**  ein oder mehrere Nachhaltigkeitskonten aus. Verwenden Sie dazu alle anwendbaren Filter. 
4. Wenn Sie als  **Summentyp**  die Option  **Formel** wählen, können Sie in der Spalte  **Summen**  mathematische Formeln verwenden.  

## <a name="see-also"></a>Siehe auch

[Nachhaltigkeitsmanagement Übersicht](finance-manage-sustainability.md)    
[Nachhaltigkeitsberichte und -analysen in Business Central](sustainability-reports.md)   
[Nachhaltigkeits-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Bereiten Sie Finanzberichterstellung vor](bi-how-work-account-schedule.md)    
[Zeilendefinition in Finanzberichterstellung](bi-row-definitions.md)    
[Spaltendefinition im Finanzberichterstellung](bi-column-definitions.md)    
[Finanzen](finance.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
