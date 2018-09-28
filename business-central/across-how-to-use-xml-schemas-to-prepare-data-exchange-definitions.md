---
title: Erstellen Sie XMLports auf Grundlage von XML-Schemata | Microsoft Docs
description: Verwenden Sie XML-Schemata, um das Belegaustauschframework festzulegen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b0e4af3fb0f886727163cc36ba7df8234d5e2a19
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="a532b-103">Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen</span><span class="sxs-lookup"><span data-stu-id="a532b-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="a532b-104">Um das Importieren/Exportieren von Daten in XML-Dateien durch das Datenaustauschframework in [!INCLUDE[d365fin](includes/d365fin_md.md)], können Sie das XML-Schema der Datei verwenden, um zu definieren, welche Datenelemente Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)] austauschen möchten.</span><span class="sxs-lookup"><span data-stu-id="a532b-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a532b-105">Sie führen diese Arbeiten im Fenster **XML Schemaansicht** aus, indem Sie die XML-Schemadatei laden, die entsprechenden Datenelemente auswählen und dann entweder eine Datenaustauschdefinition oder einen XML-Port initialisieren.</span><span class="sxs-lookup"><span data-stu-id="a532b-105">You perform this work in the **XML Schema Viewer** window by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="a532b-106">Wenn Sie festgelegt haben, welche Datenelemente Sie auf Grundlage des XML-Schemas einschließen möchten, können Sie die Aktion **XML-Port generieren** verwenden, um das XML-Port-Objekt für den Import in den Object Designer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a532b-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="a532b-107">Sie können auch die Aktion **Datenaustauschdefinition generieren** verwenden, um eine Datenaustauschdefinition basierend auf den ausgewählten Datenelementen zu initialisieren, die Sie dann im Datenaustauschframework abschließen.</span><span class="sxs-lookup"><span data-stu-id="a532b-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="a532b-108">Dies erstellt einen Datensatz im Fenster **Austauschdefinition buchen**. Darin legen Sie anschließend fest, welche Elemente in der Datei welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a532b-108">This creates a record in the **Posting Exchange Definition** window where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a532b-109">Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="a532b-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="a532b-110">In diesem Thema werden die folgenden Prozeduren beschrieben:</span><span class="sxs-lookup"><span data-stu-id="a532b-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="a532b-111">So laden Sie eine XML-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="a532b-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="a532b-112">So wählen oder löschen Sie Knoten in XML-Schema</span><span class="sxs-lookup"><span data-stu-id="a532b-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="a532b-113">So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="a532b-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="a532b-114">So generieren Sie einen XML-Port für die Datei, der auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="a532b-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="a532b-115">Einen XMLPort in den Object Designer importieren</span><span class="sxs-lookup"><span data-stu-id="a532b-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="a532b-116">So laden Sie eine XML-Schemadatei</span><span class="sxs-lookup"><span data-stu-id="a532b-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="a532b-117">Vergewissern Sie sich, dass die relevante XML-Schemadatei verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a532b-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="a532b-118">Die Dateierweiterung lautet „.xsd“.</span><span class="sxs-lookup"><span data-stu-id="a532b-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="a532b-119">Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-119">In the **Search** box, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="a532b-120">Wählen Sie auf der Registerkarte **Start** in der Gruppe **Neu** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-120">On the **Home** tab, in the **New** group, choose **New**.</span></span>  

