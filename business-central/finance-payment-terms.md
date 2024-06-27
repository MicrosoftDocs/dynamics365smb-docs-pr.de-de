---
title: Zahlungsbedingungen einrichten
description: 'Verwenden Sie Zahlungsbedingungen, um Fälligkeitsdaten und Skonti zu verwalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Zahlungsbedingungen einrichten

Die Zahlungsbedingungen bestimmen, wie Sie Fälligkeitstermine und Zahlungsrabatte verwalten. Zur Festlegung der Zahlungsbedingungen können Sie Datumsformeln verwenden. Wenn Sie sich zum ersten Mal anmelden für [!INCLUDE [prod_short](includes/prod_short.md)] stellt das Demounternehmen einige Zahlungsmethoden bereit, die Unternehmen häufig verwenden. Sie können so viele Zeilen hinzufügen, wie Sie benötigen.  

Wenn Sie können Zahlungsbedingungen zu Debitoren und Kreditoren zuweisen, werden dieselben Verfahren immer für Verkaufs- und Einkaufsbelege verwendet, die Sie für sie erstellen. Zur Berechnung der Fälligkeitstermine für Zahlungen werden die Belegdaten auf Verkaufs- und Einkaufsbelegen und nicht deren Buchungsdaten verwendet. Bei Bedarf können Sie die Bedingungen auf dem Verkaufs- oder Kaufbeleg ändern. Wenn Sie beispielsweise möchten, dass ein bestimmter Debitor innerhalb von sieben Tagen und nicht wie üblich innerhalb von 14 Tagen zahlt. Durch das Ändern der Bedingungen im Beleg wird die dem Kunden zugewiesene Standardzahlungsbedingung nicht geändert. Die gleichen Zahlungsbedingungen sind für Einkaufs- und Verkaufsbelege verfügbar.

Wenn Sie eine Rechnung buchen, berechnet [!INCLUDE [prod_short](includes/prod_short.md)] das Skonto basierend auf den Zahlungsbedingungen. Das Skontodatum ist das letzte Datum, an dem der Debitor ein Skonto erhalten kann. Das Datum wird auch berechnet, wenn Sie eine Rechnung buchen.  

Wenn Sie eine Gutschrift buchen, berechnet [!INCLUDE [prod_short](includes/prod_short.md)] mögliche Skonti basierend auf den Zahlungsbedingungen. Es berechnet den Rabatt auf Gutschriften auf dieselbe Weise wie Rabatte auf Rechnungen. Wenn Sie eine Gutschrift auf eine Rechnung anwenden, reduziert [!INCLUDE [prod_short](includes/prod_short.md)] den Rabattbetrag für die Rechnung um den Rabattbetrag der Gutschrift.  

Wenn Sie Ihren Kunden Erinnerungen an überfällige Zahlungen senden möchten, müssen Sie Erinnerungsstufen und -bedingungen einrichten. Weitere Informationen zu Mahnungen finden Sie unter [Mahnmethoden und Mahnstufen einrichten](finance-setup-reminders.md).  

## So richten Sie Zahlungsbedingungen ein

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun") Symbol. Geben Sie **Zahlungsbedingungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Weisen Sie die Zahlungsbedingungen den Debitoren und Kreditoren zu, nachdem Sie sie eingerichtet haben. Fügen Sie Ihren Zahlungsbedingungen optional Ihre Zahlungsformen hinzu.  

> [!TIP]
> In der Basisversion von [!INCLUDE [prod_short](includes/prod_short.md)] unterstützen Zahlungsbedingungen keine Teilzahlungen. Stattdessen müssen Sie die Vorauszahlungsfunktion verwenden. Um mehr über Vorauszahlungen zu erfahren, gehen Sie zu [Vorauszahlungen einrichten](finance-set-up-prepayments.md).
>
> In einigen Ländern/Regionen *können* Sie Zahlungsbedingungen mit Teilzahlungen einrichten. Informationen dazu, ob diese Funktion in Ihrem Land/Ihrer Region unterstützt wird, finden Sie im Abschnitt **Lokale Funktionalität** im Inhaltsverzeichnis auf der linken Seite eines [Microsoft Learn](about-localization.md)-Artikels.

## Siehe auch

[Zahlungsformen einrichten](finance-payment-methods.md)  
[Vorauszahlungen einrichten](finance-set-up-prepayments.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Registriert einen neuen Debitor](sales-how-register-new-customers.md)  
[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
