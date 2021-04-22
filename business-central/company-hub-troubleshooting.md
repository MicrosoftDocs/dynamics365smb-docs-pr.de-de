---
title: Fehlerbehandlung in Ihrem Unternehmens-Hub
description: Erfahren Sie, wie Sie Probleme umgehen können, wenn Sie sich im Unternehmenshub in Dynamics 365 Business Central befinden, um die Arbeit über mehrere Unternehmen hinweg zu verwalten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fc015058079e30b2db6989b246dc38498cd7a1f4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786512"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="6ee47-103">Fehlerbehandlung in Ihrem Unternehmens-Hub</span><span class="sxs-lookup"><span data-stu-id="6ee47-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="6ee47-104">Das Hinzufügen von Unternehmen zum Dashboard des Unternehmens-Hubs ist äußerst einfach, aber in diesem Artikel werden Probleme behandelt, die dabei auftreten können.</span><span class="sxs-lookup"><span data-stu-id="6ee47-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="6ee47-105">Fehler prüfen</span><span class="sxs-lookup"><span data-stu-id="6ee47-105">Check errors</span></span>

<span data-ttu-id="6ee47-106">Verwenden Sie die Aktion **Fehler prüfen** zum Anzeigen einer Liste aktueller Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ee47-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="6ee47-107">Sie können zusätzliche Details für jeden Fehler anzeigen, und Sie können das Protokoll bereinigen, indem Sie ältere Posten löschen.</span><span class="sxs-lookup"><span data-stu-id="6ee47-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="6ee47-108">Verbindung fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="6ee47-108">Connection failed</span></span>

<span data-ttu-id="6ee47-109">Es kann verschiedene Gründe geben, warum Sie keine Verbindung zu einem Unternehmen herstellen können, darunter die folgenden:</span><span class="sxs-lookup"><span data-stu-id="6ee47-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="6ee47-110">Die URL im Feld **Umgebungslink** ist ungültig</span><span class="sxs-lookup"><span data-stu-id="6ee47-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="6ee47-111">Wechseln Sie zur Seite **Umgebungslinks**, öffnen Sie die Umgebung, mit der Sie keine Verbindung herstellen können, und wählen Sie dann die Aktion **Die Verbindung testen** aus.</span><span class="sxs-lookup"><span data-stu-id="6ee47-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="6ee47-112">Das Unternehmen des Kundens ist derzeit offline, beispielsweise bei einem Upgrade</span><span class="sxs-lookup"><span data-stu-id="6ee47-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="6ee47-113">Wählen Sie in Ihrem Dashboard das Menüelement **Werkzeuge** aus, und wählen Sie dann **Fehler prüfen**.</span><span class="sxs-lookup"><span data-stu-id="6ee47-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="6ee47-114">Dadurch wird eine Liste mit technischen Details geöffnet, daher sollten Sie sich an Ihren Administrator wenden, wenn Sie Fehler finden.</span><span class="sxs-lookup"><span data-stu-id="6ee47-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="6ee47-115">Zum Beispiel weist die Fehlermeldung „*Der Server hat die Anmeldeinformationen des Kunden abgelehnt*“ darauf hin, dass Sie keinen Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="6ee47-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="6ee47-116">Sie haben nicht Zugriff auf alle Unternehmen in der Umgebung, zu der Sie eine Verbindung herstellen möchten</span><span class="sxs-lookup"><span data-stu-id="6ee47-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="6ee47-117">In [!INCLUDE [prod_short](includes/prod_short.md)] kann eine Organisation mehrere Konzernmandanten haben, die als Unternehmen bezeichnet werden, und Sie haben möglicherweise nicht Zugriff auf alle Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="6ee47-117">In [!INCLUDE [prod_short](includes/prod_short.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="6ee47-118">Arbeiten Sie mit Ihrem Administrator oder Client, um sicherzustellen, dass Sie Zugriff auf die Unternehmen haben, in denen Sie arbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="6ee47-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="6ee47-119">Daten werden nicht aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6ee47-119">Data does not refresh</span></span>

<span data-ttu-id="6ee47-120">Wenn Sie ein Unternehmen hinzufügen oder eine Aktualisierung der Daten anfordern, ruft [!INCLUDE [prod_short](includes/prod_short.md)] die Daten ab.</span><span class="sxs-lookup"><span data-stu-id="6ee47-120">When you add a company or request a refresh of the data, [!INCLUDE [prod_short](includes/prod_short.md)] fetches the data.</span></span> <span data-ttu-id="6ee47-121">Sie müssen die Seite allerdings selbst aktualisieren, z. B. durch Auswählen der Aktion **Alle Unternehmen neu laden**, die Browser-Seite aktualisieren, vom Dashboard hinweg und wieder dorthin zurück navigieren oder etwas Ähnliches.</span><span class="sxs-lookup"><span data-stu-id="6ee47-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="6ee47-122">Wenn Sie ein Unternehmen hinzugefügt haben, dieses jedoch nicht in der Liste angezeigt wird, können Sie auch die Aktion **Alle Unternehmen neu laden** zum Aktualisieren der Liste verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ee47-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ee47-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ee47-123">See also</span></span>

[<span data-ttu-id="6ee47-124">Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten</span><span class="sxs-lookup"><span data-stu-id="6ee47-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="6ee47-125">Fügen Sie Unternehmen zu Ihrem Unternehmens-Hub hinzu</span><span class="sxs-lookup"><span data-stu-id="6ee47-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="6ee47-126">Buchhaltungs-Erfahrung in Business Central</span><span class="sxs-lookup"><span data-stu-id="6ee47-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]