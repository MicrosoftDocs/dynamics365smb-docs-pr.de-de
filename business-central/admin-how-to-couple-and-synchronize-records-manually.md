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
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0c70b1ba34af32b7cf542149c8f15cb191761358
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308116"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="6ea7a-103">Datensätze manuell koppeln und synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6ea7a-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="6ea7a-104">In diesem Thema wird beschrieben, wie mindestens ein Datensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6ea7a-105">Durch das Koppeln der Datensätze können Sie [!INCLUDE[crm_md](includes/crm_md.md)]-Informationen aus [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="6ea7a-106">Die Kopplung ermöglicht Ihnen außerdem, Daten zwischen den Datensätzen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="6ea7a-107">Sie können vorhandene Datensätze koppeln, oder Sie erstellen und koppeln neue Datensätze.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="6ea7a-108">Das Koppeln und Synchronisieren von Daten mit [!INCLUDE[crm_md](includes/crm_md.md)] ist nur verfügbar, wenn Ihr Systemadministrator eine Verbindung zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6ea7a-109">Eine schnelle Art dies sicherzustellen ist, die Karte **Debitor** zu öffnen und nach der **Kopplung einrichten**-Aktion zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="6ea7a-110">Wenn die Aktion verfügbar ist, sind die Apps verbunden.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-110">If the action is available, the apps are connected.</span></span>   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="6ea7a-111">So koppeln Sie einen Datensatz</span><span class="sxs-lookup"><span data-stu-id="6ea7a-111">To couple a record</span></span>  
1.  <span data-ttu-id="6ea7a-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6ea7a-113">Zum Beispiel den die Debitor- oder Kontaktkarte.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="6ea7a-114">Sie können auch einfach die Listenseite öffnen und den Datensatz auswählen, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="6ea7a-115">Wählen Sie die **Kopplung einrichten**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="6ea7a-116">Füllen Sie die Felder aus, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="6ea7a-117">So synchronisieren Sie einen einzelnen Datensatz</span><span class="sxs-lookup"><span data-stu-id="6ea7a-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="6ea7a-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6ea7a-119">Zum Beispiel den die Debitor- oder Kontaktkarte.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="6ea7a-120">Wählen Sie die **Jetzt synchronisieren**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6ea7a-121">Falls ein Datensatz sowohl von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)] als auch von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert werden kann, wählen Sie die Option, die der Richtung der Datenaktualisierung entspricht, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="6ea7a-122">So synchronisieren Sie mehrere Datensätze</span><span class="sxs-lookup"><span data-stu-id="6ea7a-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="6ea7a-123">Öffnen Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] die Listenseite für den Datensatz, beispielsweise die Listenseiten "Debitoren" oder "Kontakte".</span><span class="sxs-lookup"><span data-stu-id="6ea7a-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="6ea7a-124">Wählen Sie die Datensätze aus, die Sie synchronisieren möchten, und wählen Sie die Aktion **Jetzt synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6ea7a-125">Falls Datensätze sowohl von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)] als auch von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert werden kann, wählen Sie die Option, die der Richtung der Datenaktualisierung entspricht, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6ea7a-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ea7a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ea7a-126">See Also</span></span>  
[<span data-ttu-id="6ea7a-127">Verwenden von Dynamics 365 Sales von Business Central</span><span class="sxs-lookup"><span data-stu-id="6ea7a-127">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
