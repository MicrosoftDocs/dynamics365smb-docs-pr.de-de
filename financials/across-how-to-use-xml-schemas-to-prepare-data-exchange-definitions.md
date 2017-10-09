---
title: Erstellen Sie XMLports auf Grundlage von XML-Schemata | Microsoft Docs
description: Verwenden Sie XML-Schemata, um das Belegaustauschframework festzulegen.
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c4b53c6a87148990102ba9eca235cf139a48396e
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="6c67f-103">Gewusst wie: Verwenden von XML-Schemata zur Vorbereitung von Datenaustauschdefinitionen</span><span class="sxs-lookup"><span data-stu-id="6c67f-103">How to: Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="6c67f-104">Um das Importieren/Exportieren von Daten in XML-Dateien durch das Datenaustauschframework in [!INCLUDE[d365fin](includes/d365fin_md.md)], können Sie das XML-Schema der Datei verwenden, um zu definieren, welche Datenelemente Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)] austauschen möchten.</span><span class="sxs-lookup"><span data-stu-id="6c67f-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6c67f-105">Sie führen diese Arbeiten im Fenster **XML Schemaansicht** aus, indem Sie die XML-Schemadatei laden, die entsprechenden Datenelemente auswählen und dann entweder eine Datenaustauschdefinition oder einen XML-Port initialisieren.</span><span class="sxs-lookup"><span data-stu-id="6c67f-105">You perform this work in the **XML Schema Viewer** window by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="6c67f-106">Wenn Sie festgelegt haben, welche Datenelemente Sie auf Grundlage des XML-Schemas einschließen möchten, können Sie die Aktion **XML-Port generieren** verwenden, um das XML-Port-Objekt für den Import in den Object Designer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c67f-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="6c67f-107">Sie können auch die Aktion **Datenaustauschdefinition generieren** verwenden, um eine Datenaustauschdefinition basierend auf den ausgewählten Datenelementen zu initialisieren, die Sie dann im Datenaustauschframework abschließen.</span><span class="sxs-lookup"><span data-stu-id="6c67f-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="6c67f-108">Dies erstellt einen Datensatz im Fenster **Austauschdefinition buchen**. Darin legen Sie anschließend fest, welche Elemente in der Datei welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6c67f-108">This creates a record in the **Posting Exchange Definition** window where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6c67f-109">Für weitere Informationen, siehe [Gewusst wie: Einrichten des Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="6c67f-109">For more information, see [How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="6c67f-110">In diesem Thema werden die folgenden Prozeduren beschrieben:</span><span class="sxs-lookup"><span data-stu-id="6c67f-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="6c67f-111">So laden Sie eine XML-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="6c67f-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="6c67f-112">So wählen oder löschen Sie Knoten in XML-Schema</span><span class="sxs-lookup"><span data-stu-id="6c67f-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="6c67f-113">So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="6c67f-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="6c67f-114">So generieren Sie einen XML-Port für die Datei, der auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="6c67f-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="6c67f-115">Einen XMLPort in den Object Designer importieren</span><span class="sxs-lookup"><span data-stu-id="6c67f-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="6c67f-116">So laden Sie eine XML-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="6c67f-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="6c67f-117">Vergewissern Sie sich, dass die relevante XML-Schemadatei verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6c67f-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="6c67f-118">Die Dateierweiterung lautet „.xsd“.</span><span class="sxs-lookup"><span data-stu-id="6c67f-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="6c67f-119">Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-119">In the **Search** box, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="6c67f-120">Wählen Sie auf der Registerkarte **Start** in der Gruppe **Neu** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-120">On the **Home** tab, in the **New** group, choose **New**.</span></span>  

