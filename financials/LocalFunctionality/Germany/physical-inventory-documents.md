---
title: Inventurbelege
description: "Sie können mithilfe der Inventurauftrags- und Inventurerfassungsbelege eine Inventur der Artikel durchführen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: cd052f3cfe91adef90047ef5c5f063f1f63020f8
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="physical-inventory-documents"></a>Inventurbelege
Sie können mithilfe der Inventurauftrags- und Inventurerfassungsbelege eine Inventur der Artikel durchführen.  

Der Inventurauftrag enthält Daten für die Planung, Umsetzung und Analyse von Inventuren. Artikel-, Lagerort- und Lagerplatzinformationen sind ebenfalls verfügbar.  

## <a name="physical-inventory-recording"></a>Inventurerfassung  
Die Inventurerfassung enthält die Artikelnamen und -mengen, die bei der Inventur gezählt wurden. Ein Artikel kann in mehreren Inventurerfassungen gezählt werden.  

Ein Inventurauftrag kann sich auf mehr als eine Inventurerfassung beziehen, doch eine Inventurerfassung kann sich nur auf einen Inventurauftrag beziehen. Weitere Informationen finden Sie unter [Vorgehensweise: Inventurhäufigkeiten für physische Lagererfassung einrichten](physical-inventory-recording-counting-physical-inventory.md)  

Nach Abschluss der Inventurerfassungen und des Inventurauftrags kann der Inventurauftrag gebucht werden. Die Informationen werden an das Inventur-Buch.-Blatt übertragen. Nach der Übertragung ist der Inventurauftrag als gebuchter Inventurauftrag zum späteren Abrufen verfügbar.  

## <a name="posted-physical-inventory-documents"></a>Gebuchte physische Inventurbelege  
Nach dem Buchen wird der Inventurauftrag gelöscht, und der Beleg kann als gebuchter Inventurauftrag angezeigt und ausgewertet werden.  

Beim Buchen von Inventuraufträgen werden auch die Inventurerfassungsköpfe und die Inventurerfassungszeilen in die gebuchten Belege übertragen.  

Die gebuchten Inventurbelege bieten die Möglichkeit, einen vollständigen Überblick über den gesamten Inventurprozess zu erhalten. Sie können die Daten von gebuchten Inventurauftragsköpfen und gebuchten Inventurauftragszeilen nicht ändern, da diese Belege bereits gebucht wurden.  

Wenn Sie Artikelverfolgungszeilen zum Registrieren von Seriennummern und Chargennummern verwendet haben, speichert die Anwendung die erwarteten Artikelverfolgungszeilen, die erfassten Artikelverfolgungszeilen und die gebuchten Artikelverfolgungsposten.  

Es ist möglich, mithilfe der Kopierfunktion auf Basis des gebuchten Inventurauftrags neue Inventuraufträge zu erstellen.  

Mit der Funktion "Navigate" können Inventurposten und andere zugehörige Posten eines gebuchten Inventurauftrags angezeigt werden.  

## <a name="see-also"></a>Siehe auch  
 [Logistik](../../warehouse-manage-warehouse.md)   
 [Inventurauftragszeilen mit Artikelverfolgungszeilen](physical-inventory-order-lines-with-item-tracking-lines.md)   
 [Inventurerfassung – Inventurzählung](physical-inventory-recording-counting-physical-inventory.md)   
 [Inventurbelege einrichten](how-to-set-up-physical-inventory-documents.md)   
 [Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md)   
 [So erstellen Sie eine physische Inventurerfassung](how-to-create-a-physical-inventory-recording.md)   
 [So buchen Sie physische Inventuraufträge](how-to-post-physical-inventory-orders.md)   
 [Lokale Funktion (Deutschland)](germany-local-functionality.md)

