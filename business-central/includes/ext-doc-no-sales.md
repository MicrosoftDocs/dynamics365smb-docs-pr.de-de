---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 50b4b331f00bdcdf030bac2332ffb5dafdfd2de6
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115961"
---
<span data-ttu-id="5295c-101">Auf Verkaufsbelegen und Buch.-Blättern können Sie eine Belegnummer angeben, die auf das Nummerierungssystem des Debitors verweist.</span><span class="sxs-lookup"><span data-stu-id="5295c-101">On sales documents and journals, you can specify a document number that refers to the customer's numbering system.</span></span> <!--You can enter a maximum of ten characters, both numbers and letters.--> <span data-ttu-id="5295c-102">Verwenden Sie dieses Feld, um die Nummer zu erfassen, die der Debitor der Bestellung, Rechnung oder Gutschrift zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="5295c-102">Use this field to record the number that the customer assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="5295c-103">Sie können die Nummer dann später verwenden, wenn Sie aus irgendeinem Grund den gebuchten Posten anhand dieser Nummer suchen müssen.</span><span class="sxs-lookup"><span data-stu-id="5295c-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>  

<span data-ttu-id="5295c-104">Das Feld **Ext. Belegnr. erforderlich** auf der Seite **Debitoren & Verkauf Einr.** gibt an, ob die Eingabe einer externen Belegnummer im Feld **Externe Belegnr.** in einem Verkaufskopf und das Feld **Externe Belegnr.** in einer Fibu Buch.-Blattzeile erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5295c-104">The **Ext. Doc. No. Mandatory** field on the **Sales & Receivables Setup** page specifies whether it is mandatory to enter an external document number in the **External Document No.** field on a sales header and the **External Document No.** field on a general journal line.</span></span>

<span data-ttu-id="5295c-105">Wenn Sie dieses Feld auswählen, ist es nicht möglich, eine Rechnung oder eine Fibu Buch.-Blattzeile ohne externe Belegnummer zu buchen.</span><span class="sxs-lookup"><span data-stu-id="5295c-105">If you select this field, it will not be possible to post an invoice or a general journal line without an external document number.</span></span>

<span data-ttu-id="5295c-106">Die externe Belegnummer ist in gebuchten Belegen enthalten, in denen Sie nach der entsprechenden Nummer suchen können.</span><span class="sxs-lookup"><span data-stu-id="5295c-106">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="5295c-107">Sie können bei der Navigation zu Debitorenposten auch über die externe Belegnummer suchen.</span><span class="sxs-lookup"><span data-stu-id="5295c-107">You can also search using the external document number when navigating on customer ledger entries.</span></span>

<span data-ttu-id="5295c-108">Eine andere Möglichkeit, externe Belegnummern zu handhaben, ist die Verwendung des Feldes **Ihre Referenz**.</span><span class="sxs-lookup"><span data-stu-id="5295c-108">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="5295c-109">Wenn Sie das Feld **Ihre Referenz** verwenden, wird die Nummer in gebuchte Belege aufgenommen und Sie können danach wie nach Werten aus den Feldern **Externe Belegnr.** suchen.</span><span class="sxs-lookup"><span data-stu-id="5295c-109">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="5295c-110">Das Feld ist jedoch in Buchungsblattzeile nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5295c-110">But the field is not available on journal lines.</span></span>