4.  <span data-ttu-id="6c67f-121">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="6c67f-122">Feld</span><span class="sxs-lookup"><span data-stu-id="6c67f-122">Field</span></span>|<span data-ttu-id="6c67f-123">[Beschreibung]</span><span class="sxs-lookup"><span data-stu-id="6c67f-123">[Description]</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6c67f-124">**Code**</span><span class="sxs-lookup"><span data-stu-id="6c67f-124">**Code**</span></span>|<span data-ttu-id="6c67f-125">Geben Sie einen Code an, um das XML-Schema zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6c67f-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="6c67f-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c67f-126">**Description**</span></span>|<span data-ttu-id="6c67f-127">Geben Sie eine Beschreibung des XML-Schemas an.</span><span class="sxs-lookup"><span data-stu-id="6c67f-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="6c67f-128">Das Feld **Ziel-Namespace** gibt den Namespace in der XML-Schemadatei an, der für die Zeile geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="6c67f-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="6c67f-129">Wählen Sie in der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Schema laden**, und wählen Sie dann die XML-Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="6c67f-129">On the **Home** tab, in the **Process** group, choose **Load Schema**, and then select the XML schema file.</span></span>  

     <span data-ttu-id="6c67f-130">Wenn die Datei geladen wird, werden die restlichen Felder auf der Zeile mit Informationen aus der Datei ausgefüllt, und das Kontrollkästchen **Schema ist geladen** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c67f-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6c67f-131">Die Struktur des geladenen XML-Schemas wird standardmäßig reduziert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c67f-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="6c67f-132">Sie erweitern die einzelnen Knoten über die Schaltfläche **+**für den Knoten.</span><span class="sxs-lookup"><span data-stu-id="6c67f-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="6c67f-133">Um alle Knoten zu erweitern, wählen Sie **Alle aufklappen** auf dem Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="6c67f-134">So wählen oder löschen Sie Knoten in XML-Schema</span><span class="sxs-lookup"><span data-stu-id="6c67f-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="6c67f-135">Geben Sie im Feld **Suchen** **XML Schema Viewer** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-135">In the **Search** box, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="6c67f-136">Füllen Sie im Kopfbereich die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="6c67f-137">Feld</span><span class="sxs-lookup"><span data-stu-id="6c67f-137">Field</span></span>|<span data-ttu-id="6c67f-138">Description</span><span class="sxs-lookup"><span data-stu-id="6c67f-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6c67f-139">**XML-Schemacode**</span><span class="sxs-lookup"><span data-stu-id="6c67f-139">**XML Schema Code**</span></span>|<span data-ttu-id="6c67f-140">Geben Sie die XML-Schemadatei an, die Sie in Schritt 5 im Abschnitt „Laden der XML-Schemadatei“ geladen haben.</span><span class="sxs-lookup"><span data-stu-id="6c67f-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="6c67f-141">**Neue New XMLport-Nr.**</span><span class="sxs-lookup"><span data-stu-id="6c67f-141">**New XMLport No.**</span></span>|<span data-ttu-id="6c67f-142">Geben Sie die Nummer des XMLPorts an, der von diesem XML-Schema erstellt wird, wenn Sie die Aktion **XMLPort generieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="6c67f-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="6c67f-143">Die Zeilen werden nun mit den Knoten ausgefüllt, die alle Elemente im XML-Schema darstellen.</span><span class="sxs-lookup"><span data-stu-id="6c67f-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="6c67f-144">Knoten für Elemente, die entsprechend dem XML-Schema erforderlich sind, sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c67f-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="6c67f-145">Erweitern Sie in der ersten Zeile in der Spalte **Knotenname**, das Dokument **Knoten**, und erweitern Sie schrittweise die zugrundeliegenden Knoten, die Sie einsehen möchten.</span><span class="sxs-lookup"><span data-stu-id="6c67f-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="6c67f-146">Oder klicken Sie mit der rechten Maustaste auf einen Knoten, und wählen Sie dann **Alle aufklappen** aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="6c67f-147">Auf der Registerkarte **Start** in der Gruppe **Ansicht** wählen Sie eine der folgenden Aktionen, um die anzuzeigenden Knoten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6c67f-147">On the **Home** tab, in the **View** group, choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="6c67f-148">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="6c67f-148">**Action**</span></span>|<span data-ttu-id="6c67f-149">Description</span><span class="sxs-lookup"><span data-stu-id="6c67f-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="6c67f-150">**Alle anzeigen**</span><span class="sxs-lookup"><span data-stu-id="6c67f-150">**Show All**</span></span>|<span data-ttu-id="6c67f-151">Alle Knoten werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c67f-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="6c67f-152">**Nicht notwendige ausblenden**</span><span class="sxs-lookup"><span data-stu-id="6c67f-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="6c67f-153">Nur Knoten, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c67f-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="6c67f-154">Diese Knoten werden in der Regel durch eine **1** im -Feld **MinOccurs**angegeben.</span><span class="sxs-lookup"><span data-stu-id="6c67f-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="6c67f-155">Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.</span><span class="sxs-lookup"><span data-stu-id="6c67f-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="6c67f-156">**Nicht ausgewählte ausblenden**</span><span class="sxs-lookup"><span data-stu-id="6c67f-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="6c67f-157">Nur Knoten, in denen das Kontrollkästchen **Ausgewählt** aktiviert ist, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c67f-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="6c67f-158">Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.</span><span class="sxs-lookup"><span data-stu-id="6c67f-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="6c67f-159">Wählen Sie auf der Registerkarte **Start** in der Gruppe **Verwalten** die Option **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-159">On the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

