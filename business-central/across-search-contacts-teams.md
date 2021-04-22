---
title: Suchen nach Kontakten von Microsoft Teams
description: Erfahren Sie, wie Sie nach Business Central-Debitoren, ‑Kreditoren und anderen Kontakten von Microsoft Teams suchen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 77108cab69a05165616ad5e1a44f1a3ddc9d4cd9
ms.sourcegitcommit: e13b80d4e5141f414109e660e0918eae561acb36
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882491"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="c7a46-103">Suche nach Debitoren, Kreditoren und anderen Kontakten von Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c7a46-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="c7a46-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="c7a46-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="c7a46-105">Eingeführt im Jahr 2021 Veröffentlichungszyklus 1.</span><span class="sxs-lookup"><span data-stu-id="c7a46-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="c7a46-106">[!INCLUDE [prod_short](includes/prod_short.md)] verfügt über ein umfassendes System zur Verwaltung von Geschäftskontakten, das für Benutzer in Vertriebs‑, Betriebs‑ oder anderen Abteilungsfunktionen unerlässlich ist.</span><span class="sxs-lookup"><span data-stu-id="c7a46-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="c7a46-107">Wenn Sie ein Benutzer in einer dieser Rollen sind, müssen Sie häufig nachsehen, sich treffen oder ein Gespräch mit Ihren Debitoren, Kreditoren und anderen Kontakten beginnen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="c7a46-108">Mit der [!INCLUDE [prod_short](includes/prod_short.md)] App für Teams können Sie diese Aufgaben direkt von Teams aus erledigen, ohne zu [!INCLUDE [prod_short](includes/prod_short.md)] wechseln zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="c7a46-109">Innerhalb von Teams können Sie:</span><span class="sxs-lookup"><span data-stu-id="c7a46-109">From within Teams, you can:</span></span>

- <span data-ttu-id="c7a46-110">[!INCLUDE [prod_short](includes/prod_short.md)]-Kontakte aus dem Befehlsfeld Teams oder aus dem Bereich zum Erstellen von Nachrichten nachschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="c7a46-111">Zu den Kontakten können potenzielle Debitoren, Kreditoren, Debitoren oder andere Geschäftsbeziehungen gehören.</span><span class="sxs-lookup"><span data-stu-id="c7a46-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="c7a46-112">Teilen Sie einen Kontakt als Karte in einem Teamgespräch.</span><span class="sxs-lookup"><span data-stu-id="c7a46-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="c7a46-113">Zeigen Sie Details zu Kontaktinformationen, Interaktionsverlauf und anderen Erkenntnissen wie ausstehenden Zahlungen oder offenen Dokumenten an.</span><span class="sxs-lookup"><span data-stu-id="c7a46-113">View details about contact information, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7a46-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c7a46-114">Prerequisites</span></span>

