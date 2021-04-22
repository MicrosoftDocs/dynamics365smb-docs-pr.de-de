---
title: Zahlungen und Abstimmungs-Erweiterung verwalten | Microsoft Docs
description: Diese Erweiterung macht es einfach, dass Exportdateien, die vorformatiert sind, den Bankbedingungen für elektronische Posten erfüllen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: fdd8fced06d8efd5ab6959267bfc0171c4decdd2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785060"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="65dc3-103">Die Zahlungs- und Abstimmungs-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="65dc3-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="65dc3-104">Machen Sie schnelle, fehlerfreie Zahlungen, indem Sie Dateien exportieren, die speziell für den Austausch mit Ihrem Kreditor oder Ihrer Bank formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="65dc3-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="65dc3-105">Diese Dateien beschleunigen die Zahlung und die Aussöhnungsprozesse und eliminieren Fehler, die auftreten können, wenn Sie versuchen, die Informationen über eine Bankwebsite einzugeben.</span><span class="sxs-lookup"><span data-stu-id="65dc3-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="65dc3-106">Diese Erweiterung unterstützt Dateiformate für mehrere dänische Banken.</span><span class="sxs-lookup"><span data-stu-id="65dc3-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="65dc3-107">Wenn Sie Zahlungsinformationen in eine Datei exportieren, packt die Erweiterungg die Daten in das Format, das Ihre Bank benötigt.</span><span class="sxs-lookup"><span data-stu-id="65dc3-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="65dc3-108">Beispielsweise enthalten die Formate Bankdaten-V3, BEC, SDC und FIK, die viele unterschiedliche Banken nutzen und einige, die mehr für bestimmte Banken spezialisiert sind, zum Beispiel, Danske Bank und Nordea.</span><span class="sxs-lookup"><span data-stu-id="65dc3-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="65dc3-109">Die Erweiterung enthält auch mehrere Formate für das Importieren und saldieren von Bankauszügen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="65dc3-110">Um die Erweiterung zu verwenden, müssen Sie das Format kennen, das die Bank oder der Kreditor benötigt.</span><span class="sxs-lookup"><span data-stu-id="65dc3-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="65dc3-111">Einige Banken oder Kreditoren können diese Information auf ihren Websites bereitstellen; Sie müssen möglicherweise die Serviceabteilung kontaktieren, um die Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="65dc3-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="65dc3-112">Unterstützte Bank-Formate</span><span class="sxs-lookup"><span data-stu-id="65dc3-112">Supported Bank Formats</span></span>
<span data-ttu-id="65dc3-113">Diese Erweiterung kann folgende Dateiformate-Zahlungsdateien anwenden:</span><span class="sxs-lookup"><span data-stu-id="65dc3-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="65dc3-114">BANKDATA-V3</span><span class="sxs-lookup"><span data-stu-id="65dc3-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="65dc3-115">BEC-INDLAND</span><span class="sxs-lookup"><span data-stu-id="65dc3-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="65dc3-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="65dc3-116">BEC-CSV</span></span>  
* <span data-ttu-id="65dc3-117">DANSKEBANK-CMKV</span><span class="sxs-lookup"><span data-stu-id="65dc3-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="65dc3-118">DANSKEBANK-CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="65dc3-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="65dc3-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="65dc3-119">DANSKEBANK</span></span>  
* <span data-ttu-id="65dc3-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="65dc3-120">FIK71</span></span>  
* <span data-ttu-id="65dc3-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="65dc3-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="65dc3-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="65dc3-122">NORDEA</span></span>  
* <span data-ttu-id="65dc3-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="65dc3-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="65dc3-124">SDC</span><span class="sxs-lookup"><span data-stu-id="65dc3-124">SDC</span></span>  
* <span data-ttu-id="65dc3-125">SDC-CSV</span><span class="sxs-lookup"><span data-stu-id="65dc3-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="65dc3-126">Erweiterungen einrichten</span><span class="sxs-lookup"><span data-stu-id="65dc3-126">To set up the extension</span></span>

