---
title: Standardmäßige wiederkehrende Einkaufszeilen
description: 'Legen Sie häufig verwendete Kaufzeilen fest, um sie in Kaufbelege einzufügen und die Zeilen schnell mit Standardinformationen zu füllen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="create-recurring-purchase-lines"></a>Wiederkehrende Einkaufspositionen erstellen

Wenn Sie häufiger Einkaufszeilen mit ähnlichen Daten erstellen müssen, können Sie die Standardzeilen einrichten, die Sie in wiederkehrenden Einkaufsbelegen, z. B. für wiederkehrende Ersatzaufträge benötigen.

## <a name="set-up-recurring-purchase-lines"></a>Wiederkehrende Einkaufszeilen einrichten

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Wiederkehrende Einkaufszeilen** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie auf der Seite **Wiederkehrende Einkaufszeilen** die Aktion **Neu** aus.
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Geben Sie im Inforegister **Zeilen** die Informationen in die Felder ein, die die Standardzeilen widerspiegeln, die Sie als wiederkehrende Zeilen auf Einkaufsbelegen verwenden möchten.

> [!NOTE]
> Sie können keine Preise für wiederkehrende Einkaufszeilen definieren, da Preise, Rabatte usw. auf den tatsächlichen Einkaufsbelegen berechnet werden, nachdem Sie die wiederkehrenden Einkaufszeilen eingefügt haben.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-purchase-lines-to-a-vendor"></a>Einem Kreditor wiederkehrende Einkaufszeilen zuweisen

Weisen Sie einem Debitor wiederkehrende Einkaufszeilen zu, sodass sie zum Einfügen in Verkaufsbelege von diesem Debitor zur Verfügung stehen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kreditoren** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte für einen entsprechendes Kreditor.
3. Wählen Sie die Aktion **Wiederkehrende Einkaufszeilen** aus.
4. Wählen Sie auf der Seite **Wiederkehrende Einkaufszeilen** Codes für die wiederkehrende Einkaufszeilen aus, die Sie auf den Einkaufsbelegen für den Kreditor einfügen können möchten.
5. Füllen Sie die anderen Felder aus, um festzulegen, wann, wie und wo die wiederkehrenden Einkaufszeilen verwendet werden sollen.
6. In den vier Feldern, in denen Sie angeben, wie die Zeilen auf jedem Belegtyp eingefügt werden, wählen Sie eine der folgenden Optionen aus:

|Option|Description|
|------|-----------|
|**Manuell**|Sie müssen eine wiederkehrende Einkaufszeile, die bereits für den Kreditor vorhanden ist, manuell suchen.|
|**Automatisch**|Wenn mehrere wiederkehrende Einkaufszeilen für den Kreditor vorhanden sind, erhalten Sie eine Benachrichtigung, in der Sie auswählen können, welche eingefügt werden soll. Wenn nur eine wiederkehrende Einkaufszeile vorhanden ist, wird sie automatisch eingefügt.<br /><br />Dies funktioniert nur, wenn der neue Beleg über eine Belegliste erstellt wurde, z. B. durch Auswahl der Aktion **Neu** auf der Seite **Bestellungen**. Dies funktioniert nicht, wenn der Beleg beispielsweise über eine Kreditorenkarte erstellt wurde.|
|**Immer bestätigen**|Eine Benachrichtigung erscheint und alle vorhandenen wiederkehrenden Einkaufszeilen werden angezeigt, sodass Sie eine auswählen können.

## <a name="insert-recurring-purchase-lines-on-a-purchase-invoice"></a>Wiederkehrende Einkaufszeilen in eine Einkaufsrechnung einfügen

Wenn für den Kreditor wiederkehrende Einkaufszeilen vorhanden sind, können Sie diese in alle Arten von Einkaufsbelegen einfügen, z. B. in eine Einkaufsrechnung. Wenn Sie die Option **Immer fragen** aktiviert haben, während Sie Kreditoren wiederkehrende Einkaufszeilen hinzufügen, werden Sie informiert, wenn wiederkehrende Einkaufszeilen vorhanden sind.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Einkaufsrechnung, in die Sie eine oder mehrere Standardeinkaufszeilen einfügen möchten.
3. Wählen Sie die **Wiederkehrende Einkaufszeilen abrufen** Aktion aus.
4. Wählen Sie auf der Seite **Wiederkehrende Einkaufszeilen** die Suchschaltfläche im Feld **Code** und dann eine Reihe von Standardeinkaufszeilen aus.
5. Wählen Sie die Schaltfläche **OK**, um die Standardeinkaufszeilen in die Rechnung einzufügen, in die Sie Informationen verwenden ist beim oder bearbeiten können.

## <a name="see-also"></a>Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Einkäufe einrichten](purchasing-setup-purchasing.md)  
[Wiederkehrende Verkaufsrechn. erstellen](sales-how-work-standard-lines.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
