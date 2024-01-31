---
title: Übertragung und Buchung von Kostenzuteilungen
description: 'Bevor Sie Kalkulationen definieren, müssen Sie die verschiedenen Quellen verstehen, aus denen Kosteneinträge stammen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '1100, 1103, 1104, 1108, 1113, 1135'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Übertragen und Buchen von Kalkulationen

Bevor Sie Kostenzuteilungen definieren, müssen Sie verstehen, wie Kostenposten aus den folgenden Quellen stammen:  

- Automatischer Transfer von Sachposten.  
- Manuelle Kostenbuchung für reine Kostenposten, inländische Abgaben und manuelle Zuweisungen.  
- Automatische Verteilungsbuchungen für tatsächliche Kosten.  
- Übertragung von Budgetposten zu tatsächlichen Posten.

## Kriterien für die Übertragung von Sachposten in Kostenposten

Es ist wichtig, die Kriterien für den Transfer von Sachposten in Kostenposten zu kennen. Während des Transfers verwendet der Batchauftrag **Sachposten in Kostenrechnung übertragen** die folgenden Kriterien, um zu ermitteln, ob und wie die Sachposten transferiert werden sollen.  

Sachposten werden transferiert, wenn Folgendes zutrifft:  

- Die Posten haben Dimensionswerte, die entweder einer Kostenstelle oder einem Kostenträger entsprechen.  
- Die Posten haben Dimensionswerte, die einer Kostenstelle und einem Kostenträger entsprechen. Bei diesen Posten hat die Kostenstelle Vorrang. Dies ist hilfreich, um eine Situation zu vermeiden, in der eine Kostenart sowohl in einem Kostenträger als auch in einer Kostenstelle auftritt und daher in der Statistik zweimal gezählt wird.  
- Die Belegnummer in den Posten ist leer, sodass sie mit einer Belegnummer von 0000 in den Kostenposten angezeigt wird.  
- Die Posten werden in eine Kostenart transferiert, die kombinierte Posten zulässt, und diese Posten werden als kombinierter monatlicher oder täglicher Posten transferiert.  

Sachposten werden nicht transferiert, wenn Folgendes zutrifft:  

- Die Posten haben Dimensionswerte, die weder einer Kostenstelle noch einem Kostenträger entsprechen.  
- Die Posten weisen einen Betrag von Null auf.  
- Die Posten haben ein Sachkonto, das gelöscht wurde.  
- Die Posten haben ein Sachkonto, das nicht vom Typ **GuV** ist.  
- Die Posten haben ein Sachkonto, dem keine Kostenart zugeordnet ist.  
- Die Posten haben ein Buchungsdatum vor **Startdatum für Sachkontenübertragung**.  
- Die Posten wurden mit einem Abschlussdatum gebucht. Dies sind typische Posten, die den Saldo der GuV am Ende des Geschäftsjahres zurücksetzen.

## Übertragung von Sachposten in Kostenposten

Sie können Sachposten in Kostenposten übertragen.  

Bevor Sie den Vorgang für das Übertragen von Sachposten in Kostenposten durchführen, müssen Sie die Übertragung vorbereiten, um manuelle Korrekturbuchungen zu vermeiden.  

### So bereiten Sie die Übertragung vor  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kostenrechnungseinrichtung** ein und wählen Sie dann den entsprechenden Link.  
2.  Stellen Sie auf der Seite **Kostenrechnungseinrichtung** sicher, dass im Feld **Startdatum für Sachkontenübertragung** der richtige Wert eingetragen ist.  
3.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kostenartenplan** ein und wählen Sie dann den zugehörigen Link.  
4.  Auf der Seite **Kostenartkarte** prüfen Sie, dass das **Sachkontobereich** Feld für jede Kostenart korrekt verknüpft ist, um Posten aus dem Sachkonto zu übernehmen.  
5.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
6.  Überprüfen Sie für jedes Sachkonto auf der Seite **Sachkontokarte**, ob die **Kostenartnr.** Feld wird korrekt zu einer Kostenart verknüpft. Weitere Informationen finden Sie unter [Einrichten von Kostenrechnung](finance-set-up-cost-accounting.md).  
7.  Vergewissern Sie sich, dass alle entsprechenden Sachposten Dimensionswerte haben, die einer Kostenstelle und zu einem Kostenträger entsprechen.  