6.  <span data-ttu-id="6c67f-160">Geben Sie mit dem **Ausgewählt**-Kontrollkästchen für jeden Knoten an, ob das Element im Datenaustauschdefinition für die entsprechende SEPA-Bankdatei unterstützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c67f-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6c67f-161">Wenn Sie den erforderlichen untergeordneten Knoten auswählen, werden alle übergeordneten Knoten dafür aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6c67f-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="6c67f-162">Wählen Sie die Aktion **Alle erforderlichen Elemente auswählen** aus, um alle Knoten erneut auszuwählen, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6c67f-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="6c67f-163">Wählen Sie die Aktion **Auswahl aufheben** aus, um alle Auswahlen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6c67f-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="6c67f-164">Das Feld **Wahl** gibt an, dass der Knoten zwei oder mehr gleichgeordnete Knoten hat, die als Optionen fungieren.</span><span class="sxs-lookup"><span data-stu-id="6c67f-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="6c67f-165">So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="6c67f-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="6c67f-166">Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-166">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="6c67f-167">Wählen Sie das relevante XML-Schema aus und dann auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **XML-Schema-Viewer öffnen**.</span><span class="sxs-lookup"><span data-stu-id="6c67f-167">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="6c67f-168">Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="6c67f-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="6c67f-169">Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.</span><span class="sxs-lookup"><span data-stu-id="6c67f-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="6c67f-170">Wählen Sie im Fenster **XML Schema Viewer** auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **Datenaustauschdefinition generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-170">In the **XML Schema Viewer** window, on the **Home** tab, in the **Process** group, choose **Generate Data Exchange Definition**.</span></span>  

 <span data-ttu-id="6c67f-171">Eine Datenaustauschdefinition wird im Fenster **Austauschdefinition buchen** erstellt, die Sie vervollständigen können, indem Sie festlegen, welche Elemente in der Datei welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c67f-171">A data exchange definition is created in the **Posting Exchange Definition** window, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6c67f-172">Für weitere Informationen, siehe [Gewusst wie: Einrichten des Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="6c67f-172">For more information, see [How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6c67f-173">Sie können auch die Funktion **Dateistruktur abrufen** im Fenster **Austauschdefinition buchen** verwenden. Hier wird die Funktion des Fensters **SML Schema Viewer** eingesetzt, um das Inforegister **Spaltendefinitionen** vorab auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="6c67f-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** window, which uses the functionality of the **XML Schema Viewer** window to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="6c67f-174">So generieren Sie einen XML-Port, der auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="6c67f-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="6c67f-175">Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6c67f-175">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="6c67f-176">Wählen Sie das relevante XML-Schema aus und dann auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **XML-Schema-Viewer öffnen**.</span><span class="sxs-lookup"><span data-stu-id="6c67f-176">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="6c67f-177">Im **Neue XMLportnr.**</span><span class="sxs-lookup"><span data-stu-id="6c67f-177">In the **New XMLport No.**</span></span> <span data-ttu-id="6c67f-178">Feld geben Sie die Nummer an, die das neue XMLport-Objekt erhalten wird, wenn es erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="6c67f-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="6c67f-179">Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="6c67f-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="6c67f-180">Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.</span><span class="sxs-lookup"><span data-stu-id="6c67f-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="6c67f-181">Auf der Registerkarte **Start** in der Gruppe **Verarbeiten** wählen Sie **XMLPort generieren** aus und speichern Sie dann das Objekt als .txt- Datei an einem entsprechenden Speicherort.</span><span class="sxs-lookup"><span data-stu-id="6c67f-181">On the **Home** tab, in the **Process** group, choose **Generate XMLport**, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="6c67f-182">Importieren Sie neue XMLPort in der [!INCLUDE[d365fin](includes/d365fin_md.md)] Entwicklungsumgebung und kompilieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="6c67f-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c67f-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c67f-183">See Also</span></span>  
<span data-ttu-id="6c67f-184">[Vorgehensweise: Richten Sie Datenaustauschdefinitionen ein.](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="6c67f-184">[How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="6c67f-185">[Vorgehensweise: Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="6c67f-185">[How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="6c67f-186">[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="6c67f-186">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="6c67f-187">Über das Datenaustauschframework</span><span class="sxs-lookup"><span data-stu-id="6c67f-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)

