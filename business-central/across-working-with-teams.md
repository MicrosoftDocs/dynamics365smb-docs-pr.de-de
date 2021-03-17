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
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: cbb505865e061bfa8017699a2127206bb25f91b4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381981"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="b4b92-103">Arbeiten mit Business Central-Daten in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b4b92-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="b4b92-104">[!INCLUDE [prod_short](includes/prod_short.md)] bietet eine App, die Microsoft Teams mit Ihren Geschäftsdaten in [!INCLUDE [prod_short](includes/prod_short.md)] verbindet. So können Sie schnell Daten zwischen Teammitgliedern austauschen und Anfragen schneller beantworten.</span><span class="sxs-lookup"><span data-stu-id="b4b92-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="b4b92-105">In diesem Artikel erfahren Sie, wie Sie die App zum Teilen von [!INCLUDE [prod_short](includes/prod_short.md)]-Daten mit Mitarbeitern in einer Unterhaltung in Teams verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4b92-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="b4b92-106">Matrix</span><span class="sxs-lookup"><span data-stu-id="b4b92-106">Overview</span></span>

<span data-ttu-id="b4b92-107">Mit der [!INCLUDE [prod_short](includes/prod_short.md)]-App können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="b4b92-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="b4b92-108">Sie können einen Link zu einem beliebigen Business Central-Datensatz kopieren und ihn in eine Teams-Unterhaltung einfügen, um ihn dann mit Ihren Mitarbeitern zu teilen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="b4b92-109">Die App dann wird zu einem kompakten, interaktiven Link erweitert, auf dem Informationen zum Datensatz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b4b92-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="b4b92-110">Wenn Sie sich in der Unterhaltung befinden, können Sie und Ihre Mitarbeiter weitere Details zum Datensatz anzeigen, Daten bearbeiten und Maßnahmen ergreifen&mdash;ohne Teams zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="b4b92-111">[![Teams-Integration in Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b4b92-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b4b92-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b4b92-112">Prerequisites</span></span>

