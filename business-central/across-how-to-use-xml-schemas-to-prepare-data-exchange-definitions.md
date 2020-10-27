---
title: Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen
description: Verwenden Sie XML-Schemata, um das Belegaustauschframework festzulegen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d2e600f3b2da20540e224cb1405a50adc4a31f25
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924953"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="f57d2-103">Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen</span><span class="sxs-lookup"><span data-stu-id="f57d2-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="f57d2-104">Um das Importieren/Exportieren von Daten in XML-Dateien durch das Datenaustauschframework in [!INCLUDE[d365fin](includes/d365fin_md.md)], können Sie das XML-Schema der Datei verwenden, um zu definieren, welche Datenelemente Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)] austauschen möchten.</span><span class="sxs-lookup"><span data-stu-id="f57d2-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f57d2-105">Sie führen diese Arbeit auf der Seite **XML-Schema-Ansicht** aus, indem Sie die XML-Schemadatei laden, die entsprechenden Datenelemente auswählen und dann eine Datenaustauschdefinition initialisieren.</span><span class="sxs-lookup"><span data-stu-id="f57d2-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="f57d2-106">Wenn Sie festgelegt haben, welche Datenelemente Sie auf Grundlage des XML-Schemas einschließen möchten, können Sie die Aktion **Datenaustauschdefinition generieren** verwenden, um eine Datenaustauschdefinition basierend auf den ausgewählten Datenelementen zu initialisieren, die Sie dann im Datenaustauschframework abschließen.</span><span class="sxs-lookup"><span data-stu-id="f57d2-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="f57d2-107">Dies erstellt einen Datensatz auf der Seite **Austauschdefinition buchen** . Darin legen Sie anschließend fest, welche Elemente in der Datei welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f57d2-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f57d2-108">Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f57d2-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="f57d2-109">In diesem Thema werden die folgenden Prozeduren beschrieben:</span><span class="sxs-lookup"><span data-stu-id="f57d2-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="f57d2-110">So laden Sie eine XML-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="f57d2-110">To load an XML schema file</span></span>  

- <span data-ttu-id="f57d2-111">So wählen oder löschen Sie Knoten in XML-Schema</span><span class="sxs-lookup"><span data-stu-id="f57d2-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="f57d2-112">So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="f57d2-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="f57d2-113">So laden Sie eine XML-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="f57d2-113">To load an XML schema file</span></span>

1. <span data-ttu-id="f57d2-114">Vergewissern Sie sich, dass die relevante XML-Schemadatei verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f57d2-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="f57d2-115">Die Dateierweiterung lautet „.xsd“.</span><span class="sxs-lookup"><span data-stu-id="f57d2-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="f57d2-116">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **XML-Schemas** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas** , and then choose the related link.</span></span>  

3. <span data-ttu-id="f57d2-117">Wählen Sie die Aktion **Neu** .</span><span class="sxs-lookup"><span data-stu-id="f57d2-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="f57d2-118">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f57d2-119">Feld</span><span class="sxs-lookup"><span data-stu-id="f57d2-119">Field</span></span>|<span data-ttu-id="f57d2-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f57d2-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f57d2-121">**Code**</span><span class="sxs-lookup"><span data-stu-id="f57d2-121">**Code**</span></span>|<span data-ttu-id="f57d2-122">Geben Sie einen Code an, um das XML-Schema zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f57d2-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="f57d2-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f57d2-123">**Description**</span></span>|<span data-ttu-id="f57d2-124">Geben Sie eine Beschreibung des XML-Schemas an.</span><span class="sxs-lookup"><span data-stu-id="f57d2-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="f57d2-125">Das Feld **Ziel-Namespace** gibt den Namespace in der XML-Schemadatei an, der für die Zeile geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="f57d2-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="f57d2-126">Wählen Sie die Aktion **Schema laden** und dann die XML-Schemadatei aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="f57d2-127">Wenn die Datei geladen wird, werden die restlichen Felder auf der Zeile mit Informationen aus der Datei ausgefüllt, und das Kontrollkästchen **Schema ist geladen** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f57d2-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f57d2-128">Die Struktur des geladenen XML-Schemas wird standardmäßig reduziert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f57d2-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="f57d2-129">Sie erweitern die einzelnen Knoten über die Schaltfläche **+** für den Knoten.</span><span class="sxs-lookup"><span data-stu-id="f57d2-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="f57d2-130">Um alle Knoten zu erweitern, wählen Sie **Alle aufklappen** auf dem Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="f57d2-131">So wählen oder löschen Sie Knoten in XML-Schema</span><span class="sxs-lookup"><span data-stu-id="f57d2-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="f57d2-132">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **XML-Schema-Viewer** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer** , and then choose the related link.</span></span>  

2. <span data-ttu-id="f57d2-133">Füllen Sie im Kopfbereich die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="f57d2-134">Feld</span><span class="sxs-lookup"><span data-stu-id="f57d2-134">Field</span></span>|<span data-ttu-id="f57d2-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f57d2-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f57d2-136">**XML-Schemacode**</span><span class="sxs-lookup"><span data-stu-id="f57d2-136">**XML Schema Code**</span></span>|<span data-ttu-id="f57d2-137">Geben Sie die XML-Schemadatei an, die Sie in Schritt 5 im Abschnitt „Laden der XML-Schemadatei“ geladen haben.</span><span class="sxs-lookup"><span data-stu-id="f57d2-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="f57d2-138">**Neue XMLport-Nr.**</span><span class="sxs-lookup"><span data-stu-id="f57d2-138">**New XMLport No.**</span></span>|<span data-ttu-id="f57d2-139">Geben Sie die Nummer des XMLport an, der von diesem XML-Schema erstellt wird, wenn Sie die Aktion **XMLport generieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="f57d2-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="f57d2-140">Die Zeilen werden nun mit den Knoten ausgefüllt, die alle Elemente im XML-Schema darstellen.</span><span class="sxs-lookup"><span data-stu-id="f57d2-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="f57d2-141">Knoten für Elemente, die entsprechend dem XML-Schema erforderlich sind, sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f57d2-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="f57d2-142">Erweitern Sie in der ersten Zeile in der Spalte **Knotenname** , das Dokument **Knoten** , und erweitern Sie schrittweise die zugrundeliegenden Knoten, die Sie einsehen möchten.</span><span class="sxs-lookup"><span data-stu-id="f57d2-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="f57d2-143">Oder klicken Sie mit der rechten Maustaste auf einen Knoten, und wählen Sie dann **Alle aufklappen** aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-143">Alternatively, right-click on a node and then choose **Expand All** .</span></span>  