### So übertragen Sie Sachposten in Kostenposten

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Sachposten in Kostenrechnung übertragen** ein und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie auf Schaltfläche **OK**, um die Umlagerung zu starten. Der Prozess überträgt alle Sachposten, die nicht bereits übertragen wurden.  

Während der Übertragung erstellt der Vorgang Verknüpfungen in den Posten **Posteneintrag** und **Kostentabelle**. Dies ermöglicht es Ihnen, die Herkunft von Kostenposten nachzuverfolgen.

## Automatische Übertragung und kombinierte Posten

In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden. Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll. Die drei Optionen werden in der folgenden Tabelle beschrieben.  

|Posten kombinieren|Description|  
|---------------------|-----------------|  
|Keine|Jeder Sachposten wird einzeln in die entsprechende Kostenart umgelagert.|  
|Tag|Sachposten mit dem gleichen Buchungsdatum werden wie ein Posten in die entsprechende Kostenart umgelagert.|  
|Monat|Alle Sachposten im selben Kalendermonat werden wie ein Posten in die entsprechende Kostenart umgelagert.|  

> [!IMPORTANT]  
>  Wenn Sie das Kontrollkästchen **Automatischer Übertrag vom Buch-Blatt** auf der Seite **Kostenrechnung einrichten** aktiviert haben, wird [!INCLUDE[prod_short](includes/prod_short.md)] die Kostenrechnung nach jeder Buchung in der Finanzbuchhaltung aktualisiert. Kombinierte Posten sind nicht möglich.

## Kriterien für die Übertragung von Sachposten in Kostenposten

Während der Übertragung der Sachposten zu den Kostenposten erstellt [!INCLUDE[prod_short](includes/prod_short.md)] Verknüpfungen in den Posten in der Tabelle **Sachposten**, der Tabelle **Kostenposten** und der Tabelle **Kostenjournal**, damit es möglich ist, Verbindungen zwischen Kostenposten und Sachposten zu verfolgen.  

### Sachposten

Für jeden Sachposten, der zur Kostenrechnung übertragen wird, füllt [!INCLUDE[prod_short](includes/prod_short.md)] das Kostenfeld **Postennr.** aus.  

### Kostenposten

Für jeden Kostenposten speichert [!INCLUDE[prod_short](includes/prod_short.md)] die Postennummer des entsprechenden Sachpostens im Feld **Sachposten Lfd. Nr.** in der Tabelle **Kostenposten**.  

Für kombinierte Kostenposten speichert [!INCLUDE[prod_short](includes/prod_short.md)] die laufende Nummer des letzten Sachpostens, der dem Posten mit der höchsten laufenden Nummer entspricht.  

Das Feld **Sachkonto** in der Tabelle **Kostenposten** enthält die Nummer des Sachkontos, von dem der Kostenposten stammt.  

Für einzelne Kostenposten überträgt [!INCLUDE[prod_short](includes/prod_short.md)] den Buchungstext aus dem Sachposten in das Textfeld **Beschreibung**. Für kombinierte Posten zeigt das Textfeld, dass diese Posten als kombinierte Posten übertragen werden. Zum Beispiel kann für einen kombinierten Posten für den Monat Oktober 2013 der Text lauten: **Kombinierte Posten, Oktober 2013**.  

### Kostenjournal

In der Tabelle **Kostenregister** erstellt [!INCLUDE[prod_short](includes/prod_short.md)] einen Posten mit der Quellenübertragung aus dem Sachkonto. Der Posten erfasst die erste und letzte Postennummer der übertragenen Sachposten sowie die erste und letzte Nummer der erstellten Kostenposten.

## Siehe auch

 [Informationen zur Kostenrechnung](finance-about-cost-accounting.md)  
 [Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md)  
 [Kosten definieren und zuweisen](finance-define-and-allocate-costs.md)  
 [Kostenrechnung](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
