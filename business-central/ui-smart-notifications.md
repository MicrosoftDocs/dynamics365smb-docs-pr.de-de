---
title: Arbeiten mit intelligenten Benachrichtigungen und angeben, wenn Sie sie sehen | Microsoft Docs
description: Sie können Benachrichtigungen erhalten, die Sie über Statusänderungen oder Ereignissen, beispielsweise, ein überfälliger Saldo oder ein Logistik Basis informieren.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c70a8fd066ffd5d312716891aa4cdf7768cd102a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249215"
---
# <a name="managing-notifications"></a><span data-ttu-id="7739c-103">Verwalten von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="7739c-103">Managing Notifications</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7739c-104">kann nützlich sein, um intelligenter zu arbeiten, indem es Sie beispielsweise informiert, wenn Sie einen Debitoren fakturieren wollen, der einen überfälligen Saldo hat oder der verfügbare Lagerbestand geringer ist als die Menge, die Sie verkaufen wollen.</span><span class="sxs-lookup"><span data-stu-id="7739c-104">can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="7739c-105">Diese Benachrichtigungen werden als diskrete Tipps im Kontext der Aufgabe angezeigt, die Sie durchführen, und Sie können wählen, ob Sie die Benachrichtigung ignorieren oder Details zu dem Problem anzeigen wollen.</span><span class="sxs-lookup"><span data-stu-id="7739c-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="7739c-106">Wenn Sie das Anzeigen der Benachrichtigungsdetails auswählen, können Sie Maßnahmen ergreifen, um das Problem zu lösen, beispielsweise den Debitor kontaktieren, mehr Lagerbestand kaufen, usw.</span><span class="sxs-lookup"><span data-stu-id="7739c-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="7739c-107">Sie können auswählen. was Sie tun wollen und [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt Ihnen Hinweise und Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="7739c-107">It's your choice what to do, and [!INCLUDE[d365fin](includes/d365fin_md.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="7739c-108">Die Benachrichtigungen helfen dem ungeübten Nutzer dabei, nicht vertraute Aufgaben abzuschließen und reduzieren nicht die Produktivität des geschulten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7739c-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="7739c-109">Schaltet Benachrichtigungen ein und aus und steuert, wann diese gesendet werden</span><span class="sxs-lookup"><span data-stu-id="7739c-109">To turn notifications on or off, and control when they are sent</span></span>
<span data-ttu-id="7739c-110">Wenn Sie zuerst mit [!INCLUDE[d365fin](includes/d365fin_md.md)] Benachrichtigungen beginnen, werden alle ausgeführt, Sie können diese aber ein- oder ausschalten, beispielsweise, wenn Sie an einem bestimmten Ereignis oder an einen Status nicht interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="7739c-110">When you first start with [!INCLUDE[d365fin](includes/d365fin_md.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="7739c-111">Darüber hinaus lassen gewisse Benachrichtigungen Sie die Bedingungen angeben, mit denen sie gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7739c-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="7739c-112">Wenn Sie beispielsweise benachrichtigt werden möchten, wenn der Lagerbestand niedrig ist, aber dies nur für Artikel, die Sie von einem bestimmten Kreditoren kaufen.</span><span class="sxs-lookup"><span data-stu-id="7739c-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="7739c-113">Aktivieren oder deaktivieren Sie bestimmte Benachrichtigungen, die auf Sie interessieren.</span><span class="sxs-lookup"><span data-stu-id="7739c-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="7739c-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Meine Benachrichtigungen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7739c-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **My Notifications**, and then choose the related link.</span></span>
2. <span data-ttu-id="7739c-115">Um eine Benachrichtigung zu aktivieren oder zu deaktivieren, markieren oder löschen Sie das Kontrollkästchen **Aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="7739c-115">To turn on or turn off a notification, select or clear the **Enabled** check box.</span></span>
3. <span data-ttu-id="7739c-116">Um Bedingungen anzugeben, die eine Benachrichtigung auslösen, wählen Sie den Link **Filterdetails ansehen** und füllen Sie die Felder aus.</span><span class="sxs-lookup"><span data-stu-id="7739c-116">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7739c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7739c-117">See Also</span></span>
<span data-ttu-id="7739c-118">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7739c-118">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
