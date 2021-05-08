---
title: Zahlungsbedingungen einrichten
description: Verwenden Sie in der Basisversion von Business Central Zahlungsbedingungen, um Fälligkeitstermine und Zahlungsrabatte zu verwalten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 82c60333f038f647fa4c9c2bbd68019b9c1f8026
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783797"
---
# <a name="set-up-payment-terms"></a>Zahlungsbedingungen einrichten

Die Zahlungsbedingungen bestimmen, wie Sie Fälligkeitstermine und Zahlungsrabatte verwalten. Sie können eine beliebige Anzahl von Zahlungsbedingungscodes einrichten. Hierbei können Sie Datumsformeln verwenden, um die Zahlungsbedingungen zu definieren. Wenn Sie sich zum ersten Mal anmelden für [!INCLUDE [prod_short](includes/prod_short.md)] stellt das Demounternehmen einige Zahlungsmethoden bereit, die Unternehmen häufig verwenden. Sie können so viele Zeilen hinzufügen, wie Sie benötigen.  

Sie können Zahlungsbedingungen Debitoren und Kreditoren zuweisen, sodass dasselbe Verfahren immer auf Verkaufs- und Einkaufsbelegen verwendet wird, die Sie für sie einrichten. Bei Bedarf können Sie die Bedingungen auf dem Verkaufs- oder Kaufbeleg ändern, z. B. wenn Sie möchten, dass ein bestimmter Debitor innerhalb von 7 Tagen statt der Standardzeit von 14 Tagen bezahlt. Dies verändert nicht die standardmäßigen Zahlungsbedingungen, die dem Debitor zugeordnet ist. Die gleichen Zahlungsbedingungen sind für Einkaufs- und Verkaufsbelege verfügbar.

Wenn Sie dann eine Rechnung buchen, berechnet [!INCLUDE [prod_short](includes/prod_short.md)] den Zahlungsrabatt basierend auf den Zahlungsbedingungen. Gleichzeitig wird auch das Skontodatum berechnet (z. B. das letzte Datum, an dem ein Debitor Skonto erhält).  

Wenn Sie einen Habenbetrag buchen, berechnet [!INCLUDE [prod_short](includes/prod_short.md)] mögliche Zahlungsrabatte basierend auf den Zahlungsbedingungen. Skonto auf Habenbeträgen wird nach den gleichen Prinzipien wie Skonto auf Rechnungen berechnet. Wird ein Habenbetrag mit einer Rechnung ausgeglichen, so wird der mögliche Skontobetrag der Rechnung um den Skontobetrag für den Habenbetrag reduziert.  

Wenn Sie Ihren Kunden Erinnerungen an überfällige Zahlungen senden möchten, müssen Sie Erinnerungsstufen und -bedingungen einrichten. Weitere Informationen finden Sie unter [Einrichten von Betimmungen und Ebenen](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>So richten Sie Zahlungsbedingungen ein

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion Wie möchten Sie weiter verfahren öffnet](media/ui-search/search_small.png "Was möchten Sie tun"), geben Sie **Zahlungsbedingungen** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Weisen Sie die Zahlungsbedingungen den Debitoren und Kreditoren zu, nachdem Sie sie eingerichtet haben. Fügen Sie Ihren Zahlungsbedingungen optional Ihre Zahlungsformen hinzu.  

> [!TIP]
> In der Basisversion von [!INCLUDE [prod_short](includes/prod_short.md)] werden Zahlungsbedingungen mit Teilzahlungen nicht unterstützt. Stattdessen müssen Sie die Vorauszahlungsfunktion verwenden. Weitere Informationen finden Sie unter [Einrichten von Vorauszahlungen](finance-set-up-prepayments.md).
>
> In bestimmten Ländern *können* Sie Zahlungsbedingungen mit Teilzahlungen einrichten. Informationen dazu, ob diese Funktion in Ihrem Land unterstützt wird, finden Sie im Abschnitt **Lokale Funktionalität** im Navigationsbereich auf der linken Seite auf der Seite [Docs.microsoft.com](about-localization.md).

## <a name="see-also"></a>Siehe auch

[Einrichten von Zahlungsformen](finance-payment-methods.md)  
[Vorauszahlungen einrichten](finance-set-up-prepayments.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Registriert einen neuen Debitor](sales-how-register-new-customers.md)  
[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]