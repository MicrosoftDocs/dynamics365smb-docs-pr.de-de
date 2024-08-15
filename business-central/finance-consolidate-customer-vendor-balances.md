---
title: 'Salden für ein Unternehmen konsolidieren, das ein Debitor und ein Kreditor ist'
description: 'Beschreibt die Konsolidierung von Salden für einen Kunden, der auch ein Lieferant ist.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 06/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="consolidate-balances-for-a-company-that-is-a-customer-and-a-vendor"></a>Salden für ein Unternehmen konsolidieren, das ein Debitor und ein Kreditor ist
Ein Unternehmen, mit dem Sie Geschäfte tätigen, kann sowohl Debitor als auch Kreditor sein. Wenn dies der Fall ist, können Sie unnötige Zahlungen oder Quittungen vermeiden und möglicherweise Transaktionsgebühren sparen, indem Sie die Debitoren- und Kreditorensalden des Unternehmens konsolidieren. Die Konsolidierung vergleicht die Salden des Unternehmens als Kreditor und als Debitor und saldiert dann den Betrag, sodass entweder der Debitoren- oder der Kreditorensaldo verbleibt, je nachdem, welcher Betrag höher war. 

Um die Salden zu konsolidieren, müssen Sie zuerst die Debitoren- und Kreditorenunternehmen über einen Kontakt mit dem Typ **Unternehmen** verknüpfen. Ein Debitor oder Kreditor kann nur einen Kontakt dieses Typs **Unternehmen** haben. Weitere Informationen finden Sie unter [Kontakte erstellen](marketing-create-contact-companies.md).

Nachdem Sie die Unternehmen verknüpft haben, bietet die **Debitorenkarte**-Seite das Feld **Saldo (MW) als Kreditor** und die **Kreditorenkarte**-Seite enthält das Feld **Saldo (MW) als Debitor**.

Obwohl dies nicht erforderlich ist, handelt es sich bei den Unternehmen des Debitors und des Kreditors in der Regel um dieselbe juristische Person. 

## <a name="before-you-start"></a>Bevor Sie beginnen
Bevor Sie Salden konsolidieren, legen Sie einige Einstellungen auf der **Marketing-Setup**-Seite fest. 

* Auf dem **Interaktionen**-Inforegister müssen Sie Geschäftsbeziehungscodes in den Feldern **Debitoren** und **Kreditoren** angeben. [!INCLUDE[prod_short](includes/prod_short.md)] verwendet diese Informationen, um den Beziehungstyp zu bestimmen, der für Kontakte angezeigt werden soll. 
* Optional: Auf dem **Duplikate**-Inforegister, Duplikatsuche ein- oder ausschalten. Standardmäßig ist die Duplikatsuche aktiviert. Weitere Informationen finden Sie unter [Behandeln von Duplikaten](#handling-duplicates). 

## <a name="link-an-existing-customer-and-vendor-company-through-a-contact"></a>Verknüpfen Sie eine bestehende Debitoren- und eine Kreditorenfirma gründlich mit einem Kontakt
Die folgenden Schritte beschreiben, wie Sie einen Debitor und einen Kreditor über einen Kontakt verknüpfen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kunde** oder **Kreditor** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Debitor oder Kreditor und dann die Aktion **Kontakt**.   
3. Wählen Sie den entsprechenden Kontakt und wählen Sie dann die Aktion **Mit vorhandenem verknüpfen** aus.
4. Wählen Sie die Art der Entität aus, mit der Sie eine Geschäftsbeziehung aufbauen möchten.
5. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="create-a-vendor-from-a-customer-or-vice-versa"></a>Erstellen Sie einen Kreditor aus einem Debitor oder umgekehrt
Sie können einen neuen Kreditor aus einem bestehenden Debitor oder einen neuen Debitor aus einem Kreditor erstellen. Öffnen Sie auf der **Debitor** oder **Kreditor**-Seite die **Kontakt**-Seite. Wählen Sie die Aktionen **Erstellen als**, und wählen Sie denn entweder **Debitor** oder **Kreditor**. 

## <a name="create-a-new-customer-or-vendor-and-link-them-through-a-vendor-or-customer-contact"></a>Erstellen Sie einen neuen Debitor oder Kreditor und verknüpfen Sie ihn über einen Kreditoren- oder Debitorenkontakt
1. Erstellen Sie einen neuen Debitor oder Kreditor. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).
2. Nachdem Sie den Debitor oder Kreditor eingerichtet haben, wählen Sie die **Erstellen**-Aktion aus, und wählen Sie dann entweder die **Debitor** oder **Kreditor**-Optionen. 

## <a name="to-consolidate-the-customer-and-vendor-balances-for-a-contact-company"></a>So konsolidieren Sie die Debitoren- und Kreditorensalden für eine Kontaktfirma
Auf der **Zahlungsjournal**-Seite verwenden Sie die **Nettosalden Debitor/Kreditor**-Aktion zur Konsolidierung der Debitoren- und Kreditorensalden zu einem einzigen Nettobetrag. Die Aktion erstellt Zahlungsjournalzeilen mit den Nettosalden, bucht diese jedoch nicht.

> [!NOTE]
> Wenn die Debitoren- oder Kreditorensalden Beträge in unterschiedlichen Währungen enthalten, wird eine Zeile für den Betrag in jeder Währung erstellt.

## <a name="handling-duplicates"></a>Umgang mit Duplikaten
Wenn Sie die Duplikatsuche auf dem Inforegister **Duplikate** auf der **Marketing-Setup**-Seite aktivieren, wird eine Warnung angezeigt, wenn Sie die Werte von Feldern ändern, die Teil der Einrichtung für doppelte Suchzeichenfolgen sind. Wenn ein Duplikat gefunden wird, können Sie die folgenden Maßnahmen ergreifen:

* Kombinieren Sie die doppelten Kontakte zu einem einzigen Kontakt, der für Debitor und Kreditor gleich ist, indem Sie die **Verbinden mit**-Fähigkeit auf der **Kontaktkarte**-Seite verwenden. Normalerweise werden Kontakte nur dann zusammengeführt, wenn Debitor und Kreditor dieselbe juristische Person sind. Weitere Informationen finden Sie unter [Doppelte Datensätze zusammenführen](sales-how-merge-duplicate-records.md). 
* Löschen Sie die Kreditorengeschäftsbeziehung für den Kreditoren- oder Kundenkontakt, und verwenden Sie dann die **Link zu Vorhanden**-Aktion zum Verknüpfen mit einem anderen Kontakt.    

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Neue Debitoren registrieren](sales-how-register-new-customers.md)  
