---
title: 'Gewusst wie: Einrichten und Exportieren von Umsatzsteuervoranmeldungen'
description: In Business Central können Sie die Umsatzsteuervoranmeldungsdatei-Benachrichtigung elektronisch an das Portal übermitteln.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: soalex
ms.openlocfilehash: 7af3ad9bd1684b069148b4e00d63037a1abb4ff3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920060"
---
# <a name="sales-vat-advance-notifications"></a><span data-ttu-id="93d85-103">Umsatzsteuervoranmeldungen</span><span class="sxs-lookup"><span data-stu-id="93d85-103">Sales VAT Advance Notifications</span></span>  
<span data-ttu-id="93d85-104">Eine Umsatzsteuervoranmeldung in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] ist eine XML-Datei, die Sie verwenden können, um MwSt die deutsche Steuerbehörden an dem das Elektronische Steuererklärungen (ELSTER) - Onlineportal zu melden.</span><span class="sxs-lookup"><span data-stu-id="93d85-104">A Sales VAT Advance Notification in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] is an XML file that you can use to report VAT to the German tax authorities on the Elektronische Steuererklärungen (ELSTER) online portal.</span></span> <span data-ttu-id="93d85-105">Die XML-Datei enthält Steuerbeträge und Bemessungsgrundlagen und Informationen über den Mandanten und wird im Format und im Layout erstellt, die deutsche Finanzämter benötigen.</span><span class="sxs-lookup"><span data-stu-id="93d85-105">The XML file includes tax and base amounts, and information about your company, and is created in the format and layout that German tax authorities require.</span></span>    

> [!NOTE]
 >  <span data-ttu-id="93d85-106">Der größte Teil der Funktionen ist in der Erweiterung **ELSTER VAT-Lokalisierung für Deutschland** enthalten.</span><span class="sxs-lookup"><span data-stu-id="93d85-106">Most of the functionality is included in the **ELSTER VAT Localization for Germany** Extension.</span></span> <span data-ttu-id="93d85-107">Stellen Sie sicher, dass dies in Ihrem [!INCLUDE[prodshort](../../includes/prodshort.md)] installiert ist.</span><span class="sxs-lookup"><span data-stu-id="93d85-107">Make sure that this is installed in your [!INCLUDE[prodshort](../../includes/prodshort.md)].</span></span>
 
 
## <a name="set-up-and-export-sales-vat-advance-notifications"></a><span data-ttu-id="93d85-108">Einrichten und Exportieren von Umsatzsteuervoranmeldungen</span><span class="sxs-lookup"><span data-stu-id="93d85-108">Set Up and Export Sales VAT Advance Notifications</span></span>
<span data-ttu-id="93d85-109">Um gültige Umsatzsteuervoranmeldungen zu erstellen, müssen Sie Folgendes einrichten:</span><span class="sxs-lookup"><span data-stu-id="93d85-109">To create valid sales VAT advance notifications, you must set up the following:</span></span>  

- <span data-ttu-id="93d85-110">Die Firmendaten und die Steuerinformationen.</span><span class="sxs-lookup"><span data-stu-id="93d85-110">The company registration information and tax office information.</span></span>  
- <span data-ttu-id="93d85-111">Grundlegende Umsatzsteuervoranmeldung auf der Seite **Elektronische Mehrwertsteuerdeklaration einrichten**.</span><span class="sxs-lookup"><span data-stu-id="93d85-111">Basic sales VAT advance notification on the **Electronic VAT Decl. Setup** page.</span></span>
- <span data-ttu-id="93d85-112">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="93d85-112">The VAT statement.</span></span>  

### <a name="to-set-up-company-information"></a><span data-ttu-id="93d85-113">Um Unternehmensinformationen einzurichten:</span><span class="sxs-lookup"><span data-stu-id="93d85-113">To set up company information</span></span>  
1. <span data-ttu-id="93d85-114">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Unternehmensinformationen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="93d85-114">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93d85-115">Auf der Seite **Firmendaten** im Inforegister Allgemein, im Feld **MwSt-Vertreter**, geben Sie die Kontaktperson für MwSt-bezogene Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="93d85-115">On the **Company Information** page, in the **VAT Representative** field, enter the contact person for VAT related information.</span></span>  
3. <span data-ttu-id="93d85-116">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-116">Choose the **OK** button.</span></span>  

### <a name="to-set-up-the-electronic-vat-decl-setup"></a><span data-ttu-id="93d85-117">Elektronische Mehrwertsteuerdeklaration einrichten</span><span class="sxs-lookup"><span data-stu-id="93d85-117">To set up the Electronic VAT Decl. Setup</span></span>
1. <span data-ttu-id="93d85-118">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Electronic VAT-Erkl.-Einrichtung** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="93d85-118">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Electronic VAT Decl. Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="93d85-119">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-119">Fill in the fields as described in the following table.</span></span>