4.  <span data-ttu-id="a532b-121">Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a532b-122">Feld</span><span class="sxs-lookup"><span data-stu-id="a532b-122">Field</span></span>|<span data-ttu-id="a532b-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a532b-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a532b-124">**Code**</span><span class="sxs-lookup"><span data-stu-id="a532b-124">**Code**</span></span>|<span data-ttu-id="a532b-125">Geben Sie einen Code an, um das XML-Schema zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a532b-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="a532b-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a532b-126">**Description**</span></span>|<span data-ttu-id="a532b-127">Geben Sie eine Beschreibung des XML-Schemas an.</span><span class="sxs-lookup"><span data-stu-id="a532b-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="a532b-128">Das Feld **Ziel-Namespace** gibt den Namespace in der XML-Schemadatei an, der für die Zeile geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="a532b-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="a532b-129">Wählen Sie in der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Schema laden**, und wählen Sie dann die XML-Schemadatei.</span><span class="sxs-lookup"><span data-stu-id="a532b-129">On the **Home** tab, in the **Process** group, choose **Load Schema**, and then select the XML schema file.</span></span>  

     <span data-ttu-id="a532b-130">Wenn die Datei geladen wird, werden die restlichen Felder auf der Zeile mit Informationen aus der Datei ausgefüllt, und das Kontrollkästchen **Schema ist geladen** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a532b-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a532b-131">Die Struktur des geladenen XML-Schemas wird standardmäßig reduziert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a532b-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="a532b-132">Sie erweitern die einzelnen Knoten über die Schaltfläche **+** für den Knoten.</span><span class="sxs-lookup"><span data-stu-id="a532b-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="a532b-133">Um alle Knoten zu erweitern, wählen Sie **Alle aufklappen** auf dem Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="a532b-134">So wählen oder löschen Sie Knoten in XML-Schema</span><span class="sxs-lookup"><span data-stu-id="a532b-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="a532b-135">Geben Sie im Feld **Suchen** **XML Schema Viewer** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-135">In the **Search** box, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="a532b-136">Füllen Sie im Kopfbereich die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="a532b-137">Feld</span><span class="sxs-lookup"><span data-stu-id="a532b-137">Field</span></span>|<span data-ttu-id="a532b-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a532b-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a532b-139">**XML-Schemacode**</span><span class="sxs-lookup"><span data-stu-id="a532b-139">**XML Schema Code**</span></span>|<span data-ttu-id="a532b-140">Geben Sie die XML-Schemadatei an, die Sie in Schritt 5 im Abschnitt „Laden der XML-Schemadatei“ geladen haben.</span><span class="sxs-lookup"><span data-stu-id="a532b-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="a532b-141">**Neue New XMLport-Nr.**</span><span class="sxs-lookup"><span data-stu-id="a532b-141">**New XMLport No.**</span></span>|<span data-ttu-id="a532b-142">Geben Sie die Nummer des XMLPorts an, der von diesem XML-Schema erstellt wird, wenn Sie die Aktion **XMLPort generieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="a532b-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="a532b-143">Die Zeilen werden nun mit den Knoten ausgefüllt, die alle Elemente im XML-Schema darstellen.</span><span class="sxs-lookup"><span data-stu-id="a532b-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="a532b-144">Knoten für Elemente, die entsprechend dem XML-Schema erforderlich sind, sind standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a532b-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="a532b-145">Erweitern Sie in der ersten Zeile in der Spalte **Knotenname**, das Dokument **Knoten**, und erweitern Sie schrittweise die zugrundeliegenden Knoten, die Sie einsehen möchten.</span><span class="sxs-lookup"><span data-stu-id="a532b-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="a532b-146">Oder klicken Sie mit der rechten Maustaste auf einen Knoten, und wählen Sie dann **Alle aufklappen** aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="a532b-147">Auf der Registerkarte **Start** in der Gruppe **Ansicht** wählen Sie eine der folgenden Aktionen, um die anzuzeigenden Knoten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a532b-147">On the **Home** tab, in the **View** group, choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="a532b-148">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="a532b-148">**Action**</span></span>|<span data-ttu-id="a532b-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a532b-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="a532b-150">**Alle anzeigen**</span><span class="sxs-lookup"><span data-stu-id="a532b-150">**Show All**</span></span>|<span data-ttu-id="a532b-151">Alle Knoten werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a532b-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="a532b-152">**Nicht notwendige ausblenden**</span><span class="sxs-lookup"><span data-stu-id="a532b-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="a532b-153">Nur Knoten, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a532b-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="a532b-154">Diese Knoten werden in der Regel durch eine **1** im -Feld **MinOccurs**angegeben.</span><span class="sxs-lookup"><span data-stu-id="a532b-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="a532b-155">Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.</span><span class="sxs-lookup"><span data-stu-id="a532b-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="a532b-156">**Nicht ausgewählte ausblenden**</span><span class="sxs-lookup"><span data-stu-id="a532b-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="a532b-157">Nur Knoten, in denen das Kontrollkästchen **Ausgewählt** aktiviert ist, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a532b-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="a532b-158">Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.</span><span class="sxs-lookup"><span data-stu-id="a532b-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="a532b-159">Wählen Sie auf der Registerkarte **Start** in der Gruppe **Verwalten** die Option **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-159">On the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

