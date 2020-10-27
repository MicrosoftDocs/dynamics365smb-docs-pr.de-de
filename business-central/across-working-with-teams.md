---
title: Arbeiten mit Business Central-Daten in Microsoft Teams | Microsoft Docs
description: Erfahren Sie, wie Sie die Business Central-App für Microsoft Teams verwenden.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989421"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="3bb65-103">Arbeiten mit Business Central-Daten in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3bb65-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="3bb65-104">[!INCLUDE [prodshort](includes/prodshort.md)] bietet eine App, die Microsoft Teams mit Ihren Geschäftsdaten in [!INCLUDE [prodshort](includes/prodshort.md)] verbindet. So können Sie schnell Daten zwischen Teammitgliedern austauschen und Anfragen schneller beantworten.</span><span class="sxs-lookup"><span data-stu-id="3bb65-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="3bb65-105">In diesem Artikel erfahren Sie, wie Sie die App zum Teilen von [!INCLUDE [prodshort](includes/prodshort.md)]-Daten mit Mitarbeitern in einer Unterhaltung in Teams verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bb65-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="3bb65-106">Matrix</span><span class="sxs-lookup"><span data-stu-id="3bb65-106">Overview</span></span>

<span data-ttu-id="3bb65-107">Mit der [!INCLUDE [prodshort](includes/prodshort.md)]-App können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="3bb65-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="3bb65-108">Sie können einen Link zu einem beliebigen Business Central-Datensatz kopieren und ihn in eine Teams-Unterhaltung einfügen, um ihn mit Ihren Mitarbeitern zu teilen.</span><span class="sxs-lookup"><span data-stu-id="3bb65-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="3bb65-109">Der Link wird zu einer kompakten, interaktiven Karte erweitert, auf der Informationen zum Datensatz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3bb65-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="3bb65-110">Wenn Sie sich in der Unterhaltung befinden, können Sie und Ihre Mitarbeiter weitere Details zum Datensatz anzeigen, Daten bearbeiten und Maßnahmen ergreifen – ohne Teams zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="3bb65-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="3bb65-111">[![Teams-Integration in Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="3bb65-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3bb65-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3bb65-112">Prerequisites</span></span>

