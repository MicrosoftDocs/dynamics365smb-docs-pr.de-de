---
title: 'Gewusst wie: Einrichten und Exportieren von Umsatzsteuervoranmeldungen'
description: In Business Central können Sie die Umsatzsteuervoranmeldungsdatei-Benachrichtigung elektronisch an das Portal übermitteln.
services: project-madeira
documentationcenter: ''
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/22/2019
ms.author: soalex
ms.openlocfilehash: 10b1074eb84244be07f8b7a633e95068223efe4e
ms.sourcegitcommit: bf5f89dfaf5ad9f8f9902941cf3dac3e9f3553e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594203"
---
# <a name="sales-vat-advance-notifications"></a><span data-ttu-id="08f9f-103">Umsatzsteuervoranmeldungen</span><span class="sxs-lookup"><span data-stu-id="08f9f-103">Sales VAT Advance Notifications</span></span>  
<span data-ttu-id="08f9f-104">Eine Umsatzsteuervoranmeldung in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] ist eine XML-Datei, die Sie verwenden können, um MwSt die deutsche Steuerbehörden an dem das Elektronische Steuererklärungen (ELSTER) - Onlineportal zu melden.</span><span class="sxs-lookup"><span data-stu-id="08f9f-104">A Sales VAT Advance Notification in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] is an XML file that you can use to report VAT to the German tax authorities on the Elektronische Steuererklärungen (ELSTER) online portal.</span></span> <span data-ttu-id="08f9f-105">Die XML-Datei enthält Steuerbeträge und Bemessungsgrundlagen und Informationen über den Mandanten und wird im Format und im Layout erstellt, die deutsche Finanzämter benötigen.</span><span class="sxs-lookup"><span data-stu-id="08f9f-105">The XML file includes tax and base amounts, and information about your company, and is created in the format and layout that German tax authorities require.</span></span>    

## <a name="set-up-and-export-sales-vat-advance-notifications"></a><span data-ttu-id="08f9f-106">Einrichten und Exportieren von Umsatzsteuervoranmeldungen</span><span class="sxs-lookup"><span data-stu-id="08f9f-106">Set Up and Export Sales VAT Advance Notifications</span></span>
<span data-ttu-id="08f9f-107">Um gültige Umsatzsteuervoranmeldungen zu erstellen, müssen Sie Folgendes einrichten:</span><span class="sxs-lookup"><span data-stu-id="08f9f-107">To create valid sales VAT advance notifications, you must set up the following:</span></span>  

- <span data-ttu-id="08f9f-108">Die Firmendaten und die Steuerinformationen.</span><span class="sxs-lookup"><span data-stu-id="08f9f-108">The company registration information and tax office information.</span></span>  
- <span data-ttu-id="08f9f-109">Grundlegende Umsatzsteuervoranmeldung auf der Seite **Elektronische Mehrwertsteuerdeklaration einrichten**.</span><span class="sxs-lookup"><span data-stu-id="08f9f-109">Basic sales VAT advance notification on the **Electronic VAT Decl. Setup** page.</span></span>
- <span data-ttu-id="08f9f-110">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="08f9f-110">The VAT statement.</span></span>  

### <a name="to-set-up-company-information"></a><span data-ttu-id="08f9f-111">Um Unternehmensinformationen einzurichten:</span><span class="sxs-lookup"><span data-stu-id="08f9f-111">To set up company information</span></span>  
1. <span data-ttu-id="08f9f-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol \"Nach Seite oder Bericht suchen\"") aus, geben Sie **Unternehmensdaten** ein, und wählen Sie dann den verknüpften Link aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Company Information**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08f9f-113">Auf der Seite **Firmendaten** im Inforegister Allgemein, im Feld **MwSt-Vertreter**, geben Sie die Kontaktperson für MwSt-bezogene Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="08f9f-113">On the **Company Information** page, in the **VAT Representative** field, enter the contact person for VAT related information.</span></span>  
3. <span data-ttu-id="08f9f-114">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-114">Choose the **OK** button.</span></span>  

### <a name="to-set-up-the-electronic-vat-decl-setup"></a><span data-ttu-id="08f9f-115">Elektronische Mehrwertsteuerdeklaration einrichten</span><span class="sxs-lookup"><span data-stu-id="08f9f-115">To set up the Electronic VAT Decl. Setup</span></span>
1. <span data-ttu-id="08f9f-116">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Elektronische Mehrwertsteuerdeklaration einrichten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-116">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Electronic VAT Decl. Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="08f9f-117">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-117">Fill in the fields as described in the following table.</span></span>

