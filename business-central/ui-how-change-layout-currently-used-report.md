---
title: Ändern Sie das Aussehen eines Berichts durch Auswahl eines anderen Layouts
description: 'Sie können unterschiedliche Layouts für einen Bericht auswählen und zwischen Layouts wechseln, um das Aussehen des Berichts zu ändern.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 03/07/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="legacy-set-the-layout-used-by-a-report"></a>(Legacy) Die von einem Bericht verwendeten Layouts festlegen

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Ein Bericht kann mit mehreren Berichtlayouts eingerichtet werden, die bei Bedarf ausgewechselt werden können.

Abhängig von den Layouts, die für einen Bericht verfügbar sind, können Sie ein integriertes RDLC-Berichtlayout, ein integriertes Word-Berichtlayout oder ein Debitorenspezifisches Layout verwenden. Weitere Informationen zu RDLC- und Word-Berichtlayouts, integrierten und benutzerdefinierten Layouts und mehr finden Sie unter [Verwalten von Berichtslayouts](ui-manage-report-layouts.md).

Wenn benutzerdefinierte Berichtslayouts definiert sind, können Sie diese aus Debitoren- und Kreditorenkarten auswählen, um anzugeben, dass die ausgewählten Layouts für Belege verwendet werden, die Sie für den betreffenden Debitoren oder Kreditoren erstellen. Weitere Informationen finden Sie unter [Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Belegberichte (keine Listen), die ein Word-Berichtslayout verwenden, sind normalerweise schneller als diejenigen, die ein RDLC-Berichtslayout verwenden. Wenn Sie also die Möglichkeit haben, zwischen einem Word- oder einem RDLC-Berichtslayout für einen Belegbericht zu wählen, verwenden Sie das Word-Berichtslayout für optimale Leistung.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>So ändern Sie das für einen Bericht oder einen Beleg zu verwendende Berichtslayout

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Auswahl des Berichtslayouts** ein und wählen Sie dann den entsprechenden Link.
  
   Auf der Seite **Berichtslayoutauswahl** sind alle Berichte aufgelistet, die für das Unternehmen verfügbar sind, das im Feld **Unternehmen** obern auf der Seite angegeben ist. Die **Beschreibung des Layouts** <!-- **Selected Layout** -->Feld gibt das Layout an, das im Bericht derzeit verwendet wird.
2. Legen Sie das Feld **Unternehmen** oben auf das Unternehmen fest, das den Bericht umfasst.

   In diesem Feld können Sie unterschiedliche Layouts für denselben Bericht in verschiedenen Unternehmen festlegen.

3. Um das Layout, das von einem Bericht verwendet wird, zu ändern, legen Sie in der Zeile für den Bericht das Feld **Ausgewähltes Layout** auf eine der folgenden Optionen fest:
   * **RDLC (integriert)** verwendet im Bericht das integrierte RDLC-Berichtslayout.
   * **Word (integriert)** verwendet im Bericht das integrierte Word-Berichtslayout.
   * **Benutzerdefiniert**, verwendet ein benutzerdefiniertes Layout im Bericht.  

> [!NOTE]
> Wenn Sie ein Berichtslayout der Art **RDLC (integriert)** oder **Word (integriert)** auswählen und Sie eine Fehlermeldung erhalten, dass der Bericht kein Layout der angegebenen Art hat, müssen Sie eine andere Layoutoption auswählen oder ein benutzerdefiniertes Berichtlayout der Art erstellen, die Sie verwenden möchten. Siehe das folgende Verfahren.

Wenn Sie ein integriertes RDLC- oder Word-Berichtslayout ausgewählt haben, ist keine weitere Aktionen erforderlich, und das Layout wird verwendet, wenn der Bericht zum nächsten Mal ausgeführt wird.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>So ändern Sie das benutzerdefinierte Layout, das für ein Berichtslayout verwendet werden soll

Möglicherweise möchten Sie auch das aktuell verwendete benutzerdefinierte Layout ändern. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

Alle benutzerdefinierten Berichtslayouts, die für Berichtslayouts in einem Unternehmen vorhanden sind, werden auf der Seite **Benutzerdefinierte Berichtslayouts** aufgeführt. Auf der Seite **Berichtslayoutauswahl** können Sie sehen, welche benutzerdefinierten Layouts für jeden Bericht in der Infobox **Benutzerdefinierte Layouts** verfügbar sind.

1. Auf der Seite **Berichtslayoutauswahl** in der Zeile für das Berichtslayout, das Sie ändern möchten, wählen Sie die Suchschaltfläche im Feld **Benutzerdefinierte Layoutbeschreibung** aus.
2. Auf der Seite **Benutzerdefinierte Berichtslayouts** wählen Sie die Zeile für das benutzerdefinierte Layout aus, das Sie verwenden möchten, und wählen Sie dann die Schaltfläche **OK** aus.

Der Name des ausgewählten benutzerdefinierten Layouts wird jetzt im Feld **Benutzerdefinierte Layoutbeschreibung** angezeigt und wird das nächste Mal verwendet, wenn der Bericht oder der Beleg in der Vorschau angezeigt, gedruckt oder gesendet wird.

Sie können jetzt zu Ihren Debitoren- und Kreditorenkarten wechseln, um anzugeben, welche der Layouts für verschiedene Belege verwendet werden sollen, die Sie für den betreffenden Debitor oder Kreditor erstellen, wie z. B. Auftragsbestätigungen oder Zahlungserinnerungen. Weitere Informationen finden Sie unter [Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md).

## <a name="see-also"></a>Siehe auch
[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
