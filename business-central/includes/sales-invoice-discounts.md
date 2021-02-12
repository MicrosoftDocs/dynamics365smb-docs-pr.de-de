---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035785"
---
<span data-ttu-id="be7ff-101">Wenn alle Artikel in den Verkaufsauftragszeilen eingegeben wurden, kann der Rechnungsrabatt für den gesamten Verkaufsbeleg berechnet werden, indem Sie auf Aktionen und dann auf die Aktion **Rechnungsrabatt berechnen** klicken.</span><span class="sxs-lookup"><span data-stu-id="be7ff-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="be7ff-102">Wenn das Feld **Rechnungsrabatt berechnen** im Fenster **Verkäufe und Debitoren einrichten** ausgewählt wird, dann wird der Rechnungsrabatt automatisch berechnet, wenn Sie eine der folgenden Aktionen auf einem Verkaufsbeleg ausführen:</span><span class="sxs-lookup"><span data-stu-id="be7ff-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="be7ff-103">Statistik anzeigen</span><span class="sxs-lookup"><span data-stu-id="be7ff-103">View statistics</span></span>
* <span data-ttu-id="be7ff-104">Anzeigen eines Testberichts</span><span class="sxs-lookup"><span data-stu-id="be7ff-104">View a test report</span></span>
* <span data-ttu-id="be7ff-105">Drucken</span><span class="sxs-lookup"><span data-stu-id="be7ff-105">Print</span></span>
* <span data-ttu-id="be7ff-106">Buchung</span><span class="sxs-lookup"><span data-stu-id="be7ff-106">Post</span></span>

<span data-ttu-id="be7ff-107">Der Rabatt wird über alle Zeilen des Verkaufsbelegs verteilt, jedoch nur für Artikel, bei denen das Feld **Rech.-Rabatt zulassen** in der Verkaufsauftragszeile die Option **Ja** enthält.</span><span class="sxs-lookup"><span data-stu-id="be7ff-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="be7ff-108">Dies ist die Standardeinstellung für Artikel.</span><span class="sxs-lookup"><span data-stu-id="be7ff-108">This is the default setting for items.</span></span>

<span data-ttu-id="be7ff-109">Zum Berechnen des Rechnungsrabatts werden die auf der Seite **Debitorenrechnungsrabatt** berechneten Rechnungsrabatte definiert.</span><span class="sxs-lookup"><span data-stu-id="be7ff-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="be7ff-110">Anhand des Währungscodes im Verkaufsbeleg werden die Rechnungsrabattbedingungen der entsprechenden Währung ermittelt.</span><span class="sxs-lookup"><span data-stu-id="be7ff-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="be7ff-111">Wenn keine Rechnungsrabatte für Fremdwährungen definiert wurden, verwendet die Anwendung die Rechnungsrabattbedingungen in Mandantenwährung, die in der Tabelle **Debitorenrechnungsrabatt** festgelegt wurden und den Wechselkurs zum Buchungsdatum des Verkaufsbelegs, um den Rechnungsrabatt in der Fremdwährung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="be7ff-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
