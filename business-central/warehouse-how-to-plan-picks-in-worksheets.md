---
title: 'Vorgehensweise: Planen von Kommissionierungen in Vorschlägen | Microsoft Docs'
description: Wenn Ihr Lager so eingerichtet wurde, dass die Bearbeitung der Kommissionierung sowie des Warenausgangs erforderlich sind, können Sie für das Lager festlegen, dass die Zeilen in Warenausgangsbelegen nicht automatisch in Kommissionieranweisungen umgewandelt, sondern stattdessen für den Kommissioniervorschlag verfügbar gemacht werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 250d85308e60f93ccba28e2354e47be185918d52
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756142"
---
# <a name="plan-picks-in-worksheets"></a>Kommissionierungen im Vorschlag bearbeiten

Wenn Ihr Lager so eingerichtet wurde, dass die Bearbeitung der Kommissionierung sowie des Warenausgangs erforderlich sind, können Sie für das Lager festlegen, dass die Zeilen in Warenausgangsbelegen nicht automatisch in Kommissionieranweisungen umgewandelt, sondern stattdessen für den Kommissioniervorschlag verfügbar gemacht werden.  

> [!NOTE]  
> Wenn bereits Kommissionieranweisungen erstellt wurden und Sie diese zu einer effizienten Kommissionieranweisung kombinieren möchten, müssen Sie die einzelnen Kommissionierungen löschen. Die Zeilen, die kommissioniert werden sollen, können jetzt im Vorschlag aufgelistet werden.  

Im Kommissioniervorschlag können Sie Kommissionierlisten für Mitarbeiter einrichten, die die Zeit minimieren, die die Mitarbeiter für das Bewegen der Artikel aufwenden müssen. Es gibt Felder, die Informationen über die Artikelmengen enthalten, die in den Zuordnungslagerplätzen verfügbar sind. Dies ist in Zuordnungssituationen nützlich, um die Arbeit zuzuweisen, da die Anwendung immer die Kommissionierung von einem Zuordnungslagerplatz vor allen anderen Lagerplätzen vorschlägt, und zwar unabhängig von der Einheit. Die Zeilen im Vorschlag können aus einer Reihe von Herkunftsbelegen stammen und nach Artikel, Regalnummer, Herkunftsbeleg, Fälligkeitsdatum oder Lieferadresse sortiert sein.  

Wenn Sie nach Fälligkeitsdatum sortieren, können Sie wählen, alle Zeilen aus dem Vorschlag zu löschen, außer denen, die sofort beachtet werden müssen. Die weniger dringenden Zeilen werden nicht wirklich gelöscht, sondern nur in den **Kommissioniervorschlag** zurückgeschickt. Wenn Sie die Kommissionierung erzeugen, wurden die Zeilen bereits nach Fälligkeitsdatum sortiert und Sie können die Kommissionierung einem bestimmten Mitarbeiter zuordnen.  

> [!NOTE]  
> Die Kommissionierung für den Warenausgang von Artikeln, die mit dem betreffenden Verkaufsauftrag montiert werden, folgt denselben Schritten wie die reguläre Kommissionierung für den Warenausgang, die in diesem Thema beschrieben ist. Jedoch kann die Anzahl der Kommissionierzeilen pro zu liefernder Menge n:1 sein, da die Kommissionierung für die Komponenten, nicht für den Montageartikel erfolgt.  
>
> Die Kommissionierzeilen werden für den Wert im Feld **Restmenge** in den Zeilen des Montageauftrags erstellt, der mit der Verkaufsauftragszeile verknüpft ist, die geliefert wird. Dadurch ist sichergestellt, dass alle Komponenten in einer Aktion kommissioniert werden.  
>
> Weitere Informationen finden Sie im Abschnitt "Verwenden von Auftragsmontageartikeln in Warenausgängen" in Warenausgang.  
>
> Allgemeine Informationen über das Kommissionieren von Komponenten für Montageaufträge, einschließlich von Situationen, in denen der Montageartikel nicht mit einer Verkaufslieferung fällig ist, finden Sie unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-plan-picks-in-the-worksheet"></a>So planen Sie Kommissionierungen im Vorschlag:

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kommissionierungsvorschlag** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die **Logistikbeleg holen** Aktion aus.  
3. Wählen Sie die Warenausgänge, für die Sie eine Kommissionierung vorbereiten möchten. Sie können die Zeilen hier bis zu einem bestimmten Grad sortieren, diese Sortierung wird jedoch nicht bis in die Kommissionieranweisung weitergegeben. Sie können auch einige der Zeilen löschen, um eine effektivere Kommissionierung zu erzielen. Wenn es z. B. eine Anzahl von Zeilen mit Artikeln in Zuordnungslagerplätzen gibt, möchten Sie möglicherweise eine Kommissionierung für alle Zeilen erzeugen, die mit diesen Zeilen zusammenhängen. Die zugeordneten Artikel werden ausgeliefert (gemeinsam mit anderen Artikeln im Warenausgang) und die Zuordnungslagerplätze haben wieder Platz für neue ankommende Artikel.  
4. Wählen Sie die Aktion **Kommissionierung erstellen** aus, und füllen Sie die Seite **Kommissionierung erstellen**. Die Sortierung, die Sie hier anfordern, sortiert die Kommissionierzeilen, die Sie erstellen. Sie können z. B. eine Kommissionierung für jede Zone erstellen und die Zeilen innerhalb jeder Kommissionierung nach der Lagerplatzpriorität sortieren.  
5. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerkommissionierungen** ein, und wählen Sie dann den entsprechenden Link aus. Die Seite **Lagerkommissionierungen** wird geöffnet.  
6. Die soeben erstellte Kommissionierung finden Sie durch Auswählen der Kommissionierung mit der höchsten Nummer.  
7. In der Kommissionierung können Sie – falls notwendig – immer noch die zugeordnete Benutzer-ID ändern sowie die Art, auf die die Zeilen sortiert sind.  
8. Wählen Sie die Aktion **Drucken** aus, um die Kommissionierungsanweisungen zu drucken.  
9. Nachdem Sie die Kommissionierung durchgeführt haben, wählen Sie die **Registrieren** Aktion aus.  

Wenn die Lagerplätze auf eine Art sortiert sind, die die physische Struktur des Lagers widerspiegelt, ermöglichen die nach Lagerplatz sortierten Zeilen dem Kommissionierer, mehrere Lieferungen in einer Runde durch das Lager zu kommissionieren. Der Mitarbeiter entnimmt die erforderliche Anzahl von Artikeln für jede Warenausgangszeile aus jedem Lagerplatz und stellt sie mit den anderen Artikeln dieser Lieferung zusammen. Ein Kommissionierer kann viel Zeit sparen, wenn er die Artikel für mehrere Warenausgänge in einem Besuch bei einem Lagerplatz entnimmt.  

Eine weitere effektive Sortieroption ist die Sortierung nach Lagerplatzprioritäten, wenn die physische Struktur des Lagers nach Lagerplatzprioritäten aufgebaut ist, anstatt nach Lagerplätzen.  

Im Kommissioniervorschlag können Sie auch nach Lieferadresse sortieren, so dass Sie z. B. die Möglichkeit haben, die Aufträge an weit entfernte Debitoren zuerst zu kommissionieren.  

## <a name="see-also"></a>Siehe auch

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
