---
title: 'Vorgehensweise: Kommissionieren von Artikeln für den Warenausgang | Microsoft Docs'
description: Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung der Kommissionierung und des Warenausgangs erforderlich ist, verwenden Sie die Kommissionierbelege, um Kommissionierinformationen vor dem Buchen des Warenausgangs zu erstellen und zu bearbeiten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dc955230953738f36bf26ec2e8b78f59325a38f9
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386124"
---
# <a name="pick-items-for-warehouse-shipment"></a>Um Artikel für den Warenausgang zu kommissionieren
Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung der Kommissionierung und des Warenausgangs erforderlich ist, verwenden Sie die Kommissionierbelege, um Kommissionierinformationen vor dem Buchen des Warenausgangs zu erstellen und zu bearbeiten.  

Sie können einen Kommissionierungsbeleg nicht von Grund auf neu erstellen, da eine Kommissionierungsaktivität immer Teil eines Workflows ist, entweder in einem Abruf- oder Push-Szenario.  

Sie können Kommissionierungsbelege in einem Abrufverfahren erstellen, indem Sie einen leeren Warenausgangsbeleg öffnen, Herkunftsbelege ermitteln, die für die Lieferung freigegeben wurden, und dann für diese Lieferungen Kommissionierzeilen erstellen. Sie können die Funktionen **Herkunftsbelege holen** oder **Filter zum Holen von Herk.-Belegen verwenden** verwenden, um Herkunftsbelege zu ermitteln, die für den Warenausgang bereit sind.

Alternativ können Sie die Seite **Kommissioniervorschlag** verwenden, um Kommissionierzeilen im Stapelbetrieb zu holen und zu erstellen. Weitere Informationen finden Sie unter [Kommissionierungen im Vorschlag bearbeiten](warehouse-how-to-plan-picks-in-worksheets.md).  

Sie können Kommissionierungsbelege auch Push-artig im Fenster **Warenausgang** erstellen, indem Sie die Seite **Kommissionierung erstellen** auswählen.  

> [!NOTE]  
>  Die Kommissionierung für den Warenausgang von Artikeln, die mit dem betreffenden Verkaufsauftrag montiert werden, folgt denselben Schritten wie die reguläre Kommissionierung für den Warenausgang, die in diesem Thema beschrieben ist. Jedoch kann die Anzahl der Kommissionierzeilen pro zu liefernder Menge n:1 sein, da die Kommissionierung für die Komponenten, nicht für den Montageartikel erfolgt.  
>   
>  Die Kommissionierzeilen werden für den Wert im Feld **Restmenge** in den Zeilen des Montageauftrags erstellt, der mit der Verkaufsauftragszeile verknüpft ist, die geliefert wird. Dadurch ist sichergestellt, dass alle Komponenten in einer Aktion kommissioniert werden.  
>   
>  Weitere Informationen finden Sie im Abschnitt "Verwenden von Auftragsmontageartikeln in Warenausgängen".  
>   
>  Allgemeine Informationen über das Kommissionieren von Komponenten für Montageaufträge, einschließlich von Situationen, in denen der Montageartikel nicht mit einer Verkaufslieferung fällig ist, finden Sie unter [Vorgehensweise: Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md).  

## <a name="to-pick-items-for-warehouse-shipment"></a>Um Artikel für den Warenausgang zu kommissionieren  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kommissionierungen** ein und wählen Sie dann den entsprechenden Link.  

    Wenn Sie an einer bestimmten Kommissionierung arbeiten möchten, wählen Sie die Kommissionierung in der Liste aus, oder filtern Sie die Liste, um die Kommissionierungen zu finden, die speziell Ihnen zugeordnet wurden. Öffnen Sie die Kommissionierungskarte.  
