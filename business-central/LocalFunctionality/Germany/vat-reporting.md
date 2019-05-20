---
title: MwSt.-Abrechnung
description: MwSt.-Erklärungen können elektronisch übermittelt werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a3c70acef8f815a89b454e0282bada23408576bb
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241713"
---
# <a name="vat-reporting"></a><span data-ttu-id="1473a-103">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="1473a-103">VAT Reporting</span></span>
<span data-ttu-id="1473a-104">MwSt.-Erklärungen können elektronisch übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="1473a-104">You can report VAT electronically to the tax authorities.</span></span> <span data-ttu-id="1473a-105">Sie können eine XML-Datei generieren, elektronisch signieren, verschlüsseln und direkt an das ELSTER-Portal senden.</span><span class="sxs-lookup"><span data-stu-id="1473a-105">You can generate, electronically sign, encrypt, and send an XML file directly to the German ELSTER portal.</span></span> <span data-ttu-id="1473a-106">Antworten werden im selben Schritt empfangen und verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1473a-106">Response messages are received and processed in the same transaction.</span></span>  

<span data-ttu-id="1473a-107">Folgende lokale MwSt.-Erklärungen können gedruckt werden:</span><span class="sxs-lookup"><span data-stu-id="1473a-107">You can print the following local VAT reports.</span></span>  

|<span data-ttu-id="1473a-108">Bericht</span><span class="sxs-lookup"><span data-stu-id="1473a-108">Report</span></span>|<span data-ttu-id="1473a-109">Description</span><span class="sxs-lookup"><span data-stu-id="1473a-109">Description</span></span>|  
|------------|---------------------------------------|  
|<span data-ttu-id="1473a-110">**MwSt.-Abrechnung Meldung**</span><span class="sxs-lookup"><span data-stu-id="1473a-110">**VAT Statement Germany**</span></span>|<span data-ttu-id="1473a-111">Eine einfache MwSt.-Erklärung.</span><span class="sxs-lookup"><span data-stu-id="1473a-111">A simple VAT report.</span></span> <span data-ttu-id="1473a-112">Die MwSt.-Abrechnung erfolgt mithilfe der ELSTER-Funktion.</span><span class="sxs-lookup"><span data-stu-id="1473a-112">The main VAT reporting is handled by the ELSTER functionality.</span></span> <span data-ttu-id="1473a-113">Die Beträge werden nach steuerpflichtiger Basis und steuerpflichtigem Betrag aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="1473a-113">The amounts are differentiated by taxable base and taxable amount.</span></span><br /><br /> <span data-ttu-id="1473a-114">Dient als Basis für die MwSt.-Erfassung für einen ausgewählten Zeitraum und wird gemäß der MwSt.-Abrechnung in der Tabelle MwSt.-Abrechnungszeile gedruckt.</span><span class="sxs-lookup"><span data-stu-id="1473a-114">Serves as the basis for VAT registration for a selected period, and is printed according to the VAT statement in the VAT Statement Line table.</span></span><br /><br /> <span data-ttu-id="1473a-115">Verwenden Sie diese Erklärung in Verbindung mit der MwSt.-Korrektur.</span><span class="sxs-lookup"><span data-stu-id="1473a-115">Use this report in conjunction with VAT correction.</span></span>|  
|<span data-ttu-id="1473a-116">**UVA Kontennachweis**</span><span class="sxs-lookup"><span data-stu-id="1473a-116">**Sales VAT Adv. Not. Acc. Proof**</span></span>|<span data-ttu-id="1473a-117">Bestätigt, dass Posten im MwSt.-Abrechnungsformular auch in Finanzbuchhaltungskonten gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="1473a-117">Confirms that entries in the VAT statement form are also posted in general ledger accounts.</span></span><br /><br /> <span data-ttu-id="1473a-118">Wählen Sie zur Überprüfung der MwSt. im Fenster Umsatzsteuervoranmeldung für das MwSt.-Abrechnungsformular und die Umsatzsteuervoranmeldung die gleichen Einstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="1473a-118">To verify VAT in sales VAT advance notifications, select the same settings for the VAT statement form and the sales VAT advance notification.</span></span>|  
|<span data-ttu-id="1473a-119">**MwSt.-Abrechnung Schema**</span><span class="sxs-lookup"><span data-stu-id="1473a-119">**VAT Statement Schedule**</span></span>|<span data-ttu-id="1473a-120">Diese Erklärung kann auf der Seite **MwSt.-Abrechnung** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1473a-120">This report can be retrieved from the **VAT Statement** page.</span></span><br /><br /> <span data-ttu-id="1473a-121">Druckt die Einstellungen in der MwSt.-Abrechnung.</span><span class="sxs-lookup"><span data-stu-id="1473a-121">Prints the settings in the VAT statement.</span></span> <span data-ttu-id="1473a-122">Druckt die Einstellungen in der MwSt.-Abrechnung. Mithilfe des Berichts können die Merkmale von **MwSt Kontennachweis** gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="1473a-122">Using this report, you can print the characteristics of the **Sales VAT Adv. Not. Acc. Proof**.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="1473a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1473a-123">See Also</span></span>  
[<span data-ttu-id="1473a-124">So gehts: Melden von MwSt. an die Steuerbehörden</span><span class="sxs-lookup"><span data-stu-id="1473a-124">How To: Report VAT to the Tax Authorities</span></span>](../../finance-how-report-vat.md)  
[<span data-ttu-id="1473a-125">Arbeiten mit MwSt im Verkauf und Einkauf</span><span class="sxs-lookup"><span data-stu-id="1473a-125">Work with VAT on Sales and Purchases</span></span>](../../finance-work-with-vat.md)  
[<span data-ttu-id="1473a-126">Richten Sie Berichte für MwSt ein.</span><span class="sxs-lookup"><span data-stu-id="1473a-126">Set Up Reports for VAT and Intrastat</span></span>](how-to-set-up-reports-for-vat-and-intrastat.md)