6.  <span data-ttu-id="a532b-160">Geben Sie mit dem **Ausgewählt**-Kontrollkästchen für jeden Knoten an, ob das Element im Datenaustauschdefinition für die entsprechende SEPA-Bankdatei unterstützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a532b-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a532b-161">Wenn Sie den erforderlichen untergeordneten Knoten auswählen, werden alle übergeordneten Knoten dafür aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a532b-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="a532b-162">Wählen Sie die Aktion **Alle erforderlichen Elemente auswählen** aus, um alle Knoten erneut auszuwählen, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a532b-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="a532b-163">Wählen Sie die Aktion **Auswahl aufheben** aus, um alle Auswahlen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a532b-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="a532b-164">Das Feld **Wahl** gibt an, dass der Knoten zwei oder mehr gleichgeordnete Knoten hat, die als Optionen fungieren.</span><span class="sxs-lookup"><span data-stu-id="a532b-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="a532b-165">So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="a532b-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="a532b-166">Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-166">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="a532b-167">Wählen Sie das relevante XML-Schema aus und dann auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **XML-Schema-Viewer öffnen**.</span><span class="sxs-lookup"><span data-stu-id="a532b-167">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="a532b-168">Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="a532b-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="a532b-169">Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.</span><span class="sxs-lookup"><span data-stu-id="a532b-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="a532b-170">Wählen Sie im Fenster **XML Schema Viewer** auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **Datenaustauschdefinition generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-170">In the **XML Schema Viewer** window, on the **Home** tab, in the **Process** group, choose **Generate Data Exchange Definition**.</span></span>  

 <span data-ttu-id="a532b-171">Eine Datenaustauschdefinition wird im Fenster **Austauschdefinition buchen** erstellt, die Sie vervollständigen können, indem Sie festlegen, welche Elemente in der Datei welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a532b-171">A data exchange definition is created in the **Posting Exchange Definition** window, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a532b-172">Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="a532b-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a532b-173">Sie können auch die Funktion **Dateistruktur abrufen** im Fenster **Austauschdefinition buchen** verwenden. Hier wird die Funktion des Fensters **SML Schema Viewer** eingesetzt, um das Inforegister **Spaltendefinitionen** vorab auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="a532b-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** window, which uses the functionality of the **XML Schema Viewer** window to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="a532b-174">So generieren Sie einen XML-Port, der auf einem XML-Schema basiert</span><span class="sxs-lookup"><span data-stu-id="a532b-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="a532b-175">Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a532b-175">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="a532b-176">Wählen Sie das relevante XML-Schema aus und dann auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **XML-Schema-Viewer öffnen**.</span><span class="sxs-lookup"><span data-stu-id="a532b-176">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="a532b-177">Im **Neue XMLportnr.**</span><span class="sxs-lookup"><span data-stu-id="a532b-177">In the **New XMLport No.**</span></span> <span data-ttu-id="a532b-178">Feld geben Sie die Nummer an, die das neue XMLport-Objekt erhalten wird, wenn es erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="a532b-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="a532b-179">Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="a532b-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="a532b-180">Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.</span><span class="sxs-lookup"><span data-stu-id="a532b-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="a532b-181">Auf der Registerkarte **Start** in der Gruppe **Verarbeiten** wählen Sie **XMLPort generieren** aus und speichern Sie dann das Objekt als .txt- Datei an einem entsprechenden Speicherort.</span><span class="sxs-lookup"><span data-stu-id="a532b-181">On the **Home** tab, in the **Process** group, choose **Generate XMLport**, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="a532b-182">Importieren Sie neue XMLPort in der [!INCLUDE[d365fin](includes/d365fin_md.md)] Entwicklungsumgebung und kompilieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="a532b-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="a532b-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a532b-183">See Also</span></span>  
<span data-ttu-id="a532b-184">[Richten Sie Datenaustauschdefinitionen ein.](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="a532b-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="a532b-185">[Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="a532b-185">[Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="a532b-186">[Einziehen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="a532b-186">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="a532b-187">Über das Datenaustauschframework</span><span class="sxs-lookup"><span data-stu-id="a532b-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)

