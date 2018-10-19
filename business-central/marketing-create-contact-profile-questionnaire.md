---
title: Verwenden Sie Profile, um Kontakte zu klassifizieren
description: "Verwenden Sie Profilbefragungen, um Geschäftskontakten zu klassieren"
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2018
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6a69a5de1ac0d6e2d238415204ec95fad9af7b9b
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="6b4bf-103">Verwenden Sie Profilbefragungen, um Geschäftskontakten zu klassieren</span><span class="sxs-lookup"><span data-stu-id="6b4bf-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="6b4bf-104">Sie können Profilbefragungen einrichten, die Sie beim Eingeben der Informationen über die Profile Ihrer Kontakte verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="6b4bf-105">In jedem Fragebogen können Sie die unterschiedlichen Fragen einrichten, die Sie Ihren Kontakten stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="6b4bf-106">Sie können die Befragung auch dazu verwenden, um einige Fragen zum Kontakt, Debitor oder Kreditor automatisch zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="6b4bf-107">So fügen Sie eine Profilbefragung hinzu</span><span class="sxs-lookup"><span data-stu-id="6b4bf-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="6b4bf-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Fragebogen-Einrichtung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6b4bf-109">Wählen Sie auf der Registerkarte **Start** in der Gruppe **Neu** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-109">On the **Home** tab, in the **New** group, choose **New**.</span></span>  
3.  <span data-ttu-id="6b4bf-110">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="6b4bf-111">So fügen Sie einen Fragebogen einer Profilbefragung hinzu</span><span class="sxs-lookup"><span data-stu-id="6b4bf-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="6b4bf-112">Wählen Sie die relevante Profilbefragung aus. Wählen Sie auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **Einrichtung Befragung bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-112">Choose the relevant profile questionnaire, and then on the **Home** tab, in the **Process** group, choose **Edit Questionnaire Setup**.</span></span>  
2.  <span data-ttu-id="6b4bf-113">Wählen Sie in der ersten leeren Zeile im Feld **Art** die Option **Frage** aus, und geben Sie im Feld **Beschreibung** Ihre Frage ein.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="6b4bf-114">Füllen Sie die anderen Felder in dieser Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="6b4bf-115">Wählen Sie in der nächsten leeren Zeile im Feld **Art** die Option **Antwort** aus, und geben Sie im Feld **Beschreibung** Ihre Antwort ein.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="6b4bf-116">Wählen Sie im Feld **Priorität** die Priorität aus.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="6b4bf-117">Definieren Sie in den Feldern **Von Wert** und **Bis Wert** einen Punktbereich.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="6b4bf-118">Kontakte, die innerhalb des definierten Bereichs Punkte erhalten, erhalten die Antwort.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="6b4bf-119">Wiederholen Sie diese Schritte, um alle Fragen und Antworten für die Profilbefragung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="6b4bf-120">Nachdem Sie eine Befragung erstellt haben, müssen Sie Kontaktbewertungen zu erstellen, um Ihre Kontakte zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="6b4bf-121">Sie können auch Fragen einrichten, die automatisch auf Grundlage der Informationen in der Kontaktkarte bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="6b4bf-122">Wenn Sie eine Frage eingeben, die automatisch beantwortet werden soll, wählen Sie die Optionen <STRONG>Zeile</STRONG> und dann <STRONG>Fragendetails</STRONG> aus, um die Kriterien einzugeben, die zur automatischen Beantwortung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="6b4bf-123">Die automatische Klassifizierung von Kontakten</span><span class="sxs-lookup"><span data-stu-id="6b4bf-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="6b4bf-124">Sie können Ihre Kontakte nach Debitoren, Kreditoren und Kontaktinformationen klassifizieren, indem Sie in dem Fenster "Profilbefragung Einrichtung" automatisch beantwortete **Profilbefragungen** einrichten.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions in the **Profile Questionnaire Setup** window.</span></span>  

