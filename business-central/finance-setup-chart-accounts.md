---
title: Einrichten des Kontenplans | Microsoft Docs
description: "Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cce6320e24ba8d73825e7cb71ada262c5af242a7
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Einrichten oder Ändern des Kontenplans
Der Kontenplan zeigt die Sachkonten an, die Financials speichern. [!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.
Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.  

## <a name="adding-or-changing-accounts"></a>Konten hinzufügen oder ändern
Im Kontenplan können Sie jedes Sachkonto öffnen und Einstellungen hinzufügen oder ändern.

> [!NOTE]  
>   Sie können ein Sachkonto löschen. Bevor es gelöscht wird, müssen allerdings folgende Bedingungen erfüllt sein:  

* Der Saldo des Kontos muss Null betragen.  
* Das Feld **Löschen v. Sachkonten zul. vor** im Fenster **Finanzbuchhaltungs-Einrichtung:** muss ausgefüllt sein, und das Konto darf keine Posten an oder nach diesem Datum enthalten.  
* Ist das Feld **Sachkontoverwendung prüfen** im Fenster **Finanzbuchhaltungs-Einrichtung:** ausgewählt, darf dieses Konto nicht in Buchungsgruppen oder der Buchungsmatrix Einrichtung verwendet werden.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] verhindert, dass Sie ein Sachkonto löschen, in dem Daten gespeichert werden, die im Kontenplan erforderlich sind.  

## <a name="see-also"></a>Siehe auch
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Aus anderen Finanzsystemen importieren](upload-data.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

