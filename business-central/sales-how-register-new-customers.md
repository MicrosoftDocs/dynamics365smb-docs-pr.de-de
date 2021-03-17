---
title: Neue Debitoren durch Erstellen einer Debitorenkarte registrieren
description: Beschreibt, wie eine Debitorenkarte erstellt wird, um Informationen zu jedem neuen Debitor oder Clients zu erfassen, an die Sie verkaufen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: d873c1546cebfccc6d2549b1de2b9d111589c553
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573426"
---
# <a name="register-new-customers"></a>Neue Debitoren registrieren

Debitoren sind die Herkunft Ihres Einkommens. Sie müssen jeden Debitor, an den Sie verkaufen, als Debitorenkarte anlegen. Debitorenkarten enthalten die Informationen, die für den Verkauf von Produkten an Debitoren erforderlich sind." Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md) und [Neue Artikel registrieren](inventory-how-register-new-items.md).  

Bevor Sie neue Debitoren erfassen können, müssen Sie verschiedene Verkaufscodes einrichten, aus denen Sie auswählen können, wenn Sie Debitorenkarten ausfüllen. Weitere Informationen finden Sie unter [Einrichten von Verkäufen](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Hinzufügen neuer Kunden

Sie müssen eine Debitorenkarte ausfüllen, um einen neuen Debitoren zu registrieren. Sie können Vorlagen für verschiedene Debitorenprofile erstellen oder Debitoren ohne Vorlagen hinzufügen.  

> [!NOTE]  
> Wenn es Debitorenvorlagen für verschiedene Debitorenarten gibt, dann erscheint eine Seite automatisch, wenn Sie eine neue Debitorenkarte erstellen, von der aus Sie eine entsprechende Debitorenvorlage auswählen können. Wenn nur eine Debitorenvorlage vorhanden ist, verwenden neue Debitorenkarten immer diese Vorlage.  

### <a name="to-create-a-new-customer-card"></a>Erstellen Sie eine neue Debitorenkarte

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Debitoren** die Aktion **Neu** aus.

    Wenn nur eine Debitorenvorlage vorhanden ist, dann öffnet sich eine neue Debitorenkarte mit den Feldern, die mit Daten aus der Vorlage ausgefüllt werden.

    Wenn mehr als eine Debitorenvorlage vorhanden ist, dann öffnet sich eine Seite mit verfügbaren Debitorenvorlagen automatisch. In diesem Fall, folgen Sie den nächsten zwei Schritten.
3. Auf der Seite **Eine Vorlage für einen neuen Debitor auswählen** wählen Sie die Vorlage, die Sie für die neue Debitorenkarte verwenden möchten.
4. Wählen Sie die Schaltfläche **OK** aus. Eine neue Debitorenkarte wird geöffnet mit den Feldern, die mit Daten aus der Vorlage ausgefüllt werden.  
5. Fahren Sie fort, um Felder auf der Debitorenkarte bei Bedarf auszufüllen und zu ändern. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Definieren Sie im Inforegister **Verkaufspreise** spezielle Preise oder Rabatte, die Sie dem Debitor gewähren, wenn bestimmte Kriterien, wie z.B. Artikel, Mindestbestellmenge oder Enddatum erfüllt sind. Jede Zeile stellt einen Sonderpreis oder einen Zeilenrabatt dar. Jede Spalte stellt ein Kriterium an, das gelten muss, um den Sonderpreis, den Sie im **VK-Preis**-Feld eingeben, oder den Zeilenrabatt, den Sie im **Zeilenrabatt**-Feld eingeben, zu rechtfertigen. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Rabatt und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)

Der Debitor ist nun erfasst und die Debitorenkarte ist bereit, in Geschäftsbelegen verwendet zu werden, in denen Sie mit dem Debitor handeln.

Wenn Sie diese Debitorenkarte als Vorlage verwenden möchten, fahren Sie fort, um sie als Debitorenvorlage zu speichern. Weitere Informationen finden Sie im folgenden Abschnitt.  

### <a name="to-save-the-customer-card-as-a-template"></a>Um die Debitorenkarte als Vorlage zu speichern