2.  Wenn das Feld **Zugewiesene Benutzer-ID** leer ist, geben Sie gegebenenfalls Ihre ID ein, um sich zu identifizieren.  
3.  Führen Sie die tatsächliche Kommissionierung der Artikel aus.  

    Wenn das Lager für die Verwendung von Lagerplätzen eingerichtet wurde, werden die Vorgabelagerplätze der Artikel als Vorschlag für den Entnahmeort verwendet. Die Anweisungen erscheinen als zwei Zeilen, mindestens eine für jede Aktivitätenart, "Entnahme" und "Einlagerung".  

    Wenn das Lager mit gesteuerter Einlagerung und Kommissionierung eingerichtet wurde, wird die Lagerplatzpriorität verwendet, um die besten Lagerplätze für die Kommissionierung zu berechnen und in den Kommissionierzeilen vorzuschlagen. Die Anweisungen erscheinen als zwei Zeilen, mindestens eine für jede Aktivitätenart, "Entnahme" und "Einlagerung".  

4.  Wenn Sie die Kommissionierung ausgeführt und die Artikel in den Ausgangsbereich oder den Ausgangslagerplatz eingelagert haben, wählen Sie die Aktionen **Kommissionierung registrieren** aus.  

Die für Lieferung verantwortliche Person kann die Artikel in den Warenausgang bringen und den Warenausgang, einschließlich dem zugehörigen Herkunftsbeleg, auf der Seite **Warenausgang** buchen. Weitere Informationen finden Sie unter [Artikel versenden](warehouse-how-ship-items.md).   

Zusätzlich zur Kommissionierung für Herkunftsbelege, die in diesem Thema beschrieben wird, können Sie Artikel ohne Bezug zu Herkunftsbelegen an Lagerorten entnehmen und einlagern. Weitere Informationen finden Sie unter [Kommissionieren und Einlagern ohne Herkunftsbeleg](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Verwenden von Auftragsmontageartikeln in Warenausgängen
In den Auftragsmontageszenarien wird das Feld **Zu liefern** in Warenausgangszeilen verwendet, um zu erfassen, wie viele Einheiten montiert werden. Die angegebene Menge wird dann als Montageausstoß gebucht, wenn der Warenausgang gebucht wird.

Für andere Warenausgangszeilen ist der Wert im Feld **Zu liefern** von Anfang an Null.

Wenn Arbeiter für montagefertige Teile oder für die gesamte Auftragsmontagemenge zuständig sind, erfassen sie diese im Feld **Vesandmenge** in der Warenausgangszeile und wählen dann die Aktion **Warenausgang buchen**. Das Ergebnis ist, dass der entsprechende Montageausstoß gebucht wird, einschließlich des Komponentenverbrauchs. Eine Verkaufslieferung für die Menge wird für den Verkaufsauftrag gebucht.

Vom Montageauftrag aus können Sie **Warenausgangszeile für Programmfertigung** wählen, um auf die Warenausgangszeile zuzugreifen. Dies ist für Arbeiter hilfreich, die die Seite **Warenausgang** üblicherweise nicht verwenden.

Nachdem der Warenausgang gebucht ist, werden verschiedene Felder in der Verkaufsauftragszeile aktualisiert, um den Status im Lager anzuzeigen. Die folgenden Felder werden auch aktualisiert, um anzuzeigen, wie viele Auftragsmontagemengen noch nicht montiert und geliefert wurden:

- **Auftragsmontage - Lagerrestbestellmenge**
- **Auftragsmontage - Lagerrestbestellmenge (Basis)**

> [!NOTE]
> In Kombinationsszenarien, in denen ein Teil der Menge zunächst montiert und ein anderer aus dem Lager geliefert werden muss, werden mindestens zwei Warenausgangszeilen erstellt. Eine für die Auftragsmontagemenge, und eine für die Lagermenge.

> In diesem Fall wird die Auftragsmontagemenge wie in diesem Thema beschrieben behandelt, und die Lagermenge wird wie jede andere reguläre Warenausgangszeile verarbeitet. Weitere Informationen finden Sie im Abschnitt "Kombinationsszenarien" in [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]