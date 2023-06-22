---
title: Standarddrucker festlegen
description: 'Erfahren Sie, welche verschiedenen Möglichkeiten es gibt, Drucker einzurichten, die standardmäßig für Druckaufträge verwendet werden.'
author: jswymer
ms.topic: how-to
ms.reviewer: na
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="a-namedefaultaspecify-a-default-printer" /><a name="default"></a>Standarddrucker festlegen

Nachdem Drucker in Business Central eingerichtet wurden, können Sie festlegen, welchen Drucker Sie standardmäßig verwenden möchten. Es gibt verschiedene Möglichkeiten, Drucker als Standarddrucker für Berichte und andere Druckaufträge festzulegen. Ein Standarddrucker ist nützlich, wenn Sie mit verschiedenen Berichten arbeiten, die aufgrund ihrer Platzierung in der Firma oder ihrer Ausgabemöglichkeiten unterschiedliche Drucker erfordern.

> [!IMPORTANT]
> Die einzigen Drucker, die Sie als Standarddrucker angeben können, sind **Microsoft-Druckausgabe in PDF** und Clouddrucker, die bereits für die Verwendung in Business Central eingerichtet wurden, wie E-Mail-Drucker und Drucker für universelles Drucken. Clouddrucker werden normalerweise von einem Administrator eingerichtet. Weitere Informationen finden Sie unter [Druckereinrichtung und -verwaltung](admin-printer-setup-overview.md).   

## <a name="set-a-printer-as-a-default-printer-for-all-print-jobs" />Einen Drucker als Standarddrucker für alle Druckaufträge festlegen

Auf der Seite **Druckerverwaltung** können Sie einen Drucker als Standarddrucker für alle Druckaufträge einrichten. Sie können den Drucker nur für Sie oder für alle Benutzer als Standard festlegen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Druckerverwaltung** ein, und wählen Sie dann den entsprechenden Link.

    > [!TIP]
    > Sie können auch die Seite **Druckerverwaltung** von der Seite **Druckerauswahl** durch Auswahl von **Druckerverwaltung** öffnen.  
2. Wählen Sie auf der Seite **Druckerverwaltung** einen Drucker aus der Liste, dann **Verwalten** und dann **Als Standarddrucker festlegen** oder **Als Standarddrucker für alle Benutzer festlegen** aus.

> [!NOTE]
> Das Festlegen eines Standarddruckers über die **Druckerverwaltung** fügt einen Eintrag in die **Druckerauswahl** hinzu.

## <a name="set-a-default-printer-for-specific-reports" />Den Standarddrucker für bestimmte Berichte festlegen

Auf der Seite **Druckerauswahl** können Sie den Drucker angeben, den ein Bericht standardmäßig verwendet. Standarddrucker werden auf Benutzerkontenbasis festgelegt. Sie können einen Standarddrucker nur für sich selbst, einen anderen Benutzer oder alle Benutzer festlegen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Druckerauswahlen** ein und wählen Sie dann den zugehörigen Link. Alternativ können Sie auf der Seite **Druckerverwaltung** einen Drucker auswählen und dann die Aktion **Druckerauswahl** wählen.
2. Wählen Sie die Aktion **Neu**, um eine Druckerauswahl für einen bestimmten Bericht hinzuzufügen.
3. Füllen Sie die Felder nach Bedarf aus.

Der angegebene Bericht ist jetzt so eingerichtet, dass er standardmäßig auf dem ausgewählten Drucker gedruckt wird.

> [!NOTE]
> Wenn Sie den betreffenden Bericht drucken, können Sie mit dem Feld **Drucken** auf der Berichtsanforderungsseite einen anderen auswählen.

> [!NOTE]
> Wenn Sie auf der Seite **Druckerauswahl** keinen Bericht für einen bestimmten Drucker einrichten, wird er auf dem Standarddrucker der Firma gedruckt, wie er auf der Seite **Druckerverwaltung** definiert ist.

Sie oder der Administrator können auch die Seite **Druckerauswahl** verwenden, um andere Varianten des Druckens für Benutzer und Berichte zu definieren. Die folgende Tabelle beschreibt die Kombination von Werten zur Angabe verschiedener Druckeinstellungensetups für einen Bericht.

|Bis                                                 |Stellen Sie die folgenden Werte ein                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Einen Bericht für alle Benutzer auf einem bestimmten Drucker ausdrucken |Geben Sie Werte in den Feldern **Berichts-ID** und **Druckername** an und lassen Sie das Feld **Benutzer-ID** leer.|
|Drucken aller Berichte auf einem bestimmten Drucker für einen bestimmten Benutzer|Geben Sie Werte in die Felder **Benutzer-ID** und **Druckername** ein und lassen Sie das Feld **Berichts-ID** leer. Dieser Eintrag macht dasselbe wie die Aktion **Als mein Standarddrucker festlegen** auf der Seite **Druckverwaltung**.|
|Den Standarddrucker für alle Benutzer festlegen|Geben Sie einen Wert in das Feld **Druckername** ein und lassen Sie die Felder **Benutzer-ID** und **Berichts-ID** leer. Dieser Eintrag macht dasselbe wie die Aktion **Als Standarddrucker für alle Benutzer festlegen** auf der Seite **Druckverwaltung**.|
|Drucken eines bestimmten Berichts auf dem Standarddrucker des Benutzers|Geben Sie einen Wert in das Feld **Berichts-ID** ein und lassen Sie die Felder **Druckername** und **Benutzer-ID** leer.|
|Drucken eines bestimmten Berichts auf einem bestimmten Drucker für einen bestimmten Benutzer|Geben Sie Werte in allen drei Feldern an.|

> [!NOTE]
> Spezifischere Druckerauswahlen haben Vorrang vor einer allgemeineren Druckerauswahl. Zum Beispiel hat eine Druckerauswahl, die Werte in den Feldern **Benutzer-ID**, **Berichts-ID** und **Druckername** hat, Vorrang vor einer Druckerauswahl, die leere Einträge in den Feldern **Benutzer-ID** oder **Berichts-ID** hat.

## <a name="choosing-the-printer-when-running-a-report" />Auswählen des Druckers beim Ausführen eines Berichts

Anstatt den Standarddrucker zu verwenden, wenn Sie einen Bericht ausführen, können Sie diese Einstellung auf der Anforderungsseite außer Kraft setzen. Wählen Sie einfach im Dropdown-Menü **Drucker** den Drucker aus, den Sie für diese Berichtsgenerierung verwenden möchten.

## <a name="sizing-print-jobs" />Größe von Druckaufträgen anpassen

Das Drucken in der Cloud ist für Dokumente mit einer angemessenen Größe vorgesehen. Die meisten Clouddienste, einschließlich PrintNode und HP ePrint, sind auf 10 MB pro Auftrag begrenzt. Wenn Sie größere Berichte drucken müssen, müssen Sie diese möglicherweise in mehrere Ausdrucke aufteilen.

[Microsoft-Schulung](/training/modules/change-documents-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Druckerverwaltung](admin-printer-setup-overview.md)  
[Drucker für Universal Print einrichten](admin-printer-setup-universal-print.md)  
[E-Mail-Drucker einrichten](admin-printer-setup-email.md)  
[Berichte drucken](ui-work-report.md#PrintReport)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ausführen von Stapelverarbeitungen](ui-how-run-batch-jobs.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
