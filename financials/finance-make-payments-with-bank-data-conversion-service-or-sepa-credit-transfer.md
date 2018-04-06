---
title: "Nehmen Sie Zahlungen mit dem| Microsoft Docs Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor | Microsoft Docs"
description: Verwalten Sie Zahlungen an Ihre Kreditoren, indem Sie eine Datei zusammen mit den Zahlungsinformationen von den Buch.-Blattzeilen exportieren.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d9388a99585eea4e9e229a2f47982f9f690e3001
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="091a9-103">Nehmen Sie Zahlungen mit dem Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor</span><span class="sxs-lookup"><span data-stu-id="091a9-103">Making Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="091a9-104">Im Fenster **Zahlungsjournal** können Sie Zahlungen an Ihre Kreditoren verarbeiten, indem Sie eine Datei zusammen mit den Zahlungsinformationen von den Buch.-Blattzeilen exportieren.</span><span class="sxs-lookup"><span data-stu-id="091a9-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="091a9-105">Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="091a9-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="091a9-106"> unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="091a9-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="091a9-107">Um SEPA-Banküberweisungen zu aktivieren, müssen Sie zunächst ein Bankkonto, einen Kreditor und das Fibu Buch.-Blatt anlegen, auf dem das Zahlungsausgangs Buch.-Blatt basiert.</span><span class="sxs-lookup"><span data-stu-id="091a9-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="091a9-108">Sie bereiten dann Zahlungen an Kreditoren vor, indem Sie das Fenster **Zahlungsjournal** automatisch mit fälligen Zahlungen mit angegebenen Buchungsdaten ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="091a9-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="091a9-109">Wenn Sie geprüft haben, ob die Zahlungen erfolgreich von der Bank verarbeitet wurden, können Sie mit der Buchung der Zahlungsausgangs Buch.-Blattzeilen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="091a9-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="091a9-110">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="091a9-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="091a9-111">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="091a9-111">**To**</span></span>|<span data-ttu-id="091a9-112">**Siehe**</span><span class="sxs-lookup"><span data-stu-id="091a9-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="091a9-113">Aktivieren Sie Bankdatenkonvertierungsfunktion, um eine beliebige Bankkontoauszugsdatei in ein Format umzuwandeln, das Sie importieren können, oder um Ihre exportierten Zahlungsdateien in das Format umzuwandeln, das Ihre Bank verlangt.</span><span class="sxs-lookup"><span data-stu-id="091a9-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="091a9-114">Einrichten des Bankdatenkonvertierungsservice</span><span class="sxs-lookup"><span data-stu-id="091a9-114">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="091a9-115">Richten Sie ein Bankkonto, einen Lieferanten und ein Zahlungsbuch für SEPA-Banküberweisung ein.</span><span class="sxs-lookup"><span data-stu-id="091a9-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="091a9-116">Einrichten von SEPA-Kreditübertragung</span><span class="sxs-lookup"><span data-stu-id="091a9-116">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="091a9-117">Füllen Sie das Zahlungsausgangs Buch.-Blatt mit Zeilen für fällige Zahlungen an Kreditoren, mit der Option, Buchungsdaten basierend auf dem Fälligkeitsdatum der zugehörigen Einkaufsbelege einzufügen.</span><span class="sxs-lookup"><span data-stu-id="091a9-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="091a9-118">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="091a9-118">Managing Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="091a9-119">Exportieren von Zahlungsausgangs Buch.-Blattzeilen in eine Datei im SEPA-Banküberweisungsformat.</span><span class="sxs-lookup"><span data-stu-id="091a9-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="091a9-120">Zahlungen in eine Bankdatei exportieren</span><span class="sxs-lookup"><span data-stu-id="091a9-120">Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="091a9-121">Wenn die elektronische Zahlung erfolgreich von der Bank verarbeitet wird, buchen Sie die Zahlungen.</span><span class="sxs-lookup"><span data-stu-id="091a9-121">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="091a9-122">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="091a9-122">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="091a9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="091a9-123">See Also</span></span>  
[<span data-ttu-id="091a9-124">Einrichten des Bankdatenkonvertierungsservice</span><span class="sxs-lookup"><span data-stu-id="091a9-124">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="091a9-125">Einrichten von SEPA-Kreditübertragung</span><span class="sxs-lookup"><span data-stu-id="091a9-125">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="091a9-126">[Verwalten von Verbindlichkeiten](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="091a9-126">[Managing Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="091a9-127">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="091a9-127">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="091a9-128">Einziehen von Zahlungen per Lastschriftverfahren SEPA</span><span class="sxs-lookup"><span data-stu-id="091a9-128">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

