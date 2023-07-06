---
title: Nicht abzugsfähige MwSt. einrichten
description: 'In diesem Artikel wird erläutert, wie Sie die nicht abzugsfähige MwSt. in Microsoft Dynamics 365 Business Central konfigurieren.'
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="set-up-non-deductible-vat"></a>Nicht abzugsfähige MwSt. einrichten

Bei der nicht abzugsfähigen Mehrwertsteuer (MwSt.) handelt es sich um die Mehrwertsteuer, die von einem Käufer zu zahlen ist, aber nicht von seiner eigenen Mehrwertsteuerschuld des Käufers abgezogen werden kann. Unternehmen können in der Regel die MwSt. beim Kauf von Waren und Dienstleistungen im Zusammenhang mit ihrer Geschäftstätigkeit zurückfordern. In manchen Situationen fällt einem Unternehmen jedoch MwSt. an, die nicht abzugsfähig ist. Diese Situationen hängen typischerweise mit den örtlichen Vorschriften zusammen und können sich von Land zu Land unterscheiden. Das Modell der Verwendung der nicht abzugsfähigen oder teilweise abzugsfähigen MwSt. ist jedoch ähnlich. Sie können die anteilige MwSt. verwenden, um die MwSt. zu berechnen, wenn es abzugsfähige und nicht abzugsfähige MwSt. gibt.

Im Allgemeinen kann die MwSt. für einige Käufe aufgrund der folgenden Faktoren nicht abgezogen werden:

- **Die Art der gekauften Waren oder Dienstleistungen**: Die MwSt. ist aufgrund einer gesetzlichen Bestimmung über Waren wie Autos, Mobiltelefone und Lebensmittel, die in Restaurants gekauft werden, ganz oder teilweise nicht abzugsfähig.
- **Teilweise abzugsfähige anteilige MwSt.**: Die MwSt. wird entsprechend dem Verhältnis zwischen den Verkaufsvorgängen, für die die MwSt. geschuldet wird, und allen durchgeführten Vorgängen anteilig berechnet. MwSt., die dieses Verhältnis übersteigt, kann nicht abgezogen werden.

Da es schwierig sein kann, zu wissen, wo und wie ein Artikel verwendet wird, müssen Sie sich an die örtlichen Steuerbehörden in Ihrem Land wenden, um herauszufinden, ob ein bestimmter Prozentsatz der MwSt. auf der Grundlage historischer Daten abzugsfähig ist. 

> [!IMPORTANT]
> Dieses globale Feature ist **außer in Belgien, Italien, Norwegen und Spanien** in allen Ländern mit aktivierter MwSt. verfügbar. Diese Lokalisierungen verfügen bereits über lokale Features und werden in Zukunft aktualisiert. Führen Sie dieses Feature in diesen Ländern nicht aus, da es kein Upgrade-Verfahren gibt.

## <a name="use-non-deductible-vat"></a>Nicht absetzbare MwSt. verwenden

1. Wählen Sie die ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **MwSt.-Einrichtung** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie das Kontrollkästchen **Nicht abzugsfähige MwSt. zulassen**.

    > [!IMPORTANT]
    > Nachdem Sie die nicht abzugsfähige MwSt. aktiviert haben, können Sie sie nicht deaktivieren, da das Feature möglicherweise Änderungen an Daten beinhaltet und möglicherweise ein Upgrade einiger Datenbanktabellen einleitet. Microsoft empfiehlt dringend, dass Sie dieses Feature zuerst in der Sandkastenumgebung aktivieren und testen, bevor Sie es in der Produktionsumgebung aktivieren.

3. Konfigurieren Sie, wie das System mit nicht abzugsfähigen Mehrwertsteuerwerten umgeht.

    1. Geben Sie im Feld **Für Artikelkosten verwenden** an, ob die nicht abzugsfähige MwSt. beim Kauf von Artikeln zu den Artikelkosten hinzugerechnet werden muss. Andernfalls hat die nicht abzugsfähige MwSt. keinen Einfluss auf die Artikelkosten, und der volle Betrag wird nur auf Sachkontoebene erfasst.
    2. Wählen Sie das Kontrollkästchen **Für Anlagenkosten verwenden**, um die nicht abzugsfähige MwSt. zu den Anlagenkosten hinzuzufügen, wenn Sie neue Anlagen kaufen. Andernfalls hat die nicht abzugsfähige MwSt. keinen Einfluss auf die Anlagenkosten, und der volle Betrag wird nur auf Sachkontoebene erfasst.
    3. Wählen Sie das Kontrollkästchen **Für Projektkosten verwenden**, um anzugeben, dass die nicht abzugsfähige MwSt. zu den Projektkosten hinzugefügt werden muss, wenn Sie Artikel für das Projekt kaufen. Andernfalls hat die nicht abzugsfähige MwSt. keinen Einfluss auf die Projektkosten, und der volle Betrag wird nur auf Sachkontoebene erfasst.
    4. Wählen Sie das Kontrollkästchen **Nicht abziehbare MwSt. in Zeilen anzeigen**, um anzugeben, dass die nicht abzugsfähige MwSt. auf Belegzeilenseiten angezeigt werden muss, um die MwSt.-Beträge einfacher bearbeiten zu können.

## <a name="use-the-non-deductible-vat-percentage"></a>Den nicht abzugsfähigen MwSt.-Prozentsatz verwenden

1. Wählen Sie die ![Glühbirne, welche die 3. „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **MwSt.-Buchungseinrichtung** ein und wählen Sie dann den entsprechenden Link aus.
2. Füllen Sie auf der Seite **MwSt.-Buchungsmatrix** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.

    | Feld | Description |
    |-------|-------------|
    | Nicht abziehbare MwSt. zulassen | Geben Sie an, ob der Betrag für die nicht abzugsfähige MwSt. für die aktuelle Kombination einer MwSt.-Geschäftsbuchungsgruppe und einer MwSt.-Produktbuchungsgruppe berücksichtigt wird. |
    | Nicht abziehbare MwSt. % | Geben Sie den Prozentsatz des Betrages der Transaktion an, auf den die MwSt. nicht angewandt wird. |
    | Nicht abziehbare MwSt. Konto Einkauf | Geben Sie das Konto an, das mit dem MwSt.-Betrag verknüpft ist, der aufgrund der Art der gekauften Waren oder Dienstleistungen nicht abgezogen wird. |

    > [!NOTE]
    > Um Sachkontoeinträge zu haben, die das dedizierte Konto anstelle des Verkaufs-/Einkaufskontos verwenden, können Sie entweder das Feld **Konto für nicht abzugsfähige Vorsteuer** leer lassen oder das Feld **Sachkonto** festlegen.

3. Wählen Sie **OK** aus.

> [!NOTE]
> Sie können die nicht realisierte MwSt. nicht zusammen mit der nicht abzugsfähigen MwSt. verwenden.
>
> Verwenden Sie nicht dasselbe **MwSt.-Kennzeichen** für beide normale MwSt., wo das Feld **Nicht abzugsfähige MwSt. %** auf **0** (Null) eingestellt ist, und die normale MwSt., wenn das Feld **Nicht abzugsfähige MwSt. %** auf einen anderen Wert als Null eingestellt ist. Andernfalls wird der gesamte nicht abzugsfähige MwSt.-Betrag falsch berechnet.

## <a name="see-also"></a>Siehe auch

[Finanzmanagement](finance.md)  
[Berechnungen und Buchungsmethoden für die Mehrwertsteuer festlegen](finance-setup-vat.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