- <span data-ttu-id="3bb65-113">Sie haben Zugriff auf Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="3bb65-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="3bb65-114">Sie haben die [!INCLUDE [prodshort](includes/prodshort.md)]-App in Teams installiert.</span><span class="sxs-lookup"><span data-stu-id="3bb65-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="3bb65-115">Weitere Informationen finden Sie unter [Die [!INCLUDE [prodshort](includes/prodshort.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md).</span><span class="sxs-lookup"><span data-stu-id="3bb65-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="3bb65-116">Alle Teilnehmer einer Teams-Unterhaltung können Karten für Business Central-Datensätze anzeigen, die Sie an die Unterhaltung senden.</span><span class="sxs-lookup"><span data-stu-id="3bb65-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="3bb65-117">Um weitere Details zu Datensätzen anzuzeigen (durch Verwenden der Schaltflächen **Details** oder **Pop-out** auf einer Karte), benötigen diese jedoch Zugriff auf [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3bb65-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3bb65-118">Weitere Informationen finden Sie unter [Verwalten der Microsoft Teams-Integration](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="3bb65-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="3bb65-119">Eine Business Central-Karte in eine Teams-Unterhaltung einfügen</span><span class="sxs-lookup"><span data-stu-id="3bb65-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="3bb65-120">Verwenden Sie Ihren Browser, um sich bei [!INCLUDE [prodshort](includes/prodshort.md)] anzumelden.</span><span class="sxs-lookup"><span data-stu-id="3bb65-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="3bb65-121">Öffnen Sie den Datensatz, den Sie teilen möchten.</span><span class="sxs-lookup"><span data-stu-id="3bb65-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="3bb65-122">Die App dient zum Anzeigen von Kartenseiten aus [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3bb65-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3bb65-123">Öffnen Sie daher eine Seite, auf der ein einzelner Datensatz angezeigt wird, z. B. ein Artikel, ein Kunde oder ein Verkaufsauftrag.</span><span class="sxs-lookup"><span data-stu-id="3bb65-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="3bb65-124">Sie können sie nicht für Rollencenter oder Seiten verwenden, auf denen mehrere Datensätze in einer Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3bb65-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="3bb65-125">Kopieren Sie die gesamte URL aus der Adressleiste des Browsers.</span><span class="sxs-lookup"><span data-stu-id="3bb65-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Die Business Central-URL aus dem Browser kopieren](media/teams-url.png)
4. <span data-ttu-id="3bb65-127">Wechseln Sie zu Teams und beginnen Sie eine Unterhaltung, die mit einer Person, einer Personengruppe oder einem Teamkanal geführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3bb65-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="3bb65-128">Fügen Sie die URL in das Feld ein, in das Sie Nachrichten einfügen.</span><span class="sxs-lookup"><span data-stu-id="3bb65-128">Paste the URL into the box where you add a message.</span></span>

   ![Business Central-URL in Teams einfügen](media/teams-paste-url.png)
6. <span data-ttu-id="3bb65-130">Wenn Sie zum ersten Mal einen Link in eine Unterhaltung einfügen, werden Sie aufgefordert, sich bei [!INCLUDE [prodshort](includes/prodshort.md)] anzumelden und der App die Zustimmung zum Datenabruf zu geben.</span><span class="sxs-lookup"><span data-stu-id="3bb65-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="3bb65-131">Folgen Sie einfach den Anweisungen auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="3bb65-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3bb65-132">Sie müssen diesen Schritt nur einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bb65-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="3bb65-133">Warten Sie einen Moment, während eine Karte im Nachrichtenfeld generiert wird.</span><span class="sxs-lookup"><span data-stu-id="3bb65-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="3bb65-134">Wenn die Karte angezeigt wird, überprüfen Sie den Inhalt der Karte sorgfältig auf sensible Informationen, bevor Sie die Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="3bb65-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="3bb65-135">Dieser Schritt ist wichtig, da nach dem Senden der Nachricht jeder Unterhaltungsteilnehmer die Karte sehen kann.</span><span class="sxs-lookup"><span data-stu-id="3bb65-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="3bb65-136">Wenn Sie mit der Karte zufrieden sind, wählen Sie **Senden** aus, um sie der Unterhaltung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3bb65-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="3bb65-137">Nachdem die Karte angezeigt wird und bevor Sie **Senden** auswählen, können Sie die eingefügte URL bei Bedarf löschen.</span><span class="sxs-lookup"><span data-stu-id="3bb65-137">After the card appears, and before you select **Send** , you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="3bb65-138">Um weitere Details anzuzeigen oder Änderungen am Datensatz vorzunehmen, wählen Sie **Details** aus.</span><span class="sxs-lookup"><span data-stu-id="3bb65-138">To view more details or make changes to the record, select **Details** .</span></span>

    <span data-ttu-id="3bb65-139">Die Detailseite ähnelt der Seite, die in [!INCLUDE [prodshort](includes/prodshort.md)] angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3bb65-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3bb65-140">Sie ist für Teams jedoch ein wenig gekürzt.</span><span class="sxs-lookup"><span data-stu-id="3bb65-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="3bb65-141">Wenn Sie mit dem Anzeigen und Vornehmen von Änderungen fertig sind, schließen Sie das Fenster, um zur Unterhaltung in Teams zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="3bb65-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3bb65-142">Alle von Ihnen vorgenommenen Änderungen werden erst dann auf der Karte angezeigt, wenn Sie ihren Link beim nächsten Mal in eine Unterhaltung einfügen.</span><span class="sxs-lookup"><span data-stu-id="3bb65-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="3bb65-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bb65-143">See Also</span></span>

[<span data-ttu-id="3bb65-144">Übersicht über die Integration von Business Central und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3bb65-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="3bb65-145">[Die [!INCLUDE [prodshort](includes/prodshort.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="3bb65-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="3bb65-146">Entwicklung für die Teams-Integration</span><span class="sxs-lookup"><span data-stu-id="3bb65-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="3bb65-147">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="3bb65-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