<span data-ttu-id="65dc3-127">Es gibt mehrere Schritte, um beginnen zu können.</span><span class="sxs-lookup"><span data-stu-id="65dc3-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="65dc3-128">Zahlungsexport erlauben</span><span class="sxs-lookup"><span data-stu-id="65dc3-128">Allow payment data exports.</span></span> <span data-ttu-id="65dc3-129">Um Ihre Daten zu schützen, stehen diese nicht zeitnah zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="65dc3-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="65dc3-130">Einrichten von Einkauf und Verbindlichkeiten, sodass Sie nicht externen Belegnummern auf Rechnungen benötigen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="65dc3-131">Bei Bedarf können Sie die Referenznummer verwenden, um eine bestimmte Rechnung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="65dc3-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="65dc3-132">Gibt die Zahlungsform für jeden Kreditor an.</span><span class="sxs-lookup"><span data-stu-id="65dc3-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="65dc3-133">Zahlungsformen definieren, wie Sie Rechnungen an Kreditoren bezahlen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="65dc3-134">Beispielsweise Bank, Kasse, Scheck oder Konto.</span><span class="sxs-lookup"><span data-stu-id="65dc3-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="65dc3-135">Geben Sie die Art des Formats an, das Sie für jede Ihrer Bankkonten verwenden.</span><span class="sxs-lookup"><span data-stu-id="65dc3-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="65dc3-136">Zum Beispiel NORDEA, DANSKEBAN, SDC etc.</span><span class="sxs-lookup"><span data-stu-id="65dc3-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="65dc3-137">Darüber hinaus müssen Sie Kreditoren einer inländischen **Gen. Bus. Buchungsgruppe** und **Kreditorenbuchungsgruppe** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="65dc3-138">Die Land/Regions-Einstellung für den Kreditor muss Dänemark (DK) sein.</span><span class="sxs-lookup"><span data-stu-id="65dc3-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="65dc3-139">Weitere Informationen finden Sie unter [Einrichten von Buchungsgruppen](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="65dc3-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-prod_short-to-export-payment-data"></a><span data-ttu-id="65dc3-140">[!INCLUDE[prod_short](includes/prod_short.md)] erlauben, Zahlungsdaten zu exportieren</span><span class="sxs-lookup"><span data-stu-id="65dc3-140">To allow [!INCLUDE[prod_short](includes/prod_short.md)] to export payment data</span></span>

1. <span data-ttu-id="65dc3-141">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Zahlungsausgangs Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="65dc3-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="65dc3-142">Wählen Sie auf der Seite **Projekt Buch.-Blatt bearbeiten** das Feld **Bank** Stapel aus.</span><span class="sxs-lookup"><span data-stu-id="65dc3-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="65dc3-143">Wählen Sie das Kontrollkästchen **Zahlungsexport erlauben**.</span><span class="sxs-lookup"><span data-stu-id="65dc3-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="65dc3-144">Gibt die Zahlungsform für jeden Kreditor an.</span><span class="sxs-lookup"><span data-stu-id="65dc3-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="65dc3-145">Die folgende Tabelle zeigt die FIK- und Kombinationen von GIRO-Zahlungsformen an, die [!INCLUDE[prod_short](includes/prod_short.md)] unterstützen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[prod_short](includes/prod_short.md)] supports.</span></span>

|<span data-ttu-id="65dc3-146">Kombination</span><span class="sxs-lookup"><span data-stu-id="65dc3-146">Combination</span></span>|<span data-ttu-id="65dc3-147">01 eingeben</span><span class="sxs-lookup"><span data-stu-id="65dc3-147">Type 01</span></span> | <span data-ttu-id="65dc3-148">04 eingeben</span><span class="sxs-lookup"><span data-stu-id="65dc3-148">Type 04</span></span> | <span data-ttu-id="65dc3-149">71 eingeben</span><span class="sxs-lookup"><span data-stu-id="65dc3-149">Type 71</span></span> | <span data-ttu-id="65dc3-150">73 eingeben</span><span class="sxs-lookup"><span data-stu-id="65dc3-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="65dc3-151">Girokonto-Nr. oder FIK-Gläubigerrn.?</span><span class="sxs-lookup"><span data-stu-id="65dc3-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="65dc3-152">Girokontorn.</span><span class="sxs-lookup"><span data-stu-id="65dc3-152">Giro Account No.</span></span> | <span data-ttu-id="65dc3-153">Girokontorn.</span><span class="sxs-lookup"><span data-stu-id="65dc3-153">Giro Account No.</span></span> | <span data-ttu-id="65dc3-154">FIK-Kreditornummer</span><span class="sxs-lookup"><span data-stu-id="65dc3-154">FIK Creditor No.</span></span> | <span data-ttu-id="65dc3-155">FIK-Kreditornummer</span><span class="sxs-lookup"><span data-stu-id="65dc3-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="65dc3-156">Nachricht an Empfänger zulassen?</span><span class="sxs-lookup"><span data-stu-id="65dc3-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="65dc3-157">Ja</span><span class="sxs-lookup"><span data-stu-id="65dc3-157">Yes</span></span> |<span data-ttu-id="65dc3-158">Nein</span><span class="sxs-lookup"><span data-stu-id="65dc3-158">No</span></span> |<span data-ttu-id="65dc3-159">Nein</span><span class="sxs-lookup"><span data-stu-id="65dc3-159">No</span></span> | <span data-ttu-id="65dc3-160">Ja</span><span class="sxs-lookup"><span data-stu-id="65dc3-160">Yes</span></span> |
|<span data-ttu-id="65dc3-161">Enthält Zahlungs-Referenznummer?</span><span class="sxs-lookup"><span data-stu-id="65dc3-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="65dc3-162">Nein</span><span class="sxs-lookup"><span data-stu-id="65dc3-162">No</span></span> | <span data-ttu-id="65dc3-163">Ja, 16 Ziffern.</span><span class="sxs-lookup"><span data-stu-id="65dc3-163">Yes, 16 digits.</span></span> | <span data-ttu-id="65dc3-164">Ja, 15 Ziffern.</span><span class="sxs-lookup"><span data-stu-id="65dc3-164">Yes, 15 digits.</span></span> | <span data-ttu-id="65dc3-165">Nein</span><span class="sxs-lookup"><span data-stu-id="65dc3-165">No</span></span>|

