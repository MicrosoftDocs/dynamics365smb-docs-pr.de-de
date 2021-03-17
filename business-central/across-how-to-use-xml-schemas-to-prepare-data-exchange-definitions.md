---
title: Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen
description: Verwenden Sie XML-Schemata, um das Belegaustauschframework festzulegen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 25073b552644c9ca013a2eae90a0d013ab57e556
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379423"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="04117-103">Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen</span><span class="sxs-lookup"><span data-stu-id="04117-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="04117-104">Um das Importieren/Exportieren von Daten in XML-Dateien durch das Datenaustauschframework in [!INCLUDE[prod_short](includes/prod_short.md)], können Sie das XML-Schema der Datei verwenden, um zu definieren, welche Datenelemente Sie mit [!INCLUDE[prod_short](includes/prod_short.md)] austauschen möchten.</span><span class="sxs-lookup"><span data-stu-id="04117-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[prod_short](includes/prod_short.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="04117-105">Sie führen diese Arbeit auf der Seite **XML-Schema-Ansicht** aus, indem Sie die XML-Schemadatei laden, die entsprechenden Datenelemente auswählen und dann eine Datenaustauschdefinition initialisieren.</span><span class="sxs-lookup"><span data-stu-id="04117-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="04117-106">Wenn Sie festgelegt haben, welche Datenelemente Sie auf Grundlage des XML-Schemas einschließen möchten, können Sie die Aktion **Datenaustauschdefinition generieren** verwenden, um eine Datenaustauschdefinition basierend auf den ausgewählten Datenelementen zu initialisieren, die Sie dann im Datenaustauschframework abschließen.</span><span class="sxs-lookup"><span data-stu-id="04117-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="04117-107">Dies erstellt einen Datensatz auf der Seite **Austauschdefinition buchen**. Darin legen Sie anschließend fest, welche Elemente in der Datei welchen Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="04117-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="04117-108">Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="04117-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="04117-109">In diesem Thema werden die folgenden Prozeduren beschrieben:</span><span class="sxs-lookup"><span data-stu-id="04117-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="04117-110">So laden Sie eine XML-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="04117-110">To load an XML schema file</span></span>  

- <span data-ttu-id="04117-111">So wählen oder löschen Sie Knoten in XML-Schema</span><span class="sxs-lookup"><span data-stu-id="04117-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="04117-112">So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="04117-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="04117-113">So laden Sie eine XML-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="04117-113">To load an XML schema file</span></span>

