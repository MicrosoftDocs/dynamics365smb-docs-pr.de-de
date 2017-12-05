---
title: "Wählen Sie die Methode elektronischen Zahlungen aus | Microsoft Docs"
description: Verwalten Sie Zahlungen an Ihre Kreditoren, indem Sie eine Datei zusammen mit den Zahlungsinformationen von den Buch.-Blattzeilen exportieren.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 20ae505bc76b8971c678de9e2664653aa5032d6e
ms.contentlocale: de-de
ms.lasthandoff: 09/27/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="6da74-103">Nemen Sie Zahlungen mit dem Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor</span><span class="sxs-lookup"><span data-stu-id="6da74-103">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="6da74-104">Im Fenster **Zahlungsjournal** können Sie Zahlungen an Ihre Kreditoren verarbeiten, indem Sie eine Datei zusammen mit den Zahlungsinformationen von den Buch.-Blattzeilen exportieren.</span><span class="sxs-lookup"><span data-stu-id="6da74-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="6da74-105">Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6da74-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6da74-106"> unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6da74-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="6da74-107">Um SEPA-Banküberweisungen zu aktivieren, müssen Sie zunächst ein Bankkonto, einen Kreditor und das Fibu Buch.-Blatt anlegen, auf dem das Zahlungsausgangs Buch.-Blatt basiert.</span><span class="sxs-lookup"><span data-stu-id="6da74-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="6da74-108">Sie bereiten dann Zahlungen an Kreditoren vor, indem Sie das Fenster **Zahlungsjournal** automatisch mit fälligen Zahlungen mit angegebenen Buchungsdaten ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="6da74-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6da74-109">Wenn Sie geprüft haben, ob die Zahlungen erfolgreich von der Bank verarbeitet wurden, können Sie mit der Buchung der Zahlungsausgangs Buch.-Blattzeilen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="6da74-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="6da74-110">Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="6da74-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="6da74-111">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="6da74-111">**To**</span></span>|<span data-ttu-id="6da74-112">**Siehe**</span><span class="sxs-lookup"><span data-stu-id="6da74-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="6da74-113">Aktivieren Sie Bankdatenkonvertierungsfunktion, um eine beliebige Bankkontoauszugsdatei in ein Format umzuwandeln, das Sie importieren können, oder um Ihre exportierten Zahlungsdateien in das Format umzuwandeln, das Ihre Bank verlangt.</span><span class="sxs-lookup"><span data-stu-id="6da74-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="6da74-114">Gewusst wie: Einrichten des Bankdatenkonvertierungsservice</span><span class="sxs-lookup"><span data-stu-id="6da74-114">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="6da74-115">Richten Sie ein Bankkonto, einen Lieferanten und ein Zahlungsbuch für SEPA-Banküberweisung ein.</span><span class="sxs-lookup"><span data-stu-id="6da74-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="6da74-116">So wird's gemacht: SEPA-Kreditübertragungen einrichten</span><span class="sxs-lookup"><span data-stu-id="6da74-116">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="6da74-117">Füllen Sie das Zahlungsausgangs Buch.-Blatt mit Zeilen für fällige Zahlungen an Kreditoren, mit der Option, Buchungsdaten basierend auf dem Fälligkeitsdatum der zugehörigen Einkaufsbelege einzufügen.</span><span class="sxs-lookup"><span data-stu-id="6da74-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="6da74-118">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="6da74-118">Manage Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="6da74-119">Exportieren von Zahlungsausgangs Buch.-Blattzeilen in eine Datei im SEPA-Banküberweisungsformat.</span><span class="sxs-lookup"><span data-stu-id="6da74-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="6da74-120">Vorgehensweise: Zahlungen in eine Bankdatei exportieren</span><span class="sxs-lookup"><span data-stu-id="6da74-120">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="6da74-121">Prüfen Sie, welche Zahlungen exportiert wurden und in welche Dateien.</span><span class="sxs-lookup"><span data-stu-id="6da74-121">Review which payments have been exported and into which files.</span></span>|<span data-ttu-id="6da74-122">Kreditübertragungsjournale</span><span class="sxs-lookup"><span data-stu-id="6da74-122">Credit Transfer Registers</span></span>|  
|<span data-ttu-id="6da74-123">Wenn die elektronische Zahlung erfolgreich von der Bank verarbeitet wird, buchen Sie die Zahlungen.</span><span class="sxs-lookup"><span data-stu-id="6da74-123">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="6da74-124">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="6da74-124">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="6da74-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6da74-125">See Also</span></span>  
[<span data-ttu-id="6da74-126">Gewusst wie: Einrichten des Bankdatenkonvertierungsservice</span><span class="sxs-lookup"><span data-stu-id="6da74-126">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="6da74-127">So wird's gemacht: SEPA-Kreditübertragungen einrichten</span><span class="sxs-lookup"><span data-stu-id="6da74-127">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="6da74-128">[Verwalten von Verbindlichkeiten](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="6da74-128">[Manage Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="6da74-129">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="6da74-129">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="6da74-130">Einziehen von Zahlungen per Lastschriftverfahren SEPA</span><span class="sxs-lookup"><span data-stu-id="6da74-130">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

