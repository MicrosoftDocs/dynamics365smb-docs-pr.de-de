---
title: Fibu-Buchungszeile - Überblick | Microsoft Docs
description: Dieses Thema enthält Änderungen für Codeunit 12, **Jnl.-Beitrags-Zeile**, welche das größte Anwendungsobjekt für Sachpostenbuchung ist und der einzige Bereich, um in der Finanzbuchhaltung MwSt. und Debitoren- und Kreditorenposten einzufügen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215253"
---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="54983-103">Fibu-Buchungszeile - Überblick</span><span class="sxs-lookup"><span data-stu-id="54983-103">General Journal Post Line Overview</span></span>

<span data-ttu-id="54983-104">Codeunit 12, **Jnl.-Beitrags-Zeile**, ist das größte Anwendungsobjekt für Sachpostenbuchung und ist der einzige Bereich, um die Finanzbuchhaltung, MwSt. und Debitoren- und Kreditorenposten einzufügen.</span><span class="sxs-lookup"><span data-stu-id="54983-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="54983-105">Diese Codeunit wird auch für Ausgleich-, Ausgleich aufheben- und Zurücksetzen-Arbeitsgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="54983-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="54983-106">In Microsoft Dynamics NAV 2013 R2 wurde die Codeunit überarbeitet, da sie mit ca. 7.600 Codezeilen sehr groß geworden war.</span><span class="sxs-lookup"><span data-stu-id="54983-106">In Microsoft Dynamics NAV 2013 R2, the codeunit was redesigned because it had become very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="54983-107">Die Architektur wurde geändert und die Codeunit vereinfacht uns somit leichter zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="54983-107">The architecture was changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="54983-108">In dieser Dokumentation werden die Änderungen beschrieben und Informationen bereitgestellt, die Sie für das Upgrade benötigen.</span><span class="sxs-lookup"><span data-stu-id="54983-108">This documentation describes the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="54983-109">Alte Architektur</span><span class="sxs-lookup"><span data-stu-id="54983-109">Old Architecture</span></span>  
<span data-ttu-id="54983-110">Die alte Architektur hatte die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="54983-110">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="54983-111">Es wurde umfangreicher Gebrauch von globalen Variablen gemacht, wodurch sich die Möglichkeit verborgener Fehler aufgrund der Verwendung von Variablen mit dem falschen Bereich erhöhten.</span><span class="sxs-lookup"><span data-stu-id="54983-111">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="54983-112">Es gab viele lange Verfahren (mit mehr als 100 Codezeilen), die auch hohe zyklomatische Komplexität haten (das heißt, viele geschachtelte CASE, REPEAT-, IF-Anweisungen), durch die der Code sehr schwierig zu lesen und zu warten wurde.</span><span class="sxs-lookup"><span data-stu-id="54983-112">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="54983-113">Einige Verfahren, die nur lokal verwendet wurdne und nur lokal verwendet werden sollten, wurden nicht als lokale Variable markiert.</span><span class="sxs-lookup"><span data-stu-id="54983-113">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="54983-114">Die meisten Verfahren hatten keine Parameter und verwendeten globale Variablen.</span><span class="sxs-lookup"><span data-stu-id="54983-114">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="54983-115">Einige verwendeten Parameter und setzten globale Variablen durch lokale Variablen außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="54983-115">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="54983-116">Codeschemata für das Auffinden der Sachkonten und die Erstellung der Finanzbuchhaltung und MwSt.-Posten waren nicht standardisiert und variierten von Ort zu Ort.</span><span class="sxs-lookup"><span data-stu-id="54983-116">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="54983-117">Darüber gab es viele Codeverdopplung und unterbrochene Symmetrie zwischen Debitoren- und Kreditorencode.</span><span class="sxs-lookup"><span data-stu-id="54983-117">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="54983-118">Ein großer Teil des Codes in Codeunit 12, in etwa 30 Prozent, bezog sich auf Rabatt- und Toleranzberechnungen, obwohl Diese Funktion in vielen Ländern oder Regionen nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="54983-118">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="54983-119">Buchen, Ausgleichen, Ausgleich aufheben, Zahlungsrabatt und -Toleranz und Wechselkursregulierung wurden in Codeunit 12 unter Verwendung einer langen Liste von globalen Variablen vereint.</span><span class="sxs-lookup"><span data-stu-id="54983-119">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="54983-120">Neue Architektur</span><span class="sxs-lookup"><span data-stu-id="54983-120">New Architecture</span></span>  
<span data-ttu-id="54983-121">In [!INCLUDE[prod_short](includes/prod_short.md)] hat Codeunit 12 die folgenden Verbesserungen:</span><span class="sxs-lookup"><span data-stu-id="54983-121">In [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="54983-122">Codeunit 12 ist in kleinere Verfahren umgestaltet worden (insgesamt weniger als 100 Codezeilen).</span><span class="sxs-lookup"><span data-stu-id="54983-122">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="54983-123">Standardisierte Muster für die Suche von Sachkonten wurden implementiert, indem Hilfsfunktionen aus den Buchungsgruppen verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="54983-123">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="54983-124">Ein Buchungs-Modul-Framework wurde implementiert, um den Startund das Ende von Transaktionen zu verwalten und die Erstellung auf Sach- und MwSt.-Posten zu isolieren, die Sammlung von MwSt.-Ausgleich und die Berechnung von zusätzlichen Währungsbeträgen.</span><span class="sxs-lookup"><span data-stu-id="54983-124">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="54983-125">Codeverdopplung ist gelöscht worden.</span><span class="sxs-lookup"><span data-stu-id="54983-125">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="54983-126">Viele Hilfsfunktionen wurden zu den entsprechenden Debitoren- und Kreditorenpostentabellen übertragen.</span><span class="sxs-lookup"><span data-stu-id="54983-126">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="54983-127">Die Verwendung von globalen Variablen ist minimiert worden, sodass jedes Verfahren Parameter verwendet und eine eigene Anwendungslogik enthält.</span><span class="sxs-lookup"><span data-stu-id="54983-127">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54983-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54983-128">See Also</span></span>

[<span data-ttu-id="54983-129">Designdetails: Buchungs-Schnittstellenstruktur</span><span class="sxs-lookup"><span data-stu-id="54983-129">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="54983-130">Designdetails: Buchungs-Modul-Struktur</span><span class="sxs-lookup"><span data-stu-id="54983-130">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="54983-131">Designdetails: Fibu Buch.-Blatt-Beitrags-Zeile (Dynamics NAV)</span><span class="sxs-lookup"><span data-stu-id="54983-131">Design Details: General Journal Post Line (Dynamics NAV)</span></span>](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]