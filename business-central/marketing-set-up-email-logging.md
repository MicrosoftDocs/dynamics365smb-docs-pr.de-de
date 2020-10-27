---
title: E-Mail-Protokollierung einrichten | Microsoft Docs
description: Erfahren Sie, wie Sie E-Mail-Interaktionen zwischen Verkäufern und Kunden in echte Verkaufschancen verwandeln können.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f02e78e0b5c7d7f6d3c22cd12e37bdaf74f4b90f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923620"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="95c40-103">Verfolgen Sie den Austausch von E-Mail-Nachrichten zwischen Verkäufern und Kontakten</span><span class="sxs-lookup"><span data-stu-id="95c40-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>

<span data-ttu-id="95c40-104">Machen Sie mehr aus der Kommunikation zwischen Verkäufern und Ihren bestehenden oder potenziellen Kunden, indem Sie den E-Mail-Austausch nachverfolgen und diese dann in umsetzbare Gelegenheiten umwandeln.</span><span class="sxs-lookup"><span data-stu-id="95c40-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="95c40-105">kann mit Exchange Online arbeiten, um ein Protokoll der eingehenden und ausgehenden Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="95c40-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="95c40-106">Sie können den Inhalt jeder Nachricht auf der Seite **Aktivitätenprotokollposten** anzeigen und analysieren.</span><span class="sxs-lookup"><span data-stu-id="95c40-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><span data-ttu-id="95c40-107">Öffentliche Ordner und Regeln für die E-Mail-Anmeldung in Exchange Online einrichten</span><span class="sxs-lookup"><span data-stu-id="95c40-107">Set up Public Folders and Rules for Email Logging in Exchange Online</span></span>

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

<span data-ttu-id="95c40-108">Als nächstes verbinden Sie [!INCLUDE[prodshort](includes/prodshort.md)] mit Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="95c40-108">Next, you connect [!INCLUDE[prodshort](includes/prodshort.md)] with Exchange Online.</span></span>

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="95c40-109">Einrichten von [!INCLUDE[d365fin](includes/d365fin_md.md)], um E-Mail-Nachrichten zu protokollieren</span><span class="sxs-lookup"><span data-stu-id="95c40-109">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>

<span data-ttu-id="95c40-110">Beginnen Sie mit der E-Mail-Protokollierung in zwei einfachen Schritten:</span><span class="sxs-lookup"><span data-stu-id="95c40-110">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="95c40-111">Stellen Sie eine Verbindung von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Exchange Online her für Ihr Microsoft 365-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95c40-111">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Microsoft 365 subscription.</span></span> <span data-ttu-id="95c40-112">Exchange Online verarbeitet Ihre E-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="95c40-112">Exchange Online handles your email messages.</span></span> <span data-ttu-id="95c40-113">Wir haben diesen Schritt vereinfacht, indem wir eine Anleitung für Unterstützte Einrichtung bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="95c40-113">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="95c40-114">Sie benötigen lediglich Ihre Administratoranmeldeinformationen für Ihr Administratorkonto in Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="95c40-114">You just need your administrator credentials for your administrator account in Microsoft 365.</span></span> <span data-ttu-id="95c40-115">Um die Anleitung zu starten, gehen Sie zu **Unterstützte Einrichtung** , und wählen Sie dann **E-Mail-Protokollierung einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="95c40-115">To start the guide, go to **Assisted Setup** , and then choose **Set up email logging** .</span></span>  

2. <span data-ttu-id="95c40-116">Stellen Sie sicher, dass in [!INCLUDE[d365fin](includes/d365fin_md.md)] gültige E-Mail-Adressen für Ihre Verkäufer und Kontakte eingegeben wurden, je nachdem, ob es sich um potenzielle oder bestehende Kunden handelt.</span><span class="sxs-lookup"><span data-stu-id="95c40-116">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="95c40-117">Öffnen Sie dazu für jeden Kunden oder Verkäufer die Karte **Kontakt** oder **Verkäufer/Käufer** , und überprüfen Sie das Feld **E-Mail** .</span><span class="sxs-lookup"><span data-stu-id="95c40-117">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="95c40-118">Nachdem Sie die Schritte in der Anleitung ausgeführt haben, können Sie überprüfen, ob die Verbindung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="95c40-118">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="95c40-119">Suchen Sie nach **Marketingeinrichtung** , wählen Sie **Verarbeiten** aus, dann **Funktionen** , und dann **E-Mail-Protokollierungseinr. überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="95c40-119">Search for **Marketing Setup** , choose **Process** , then **Functions** , and then **Validate Email Logging Setup** .</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="95c40-120">Anzeigen des E-Mail-Nachrichtenaustauschs im Aktivitätenprotokoll</span><span class="sxs-lookup"><span data-stu-id="95c40-120">Viewing Email Message Exchanges in the Interaction Log</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="95c40-121">erstellt einen Eintrag auf der Seite **Aktivitätenprotokoll** , jedes Mal, wenn ein Verkäufer und ein Kontakt eine E-Mail-Nachricht austauschen.</span><span class="sxs-lookup"><span data-stu-id="95c40-121">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="95c40-122">Um das Interaktionsprotokoll anzuzeigen, öffnen Sie die Karte **Kontakt** oder **Verkäufer/Einkäufer** für die Person, und wählen Sie dann **Verkauf** und dann **Interaktionsprotokollposten** aus.</span><span class="sxs-lookup"><span data-stu-id="95c40-122">To view the interaction log, open the **Contact** or **Salesperson Purchaser** card for the person, and then choose **History** , and then choose **Interaction Log Entries** .</span></span> <span data-ttu-id="95c40-123">Es gibt einige Dinge, die wir mit jedem Eintrag im Protokoll tun können, zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="95c40-123">There are a few things we can do with each entry in the log, for example:</span></span>

- <span data-ttu-id="95c40-124">Zeigen Sie den Inhalt der E-Mail-Nachricht an, die ausgetauscht wurde, indem Sie auf die Aktion **Dateianhänge anzeigen** klicken.</span><span class="sxs-lookup"><span data-stu-id="95c40-124">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
- <span data-ttu-id="95c40-125">Verwandeln Sie einen E-Mail-Austausch in eine Verkaufschance: Wenn ein Eintrag vielversprechend aussieht, können Sie ihn in eine Verkaufschance verwandeln und dann den Fortschritt in Richtung Verkauf steuern.</span><span class="sxs-lookup"><span data-stu-id="95c40-125">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="95c40-126">Wählen Sie hierzu den Eintrag aus, und wählen Sie dann die Aktion **Verkaufschance erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="95c40-126">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="95c40-127">Weitere Informationen finden Sie unter [Verkaufschancen verwalten](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="95c40-127">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="95c40-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95c40-128">See Also</span></span>
[<span data-ttu-id="95c40-129">Verwalten von Beziehungen</span><span class="sxs-lookup"><span data-stu-id="95c40-129">Managing Relationships</span></span>](marketing-relationship-management.md)

