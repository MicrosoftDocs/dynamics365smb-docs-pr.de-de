---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470287"
---
<span data-ttu-id="1ee2e-101">Wenn alle Artikel in den Verkaufszeilen eingegeben wurden, kann der Rechnungsrabatt für den gesamten Beleg berechnet werden, indem Sie auf Aktionen und dann auf die Aktion **Rechnungsrabatt berechnen** klicken.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-101">When all the items have been entered on the sales lines, you can calculate the invoice discount for the entire document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="1ee2e-102">Der Rabatt wird basierend auf allen Zeilen des Verkaufsbelegs berechnet, jedoch nur für Artikel, bei denen das Feld **Rech.-Rabatt zulassen** in der Verkaufsauftragszeile die Option **Ja** enthält.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="1ee2e-103">Dies ist die Standardeinstellung für Artikel.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-103">This is the default setting for items.</span></span> <span data-ttu-id="1ee2e-104">Beispielsweise werden Zeilen mit Artikelgebühren nicht in die Berechnung des Rechnungsrabattes einbezogen.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="1ee2e-105">Wenn Sie einen Rabatt auf solche Zeilen gewähren möchten, müssen Sie das Feld **Zeilenrabatt %** in den entsprechenden Zeilen festlegen.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="1ee2e-106">Wenn das Feld **Rechnungsrabatt berechnen** auf der Seite **Verkäufe und Debitoren einrichten** ausgewählt wird, dann wird der Rechnungsrabatt automatisch berechnet, wenn Sie eine der folgenden Aktionen auf einem Verkaufsbeleg ausführen:</span><span class="sxs-lookup"><span data-stu-id="1ee2e-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="1ee2e-107">Statistik anzeigen</span><span class="sxs-lookup"><span data-stu-id="1ee2e-107">View statistics</span></span>
> * <span data-ttu-id="1ee2e-108">Anzeigen eines Testberichts</span><span class="sxs-lookup"><span data-stu-id="1ee2e-108">View a test report</span></span>
> * <span data-ttu-id="1ee2e-109">Drucken</span><span class="sxs-lookup"><span data-stu-id="1ee2e-109">Print</span></span>
> * <span data-ttu-id="1ee2e-110">Buchung</span><span class="sxs-lookup"><span data-stu-id="1ee2e-110">Post</span></span>

<span data-ttu-id="1ee2e-111">Zum Berechnen des Rechnungsrabatts für einen Debitor werden auf der Seite **Debitorenrechnungsrabatt** für den Debitor definiert.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="1ee2e-112">Anhand des Währungscodes im Verkaufsbeleg werden die Rechnungsrabattbedingungen der entsprechenden Währung ermittelt.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="1ee2e-113">Wenn keine Rechnungsrabatte für Fremdwährungen definiert wurden, verwendet die Anwendung die Rechnungsrabattbedingungen in Mandantenwährung, die in der Tabelle **Debitorenrechnungsrabatt** festgelegt wurden und den Wechselkurs zum Buchungsdatum des Verkaufsbelegs, um den Rechnungsrabatt in der Fremdwährung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