4. <span data-ttu-id="f57d2-144">Wählen Sie eine der folgenden Aktionen, um zu ändern, welche Knoten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f57d2-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="f57d2-145">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="f57d2-145">**Action**</span></span>|<span data-ttu-id="f57d2-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f57d2-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="f57d2-147">**Alle anzeigen**</span><span class="sxs-lookup"><span data-stu-id="f57d2-147">**Show All**</span></span>|<span data-ttu-id="f57d2-148">Alle Knoten werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f57d2-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="f57d2-149">**Nicht notwendige ausblenden**</span><span class="sxs-lookup"><span data-stu-id="f57d2-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="f57d2-150">Nur Knoten, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f57d2-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="f57d2-151">Diese Knoten werden in der Regel durch eine **1** im -Feld **MinOccurs** angegeben.</span><span class="sxs-lookup"><span data-stu-id="f57d2-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="f57d2-152">Wählen Sie **Alle anzeigen** , um die Ansicht umzukehren.</span><span class="sxs-lookup"><span data-stu-id="f57d2-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="f57d2-153">**Nicht ausgewählte ausblenden**</span><span class="sxs-lookup"><span data-stu-id="f57d2-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="f57d2-154">Nur Knoten, in denen das Kontrollkästchen **Ausgewählt** aktiviert ist, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f57d2-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="f57d2-155">Wählen Sie **Alle anzeigen** , um die Ansicht umzukehren.</span><span class="sxs-lookup"><span data-stu-id="f57d2-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="f57d2-156">Wählen Sie die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="f57d2-157">Geben Sie mit dem **Ausgewählt** -Kontrollkästchen für jeden Knoten an, ob das Element im Datenaustauschdefinition für die entsprechende SEPA-Bankdatei unterstützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f57d2-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f57d2-158">Wenn Sie den erforderlichen untergeordneten Knoten auswählen, werden alle übergeordneten Knoten dafür aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f57d2-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="f57d2-159">Wählen Sie die Aktion **Alle erforderlichen Elemente auswählen** aus, um alle Knoten erneut auszuwählen, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f57d2-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="f57d2-160">Wählen Sie die Aktion **Auswahl aufheben** aus, um alle Auswahlen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f57d2-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="f57d2-161">Das Feld **Wahl** gibt an, dass der Knoten zwei oder mehr gleichgeordnete Knoten hat, die als Optionen fungieren.</span><span class="sxs-lookup"><span data-stu-id="f57d2-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="f57d2-162">So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="f57d2-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="f57d2-163">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **XML-Schemas** ein, und wählen Sie dann den entsprechenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="f57d2-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas** , and then choose the related link.</span></span>  

2. <span data-ttu-id="f57d2-164">Wählen Sie das entsprechende XML-Schema aus und wählen Sie dann die Aktion **XML Schema Viewer öffnen** .</span><span class="sxs-lookup"><span data-stu-id="f57d2-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="f57d2-165">Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="f57d2-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="f57d2-166">Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.</span><span class="sxs-lookup"><span data-stu-id="f57d2-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="f57d2-167">Wählen Sie auf der Seite **XML Schema Viewer** die Aktion **Datenaustauschdefinition generieren** .</span><span class="sxs-lookup"><span data-stu-id="f57d2-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="f57d2-168">Eine Datenaustauschdefinition wird auf der Seite **Austauschdefinition buchen** erstellt, die Sie vervollständigen können, indem Sie festlegen, welche Elemente in der Datei welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f57d2-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f57d2-169">Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f57d2-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="f57d2-170">Sie können auch die Funktion **Dateistruktur abrufen** im Fenster **Austauschdefinition buchen** verwenden. Hier wird die Funktion auf der Seite **SML Schema Viewer** eingesetzt, um das Inforegister **Spaltendefinitionen** vorab auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="f57d2-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="f57d2-171">In der Veröffentlichungswelle 1 von 2019 und früheren Versionen konnten Sie einen auf dem Schema basierenden XMLport generieren und diesen anschließend in Ihre Lösung importieren.</span><span class="sxs-lookup"><span data-stu-id="f57d2-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="f57d2-172">Dies wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f57d2-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="f57d2-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f57d2-173">See Also</span></span>

[<span data-ttu-id="f57d2-174">Richten Sie Datenaustauschdefinitionen ein.</span><span class="sxs-lookup"><span data-stu-id="f57d2-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="f57d2-175">Zahlungen in eine Bankdatei exportieren</span><span class="sxs-lookup"><span data-stu-id="f57d2-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="f57d2-176">Erfassen von Zahlungen per Lastschriftverfahren SEPA</span><span class="sxs-lookup"><span data-stu-id="f57d2-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="f57d2-177">Über das Datenaustauschframework</span><span class="sxs-lookup"><span data-stu-id="f57d2-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  
