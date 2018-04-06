---
title: "So erstellen Sie Buch.-Blatt-Eröffnungssalden | Microsoft Docs"
description: "Business Central enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten mithilfe von Buch.-Blatt-Buchungen einfach übertragen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="0b6b9-104">So erstellen Sie Buch.-Blatt-Eröffnungssalden</span><span class="sxs-lookup"><span data-stu-id="0b6b9-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0b6b9-105"> enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="0b6b9-106">Sie können diese Daten auf das Debitorbuch.-Blatt, das Kreditorbuch.-Blatt, das Artikel Buch.-Blatt und das Hauptbuchbuch.-Blatt übertragen.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="0b6b9-107">Der erste Schritt besteht darin, ein Konfigurationspaket zu erstellen, das die Einrichtungstabellen für alle Buch.-Blätter enthält.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="0b6b9-108">Nachfolgend wird davon ausgegangen, dass dieser Schritt abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="0b6b9-109">Weitere Informationen finden Sie unter [Unternehmenskonfiguration einrichten](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="0b6b9-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="0b6b9-110">Das Verfahren beschreibt die folgenden Schritte, die das Übernehmen des Pakets, das von einem Partner bereitgestellt wird, enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="0b6b9-111">Bevor Sie den Buchungsvorgang starten, prüfen Sie, ob Sie in der RapidStart Service-Implementierungs-Rollencenterseite sind, da sie den korrekten Kontext für Ihre Konfigurationsarbeit bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="0b6b9-112">Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0b6b9-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="0b6b9-113">So übernehmen Sie die Posten in einem Buch.-Blatt für einen neuen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="0b6b9-114">Konfigurieren Sie einen neuen Mandanten und wenden Sie ein Konfigurationspaket darauf an.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="0b6b9-115">Weitere Informationen finden Sie unter [Vorgehensweise: Konfigurieren Sie einen Mandanten mit dem RapidStart-Assistenten](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="0b6b9-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="0b6b9-116">Der neue Mandant enthält keine Informationen über Buch.-Blatt-Eröffnungssalden.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="0b6b9-117">Öffnen Sie das Konfigurationsarbeitsblatt, und importieren Sie vorhandene Daten zu Debitoren, Kreditoren, Artikeln, Kreditoren und dem Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="0b6b9-118">Weitere Informationen finden Sie unter [Gewusst wie: Kundendaten zusammenführen](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="0b6b9-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="0b6b9-119">Wählen Sie die Aktion **Buch.-Blattzeilen erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="0b6b9-120">Füllen Sie das Inforegister **Optionen** entsprechend aus und legen Sie nach Bedarf Filter fest.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="0b6b9-121">Geben Sie beispielsweise im Feld **Buch.-Blattvorlage** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="0b6b9-122">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-122">Choose the **OK** button.</span></span> <span data-ttu-id="0b6b9-123">Die Datensätze stehen jetzt im Buch.-Blatt, die Beträge sind jedoch leer.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="0b6b9-124">Exportieren Sie die Buch.-Blatt-Tabelle in Excel und geben Sie die Buchung und die Gegenkontoinformationen aus den Stammdaten manuell ein.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="0b6b9-125">Importieren Sie die Tabelleninformationen in den neuen Mandanten und gleichen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="0b6b9-126">Die Erfassungspositionen sind für die Buchung bereit.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="0b6b9-127">Wählen Sie im Konfigurationsarbeitsblatt die Buch.-Blattzeile, und wählen Sie in der Registerkarte Aktionen in der Gruppe Anzeigen die Option **Datenbank-Daten** aus.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="0b6b9-128">Überprüfen Sie die Informationen und wählen Sie dann die Schaltfläche **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="0b6b9-129">Wiederholen Sie die Schritte, um verschiedene Salden zu importieren und zu buchen.</span><span class="sxs-lookup"><span data-stu-id="0b6b9-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b6b9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b6b9-130">See Also</span></span>  
[<span data-ttu-id="0b6b9-131">Übernehmen von Konfiguration in neue Mandanten</span><span class="sxs-lookup"><span data-stu-id="0b6b9-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="0b6b9-132">Einrichten von Mandanten mit RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="0b6b9-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="0b6b9-133">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="0b6b9-133">Administration</span></span>](admin-setup-and-administration.md)

