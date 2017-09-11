---
title: Einrichten des Kontenplans | Microsoft Docs
description: "Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ceb01999525139cabc7c31e2304f738dcc9267f8
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2017

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="f6b0f-103">Einrichten oder Ändern des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="f6b0f-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="f6b0f-104">Der Kontenplan zeigt die Sachkonten an, die Ihre Finanzdaten speichern.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]<span data-ttu-id="f6b0f-105"> umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="f6b0f-106">Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="f6b0f-107">Konten hinzufügen oder ändern</span><span class="sxs-lookup"><span data-stu-id="f6b0f-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="f6b0f-108">Im Kontenplan können Sie jedes Sachkonto öffnen und Einstellungen hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f6b0f-109">Sie können ein Sachkonto löschen.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-109">You can delete a general ledger account.</span></span> <span data-ttu-id="f6b0f-110">Bevor es gelöscht wird, müssen allerdings folgende Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="f6b0f-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="f6b0f-111">Der Saldo des Kontos muss Null betragen.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="f6b0f-112">Das Feld **Löschen v. Sachkonten zul. vor** im Fenster **Finanzbuchhaltung Einrichtung** muss ausgefüllt sein, und das Konto darf keine Posten an oder nach diesem Datum enthalten.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="f6b0f-113">Ist das Feld **Sachkontoverwendung prüfen** im Fenster **Finanzbuchhaltung Einrichtung** ausgewählt, darf dieses Konto nicht in Buchungsgruppen oder der Buchungsmatrix Einrichtung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f6b0f-114"> verhindert, dass Sie ein Sachkonto löschen, in dem Daten gespeichert werden, die im Kontenplan erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f6b0f-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6b0f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6b0f-115">See Also</span></span>
[<span data-ttu-id="f6b0f-116">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="f6b0f-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="f6b0f-117">Verwalten von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="f6b0f-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="f6b0f-118">Arbeiten mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="f6b0f-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="f6b0f-119">Aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="f6b0f-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="f6b0f-120">So gehts: Arbeiten mit GIFI-Codes in Kanada</span><span class="sxs-lookup"><span data-stu-id="f6b0f-120">How to: Work With GIFI Codes in Canada</span></span>](ca-finance-work-gifi-codes.md)  
<span data-ttu-id="f6b0f-121">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f6b0f-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
