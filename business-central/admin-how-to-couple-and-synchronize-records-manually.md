---
title: Koppeln und Synchronisieren | Microsoft Docs
description: Die Synchronisierung einer Integrationstabellenzuordnung ermöglicht die Datensynchronisierung in allen Datensätzen in einer Tabelle in Business Central und der Dynamics 365 Sales-Tabellen, die gekoppelt sind.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: fa4d6cfe13662613a73c14d68542f8319798ea80
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752675"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="09544-103">Koppeln und Synchronisieren</span><span class="sxs-lookup"><span data-stu-id="09544-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="09544-104">Dieses Thema beschreibt, wie man einen oder mehrere Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] mit Datensätzen in Dataverse oder [!INCLUDE[crm_md](includes/crm_md.md)] koppelt.</span><span class="sxs-lookup"><span data-stu-id="09544-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="09544-105">Durch das Koppeln der Datensätze können Sie Dataverse-Informationen aus [!INCLUDE[prod_short](includes/prod_short.md)] anzeigen und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="09544-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="09544-106">Die Kopplung ermöglicht Ihnen außerdem, Daten zwischen den Datensätzen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="09544-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="09544-107">Sie können vorhandene Datensätze koppeln, oder Sie erstellen und koppeln neue Datensätze.</span><span class="sxs-lookup"><span data-stu-id="09544-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="09544-108">Die Kopplung und Synchronisierung von Daten ist nur verfügbar, wenn Ihr Systemadministrator eine Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Dataverse oder [!INCLUDE[crm_md](includes/crm_md.md)] hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="09544-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="09544-109">Eine schnelle Art dies sicherzustellen ist, die Karte **Debitor** zu öffnen und nach der **Kopplung einrichten**-Aktion zu suchen.</span><span class="sxs-lookup"><span data-stu-id="09544-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="09544-110">Wenn die Aktion verfügbar ist, sind die Apps verbunden.</span><span class="sxs-lookup"><span data-stu-id="09544-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="09544-111">Video-Beispiel</span><span class="sxs-lookup"><span data-stu-id="09544-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="09544-112">So koppeln Sie einen Datensatz</span><span class="sxs-lookup"><span data-stu-id="09544-112">To couple a record</span></span>  
1.  <span data-ttu-id="09544-113">In [!INCLUDE[prod_short](includes/prod_short.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="09544-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="09544-114">Zum Beispiel den die Debitor- oder Kontaktkarte.</span><span class="sxs-lookup"><span data-stu-id="09544-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="09544-115">Sie können auch einfach die Listenseite öffnen und den Datensatz auswählen, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="09544-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="09544-116">Wählen Sie die **Kopplung einrichten**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="09544-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="09544-117">Füllen Sie die Felder aus, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="09544-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="09544-118">So synchronisieren Sie einen einzelnen Datensatz</span><span class="sxs-lookup"><span data-stu-id="09544-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="09544-119">In [!INCLUDE[prod_short](includes/prod_short.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="09544-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="09544-120">Zum Beispiel den die Debitor- oder Kontaktkarte.</span><span class="sxs-lookup"><span data-stu-id="09544-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="09544-121">Wählen Sie die **Jetzt synchronisieren**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="09544-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="09544-122">Wenn ein Datensatz in eine Richtung synchronisiert werden kann, wählen Sie die Option, die die Richtung der Datenaktualisierung angibt, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="09544-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="09544-123">So synchronisieren Sie einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] aus</span><span class="sxs-lookup"><span data-stu-id="09544-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="09544-124">Öffnen Sie in [!INCLUDE[crm_md](includes/crm_md.md)] das Formular für den Datensatz, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="09544-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="09544-125">Zum Beispiel das Formular „Kontokarte“ oder „Kontaktkarte“.</span><span class="sxs-lookup"><span data-stu-id="09544-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="09544-126">Wählen Sie die Aktion **[!INCLUDE[prod_short](includes/prod_short.md)]** in der Multifunktionsleiste, um den Datensatz automatisch zu öffnen und zu koppeln.</span><span class="sxs-lookup"><span data-stu-id="09544-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="09544-127">Sie können einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] nur dann automatisch synchronisieren, wenn **Synchronisieren nur gekoppelte Datensätze** deaktiviert ist und die Synchronisierungsrichtung auf der Seite **Integrationstabellenzuordnung** für den Datensatz auf Bidirektional oder Von Integrationstabelle eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="09544-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="09544-128">Weitere Informationen finden Sie unter [Zuordnen der zu synchronisierenden Tabellen und Felder](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="09544-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="09544-129">So synchronisieren Sie mehrere Datensätze</span><span class="sxs-lookup"><span data-stu-id="09544-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="09544-130">Öffnen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die Listenseite für den Datensatz, beispielsweise die Listenseiten "Debitoren" oder "Kontakte".</span><span class="sxs-lookup"><span data-stu-id="09544-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="09544-131">Wählen Sie die Datensätze aus, die Sie synchronisieren möchten, und wählen Sie die Aktion **Jetzt synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="09544-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="09544-132">Wenn Datensätze in eine Richtung synchronisiert werden können, wählen Sie die Option, die die Richtung angibt, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="09544-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="09544-133">Kopplung von Datensätzen aufheben</span><span class="sxs-lookup"><span data-stu-id="09544-133">Uncoupling Records</span></span>
<span data-ttu-id="09544-134">Sie können einen oder mehrere Datensätze von Listenseiten oder der Seite **Fehler bei der Synchronisierung gekoppelter Daten** durch Auswahl einer oder mehrerer Zeilen und Auswahl von **Kopplung löschen** entkoppeln.</span><span class="sxs-lookup"><span data-stu-id="09544-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="09544-135">Sie können auch alle Kupplungen für eine oder mehrere Tabellenzuordnungen auf der Seite **Zuordnungen der Integrationstabelle** entfernen.</span><span class="sxs-lookup"><span data-stu-id="09544-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="09544-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09544-136">See Also</span></span>  
[<span data-ttu-id="09544-137">Verwenden von Dynamics 365 Sales von Business Central</span><span class="sxs-lookup"><span data-stu-id="09544-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
