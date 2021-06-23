---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115958"
---
<span data-ttu-id="ecbf8-101">Auf Einkaufsbelegen und Buch.-Blättern können Sie eine Belegnummer angeben, die auf das Nummerierungssystem des Kreditors verweist.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="ecbf8-102">Verwenden Sie dieses Feld, um die Nummer zu erfassen, die der Kreditor der Bestellung, Rechnung oder Gutschrift zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="ecbf8-103">Sie können die Nummer dann später verwenden, wenn Sie aus irgendeinem Grund den gebuchten Posten anhand dieser Nummer suchen müssen.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="ecbf8-104">Das Feld **Ext. Belegnr. erforderlich** auf der Seite **Kreditoren & Einkauf Einr.** gibt an, ob in folgenden Situationen die Eingabe einer externen Belegnummer obligatorisch ist:</span><span class="sxs-lookup"><span data-stu-id="ecbf8-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="ecbf8-105">Im Feld **Kred.-Rechnungsnr.**, im Feld **Lieferanten-Bestell-Nr.**</span><span class="sxs-lookup"><span data-stu-id="ecbf8-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="ecbf8-106">oder im Feld **Kred.-Gutschriftsnr.**</span><span class="sxs-lookup"><span data-stu-id="ecbf8-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="ecbf8-107">in einem Einkaufskopf.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-107">field on a purchase header</span></span>

* <span data-ttu-id="ecbf8-108">Im Feld **Externe Belegnummer** in der Buch.-Blattzeile, wenn das Feld **Belegart** auf *Rechnung*, *Gutschrift* oder *Zinsrechnung* und das Feld **Kontoart** auf *Kreditor* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="ecbf8-109">Wenn Sie dieses Feld aktivieren, ist es nicht möglich, eine Rechnung, Gutschrift oder Buch.-Blattzeile ohne die Angabe einer externen Belegnummer zu buchen.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="ecbf8-110">Die externe Belegnummer ist in gebuchten Belegen enthalten, in denen Sie nach der entsprechenden Nummer suchen können.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="ecbf8-111">Sie können bei der Navigation zu Kreditorenposten auch über die externe Belegnummer suchen.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="ecbf8-112">Eine andere Möglichkeit, externe Belegnummern zu handhaben, ist die Verwendung des Feldes **Ihre Referenz**.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="ecbf8-113">Wenn Sie das Feld **Ihre Referenz** verwenden, wird die Nummer in gebuchte Belege aufgenommen und Sie können danach wie nach Werten aus den Feldern **Externe Belegnr.** suchen.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="ecbf8-114">Das Feld ist jedoch in Buchungsblattzeile nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ecbf8-114">But the field is not available on journal lines.</span></span>
