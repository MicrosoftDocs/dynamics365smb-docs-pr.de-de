---
title: 'Tipps und Tricks: RapidStart Servicesen | Microsoft Docs'
description: "Wenn Sie Unternehmen mit RapidStart Services konfigurieren, gibt es einige Tipps und Tricks, die Sie für eine reibungslose Implementierung nutzen können."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e43859a6095f0087c12d0f9c071c0504d3781ad2
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a>Tipps und Tricks: RapidStart Servicesen
Wenn Sie Unternehmen mit RapidStart Services konfigurieren, gibt es einige Tipps und Tricks, die Sie für eine reibungslose Implementierung nutzen können.  

## <a name="take-advantage-of-configuration-templates"></a>Konfigurationsvorlagen nutzen  
Mit Konfigurationsvorlagen können Sie Ihren Implementierungsprozess optimieren. Sie können damit ähnliche Debitoren in Segmente einbinden und dann ein Implementierungsprotokoll entwickeln, das alle Debitoren in einem Segment in ähnlicher Weise behandelt. Auf diese Art können Sie bei jedem Segment eine bestimmte Vorkonfiguration anwenden und mit einer schnelle Implementierung fortfahren.  

## <a name="configuration-questionnaires"></a>Konfigurationsfragebögen  
Um das Ausfüllen eines Konfigurationsfragebogens zu unterstützen, erwägen Sie, Standardantworten zu definieren, um auf bewährte Methoden hinzuweisen.  

## <a name="batch-creation-of-journal-lines"></a>Stapelerstellung von Buch.-Blattzeilen  
Es wird empfohlen, die Datenmigrationswerkzeuge für die Migration von Blatteinträgen zu verwenden. Bei der Erstellung von Buch.-Blattzeilen mit der Stapelverarbeitung steht andernfalls nur ein begrenzter Bereich zur Verfügung, und es werden nur Verzugsfelder in einem Buch.-Blatt generiert. Der Rest des Buch.-Blattes muss anschließend manuell ausgefüllt werden werden.  

## <a name="migrating-transactions"></a>Migrierung von Transaktionen  
Es wird empfohlen, Eröffnungssalden in der folgenden Reihenfolge in mehreren Schritten zu migrieren.  

1.  Migrieren Sie die Eröffnungssalden des Sachkontos, ohne die untergeordneten Konten des Sachkontos zu verwenden. Verwenden Sie bestimmte Ausgleichskonten für Eröffnungssalden, wobei pro untergeordnetes Sachkonto eines eingerichtet werden sollte. Richten Sie für direkte Buchungen Ausgleichskonten ein.  
2.  Migrieren Sie offene Debitorenposten.  
3.  Migrieren Sie offene Artikelposten.  
4.  Migrieren Sie offene Anlagenposten.  

## <a name="see-also"></a>Siehe auch  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)