- <span data-ttu-id="b4b92-113">Sie haben Zugriff auf Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b4b92-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="b4b92-114">Sie haben die [!INCLUDE [prod_short](includes/prod_short.md)]-App in Teams installiert.</span><span class="sxs-lookup"><span data-stu-id="b4b92-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="b4b92-115">Weitere Informationen finden Sie unter [Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md).</span><span class="sxs-lookup"><span data-stu-id="b4b92-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="b4b92-116">Alle Teilnehmer einer Teams-Unterhaltung können Karten für Business Central-Datensätze anzeigen, die Sie an die Unterhaltung senden.</span><span class="sxs-lookup"><span data-stu-id="b4b92-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="b4b92-117">Um weitere Details zu Datensätzen anzuzeigen (durch Verwenden der Schaltflächen **Details** oder **Pop-out** auf einer Karte), benötigen diese jedoch Zugriff auf [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b4b92-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b4b92-118">Weitere Informationen finden Sie unter [Verwalten der Microsoft Teams-Integration](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="b4b92-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="b4b92-119">Eine Business Central-Karte in eine Teams-Unterhaltung einfügen</span><span class="sxs-lookup"><span data-stu-id="b4b92-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="b4b92-120">Verwenden Sie Ihren Browser, um sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anzumelden.</span><span class="sxs-lookup"><span data-stu-id="b4b92-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="b4b92-121">Öffnen Sie den Datensatz, den Sie teilen möchten.</span><span class="sxs-lookup"><span data-stu-id="b4b92-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="b4b92-122">Die App dient zum Anzeigen von Kartenseiten aus [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b4b92-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b4b92-123">Öffnen Sie daher eine Seite, auf der ein einzelner Datensatz angezeigt wird, z. B. ein Artikel, ein Kunde oder ein Verkaufsauftrag.</span><span class="sxs-lookup"><span data-stu-id="b4b92-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="b4b92-124">Sie können sie nicht für Rollencenter oder Seiten verwenden, auf denen mehrere Datensätze in einer Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b4b92-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="b4b92-125">Kopieren Sie die gesamte URL aus der Adressleiste des Browsers.</span><span class="sxs-lookup"><span data-stu-id="b4b92-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Die Business Central-URL aus dem Browser kopieren](media/teams-url-v2.png)
4. <span data-ttu-id="b4b92-127">Wechseln Sie zu Teams und beginnen Sie eine Unterhaltung, die mit einer Person, einer Personengruppe oder einem Teamkanal geführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b4b92-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="b4b92-128">Fügen Sie die URL in das Feld Nachrichten ein, in dem Sie die Nachricht erstellen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Business Central-URL in Teams einfügen](media/teams-paste-url-v2.png)
6. <span data-ttu-id="b4b92-130">Wenn Sie zum ersten Mal einen Link in eine Unterhaltung einfügen, werden Sie aufgefordert, sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anzumelden und der App die Zustimmung zum Datenabruf zu geben.</span><span class="sxs-lookup"><span data-stu-id="b4b92-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="b4b92-131">Folgen Sie einfach den Anweisungen auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="b4b92-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4b92-132">Sie müssen diesen Schritt nur einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="b4b92-133">Warten Sie einen Moment, während eine Karte im Nachrichtenfeld generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b4b92-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="b4b92-134">Wenn die Karte angezeigt wird, überprüfen Sie den Inhalt der Karte sorgfältig auf sensible Informationen, bevor Sie die Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="b4b92-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="b4b92-135">Dieser Schritt ist wichtig, da nach dem Senden der Nachricht jeder Unterhaltungsteilnehmer die Karte sehen kann.</span><span class="sxs-lookup"><span data-stu-id="b4b92-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="b4b92-136">Wenn Sie mit der Karte zufrieden sind, wählen Sie **Senden** aus, um sie der Unterhaltung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="b4b92-137">Nachdem die Karte angezeigt wird und bevor Sie **Senden** auswählen, können Sie die eingefügte URL bei Bedarf löschen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="b4b92-138">Um weitere Details anzuzeigen oder Änderungen an der Karte vorzunehmen, wählen Sie **Details** aus.</span><span class="sxs-lookup"><span data-stu-id="b4b92-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="b4b92-139">Weitere Informationen finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="b4b92-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="b4b92-140">Kartendetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="b4b92-140">View card details</span></span>

<span data-ttu-id="b4b92-141">Sobald eine Karte an ein Gespräch gesendet wurde, können alle Teilnehmer mit den [ordnungsgemäßen Berechtigungen](admin-teams-integration.md#permissions) **Einzelheiten** auswählen, um ein Fenster zu öffnen, in dem weitere Informationen zum Datensatz angezeigt werden&mdash; und möglicherweise Änderungen am Datensatz vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="b4b92-142">Es spielt keine Rolle, ob Sie die Karte senden oder die Karte empfangen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="b4b92-143">Die Funktion **Details** ist besonders für Empfänger nützlich, da sie ihnen schnell präzise und zielgerichtete Informationen über den Datensatz liefert, anstatt den gesamten Datensatz scannen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="b4b92-144">Das Detailfenster ähnelt der Seite, die im [!INCLUDE [prod_short](includes/prod_short.md)] Datensatz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b4b92-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="b4b92-145">Sie ist für Teams jedoch ein wenig gekürzt.</span><span class="sxs-lookup"><span data-stu-id="b4b92-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="b4b92-146">Wenn Sie mit dem Anzeigen und Vornehmen von Änderungen fertig sind, schließen Sie das Fenster, um zur Unterhaltung in Teams zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b4b92-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="b4b92-147">Hier sind einige Dinge zu beachten, wenn Sie mit den Kartendetails arbeiten:</span><span class="sxs-lookup"><span data-stu-id="b4b92-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="b4b92-148">Um weitere Details für eine Karte anzuzeigen oder den Datensatz in [!INCLUDE [prod_short](includes/prod_short.md)] zu öffnen, müssen Benutzer über Leseberechtigung für die Seite und ihre Daten verfügen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="b4b92-149">Karten in Team-Chats werden nicht automatisch auf Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b4b92-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="b4b92-150">Alle Änderungen, die Sie an einem Datensatz im Detailfenster speichern, werden in [!INCLUDE [prod_short](includes/prod_short.md)] gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b4b92-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b4b92-151">Auf der Karte in Teams werden die Änderungen in der Konvertierung jedoch erst angezeigt, wenn Sie den Link erneut einfügen.</span><span class="sxs-lookup"><span data-stu-id="b4b92-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="b4b92-152">Weitere Informationen zum Arbeiten mit Karten und Kartendetails finden Sie unter [Teams FAQ](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="b4b92-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b4b92-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4b92-153">See Also</span></span>

[<span data-ttu-id="b4b92-154">Übersicht über die Integration von Business Central und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b4b92-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="b4b92-155">[Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="b4b92-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="b4b92-156">Teams FAQ</span><span class="sxs-lookup"><span data-stu-id="b4b92-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="b4b92-157">Teams Problembehebung</span><span class="sxs-lookup"><span data-stu-id="b4b92-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="b4b92-158">Entwicklung für die Teams-Integration</span><span class="sxs-lookup"><span data-stu-id="b4b92-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]