1. <span data-ttu-id="04117-114">Vergewissern Sie sich, dass die relevante XML-Schemadatei verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="04117-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="04117-115">Die Dateierweiterung lautet „.xsd“.</span><span class="sxs-lookup"><span data-stu-id="04117-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="04117-116">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **XML-Schemas** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="04117-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="04117-117">Wählen Sie die Aktion **Neu**.</span><span class="sxs-lookup"><span data-stu-id="04117-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="04117-118">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="04117-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="04117-119">Feld</span><span class="sxs-lookup"><span data-stu-id="04117-119">Field</span></span>|<span data-ttu-id="04117-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04117-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="04117-121">**Code**</span><span class="sxs-lookup"><span data-stu-id="04117-121">**Code**</span></span>|<span data-ttu-id="04117-122">Geben Sie einen Code an, um das XML-Schema zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="04117-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="04117-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="04117-123">**Description**</span></span>|<span data-ttu-id="04117-124">Geben Sie eine Beschreibung des XML-Schemas an.</span><span class="sxs-lookup"><span data-stu-id="04117-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="04117-125">Das Feld **Ziel-Namespace** gibt den Namespace in der XML-Schemadatei an, der für die Zeile geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="04117-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="04117-126">Wählen Sie die Aktion **Schema laden** und dann die XML-Schemadatei aus.</span><span class="sxs-lookup"><span data-stu-id="04117-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="04117-127">Wenn die Datei geladen wird, werden die restlichen Felder auf der Zeile mit Informationen aus der Datei ausgefüllt, und das Kontrollkästchen **Schema ist geladen** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="04117-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="04117-128">Die Struktur des geladenen XML-Schemas wird standardmäßig reduziert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="04117-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="04117-129">Sie erweitern die einzelnen Knoten über die Schaltfläche **+** für den Knoten.</span><span class="sxs-lookup"><span data-stu-id="04117-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="04117-130">Um alle Knoten zu erweitern, wählen Sie **Alle aufklappen** auf dem Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="04117-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="04117-131">So wählen oder löschen Sie Knoten in XML-Schema</span><span class="sxs-lookup"><span data-stu-id="04117-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="04117-132">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **XML-Schema-Viewer** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="04117-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="04117-133">Füllen Sie im Kopfbereich die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="04117-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="04117-134">Feld</span><span class="sxs-lookup"><span data-stu-id="04117-134">Field</span></span>|<span data-ttu-id="04117-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04117-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="04117-136">**XML-Schemacode**</span><span class="sxs-lookup"><span data-stu-id="04117-136">**XML Schema Code**</span></span>|<span data-ttu-id="04117-137">Geben Sie die XML-Schemadatei an, die Sie in Schritt 5 im Abschnitt „Laden der XML-Schemadatei“ geladen haben.</span><span class="sxs-lookup"><span data-stu-id="04117-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="04117-138">**Neue XMLport-Nr.**</span><span class="sxs-lookup"><span data-stu-id="04117-138">**New XMLport No.**</span></span>|<span data-ttu-id="04117-139">Geben Sie die Nummer des XMLport an, der von diesem XML-Schema erstellt wird, wenn Sie die Aktion **XMLport generieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="04117-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="04117-140">Die Zeilen werden nun mit den Knoten ausgefüllt, die alle Elemente im XML-Schema darstellen.</span><span class="sxs-lookup"><span data-stu-id="04117-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="04117-141">Knoten für Elemente, die entsprechend dem XML-Schema erforderlich sind, sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="04117-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="04117-142">Erweitern Sie in der ersten Zeile in der Spalte **Knotenname**, das Dokument **Knoten**, und erweitern Sie schrittweise die zugrundeliegenden Knoten, die Sie einsehen möchten.</span><span class="sxs-lookup"><span data-stu-id="04117-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="04117-143">Oder klicken Sie mit der rechten Maustaste auf einen Knoten, und wählen Sie dann **Alle aufklappen** aus.</span><span class="sxs-lookup"><span data-stu-id="04117-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="04117-144">Wählen Sie eine der folgenden Aktionen, um zu ändern, welche Knoten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="04117-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="04117-145">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="04117-145">**Action**</span></span>|<span data-ttu-id="04117-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04117-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="04117-147">**Alle anzeigen**</span><span class="sxs-lookup"><span data-stu-id="04117-147">**Show All**</span></span>|<span data-ttu-id="04117-148">Alle Knoten werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="04117-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="04117-149">**Nicht notwendige ausblenden**</span><span class="sxs-lookup"><span data-stu-id="04117-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="04117-150">Nur Knoten, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="04117-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="04117-151">Diese Knoten werden in der Regel durch eine **1** im -Feld **MinOccurs** angegeben.</span><span class="sxs-lookup"><span data-stu-id="04117-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="04117-152">Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.</span><span class="sxs-lookup"><span data-stu-id="04117-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="04117-153">**Nicht ausgewählte ausblenden**</span><span class="sxs-lookup"><span data-stu-id="04117-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="04117-154">Nur Knoten, in denen das Kontrollkästchen **Ausgewählt** aktiviert ist, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="04117-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="04117-155">Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.</span><span class="sxs-lookup"><span data-stu-id="04117-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="04117-156">Wählen Sie die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="04117-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="04117-157">Geben Sie mit dem **Ausgewählt**-Kontrollkästchen für jeden Knoten an, ob das Element im Datenaustauschdefinition für die entsprechende SEPA-Bankdatei unterstützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04117-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="04117-158">Wenn Sie den erforderlichen untergeordneten Knoten auswählen, werden alle übergeordneten Knoten dafür aktiviert.</span><span class="sxs-lookup"><span data-stu-id="04117-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="04117-159">Wählen Sie die Aktion **Alle erforderlichen Elemente auswählen** aus, um alle Knoten erneut auszuwählen, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="04117-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="04117-160">Wählen Sie die Aktion **Auswahl aufheben** aus, um alle Auswahlen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="04117-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="04117-161">Das Feld **Wahl** gibt an, dass der Knoten zwei oder mehr gleichgeordnete Knoten hat, die als Optionen fungieren.</span><span class="sxs-lookup"><span data-stu-id="04117-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="04117-162">So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="04117-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="04117-163">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **XML-Schemas** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="04117-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="04117-164">Wählen Sie das entsprechende XML-Schema aus und wählen Sie dann die Aktion **XML Schema Viewer öffnen**.</span><span class="sxs-lookup"><span data-stu-id="04117-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="04117-165">Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="04117-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="04117-166">Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.</span><span class="sxs-lookup"><span data-stu-id="04117-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="04117-167">Wählen Sie auf der Seite **XML Schema Viewer** die Aktion **Datenaustauschdefinition generieren**.</span><span class="sxs-lookup"><span data-stu-id="04117-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="04117-168">Eine Datenaustauschdefinition wird auf der Seite **Austauschdefinition buchen** erstellt, die Sie vervollständigen können, indem Sie festlegen, welche Elemente in der Datei welchen Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04117-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="04117-169">Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="04117-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="04117-170">Sie können auch die Funktion **Dateistruktur abrufen** im Fenster **Austauschdefinition buchen** verwenden. Hier wird die Funktion auf der Seite **SML Schema Viewer** eingesetzt, um das Inforegister **Spaltendefinitionen** vorab auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="04117-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="04117-171">In der Veröffentlichungswelle 1 von 2019 und früheren Versionen konnten Sie einen auf dem Schema basierenden XMLport generieren und diesen anschließend in Ihre Lösung importieren.</span><span class="sxs-lookup"><span data-stu-id="04117-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="04117-172">Dies wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04117-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="04117-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04117-173">See Also</span></span>

[<span data-ttu-id="04117-174">Richten Sie Datenaustauschdefinitionen ein.</span><span class="sxs-lookup"><span data-stu-id="04117-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="04117-175">Zahlungen in eine Bankdatei exportieren</span><span class="sxs-lookup"><span data-stu-id="04117-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="04117-176">Erfassen von Zahlungen per Lastschriftverfahren SEPA</span><span class="sxs-lookup"><span data-stu-id="04117-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="04117-177">Über das Datenaustauschframework</span><span class="sxs-lookup"><span data-stu-id="04117-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]