1. Wählen Sie auf der Seite **Debitorenkarte** die Aktion **Als Vorlage speichern** aus. Die Seite **Debitorenvorlage** wird geöffnet und zeigt die Debitorenkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Die Seite **Dimensionen Vorlagen** wird geöffnet und zeigt alle Dimensionscodes, die für den Debitor eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Debitorenkarten gelten, die mit der Vorlage erstellt wurden.  
5. Wenn Sie die neue Debitorenvorlage abgeschlossen haben, wählen Sie die Schaltfläche **OK**.

Die Debitorenvorlage wird der Liste von Debitorenvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Debitorenkarten zu erstellen.

## <a name="deleting-customer-cards"></a>Löschen von Debitorenkarten

Wenn Sie eine Transaktion für einen Debitor gebucht haben, können Sie die Karte nicht löschen, da die Posten möglicherweise für die Prüfung erforderlich sind. Um Debitorenkarten mit Posten zu löschen, wenden Sie sich an Ihren Microsoft-Partner, um dies über einen Code durchzuführen.  

## <a name="managing-credit-limits"></a>Kreditlimits verwalten

Kreditlimits, Restbeträge und Zahlungsbedingungen ermöglichen [!INCLUDE [prod_short](includes/prod_short.md)] die Anwendung eine Kreditlimitwarnung oder eine Warnung bei einem überfälligen Saldo anzeigt, wenn Sie einen Verkaufsauftrag anlegen.  Außerdem ermöglichen Ihnen die Funktionen für Mahnungs- und Zinskonditionen die Fakturierung von Zinsen und/oder Gebühren.  

Das Feld **Kreditlimit** auf einer Debitorenkarte gibt den Höchstbetrag an, mit dem der Kunde den Zahlungssaldo überschreiten darf, bevor Warnungen ausgegeben werden. Wenn Sie dann Informationen in Journale, Angebote, Bestellungen und Rechnungen eingeben, testet [!INCLUDE [prod_short](includes/prod_short.md)] den Verkaufskopf und die einzelnen Verkaufszeilen, um festzustellen, ob das Kreditlimit überschritten wurde.

Sie können jedoch weiterhin Buchungen vornehmen, auch wenn das Kreditlimit überschritten wird. Wenn Sie das Feld leer lassen, verfügt der Debitor über ein unbegrenztes Kreditlimit.  

Sie können festlegen, dass keine Warnungen angezeigt werden, die darauf hinweisen, dass das Kreditlimit des Kunden überschritten wurde, und Sie können angeben, welche Arten von Warnungen angezeigt werden sollen.

### <a name="to-specify-credit-limit-warnings"></a>So legen Sie Kreditlimitwarnungen fest

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Einrichten von Verkauf und Forderungen** ein, und wählen Sie dann den zugehörigen Link aus.

2. Wählen Sie im Inforegister **Allgemein** im Feld **Kreditlimitwarnung** die entsprechende Option aus, wie in der folgenden Tabelle beschrieben:

    |Option| Beschreibung|
    |------|------------|
    |**Beide Warnungen**| Die Felder **Kreditlimit** und **Fälliger Saldo** auf der Debitorenkarte werden überprüft, und eine Warnung wird ausgegeben, falls der Debitor sein Kreditlimit überschritten hat oder sich im Zahlungsrückstand befindet.|
    |**Kreditlimit**|Der Wert im Feld **Kreditlimit** der Debitorenkarte wird mit dem Saldo des Debitors verglichen, und eine Warnung wird angezeigt, falls der Saldo des Debitors diesen Betrag übersteigt.|
    |**Fälliger Saldo**|Das Feld **Fälliger Saldo** auf der Debitorenkarte wird geprüft, und eine Warnung wird angezeigt, wenn sich der Debitor im Zahlungsrückstand befindet.|
    |**Keine Warnung**|Keine Warnungen werden über den Status des Debitors angezeigt.|

## <a name="see-also"></a>Siehe auch

[Zahlungsformen definieren](finance-payment-methods.md)  
[Doppelt Datensätze zusammenführen](sales-how-merge-duplicate-records.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]