- <span data-ttu-id="c7a46-115">Sie haben Zugriff auf Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c7a46-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="c7a46-116">Sie haben die [!INCLUDE [prod_short](includes/prod_short.md)]-App in Teams installiert.</span><span class="sxs-lookup"><span data-stu-id="c7a46-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="c7a46-117">Weitere Informationen finden Sie unter [Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md).</span><span class="sxs-lookup"><span data-stu-id="c7a46-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="c7a46-118">Sie haben ein [!INCLUDE [prod_short](includes/prod_short.md)]-Konto mit Zugriff auf Kontakte in mindestens einem Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="c7a46-119">Unabhängig davon, ob Sie über das Befehlsfeld oder das Nachrichtenerstellungsfeld suchen, werden Sie möglicherweise aufgefordert, sich beim ersten Mal anzumelden oder die App einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c7a46-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="c7a46-120">Dieser Schritt ist erforderlich, um nach Kontakten im richtigen Business Central-Unternehmen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="c7a46-121">Informationen zum Einrichten der App zur Auswahl Ihres Unternehmens finden Sie unter [Ändern der Unternehmens und anderen Einstellungen in Teams](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c7a46-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="c7a46-122">Vom Befehlsfeld nach Kontakten suchen</span><span class="sxs-lookup"><span data-stu-id="c7a46-122">Look up contacts from the command box</span></span>

<span data-ttu-id="c7a46-123">Das Befehlsfeld befindet sich in Teams oben auf jedem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="c7a46-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="c7a46-124">Sie können damit suchen, schnelle Aktionen ausführen oder Apps wie die [!INCLUDE [prod_short](includes/prod_short.md)]-App starten.</span><span class="sxs-lookup"><span data-stu-id="c7a46-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="c7a46-125">Die Suche über das Befehlsfeld ist ideal, um schnell nach Kontakten und den zugehörigen Daten für Ihren eigenen Gebrauch zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="c7a46-126">Angenommen, Sie möchten eine E-Mail-Adresse eines Kreditors nachschlagen, um eine Kalenderbesprechung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c7a46-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="c7a46-127">Oder Sie möchten den Interaktionsverlauf während eines Meetings mit einem Debitor nachschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="c7a46-128">Geben Sie in das Befehlsfeld **@Business Central** ein, und wählen Sie dann die Business Central-App aus den Ergebnissen aus.</span><span class="sxs-lookup"><span data-stu-id="c7a46-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Die Business Central-App öffnen, um über das Befehlsfeld nach Kontakten zu suchen](media/teams-contacts-command-1.png)

2. <span data-ttu-id="c7a46-130">Geben Sie im Feld **Business Central** einen Suchtext wie einen Namen, eine Adresse oder eine Telefonnummer ein.</span><span class="sxs-lookup"><span data-stu-id="c7a46-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="c7a46-131">Während der Eingabe werden übereinstimmende Ergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7a46-131">As you type, matching results will appear.</span></span>

    ![Nach Business Central-Kontakten über das Befehlsfeld in Teams suchen](media/teams-contacts-command-2.png)
3. <span data-ttu-id="c7a46-133">Wählen Sie einen Kontakt aus den Ergebnissen aus.</span><span class="sxs-lookup"><span data-stu-id="c7a46-133">Select a contact from the results.</span></span>

    <span data-ttu-id="c7a46-134">Die Kontaktkarte wird unter dem Befehlsfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7a46-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="c7a46-135">Wenn Sie die Kontaktkarte zu einem Gespräch hinzufügen möchten, gehen Sie in die obere rechte Ecke der Karte und wählen Sie **... (Weitere Optionen)** > **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="c7a46-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="c7a46-136">Fügen Sie dann die Kopie in das Feld zum Erstellen einer Nachricht einer Konversation ein.</span><span class="sxs-lookup"><span data-stu-id="c7a46-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="c7a46-137">Weitere allgemeine Informationen zum Befehlsfeld in Teams finden Sie unter [Teams – Das Befehlsfeld verwenden](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="c7a46-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="c7a46-138">Vom Feld zum Erstellen einer Nachricht nach Kontakten suchen</span><span class="sxs-lookup"><span data-stu-id="c7a46-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="c7a46-139">Der Vorteil der Verwendung des Felds zum Erstellen von Nachrichten besteht darin, dass Sie einer Konversation eine Kontaktkarte direkt hinzufügen können, damit andere sie sehen können.</span><span class="sxs-lookup"><span data-stu-id="c7a46-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="c7a46-140">Wählen Sie unter dem Feld zum Verfassen von Nachrichten das Symbol **Business Central** aus, um die App zu starten.</span><span class="sxs-lookup"><span data-stu-id="c7a46-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="c7a46-141">Wenn Sie das Symbol **Business Central** nicht sehen, wählen Sie **... (Messaging-Erweiterungen)** aus.</span><span class="sxs-lookup"><span data-stu-id="c7a46-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Die Business Central-App öffnen, um über das Feld Nachrichten nach Kontakten zu suchen](media/teams-contacts-message-box.png)

2. <span data-ttu-id="c7a46-143">Geben Sie im Feld **Business Central** einen Suchtext wie einen Namen, eine Adresse oder eine Telefonnummer ein.</span><span class="sxs-lookup"><span data-stu-id="c7a46-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="c7a46-144">Während der Eingabe werden übereinstimmende Ergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7a46-144">As you type, matching results will appear.</span></span>

    ![Über das Feld Nachrichten nach Business Central-Kontakten suchen](media/teams-contacts-5.png)
3. <span data-ttu-id="c7a46-146">Wählen Sie einen Kontakt aus den Ergebnissen aus.</span><span class="sxs-lookup"><span data-stu-id="c7a46-146">Select a contact from the results.</span></span>

    <span data-ttu-id="c7a46-147">Die Kontaktkarte wird im Feld zum Erstellen von Nachrichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7a46-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c7a46-148">Die Kontaktkarte wird nicht sofort an das Gespräch gesendet, damit andere sie sehen können.</span><span class="sxs-lookup"><span data-stu-id="c7a46-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="c7a46-149">Sie haben die Möglichkeit, den Inhalt der Karte zu überprüfen und nach Belieben Text davor oder danach hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="c7a46-150">Senden Sie dann Ihre Nachricht an den Chat, wenn Sie bereit sind.</span><span class="sxs-lookup"><span data-stu-id="c7a46-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="c7a46-151">Hier ist eine andere Möglichkeit</span><span class="sxs-lookup"><span data-stu-id="c7a46-151">Here's another way</span></span>

1. <span data-ttu-id="c7a46-152">Anstatt das Symbol **Business Central** zu verwenden, geben Sie **@ Business Central** direkt im Feld zum Verfassen von Nachrichten ein.</span><span class="sxs-lookup"><span data-stu-id="c7a46-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="c7a46-153">Geben Sie Ihre Suchbegriffe in dem Feld ein.</span><span class="sxs-lookup"><span data-stu-id="c7a46-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="c7a46-154">Verwenden Sie die Aufwärts‑ und Abwärtspfeiltasten auf der Tastatur, um einen Kontakt auszuwählen, und drücken Sie die Eingabetaste, um ihn auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c7a46-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="c7a46-155">Kontaktkartendetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="c7a46-155">Viewing contact card details</span></span>

<span data-ttu-id="c7a46-156">Die Kontaktkarte in Teams gibt Ihnen einen schnellen Überblick über den Debitor, Kreditor oder Kontakt.</span><span class="sxs-lookup"><span data-stu-id="c7a46-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="c7a46-157">Die Karte ist interaktiv&mdash;, das heißt, Sie können weitere Informationen anzeigen oder sogar einen Kontakt ändern, indem Sie die Schaltflächen **Details** oder **Pop-out** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7a46-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="c7a46-158">Die Schaltfläche **Details** öffnet ein Fenster in Teams, in dem weitere Informationen zum Kontakt angezeigt werden, jedoch nicht so viele, wie Sie in [!INCLUDE [prod_short](includes/prod_short.md)] sehen würden.</span><span class="sxs-lookup"><span data-stu-id="c7a46-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="c7a46-159">Um alle Informationen zu einem Kontakt in [!INCLUDE [prod_short](includes/prod_short.md)] zu sehen, wählen Sie **Pop-out** aus.</span><span class="sxs-lookup"><span data-stu-id="c7a46-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="c7a46-160">Die Kontaktkarte funktioniert genau wie Karten für Aufzeichnungen, z. B. Artikel, Debitoren oder Verkaufsaufträge.</span><span class="sxs-lookup"><span data-stu-id="c7a46-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="c7a46-161">Weitere Informationen zu Karten finden Sie unter [Kartendetails anzeigen](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="c7a46-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="c7a46-162">Alle Teilnehmer einer Teams-Unterhaltung können Karten für Business Central-Kontakte anzeigen, die Sie an die Unterhaltung senden.</span><span class="sxs-lookup"><span data-stu-id="c7a46-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="c7a46-163">Um weitere Details zu Datensätzen anzuzeigen (durch Verwenden der Schaltflächen **Details** oder **Pop-out** auf einer Karte), benötigen diese jedoch Zugriff auf [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c7a46-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="c7a46-164">Weitere Informationen finden Sie unter [Verwalten der Microsoft Teams-Integration](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="c7a46-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="c7a46-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7a46-165">See Also</span></span>

[<span data-ttu-id="c7a46-166">Übersicht über die Integration von Business Central und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c7a46-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="c7a46-167">[Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="c7a46-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="c7a46-168">Teams FAQ</span><span class="sxs-lookup"><span data-stu-id="c7a46-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="c7a46-169">Teams Problembehebung</span><span class="sxs-lookup"><span data-stu-id="c7a46-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="c7a46-170">Entwicklung für die Teams-Integration</span><span class="sxs-lookup"><span data-stu-id="c7a46-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]