|<span data-ttu-id="93d85-120">Feld</span><span class="sxs-lookup"><span data-stu-id="93d85-120">Field</span></span>|<span data-ttu-id="93d85-121">Description</span><span class="sxs-lookup"><span data-stu-id="93d85-121">Description</span></span>|
|-----|-----|
|<span data-ttu-id="93d85-122">**USt.-Voranmeldungsnr.**</span><span class="sxs-lookup"><span data-stu-id="93d85-122">**Sales VAT Adv. Notif. Nos.**</span></span>|<span data-ttu-id="93d85-123">Wählen Sie den Nummernseriencode, der zum Zuweisen von Nummern zur Umsatzsteuervoranmeldung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93d85-123">Choose the number series to use to assign identification numbers to new sales VAT advance notifications.</span></span>|
|<span data-ttu-id="93d85-124">**USt.-Voranmeldungspfad**</span><span class="sxs-lookup"><span data-stu-id="93d85-124">**Sales VAT Adv. Notif. Path**</span></span>|<span data-ttu-id="93d85-125">Gibt den Pfad und den Namen des Ordners an, in dem Sie die XML-Dateien speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="93d85-125">Enter the path and name of the folder where you want to store the XML files.</span></span>|
|<span data-ttu-id="93d85-126">**Standardname der XML-Datei**</span><span class="sxs-lookup"><span data-stu-id="93d85-126">**XML File Default Name**</span></span>|<span data-ttu-id="93d85-127">Geben Sie den Namen der Datei ein.</span><span class="sxs-lookup"><span data-stu-id="93d85-127">Enter the name of the file.</span></span>|

### <a name="to-set-up-a-vat-statement-for-sales-vat-advance-notifications"></a><span data-ttu-id="93d85-128">Um MwSt-Berichte für Umsatzsteuervoranmeldungs-Benachrichtigungen einzurichten</span><span class="sxs-lookup"><span data-stu-id="93d85-128">To set up a VAT statement for sales VAT advance notifications</span></span>  
1.  <span data-ttu-id="93d85-129">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") öffnet, geben Sie **MwSt.-Abrechnung** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="93d85-129">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Statement**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="93d85-130">Wählen Sie auf der Seite **MwSt-Bericht** im Feld **Name**, den Drop-Down-Pfeil.</span><span class="sxs-lookup"><span data-stu-id="93d85-130">On the **VAT Statement** page, in the **Name** field, choose the drop-down arrow.</span></span>  
3.  <span data-ttu-id="93d85-131">Auf der Seite **MwSt.-Abrechnungsnamen** in der Zeile für den entsprechenden MwSt.-Abrechnungsnamen wählen Sie das Feld **Verkaufs MwSt-Benachrichtigung** aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-131">On the **VAT Statement Names** page, in the line for the appropriate VAT statement name, select the **Sales VAT Adv. Notification** check box.</span></span>

> [!NOTE]  
 >  <span data-ttu-id="93d85-132">Die MwSt.-Abrechnung muss eine MwSt.-Abrechnungszeile für jede Kennzahl aufweisen, die vom Finanzamt, in der **Zeilennr.** gefordert wird</span><span class="sxs-lookup"><span data-stu-id="93d85-132">The VAT statement must have a VAT statement line for each key figure required by the tax authority, where the **Row No.**</span></span> <span data-ttu-id="93d85-133">Feld enthält die Kennzahl und das Feld **Betragsart** gibt an, ob es sich um eine Bemessungsgrundlage oder um einen Steuerbetrag handelt.</span><span class="sxs-lookup"><span data-stu-id="93d85-133">field contains the key figure and the **Amount Type** field specifies whether this is a base amount or a tax amount.</span></span> <span data-ttu-id="93d85-134">Wenden Sie sich an Ihr Finanzamt, wenn Fragen zu den Schlüsselnummern und ihrer Definition bestehen.</span><span class="sxs-lookup"><span data-stu-id="93d85-134">Ask your tax office if you have questions concerning the key figures and their definition.</span></span>

4. <span data-ttu-id="93d85-135">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-135">Choose the **OK** button.</span></span>  

## <a name="to-create-an-xml-document-for-sales-vat-advance-notification"></a><span data-ttu-id="93d85-136">So erstellen Sie ein XML-Dokument für Umsatzsteuervoranmeldung</span><span class="sxs-lookup"><span data-stu-id="93d85-136">To create an XML document for Sales VAT advance notification</span></span>  
1. <span data-ttu-id="93d85-137">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Umsatzsteuer-Vorankündigungsliste** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="93d85-137">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Vat Advanced Notification List**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93d85-138">Auf der Seite **Umsatzsteuervoranmeldungsliste** auf der Registerkarte Aktionen, wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-138">On the **Sales Vat Advanced Notification List** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="93d85-139">Füllen Sie auf der Seite **MehrwertsteuerLagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-139">On the **Sales VAT Adv. Notif. Card** page, fill in the fields.</span></span>
4. <span data-ttu-id="93d85-140">Wählen Sie **Verarbeiten** und wählen die **XML-Datei erstellen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-140">Choose **Process**, and then choose the **Create XML-File** action.</span></span>  
5. <span data-ttu-id="93d85-141">Wählen Sie auf Seite **XML - MwSt Kontennachweis erstellen** im Feld **XML-Datei**, wählen Sie entweder **Erstellen** oder die Option **Erstellen und exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-141">On the **Create XML - VAT Adv. Notif.** page, in the **XML-File** field, choose either the **Create** or the **Create and Export** option.</span></span>  
6. <span data-ttu-id="93d85-142">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="93d85-142">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="93d85-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93d85-143">See Also</span></span>
[<span data-ttu-id="93d85-144">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="93d85-144">VAT Reporting</span></span>](vat-reporting.md)  
[<span data-ttu-id="93d85-145">Lokale Funktion (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="93d85-145">Germany Local Functionality</span></span>](germany-local-functionality.md)  
[<span data-ttu-id="93d85-146">Anpassen von Business Central mithilfe der Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="93d85-146">Customizing Business Central Using Extensions</span></span>](../../ui-extensions.md)  
