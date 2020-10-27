---
title: Arbeiten mit intelligenten Benachrichtigungen und angeben, wenn Sie sie sehen | Microsoft Docs
description: Sie können Benachrichtigungen erhalten, die Sie über Statusänderungen oder Ereignissen, beispielsweise, ein überfälliger Saldo oder ein Logistik Basis informieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9ea6568f858dd154b7126f6444b45e4e548c6d18
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923345"
---
# <a name="manage-notifications"></a><span data-ttu-id="d9e30-103">Verwalten von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d9e30-103">Manage Notifications</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d9e30-104">kann nützlich sein, um intelligenter zu arbeiten, indem es Sie beispielsweise informiert, wenn Sie einen Debitoren fakturieren wollen, der einen überfälligen Saldo hat oder der verfügbare Lagerbestand geringer ist als die Menge, die Sie verkaufen wollen.</span><span class="sxs-lookup"><span data-stu-id="d9e30-104">can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="d9e30-105">Diese Benachrichtigungen werden als diskrete Tipps im Kontext der Aufgabe angezeigt, die Sie durchführen, und Sie können wählen, ob Sie die Benachrichtigung ignorieren oder Details zu dem Problem anzeigen wollen.</span><span class="sxs-lookup"><span data-stu-id="d9e30-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="d9e30-106">Wenn Sie das Anzeigen der Benachrichtigungsdetails auswählen, können Sie Maßnahmen ergreifen, um das Problem zu lösen, beispielsweise den Debitor kontaktieren, mehr Lagerbestand kaufen, usw.</span><span class="sxs-lookup"><span data-stu-id="d9e30-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="d9e30-107">Sie können auswählen. was Sie tun wollen und [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt Ihnen Hinweise und Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="d9e30-107">It's your choice what to do, and [!INCLUDE[d365fin](includes/d365fin_md.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="d9e30-108">Die Benachrichtigungen helfen dem ungeübten Nutzer dabei, nicht vertraute Aufgaben abzuschließen und reduzieren nicht die Produktivität des geschulten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d9e30-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="d9e30-109">Schaltet Benachrichtigungen ein und aus und steuert, wann diese gesendet werden</span><span class="sxs-lookup"><span data-stu-id="d9e30-109">To turn notifications on or off, and control when they are sent</span></span>

<span data-ttu-id="d9e30-110">Wenn Sie zuerst mit [!INCLUDE[d365fin](includes/d365fin_md.md)] Benachrichtigungen beginnen, werden alle ausgeführt, Sie können diese aber ein- oder ausschalten, beispielsweise, wenn Sie an einem bestimmten Ereignis oder an einen Status nicht interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="d9e30-110">When you first start with [!INCLUDE[d365fin](includes/d365fin_md.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="d9e30-111">Darüber hinaus lassen gewisse Benachrichtigungen Sie die Bedingungen angeben, mit denen sie gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d9e30-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="d9e30-112">Wenn Sie beispielsweise benachrichtigt werden möchten, wenn der Lagerbestand niedrig ist, aber dies nur für Artikel, die Sie von einem bestimmten Kreditoren kaufen.</span><span class="sxs-lookup"><span data-stu-id="d9e30-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="d9e30-113">Aktivieren oder deaktivieren Sie bestimmte Benachrichtigungen, die auf Sie interessieren.</span><span class="sxs-lookup"><span data-stu-id="d9e30-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="d9e30-114">In der oberen rechter Ecke wählen Sie das Symbol **Einstellungen** aus ![Einstellungen](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollencenter") und wählen dann die Aktion **Meine Einstellungen** .</span><span class="sxs-lookup"><span data-stu-id="d9e30-114">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose the **My Settings** action.</span></span>  
2. <span data-ttu-id="d9e30-115">Auf der Seite **Meine Einstellungen** , im Feld **Benachrichtigungen** wählen Sie den *Ändern, wenn ich Benachrichtigungen erhalte.*</span><span class="sxs-lookup"><span data-stu-id="d9e30-115">On the **My Settings** page, in the **Notifications** field, choose the *Change when I receive notifications.*</span></span> <span data-ttu-id="d9e30-116">Link.</span><span class="sxs-lookup"><span data-stu-id="d9e30-116">link.</span></span>  
3. <span data-ttu-id="d9e30-117">Auf der Seite, die angezeigt wird, aktivieren oder deaktivieren Sie eine Benachrichtigung, indem Sie das Kontrollkästchen **Aktiviert** aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d9e30-117">In the page that appears, turn on or turn off a notification by selecting or clearing the **Enabled** check box.</span></span>  
4. <span data-ttu-id="d9e30-118">Um Bedingungen anzugeben, die eine Benachrichtigung auslösen, wählen Sie den Link **Filterdetails ansehen** und füllen Sie die Felder aus.</span><span class="sxs-lookup"><span data-stu-id="d9e30-118">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d9e30-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9e30-119">See Also</span></span>

<span data-ttu-id="d9e30-120">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9e30-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
