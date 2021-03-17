---
title: Lohntransaktionen importieren| Microsoft Docs
description: Um Gehalt zu verwalten, importieren Sie buchen und finanzieller Transaktionen von Ihrem Gehaltsabrechnungsanbieter auf Sach-, mithilfe einer Gehaltsabrechnungserweiterung wie Ceridian oder Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6bd078c6cf12023088dfa2f925e5a61bcc61778
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387449"
---
# <a name="import-payroll-transactions"></a><span data-ttu-id="fc341-103">Lohntransaktionen importieren</span><span class="sxs-lookup"><span data-stu-id="fc341-103">Import Payroll Transactions</span></span>
<span data-ttu-id="fc341-104">Um Gehaltszahlungen und verwandte Transaktionen zu berücksichtigen, müssen Sie die Gehaltstransaktionen importieren und finanzielle Transaktionen buchen, die durch Ihr Gehaltsabrechnungsanbieter in die Finanzbuchhaltung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="fc341-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="fc341-105">Dazu importieren Sie zuerst eine Datei, die Sie vom Gehaltsabrechnungsanbieter erhalten in die Seite **Fibur Buch.Blatt**.</span><span class="sxs-lookup"><span data-stu-id="fc341-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="fc341-106">Anschließend ordnen Sie die externen Konten in der Gehaltsabrechnungsdatei den jeweiligen Sachkonten zu.</span><span class="sxs-lookup"><span data-stu-id="fc341-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="fc341-107">Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen entsprechend der Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="fc341-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="fc341-108">Um diese Funktionalität nutzen zu können, muss für den Gehaltsabrechnungsimport eine Erweiterung eingerichtet und aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="fc341-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="fc341-109">Die Ceridian-Gehaltsliste und die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterungen werden in [!INCLUDE[prod_short](includes/prod_short.md)] vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="fc341-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="fc341-110">Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe der Erweiterungen](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="fc341-110">For more information, see [Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="fc341-111">Um eine Lohndatei zu importieren</span><span class="sxs-lookup"><span data-stu-id="fc341-111">To import a payroll file</span></span>
1. <span data-ttu-id="fc341-112">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Fibu Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="fc341-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc341-113">Wählen Sie im relevanten Fibu Buch.-Blattname die Aktion **Gehaltsabrechnungstransaktionen importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="fc341-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="fc341-114">Ein unterstützter Einrichtungsleitfaden wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fc341-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="fc341-115">Befolgen Sie die Schritte auf der Seite **Gehaltsabrechnungstransaktionen importieren**.</span><span class="sxs-lookup"><span data-stu-id="fc341-115">Follow the steps on the **Import Payroll Transactions** page.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="fc341-116">Im Schritt zum Zuordnen der externen Lohn- und Gehaltsabrechnungsdatensätze zu den Sachkonten, erinnert sich das Programm an die Zuordnungen, die Sie erstellen, das nächste Mal, wenn dieselben Daten importiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc341-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="fc341-117">Das spart Zeit, weil Sie nicht jedes Mal manuell das Feld **Kontonr.** im Fibu Buch.-Blatt ausfüllen müssen, wenn Sie wiederkehrende Gehaltsabrechnungstransaktionen importiert haben.</span><span class="sxs-lookup"><span data-stu-id="fc341-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="fc341-118">Wenn Sie die Schaltfläche **OK** im unterstützten Einrichtungsleitfaden auswählen, wird die Seite **Fibu Buch.-Blatt** mit den Zeilen ausgefüllt, die die Transaktionen darstellen, die die Gehaltsabrechnungsdatei enthält und dabei werden die relevanten Konten in den Feldern **Sachkonto** vorausgefüllt, gemäß den Zuordnungen, die Sie im Leitfaden vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="fc341-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** page is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="fc341-119">Bearbeiten oder buchen Sie die Buch.-Blattzeilen für andere Finanzbuchhaltungstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="fc341-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="fc341-120">Weitere Informationen finden Sie unter [Transaktionen direkt in der Finanzbuchhaltung buchen.](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="fc341-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="fc341-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc341-121">See Also</span></span>
[<span data-ttu-id="fc341-122">Finanzen</span><span class="sxs-lookup"><span data-stu-id="fc341-122">Finance</span></span>](finance.md)  
<span data-ttu-id="fc341-123">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="fc341-123">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="fc341-124">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="fc341-124">Working with General Journals</span></span>](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]