|<span data-ttu-id="08f9f-118">Feld</span><span class="sxs-lookup"><span data-stu-id="08f9f-118">Field</span></span>|<span data-ttu-id="08f9f-119">Description</span><span class="sxs-lookup"><span data-stu-id="08f9f-119">Description</span></span>|
|-----|-----|
|<span data-ttu-id="08f9f-120">**USt.-Voranmeldungsnr.**</span><span class="sxs-lookup"><span data-stu-id="08f9f-120">**Sales VAT Adv. Notif. Nos.**</span></span>|<span data-ttu-id="08f9f-121">Wählen Sie den Nummernseriencode, der zum Zuweisen von Nummern zur Umsatzsteuervoranmeldung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08f9f-121">Choose the number series to use to assign identification numbers to new sales VAT advance notifications.</span></span>|
|<span data-ttu-id="08f9f-122">**USt.-Voranmeldungspfad**</span><span class="sxs-lookup"><span data-stu-id="08f9f-122">**Sales VAT Adv. Notif. Path**</span></span>|<span data-ttu-id="08f9f-123">Gibt den Pfad und den Namen des Ordners an, in dem Sie die XML-Dateien speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="08f9f-123">Enter the path and name of the folder where you want to store the XML files.</span></span>|
|<span data-ttu-id="08f9f-124">**Standardname der XML-Datei**</span><span class="sxs-lookup"><span data-stu-id="08f9f-124">**XML File Default Name**</span></span>|<span data-ttu-id="08f9f-125">Geben Sie den Namen der Datei ein.</span><span class="sxs-lookup"><span data-stu-id="08f9f-125">Enter the name of the file.</span></span>|

### <a name="to-set-up-a-vat-statement-for-sales-vat-advance-notifications"></a><span data-ttu-id="08f9f-126">Um MwSt-Berichte für Umsatzsteuervoranmeldungs-Benachrichtigungen einzurichten</span><span class="sxs-lookup"><span data-stu-id="08f9f-126">To set up a VAT statement for sales VAT advance notifications</span></span>  
1.  <span data-ttu-id="08f9f-127">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **MwSt-Bericht** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-127">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Statement**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="08f9f-128">Wählen Sie auf der Seite **MwSt-Bericht** im Feld **Name**, den Drop-Down-Pfeil.</span><span class="sxs-lookup"><span data-stu-id="08f9f-128">On the **VAT Statement** page, in the **Name** field, choose the drop-down arrow.</span></span>  
3.  <span data-ttu-id="08f9f-129">Auf der Seite **MwSt.-Abrechnungsnamen** in der Zeile für den entsprechenden MwSt.-Abrechnungsnamen wählen Sie das Feld **Verkaufs MwSt-Benachrichtigung** aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-129">On the **VAT Statement Names** page, in the line for the appropriate VAT statement name, select the **Sales VAT Adv. Notification** check box.</span></span>

> [!NOTE]  
 >  <span data-ttu-id="08f9f-130">Die MwSt.-Abrechnung muss eine MwSt.-Abrechnungszeile für jede Kennzahl aufweisen, die vom Finanzamt, in der **Zeilennr.** gefordert wird</span><span class="sxs-lookup"><span data-stu-id="08f9f-130">The VAT statement must have a VAT statement line for each key figure required by the tax authority, where the **Row No.**</span></span> <span data-ttu-id="08f9f-131">Feld enthält die Kennzahl und das Feld **Betragsart** gibt an, ob es sich um eine Bemessungsgrundlage oder um einen Steuerbetrag handelt.</span><span class="sxs-lookup"><span data-stu-id="08f9f-131">field contains the key figure and the **Amount Type** field specifies whether this is a base amount or a tax amount.</span></span> <span data-ttu-id="08f9f-132">Wenden Sie sich an Ihr Finanzamt, wenn Fragen zu den Schlüsselnummern und ihrer Definition bestehen.</span><span class="sxs-lookup"><span data-stu-id="08f9f-132">Ask your tax office if you have questions concerning the key figures and their definition.</span></span>

4. <span data-ttu-id="08f9f-133">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-133">Choose the **OK** button.</span></span>  

## <a name="to-create-an-xml-document-for-sales-vat-advance-notification"></a><span data-ttu-id="08f9f-134">So erstellen Sie ein XML-Dokument für Umsatzsteuervoranmeldung</span><span class="sxs-lookup"><span data-stu-id="08f9f-134">To create an XML document for Sales VAT advance notification</span></span>  
1. <span data-ttu-id="08f9f-135">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”") aus, und geben Sie **Umsatzsteuervoranmeldungsliste** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-135">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Vat Advanced Notification List**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08f9f-136">Auf der Seite **Umsatzsteuervoranmeldungsliste** auf der Registerkarte Aktionen, wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-136">On the **Sales Vat Advanced Notification List** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="08f9f-137">Füllen Sie auf der Seite **MehrwertsteuerLagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-137">On the **Sales VAT Adv. Notif. Card** page, fill in the fields.</span></span>
4. <span data-ttu-id="08f9f-138">Wählen Sie **Verarbeiten** und wählen die **XML-Datei erstellen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-138">Choose **Process**, and then choose the **Create XML-File** action.</span></span>  
5. <span data-ttu-id="08f9f-139">Wählen Sie auf Seite **XML - MwSt Kontennachweis erstellen** im Feld **XML-Datei**, wählen Sie entweder **Erstellen** oder die Option **Erstellen und exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-139">On the **Create XML - VAT Adv. Notif.** page, in the **XML-File** field, choose either the **Create** or the **Create and Export** option.</span></span>  
6. <span data-ttu-id="08f9f-140">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="08f9f-140">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="08f9f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08f9f-141">See Also</span></span>
[<span data-ttu-id="08f9f-142">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="08f9f-142">VAT Reporting</span></span>](vat-reporting.md)  
[<span data-ttu-id="08f9f-143">Lokale Funktion (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="08f9f-143">Germany Local Functionality</span></span>](germany-local-functionality.md)
