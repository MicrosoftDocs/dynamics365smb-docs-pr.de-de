---
title: Anzeigen und Arbeit in Excel aus Business Central | Microsoft Docs
description: "Mehr erfahren, wie Sie die Finanzaufstellungen in Microsoft Excel von  Business Central für eine Analyse der Daten öffnen können."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: 27c137ea6309d40cddc94bc676ec7ea27d5c01fa
ms.contentlocale: de-de
ms.lasthandoff: 01/22/2019

---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="85009-103">Anzeigen und Arbeit in Excel aus Business Central</span><span class="sxs-lookup"><span data-stu-id="85009-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="85009-104">Mit Seiten, die eine Liste der Datensätze in den Zeilen und Spalten anzeigen, wie eine Liste von Debitoren von Verkaufsaufträgen oder Rechnungen können Sie die Daten mithilfe von Microsoft Excel anzeigen.</span><span class="sxs-lookup"><span data-stu-id="85009-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="85009-105">Dazu haben Sie zwei Optionen.</span><span class="sxs-lookup"><span data-stu-id="85009-105">To do this, you have two options.</span></span> <span data-ttu-id="85009-106">Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="85009-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="85009-107">Der Unterschied zwischen den beiden Methoden ist der folgende:</span><span class="sxs-lookup"><span data-stu-id="85009-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="85009-108">In Excel öffnen</span><span class="sxs-lookup"><span data-stu-id="85009-108">Open in Excel</span></span>

-    <span data-ttu-id="85009-109">Mit dieser Aktion berücksichtigt Excel sämtliche Filter auf der Seite, mit der die angezeigten Datensätze eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="85009-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="85009-110">Das bedeutet, dass die Excel-Arbeitsmappe dieselben Zeilen und Spalten enthält, die auf der Seite unter [!INCLUDE[prodshort](includes/prodshort.md)] erscheinen.</span><span class="sxs-lookup"><span data-stu-id="85009-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="85009-111">Sie können Änderungen mit Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht auf  [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="85009-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="85009-112">Sie können die Änderungen in die Excel-Datei nur auf dem Computer speichern.</span><span class="sxs-lookup"><span data-stu-id="85009-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="85009-113">Diese Aktion geht auf Windows und Mac Os.</span><span class="sxs-lookup"><span data-stu-id="85009-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="85009-114">Für [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist die **In Excel öffnen** Aktion nicht verfügbar, wenn die **Bearbeiten Sie in Excel** Aktion nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85009-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="85009-115">In Excel bearbeiten</span><span class="sxs-lookup"><span data-stu-id="85009-115">Edit in Excel</span></span>

-    <span data-ttu-id="85009-116">Mit dieser Aktion berücksichtigt Excel sämtliche Filter auf der Seite, mit der die angezeigten Datensätze eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="85009-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="85009-117">Das bedeutet, dass die Excel-Arbeitsmappe alle verfügbaren Datensätze und Spalten enthält, unabhängig davon, was auf der Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="85009-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="85009-118">Der Vorteil der **Bearbeiten Sie in Excel** Aktion ist, dass es Sie Änderungen mit Datensätzen in Excel vornimmt und die Änderungen zurück in [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlichen können,</span><span class="sxs-lookup"><span data-stu-id="85009-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="85009-119">Das geht nur auf Windows; nicht Mac Os.</span><span class="sxs-lookup"><span data-stu-id="85009-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="85009-120">Für [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist die **Bearbeiten Sie in Excel** Aktion nur verfügbar, wenn das Excel-Add-In vom Administrator speziell eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="85009-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="85009-121">Für Administratoren wenn Sie erfahren möchten, wie das Excel-Add-In installiert wird gehen sie zu [Einrichten des Excel-Add-Ins](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="85009-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

## <a name="see-also"></a><span data-ttu-id="85009-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85009-122">See Also</span></span>

[<span data-ttu-id="85009-123">Arbeiten mit Business Central</span><span class="sxs-lookup"><span data-stu-id="85009-123">Working with Business Central</span></span>](ui-work-product.md)  

