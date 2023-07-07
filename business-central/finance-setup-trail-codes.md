---
title: Codes für Audit-Trails festlegen
description: 'Erfahren Sie mehr über die Aufgaben zum Einrichten von Herkunftscodes und Ursachencodes ein, mit denen Sie Audit-Trails verfolgen können.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Herkunftscodes und Ursachencodes für Audit Trails einrichten

Allen gebuchten Posten werden automatisch einem Herkunftscode zugewiesen, sodass Transaktionen bis zu ihrem Ursprung nachverfolgt werden können. Wenn Sie Posten einen zusätzlichen Herkunftscode zuordnen möchten, können Sie Ursachencodes verwenden. Ursachencodes werden verwendet, um den Grund für eine Buchung anzugeben. Ursachencodes können gesamten Buch.-Blattvorlagen und Buch.-Blattnamen oder auch einzelnen Buch.-Blattzeilen und Belegen zugeordnet werden.  

Verwenden Sie als Herkunfstcodes und Ursachencodes aussagekräftige Codes, an die Sie sich leicht erinnern können. Der Code muss eindeutig sein, und Sie können beliebig viele Codes einrichten.

## <a name="define-source-codes"></a>Herkunftscodes definieren

Gelegentlich möchten Sie nachvollziehen, wie ein bestimmter Posten entstanden ist, ob er z. B. beim Buchen eines Buch.-Blattes oder einer Einkaufsrechnung erzeugt wurde. Ein Herkunftscode gibt an, wo ein Posten erstellt wurde. Posten werden erstellt, wenn Buch.-Blätter und Rechnungen gebucht und bestimmte Stapelverarbeitungen ausgeführt werden. Jede Buchungsart hat einen bestimmten Herkunftscode, der zugewiesen wird, wenn Posten erstellt werden.  

Beim Buchen von Buch.-Blättern, Aufträgen, Rechnungen oder Gutschriften sowie beim Ausführen bestimmter Stapelverarbeitungen werden Posten in der Finanzaufstellungen erstellt. Die Seite **Herkunftscode Einrichtung** enthält für jeden Anwendungsbereich mehrere Inforegister. Jedes Inforegister enthält die Herkunftscodes, die für diesen Anwendungsbereich anwendbar sind.

Beim Buchen oder Ausführen einer Stapelverarbeitung wird dem Posten automatisch der richtige Herkunftscode zugeordnet. Wenn Sie z. B. von einem Fibu Buch.-Blatt aus buchen, erhält der Posten den Code *FIBUBUCHBL*. Sie können dann die Seite **Sachposten** filtern, um anzuzeigen, welche Einträge beispielsweise aus dem Fibu Buch.-Blatt oder aus Verkaufsbelegen gebucht wurden.

### <a name="to-define-source-codes"></a>So definieren Sie Herkunftscodes

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Nach dem Symbol für „Seite“ oder „Bericht“ suchen") Symbol. Geben Sie **Herkunftscode Einrichtung** ein, und wählen Sie dann den entsprechenden Link.  

2. Geben Sie im Fenster **Herkunftscode Einrichtung** für jede Buchungsart und jede Stapelverarbeitung den entsprechenden Herkunftscode ein.  

Sie können den Inhalt eines Felds später ändern. Diese Änderung wirkt sich dann auf zukünftige Buchungen aus.

## <a name="change-source-codes"></a>Herkunftscodes ändern

Sie können einen Herkunftscode ändern. Sie können den Herkunftscode *FIBUBUCHBL* beispielsweise in *FIBUBL* ändern.

### <a name="to-change-source-codes"></a>So ändern Sie Herkunftscodes

1. Wählen Sie die ![Suche nach Seite oder Bericht.](media/ui-search/search_small.png "Nach dem Symbol für „Seite“ oder „Bericht“ suchen") Symbol. Geben Sie **Herkunftscodes** ein und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Zeile mit dem zu ändernden den Code im Feld **Code** aus.

3. Geben Sie den neuen Code ein, und klicken Sie dann auf die Schaltfläche **Ja**. Sie können auch den Inhalt des Feldes **Beschreibung** ändern.

Alle neuen Posten, die über das Fibu Buch.-Blatt gebucht werden, weisen den neuen Herkunftscode auf.

## <a name="define-reason-codes"></a>Ursachencodes definieren

Ursachencodes ergänzen die Herkunftcodes und geben an, warum ein Eintrag erstellt wurde. Sie können Ursachencodes für einzelne Posten und permanente Codes bestimmten Buch.-Blattvorlagen und Buch.-Blattnamen zuweisen. Wenn ein Ursachencodes mit einer Buch.-Blattzeile bzw. einem Einkaufs- oder Verkaufskopf verknüpft ist, werden beim Buchen alle Posten mit dem entsprechenden Ursachencode markiert.  

### <a name="to-set-up-reason-codes"></a>So richten Sie Ursachencodes ein

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“")  Symbol. Geben Sie **Ursachencodes** ein und wählen Sie dann den zugehörigen Link.

2. Geben Sie im Fenster **Ursachencodes** den ersten Code im Feld **Code** ein. Geben Sie im Feld **Beschreibung** einen erklärenden Text ein.

Wiederholen Sie den Ablauf für jeden Code, den Sie verwenden möchten. Sie können eine beliebige Anzahl von Codes einrichten.

Nachfolgend wird beschrieben, wie Sie einer Buch.-Blattvorlage einen Ursachencodes hinzufügen. Ähnliche Schritte gelten jedoch für das Hinzufügen eines Ursachencodes zu einer Buch.-Blattzeile oder einer Stapelverarbeitung.  

### <a name="to-assign-reason-codes-to-journal-templates"></a>So weisen Sie Buch.-Blattvorlagen Ursachencodes zu

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“")  Symbol. Geben Sie **Allgemeine Fibu Buch.-Blattvorlagen** ein, und wählen Sie dann den zugehörigen Link.

2. Geben Sie in der Zeile mit der ausgewählten Buch.-Blattvorlage den entsprechenden Code in das Feld **Ursachencode** ein.

3. Schließen Sie die Buch.-Blattvorlage.

Der ausgewählte Ursachencode wird in neue Buch.-Blätter eingefügt, die unter dieser Buch.-Blattvorlage erstellt werden. In anderen Anwendungsbereichen weisen Sie auf dieselbe Art und Weise Buch.-Blattvorlagen Ursachencodes zu.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>So verwenden Sie Ursachencodes in Verkaufs- und Einkaufsbelegen

1. Öffnen Sie den gewünschten Verkaufs- oder Einkaufsbeleg.

2. Geben Sie im Einkaufskopf im Feld **Ursachencode** den Code ein.

Wenn die Rechnung gebucht wird, wird der Ursachencode in jeden Sach-, Debitor- und Kreditorposten kopiert. Sie können einzelnen Einkaufs- oder Verkaufszeilen nicht unterschiedliche Ursachencodes zuordnen, da alle Zeilen als ein Posten gebucht werden.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)  
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
