---
title: Datensätze manuell koppeln und synchronisieren | Microsoft Docs
description: Die Synchronisierung einer Integrationstabellenzuordnung ermöglicht die Datensynchronisierung in allen Datensätzen in einer Tabelle in Business Central und der Dynamics 365 Sales-Entität, die gekoppelt sind.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: fdc407ef26d238ba54a2566cdd9003c29da2eeb3
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196663"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="5e6a1-103">Datensätze manuell koppeln und synchronisieren</span><span class="sxs-lookup"><span data-stu-id="5e6a1-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="5e6a1-104">Dieses Thema beschreibt, wie man einen oder mehrere Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Datensätzen in Common Data Service oder [!INCLUDE[crm_md](includes/crm_md.md)] koppelt.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="5e6a1-105">Durch das Koppeln der Datensätze können Sie Common Data Service-Informationen aus [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-105">Coupling records lets you view Common Data Service information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="5e6a1-106">Die Kopplung ermöglicht Ihnen außerdem, Daten zwischen den Datensätzen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="5e6a1-107">Sie können vorhandene Datensätze koppeln, oder Sie erstellen und koppeln neue Datensätze.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="5e6a1-108">Die Kopplung und Synchronisierung von Daten ist nur verfügbar, wenn Ihr Systemadministrator eine Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Common Data Service oder [!INCLUDE[crm_md](includes/crm_md.md)] hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="5e6a1-109">Eine schnelle Art dies sicherzustellen ist, die Karte **Debitor** zu öffnen und nach der **Kopplung einrichten**-Aktion zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="5e6a1-110">Wenn die Aktion verfügbar ist, sind die Apps verbunden.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="5e6a1-111">Video-Beispiel</span><span class="sxs-lookup"><span data-stu-id="5e6a1-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="5e6a1-112">So koppeln Sie einen Datensatz</span><span class="sxs-lookup"><span data-stu-id="5e6a1-112">To couple a record</span></span>  
1.  <span data-ttu-id="5e6a1-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="5e6a1-114">Zum Beispiel den die Debitor- oder Kontaktkarte.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="5e6a1-115">Sie können auch einfach die Listenseite öffnen und den Datensatz auswählen, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="5e6a1-116">Wählen Sie die **Kopplung einrichten**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="5e6a1-117">Füllen Sie die Felder aus, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="5e6a1-118">So synchronisieren Sie einen einzelnen Datensatz</span><span class="sxs-lookup"><span data-stu-id="5e6a1-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="5e6a1-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="5e6a1-120">Zum Beispiel den die Debitor- oder Kontaktkarte.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="5e6a1-121">Wählen Sie die **Jetzt synchronisieren**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="5e6a1-122">Wenn ein Datensatz in eine Richtung synchronisiert werden kann, wählen Sie die Option, die die Richtung der Datenaktualisierung angibt, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="5e6a1-123">So synchronisieren Sie einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] aus</span><span class="sxs-lookup"><span data-stu-id="5e6a1-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="5e6a1-124">Öffnen Sie in [!INCLUDE[crm_md](includes/crm_md.md)] das Formular für den Datensatz, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="5e6a1-125">Zum Beispiel das Formular „Kontokarte“ oder „Kontaktkarte“.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="5e6a1-126">Wählen Sie die Aktion **[!INCLUDE[d365fin](includes/d365fin_md.md)]** in der Multifunktionsleiste, um den Datensatz automatisch zu öffnen und zu koppeln.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-126">Choose the **[!INCLUDE[d365fin](includes/d365fin_md.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="5e6a1-127">Sie können einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] nur dann automatisch synchronisieren, wenn **Synchronisieren nur gekoppelte Datensätze** deaktiviert ist und die Synchronisierungsrichtung auf der Seite **Integrationstabellenzuordnung** für den Datensatz auf Bidirektional oder Von Integrationstabelle eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="5e6a1-128">Weitere Informationen finden Sie unter [Zuordnen der zu synchronisierenden Tabellen und Felder](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="5e6a1-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="5e6a1-129">So synchronisieren Sie mehrere Datensätze</span><span class="sxs-lookup"><span data-stu-id="5e6a1-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="5e6a1-130">Öffnen Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] die Listenseite für den Datensatz, beispielsweise die Listenseiten "Debitoren" oder "Kontakte".</span><span class="sxs-lookup"><span data-stu-id="5e6a1-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="5e6a1-131">Wählen Sie die Datensätze aus, die Sie synchronisieren möchten, und wählen Sie die Aktion **Jetzt synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="5e6a1-132">Wenn Datensätze in eine Richtung synchronisiert werden können, wählen Sie die Option, die die Richtung angibt, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e6a1-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5e6a1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e6a1-133">See Also</span></span>  
[<span data-ttu-id="5e6a1-134">Verwenden von Dynamics 365 Sales von Business Central</span><span class="sxs-lookup"><span data-stu-id="5e6a1-134">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
