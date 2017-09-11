---
title: Lohntransaktionen importieren| Microsoft Docs
description: Um Gehalt zu verwalten, importieren Sie buchen und finanzieller Transaktionen von Ihrem Gehaltsabrechnungsanbieter auf Sach-, mithilfe einer Gehaltsabrechnungserweiterung wie Ceridian oder Quickbooks.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d53dfb26a3fea663e68a3b558579a59184e9de26
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-import-payroll-transactions"></a><span data-ttu-id="132bd-103">Vorgehensweise: Lohntransaktion importieren</span><span class="sxs-lookup"><span data-stu-id="132bd-103">How to: Import Payroll Transactions</span></span>
<span data-ttu-id="132bd-104">Um Gehaltszahlungen und verwandte Transaktionen zu berücksichtigen, müssen Sie die Gehaltstransaktionen importieren und finanzielle Transaktionen buchen, die durch Ihr Gehaltsabrechnungsanbieter in die Finanzbuchhaltung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="132bd-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="132bd-105">Dazu importieren Sie zuerst eine Datei, die Sie vom Gehaltsabrechnungsanbieter erhalten in das Fenster **Fibur Buch.Blatt**.</span><span class="sxs-lookup"><span data-stu-id="132bd-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="132bd-106">Anschließend ordnen Sie die externen Konten in der Gehaltsabrechnungsdatei den jeweiligen Sachkonten zu.</span><span class="sxs-lookup"><span data-stu-id="132bd-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="132bd-107">Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen entsprechend der Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="132bd-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="132bd-108">Um diese Funktionalität nutzen zu können, muss für den Gehaltsabrechnungsimport eine Erweiterung eingerichtet und aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="132bd-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="132bd-109">Die Ceridian-Gehaltsliste und die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterungen werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="132bd-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="132bd-110">Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-extensions.md) mithilfe der Erweiterungen .</span><span class="sxs-lookup"><span data-stu-id="132bd-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="132bd-111">Um eine Lohndatei zu importieren</span><span class="sxs-lookup"><span data-stu-id="132bd-111">To import a payroll file</span></span>
1. <span data-ttu-id="132bd-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="132bd-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="132bd-113">Wählen Sie im relevanten Fibu Buch.-Blattname die Aktion **Gehaltsabrechnungstransaktionen importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="132bd-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="132bd-114">Ein unterstützter Einrichtungsleitfaden wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="132bd-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="132bd-115">Befolgen Sie die Schritte im Fenster **Gehaltsabrechnungstransaktionen importieren**.</span><span class="sxs-lookup"><span data-stu-id="132bd-115">Follow the steps in the **Import Payroll Transactions** window.</span></span>

    > [!TIP]  
>   <span data-ttu-id="132bd-116">Im Schritt zum Zuordnen der externen Lohn- und Gehaltsabrechnungsdatensätze zu den Sachkonten, erinnert sich das Programm an die Zuordnungen, die Sie erstellen, das nächste Mal, wenn dieselben Daten importiert werden.</span><span class="sxs-lookup"><span data-stu-id="132bd-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="132bd-117">Dadurch sparen Sie Zeit, da Sie das Feld **Kontonr.** nicht manuell ausfüllen müssen,</span><span class="sxs-lookup"><span data-stu-id="132bd-117">This will save you time as you do not have to manually fill in the **Account No.**</span></span> <span data-ttu-id="132bd-118">im Fibu Buch.-Blatt, jedes Mal wenn Sie wiederkehrende Gehaltsabrechnungstransaktionen importiert haben.</span><span class="sxs-lookup"><span data-stu-id="132bd-118">field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="132bd-119">Wenn Sie die Schaltfläche **OK** im unterstützten Einrichtungsleitfaden auswählen, wird das Fenster **Fibu Buch.-Blatt** mit den Zeilen ausgefüllt, die die Transaktionen darstellen, die die Gehaltsabrechnungsdatei enthält und dabei werden die relevanten Konten in den Feldern **Sachkonto** vorausgefüllt, gemäß den Zuordnungen, die Sie im Leitfaden vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="132bd-119">When you choose the **OK** button in the assisted setup guide, the **General Journal** window is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="132bd-120">Bearbeiten oder buchen Sie die Buch.-Blattzeilen für andere Finanzbuchhaltungstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="132bd-120">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="132bd-121">Weitere Informationen finden Sie unter [So gehts: Transaktionen direkt in der Finanzbuchhaltung buchen.](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="132bd-121">For more information, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="132bd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="132bd-122">See Also</span></span>
[<span data-ttu-id="132bd-123">Finanzen</span><span class="sxs-lookup"><span data-stu-id="132bd-123">Finance</span></span>](finance.md)  
<span data-ttu-id="132bd-124">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="132bd-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="132bd-125">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="132bd-125">Working with General Journals</span></span>](ui-work-general-journals.md)  

