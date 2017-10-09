---
title: "So werden MwSt.-Registrationsnummern überprüft | Microsoft Docs"
description: "Sie können einen EU-Webdienst verwenden, um sicherzustellen, dass die USt-IdNr., die Sie auf Debitoren-, Kreditoren- oder Kontaktkarten eingeben, gültig sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="20fde-103">Vorgehensweise: Überprüfen der USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="20fde-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="20fde-104">Sie können einen EU-Webdienst verwenden, um sicherzustellen, dass die MwSt-IdNr., die Sie auf Debitoren-, Kreditoren- oder Kontaktkarten eingeben, gültig sind.</span><span class="sxs-lookup"><span data-stu-id="20fde-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="20fde-105">Wenn Sie das **MwSt-Identifikationsnr.** auf einer Karte ändern, auf der der Wert im Feld **Land/Regionencode** ein EU-Land/Region ist, wird die neue MwSt-Identifikationsnummer und Ihre Benutzer-ID im Feld **MwSt-Identifikationsnr.** protokolliert.</span><span class="sxs-lookup"><span data-stu-id="20fde-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="20fde-106">Überpürfen Sie die MwSt-IdNr., indem Sie die **Steuernummer** prüfen-Schaltfläche im **MwSt Identifikations-Protokoll**-Fenster auswählen.</span><span class="sxs-lookup"><span data-stu-id="20fde-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="20fde-107">Eine neue Zeile wird jedes Mal erzeugt, wenn Sie die Überprüfungsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="20fde-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="20fde-108">Wenn die Nummer verifiziert werden konnte, enthält das **Status**-Feld **Gültig**.</span><span class="sxs-lookup"><span data-stu-id="20fde-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="20fde-109">Wenn die Zahl nicht verifiziert werden konnte, enthält das **Status**-Feld **Ungültig**, und Sie müssen die Zahl im **MwSt Identifikationsnr.**-Feld auf der Karte ändern und die Überprüfungsfunktion erneut starten.</span><span class="sxs-lookup"><span data-stu-id="20fde-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="20fde-110">Die URL des Standardwebdiensts wird im Feld **MwSt Reg. Nr Prüfung URL** im Feld **Finanzbuchhaltung Einrichtung** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="20fde-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="20fde-111">In der **MwSt Registrierungsnummer-Format**-Tabelle können Sie für jedes Land/jede Region die verschiedenen Formate der MwSt-IdNr. ändern, die Benutzer im **MwSt-Registrierungsnummer**-Feld eingeben können.</span><span class="sxs-lookup"><span data-stu-id="20fde-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="20fde-112">Dieser Webdienst verwendet das HTTP-Protokoll, d. h., dass die Daten, die durch den Service übertragen werden, nicht verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="20fde-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="20fde-113">Möglicherweise treten Ausfallzeiten für diesen Service auf, für die Microsoft nicht verantwortlich ist, da der Service Teil eines breiten EU-Netzwerks nationaler MwSt.-Register ist.</span><span class="sxs-lookup"><span data-stu-id="20fde-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="20fde-114">Überprüfen der USt-IdNr. aus einer Debitorenkarte</span><span class="sxs-lookup"><span data-stu-id="20fde-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="20fde-115">Nachfolgend wird erläutert, wie einer MwSt-IdNr. eines Debitors überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="20fde-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="20fde-116">Die Schritte sind für einen Debitior ähnlich.</span><span class="sxs-lookup"><span data-stu-id="20fde-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="20fde-117">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="20fde-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="20fde-118">Öffnen Sie die Karte eines Debitors, auf der Sie die USt-IdNr. prüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="20fde-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="20fde-119">Das -Feld **Land-/Regionencode** der Debitorenkarte muss ein EU-Land/Region enthalten.</span><span class="sxs-lookup"><span data-stu-id="20fde-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="20fde-120">Wählen Sie im Inforegister **Rechnungsstellung** die Dropdownschaltfläche neben dem Feld **MwSt-Registrierungsnummer**aus.</span><span class="sxs-lookup"><span data-stu-id="20fde-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="20fde-121">Das **Protokoll MwSt-Registrierungs**-Fenster wird geöffnet und zeigt eine Zeile, in der das Feld **Status** **Nicht überprüft** enthält.</span><span class="sxs-lookup"><span data-stu-id="20fde-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="20fde-122">Wählen Sie die **Steuernummer prüfen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="20fde-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="20fde-123">Eine neue Zeile wird erstellt, wo das Feld **Status** entweder **Gültig** oder **Ungültig** enthält.</span><span class="sxs-lookup"><span data-stu-id="20fde-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="20fde-124">Wenn das -**Status**Feld  **Ungültig** enthält, ändern Sie die Nummer im **MwSt**-Feld auf der Karte, und wiederholen Sie dann die Schritte 3 bis 4.</span><span class="sxs-lookup"><span data-stu-id="20fde-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="20fde-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20fde-125">See Also</span></span>  
[<span data-ttu-id="20fde-126">Finanzen</span><span class="sxs-lookup"><span data-stu-id="20fde-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="20fde-127">Vorgehensweise: Einen neuen Debitor registrieren</span><span class="sxs-lookup"><span data-stu-id="20fde-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="20fde-128">Vorgehensweise: Einen neuen Kreditor registrieren</span><span class="sxs-lookup"><span data-stu-id="20fde-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="20fde-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20fde-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