> [!NOTE]
> <span data-ttu-id="6b4bf-125">Nur als Debitor gespeicherten Kontakten kann eine Klassifizierung auf Debitordatenbasis zugeordnet werden und nur als Kreditor gespeicherten Kontakten kann eine Klassifizierung auf Kreditordatenbasis zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="6b4bf-126">Die automatische Klassifizierung wird nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="6b4bf-127">Deshalb können Sie die Profilbefragungen aktualisieren, nachdem Sie die Debitor-, Kreditor- oder Kontaktdaten aktualisiert haben, auf denen sie basieren.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="6b4bf-128">Nachdem Sie automatische beantwortete Profilbefragungen eingerichtet haben, werden dem Kontakt [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch die richtigen Antworten zugeordnet, wenn Sie die Profilbefragung mit diesen Fragen einem Kontakt zuordnen.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="6b4bf-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6b4bf-129">Example</span></span>
<span data-ttu-id="6b4bf-130">Sie können Ihre Kontakte danach klassifizieren, wie viel sie bei Ihnen gekauft haben:</span><span class="sxs-lookup"><span data-stu-id="6b4bf-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b4bf-131"><strong>Antwort</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="6b4bf-132"><strong>Gilt für</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b4bf-133">A</span><span class="sxs-lookup"><span data-stu-id="6b4bf-133">A</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-134">Kontakte, die für 500.000 MW oder mehr gekauft haben</span><span class="sxs-lookup"><span data-stu-id="6b4bf-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b4bf-135">B</span><span class="sxs-lookup"><span data-stu-id="6b4bf-135">B</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-136">Kontakte, die von 100.000 bis 499.000 MW gekauft haben</span><span class="sxs-lookup"><span data-stu-id="6b4bf-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b4bf-137">C</span><span class="sxs-lookup"><span data-stu-id="6b4bf-137">C</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-138">Kontakte, die für 99.999 MW oder weniger gekauft haben</span><span class="sxs-lookup"><span data-stu-id="6b4bf-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6b4bf-139">Füllen Sie hierzu das Fenster **Profilbefragung Einrichtung** folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="6b4bf-139">To do this, fill in the **Profile Questionnaire Setup** window as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b4bf-140"><strong>Art</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="6b4bf-141"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="6b4bf-142"><strong>Automatische Klassifizierung</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="6b4bf-143"><strong>Von Wert</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="6b4bf-144"><strong>Bis Wert</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b4bf-145">Frage</span><span class="sxs-lookup"><span data-stu-id="6b4bf-145">Question</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-146">ABC Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="6b4bf-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-147">Klicken Sie in das Feld, um ein Häkchen einzufügen.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b4bf-148">Antwort</span><span class="sxs-lookup"><span data-stu-id="6b4bf-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-149">A</span><span class="sxs-lookup"><span data-stu-id="6b4bf-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b4bf-150">500.000</span><span class="sxs-lookup"><span data-stu-id="6b4bf-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b4bf-151">Antwort</span><span class="sxs-lookup"><span data-stu-id="6b4bf-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-152">B</span><span class="sxs-lookup"><span data-stu-id="6b4bf-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b4bf-153">100.000</span><span class="sxs-lookup"><span data-stu-id="6b4bf-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-154">499.999</span><span class="sxs-lookup"><span data-stu-id="6b4bf-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b4bf-155">Antwort</span><span class="sxs-lookup"><span data-stu-id="6b4bf-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="6b4bf-156">L</span><span class="sxs-lookup"><span data-stu-id="6b4bf-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b4bf-157">99.999</span><span class="sxs-lookup"><span data-stu-id="6b4bf-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6b4bf-158">Füllen Sie dann das Fenster **Profilbefragungsdetails** folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="6b4bf-158">Then fill in the **Profile Question Details** window as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b4bf-159"><strong>Feld</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="6b4bf-160"><strong>Wert</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6b4bf-161"><strong>Debitorenklassifizierungsfeld</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="6b4bf-162"><emphasis>Verkauf (MW)</emphasis></span><span class="sxs-lookup"><span data-stu-id="6b4bf-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b4bf-163"><strong>Klassifizierungsmethode</strong></span><span class="sxs-lookup"><span data-stu-id="6b4bf-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="6b4bf-164"><emphasis>Definierter Wert</emphasis></span><span class="sxs-lookup"><span data-stu-id="6b4bf-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6b4bf-165">Wenn Sie einem Kontakt die Profilbefragung mit dieser Frage zuordnen, wird in die Profilzeilen der Kontaktkarte automatisch die entsprechende Antwort für diesen Kontakt eingetragen.</span><span class="sxs-lookup"><span data-stu-id="6b4bf-165">When you assign the profile questionnaire containing this question to a contact, the program automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b4bf-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b4bf-166">See Also</span></span>
[<span data-ttu-id="6b4bf-167">Kontaktpersonen erstellen</span><span class="sxs-lookup"><span data-stu-id="6b4bf-167">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="6b4bf-168">Anlegen von Kontaktpersonen</span><span class="sxs-lookup"><span data-stu-id="6b4bf-168">Create Contact Persons</span></span>](marketing-how-create-contact-persons.md)  
[<span data-ttu-id="6b4bf-169">Kontaktunternehmenerstellen</span><span class="sxs-lookup"><span data-stu-id="6b4bf-169">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  