1. <span data-ttu-id="65dc3-166">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Anbieter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="65dc3-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="65dc3-167">Öffnen Sie die Karte, erweitern Sie die Registerkarte **Zahlungen**, im Feld **Zahlungsform** und wählen Sie die Zahlungsform.</span><span class="sxs-lookup"><span data-stu-id="65dc3-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="65dc3-168">Abhängig von Ihrer Wahl müssen Sie weitere Felder ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="65dc3-169">Siehe die Tabelle oben für eine Beschreibung der Kombinationen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="65dc3-170">Das Adressformat definieren, um ein Bankkonto zu verwenden</span><span class="sxs-lookup"><span data-stu-id="65dc3-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="65dc3-171">Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="65dc3-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="65dc3-172">Öffnen Sie die Karte für das Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="65dc3-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="65dc3-173">Im Feld **Format Zahlungsexport** wählen Sie das Format für Ihre Exportdatei aus.</span><span class="sxs-lookup"><span data-stu-id="65dc3-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="65dc3-174">Auswählen des FIK oder der Autogirozahlungsinformationen für Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="65dc3-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="65dc3-175">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Einkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="65dc3-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="65dc3-176">Wählen Sie das Feld Debitor.</span><span class="sxs-lookup"><span data-stu-id="65dc3-176">Choose the vendor.</span></span> <span data-ttu-id="65dc3-177">Beachten Sie, dass dies ein dänischer Kreditor mit eine Adresse in Dänemark sein muss.</span><span class="sxs-lookup"><span data-stu-id="65dc3-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="65dc3-178">Eine Rechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-178">Create an invoice.</span></span> <span data-ttu-id="65dc3-179">Die Felder **Zahlungsform** und **Kreditorennummer** werden entsprechend den Einstellungen auf der Kreditorenkarte ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="65dc3-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="65dc3-180">Sie können diese bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="65dc3-180">You can change them if you want.</span></span>
4. <span data-ttu-id="65dc3-181">Geben Sie im Feld **Zahlungsreferenz** die Nummer mit 15 Ziffern von den Rechnungsbeträgen des Kreditors ein.</span><span class="sxs-lookup"><span data-stu-id="65dc3-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="65dc3-182">Sie müssen nur die letzten 11 Ziffern der Nummer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="65dc3-183">fügt vier Null für den Anfang der Nummer hinzu.</span><span class="sxs-lookup"><span data-stu-id="65dc3-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="65dc3-184">Buchen Sie die Rechnung.</span><span class="sxs-lookup"><span data-stu-id="65dc3-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="65dc3-185">Nutzung der Erweiterung, um Zahlungsdaten zu exportieren</span><span class="sxs-lookup"><span data-stu-id="65dc3-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="65dc3-186">Wählen Sie die ![Glühbirne , die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Zahlungsjournale** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="65dc3-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="65dc3-187">Wählen Sie die **Zahlungsvorschlag-Buch.-Blätter** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="65dc3-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="65dc3-188">Wenn Sie nur bestimmte Zahlungen exportieren möchten, können Sie die Optionen zum Filtern der Daten nutzen.</span><span class="sxs-lookup"><span data-stu-id="65dc3-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="65dc3-189">Bei Bedarf können Sie Filter hinzufügen, um nur bestimmte Zahlungen zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="65dc3-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="65dc3-190">Wählen Sie im Feld **Bankkontozahlungsart** die Option **Elektronische Zahlung** aus.</span><span class="sxs-lookup"><span data-stu-id="65dc3-190">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="65dc3-191">Wählen Sie die Aktion **Exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="65dc3-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="65dc3-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65dc3-192">See also</span></span>

<span data-ttu-id="65dc3-193">[Anpassen von Business Central für [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe der Erweiterungen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="65dc3-193">[Customizing Business Central for [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="65dc3-194">Erfassen von Zahlungen per Lastschriftverfahren SEPA</span><span class="sxs-lookup"><span data-stu-id="65dc3-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="65dc3-195">Arbeiten mit allgemeinen Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="65dc3-195">Working with General Journals</span></span>](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]