---
title: 'Vorgehensweise: Einrichten von MwSt.-Berichten'
description: Informationen aus verschiedenen Rechnungstypen werden verwendet, um Daten in den Ausfuhr-Listenbericht EU zu speisen. Um einen MwSt-Bericht unter dem System ELMA5 von Business Central einzurichten, müssen Sie die Parameter melden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 183fc0321a44b076afcd6c7f3c01fda64db76fa7
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677079"
---
# <a name="set-up-vat-reports"></a><span data-ttu-id="bd191-104">Richten Sie die MwSt.-Berichte ein.</span><span class="sxs-lookup"><span data-stu-id="bd191-104">Set Up VAT Reports</span></span>
<span data-ttu-id="bd191-105">Informationen aus verschiedenen Rechnungstypen werden verwendet, um Daten in den Ausfuhr-Listenbericht EU zu speisen.</span><span class="sxs-lookup"><span data-stu-id="bd191-105">Information from various invoice types is used to feed data into the EU Sales List report.</span></span> <span data-ttu-id="bd191-106">Um einen MwSt-Bericht unter dem System ELMA5 von [!INCLUDE[d365fin](../../includes/d365fin_md.md)] einzurichten, müssen Sie die Parameter melden.</span><span class="sxs-lookup"><span data-stu-id="bd191-106">To file a VAT report under the ELMA5 system from [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you need to set up report parameters.</span></span>  

## <a name="to-set-up-a-vat-report"></a><span data-ttu-id="bd191-107">So richten Sie einen MwSt-Bericht ein</span><span class="sxs-lookup"><span data-stu-id="bd191-107">To set up a VAT report</span></span>  

1.  <span data-ttu-id="bd191-108">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **VAT-Bereichtsservice** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="bd191-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Report Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bd191-109">Wählen Sie im Inforegister **Allgemein** das Feld **Übermittelte Berichte bearbeiten** aus, damit Benutzer MwSt.-Erklärungen, die an die Steuerbehörden übermittelt wurden, ändern können.</span><span class="sxs-lookup"><span data-stu-id="bd191-109">On the **General** FastTab, select the **Modify Submitted Reports** check box to let users modify VAT reports that have been submitted to the tax authorities.</span></span>  

    <span data-ttu-id="bd191-110">Wenn Sie das Feld leer lassen, müssen Benutzer stattdessen eine Korrektur-MwSt.-Erklärung erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd191-110">If the field is left blank, users must create a corrective VAT report instead.</span></span>  

3.  <span data-ttu-id="bd191-111">Wählen Sie das Kontrollkästchen **Stornozeilen exportieren**, wenn Sie Informationen über Stornierungszeilen berücksichtigen wollen, wenn Sie Daten für den MwSt von EU-Verkäufen exportieren.</span><span class="sxs-lookup"><span data-stu-id="bd191-111">Select the **Export Cancellation Lines** check box if you want to include information about cancellation lines when you export data for the VAT report of EU sales.</span></span> <span data-ttu-id="bd191-112">Weitere Informationen finden Sie unter [Gewusst wie: MwSt korrigieren](how-to-correct-vat-reports.md)</span><span class="sxs-lookup"><span data-stu-id="bd191-112">For more information, see [Correct VAT Reports](how-to-correct-vat-reports.md).</span></span>  
4.  <span data-ttu-id="bd191-113">Geben Sie im Inforegister **Nummerierung** die Nummernserie an, die für Standard-MwSt.-Erklärungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd191-113">On the **Numbering** FastTab, specify the number series that will be used for standard VAT reports.</span></span> <span data-ttu-id="bd191-114">Dieses ist standardmäßig die Seriennummer, die in beliebigen MwSt Berichten verwendet wird, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd191-114">This will be the default numbering series that is used on any VAT Report that you then create.</span></span>  

    <span data-ttu-id="bd191-115">Abhängig von den Anforderungen können Sie die gleichen Nummernserien für alle MwSt.-Erklärungen oder separate Nummernserien für jede Art von MwSt.-Erklärung verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd191-115">Depending on the requirements, you can use the same number series for all VAT reports, or separate number series for each type of VAT report.</span></span>

    <span data-ttu-id="bd191-116">Wenn beispielsweise Ihre Unternehmen separate Nummernserien für Standard- und für Korrektur-MwSt.-Erklärungen verwendet, ist diese Nummernserie die Standardnummernserie.</span><span class="sxs-lookup"><span data-stu-id="bd191-116">For example, if your company uses separate number series for standard and corrective VAT reports, this number series is the default number series.</span></span> <span data-ttu-id="bd191-117">Benutzer können eine andere Nummernserie in **Nr.** auswählen</span><span class="sxs-lookup"><span data-stu-id="bd191-117">Users can select a different number series in the **No.**</span></span> <span data-ttu-id="bd191-118">Feld, wenn sie Korrekturberichte erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd191-118">field when they create corrective reports.</span></span>  

5.  <span data-ttu-id="bd191-119">Im Inforegister **ZIVIT** können Sie Informationen für die Felder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bd191-119">On the **ZIVIT** FastTab, specify information for the fields.</span></span>  
6.  <span data-ttu-id="bd191-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="bd191-120">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bd191-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd191-121">See Also</span></span>  
 <span data-ttu-id="bd191-122">[MwSt.-Abrechnung](vat-reporting.md) </span><span class="sxs-lookup"><span data-stu-id="bd191-122">[VAT Reporting](vat-reporting.md) </span></span>  
 [<span data-ttu-id="bd191-123">Erstellen von MwsT-Berichten.</span><span class="sxs-lookup"><span data-stu-id="bd191-123">Create VAT Reports</span></span>](how-to-create-vat-reports.md)
