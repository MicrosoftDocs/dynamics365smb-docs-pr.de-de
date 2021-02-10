---
title: Die Kontenpläne einrichten
description: Sie können jedoch die Standardkonten im Konenplan ändern und neue Konten hinzufügen
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b20c4680393fa13b260beca366c7e4ba04abb291
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750380"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="59a69-103">Einrichten oder Ändern des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="59a69-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="59a69-104">Der Kontenplan zeigt die Sachkonten an, die Finanzdaten speichern.</span><span class="sxs-lookup"><span data-stu-id="59a69-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="59a69-105">umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.</span><span class="sxs-lookup"><span data-stu-id="59a69-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="59a69-106">Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="59a69-106">However, you can change the default accounts, and you can add new accounts.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="59a69-107">Konten hinzufügen oder ändern</span><span class="sxs-lookup"><span data-stu-id="59a69-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="59a69-108">Im Kontenplan können Sie jedes Sachkonto öffnen und Einstellungen hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="59a69-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="59a69-109">Sie können ein Sachkonto löschen.</span><span class="sxs-lookup"><span data-stu-id="59a69-109">You can delete a general ledger account.</span></span> <span data-ttu-id="59a69-110">Bevor es gelöscht wird, müssen allerdings folgende Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="59a69-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="59a69-111">Der Saldo des Kontos muss Null betragen.</span><span class="sxs-lookup"><span data-stu-id="59a69-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="59a69-112">Das Feld **Löschen v. Sachkonten zul. vor** auf der Seite **Finanzbuchhaltungs-Einrichtung:** muss ausgefüllt sein, und das Konto darf keine Posten an oder nach diesem Datum enthalten.</span><span class="sxs-lookup"><span data-stu-id="59a69-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="59a69-113">Ist das Feld **Sachkontoverwendung prüfen** auf der Seite **Finanzbuchhaltungs-Einrichtung:** ausgewählt, darf dieses Konto nicht in Buchungsgruppen oder der Buchungsmatrix Einrichtung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59a69-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="59a69-114">verhindert, dass Sie ein Sachkonto löschen, in dem Daten gespeichert werden, die im Kontenplan erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="59a69-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="59a69-115">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="59a69-115">See Related Training at [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="59a69-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59a69-116">See Also</span></span>
[<span data-ttu-id="59a69-117">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="59a69-117">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="59a69-118">Abstimmen von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="59a69-118">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="59a69-119">Arbeiten mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="59a69-119">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="59a69-120">Daten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="59a69-120">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="59a69-121">Arbeiten mit Kontenschemata</span><span class="sxs-lookup"><span data-stu-id="59a69-121">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="59a69-122">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="59a69-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]
