---
title: 'Designdetails: Aktive vs. historische Artikelverfolgungsposten | Microsoft Docs'
description: "Wenn Teile einer Belegzeilenmenge gebucht werden, wird nur diese bestimmte Menge in Artikelposten und deren Artikelverfolgungsnummern übertragen. Jedoch möchten Sie sicher auf alle relevanten Nachverfolgungsinformationen des Artikels direkt aus der aktiven Belegzeile heraus zugreifen. Anders ausgedrückt, Sie möchten nicht nur die Posten, die mit der Restmenge verbunden sind, sondern Sie wünschen auch Informationen über die gebuchten Einheiten. Wenn Sie die Seite **Artikelverfolgungszeilen** anzeigen oder ändern, werden die Kollektivinhalte der Tabelle **Verfolgungsspezifikation** (T336) und der Tabelle **Reservierungsposten** (T337) in einer temporären Version von T336 dargestellt. Dadurch ist sichergestellt, dass auf historische und aktive Artikelverfolgungsdaten als Einheit zugegriffen wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 30a15b664c46729b8e3901bc49982eefc21f1c2a
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Designdetails: Aktive vs. historische Artikelverfolgungsposten
Wenn Teile einer Belegzeilenmenge gebucht werden, wird nur diese bestimmte Menge in Artikelposten und deren Artikelverfolgungsnummern übertragen. Jedoch möchten Sie sicher auf alle relevanten Nachverfolgungsinformationen des Artikels direkt aus der aktiven Belegzeile heraus zugreifen. Anders ausgedrückt, Sie möchten nicht nur die Posten, die mit der Restmenge verbunden sind, sondern Sie wünschen auch Informationen über die gebuchten Einheiten. Wenn Sie die Seite **Artikelverfolgungszeilen** anzeigen oder ändern, werden die Kollektivinhalte der Tabelle **Verfolgungsspezifikation** (T336) und der Tabelle **Reservierungsposten** (T337) in einer temporären Version von T336 dargestellt. Dadurch ist sichergestellt, dass auf historische und aktive Artikelverfolgungsdaten als Einheit zugegriffen wird.  

 Die nachstehende Tabelle zeigt, wie T336 und T337 in einem Einkaufsszenario verwendet werden. Die fettgedruckten Zahlen stellen Werte dar, die der Benutzer manuell auf der **Artikelnachverfolgungszeilen**-Seite eingibt.  

 Schritt 1: Erstellen Sie eine Einkaufszeile von sieben Stück mit Artikelverfolgungsnummern.  

||**Menge (Basis)**|**Bewegungsmge.**|**Menge akt. Rechnung (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Bereits berech. Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Schritt 2: Empfangen Sie vier Teile.  

||**Menge (Basis)**|**Bewegungsmge.**|**Menge akt. Rechnung (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Bereits berech. Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Logistik Artikelverf.-Zeilen** Seite|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Schritt 3: Empfangen Sie zwei Teile, und fakturieren Sie zwei Teile.  

||**Menge (Basis)**|**Bewegungsmge.**|**Menge akt. Rechnung (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Bereits berech. Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Logistik Artikelverf.-Zeilen** Seite|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Schritt 4: Empfangen Sie ein Stück.  

||**Menge (Basis)**|**Bewegungsmge.**|**Menge akt. Rechnung (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Bereits berech. Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Logistik Artikelverf.-Zeilen** Seite|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Fakturieren von 5 Stück.  

||**Menge (Basis)**|**Bewegungsmge.**|**Menge akt. Rechnung (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Bereits berech. Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Logistik Artikelverf.-Zeilen** Seite|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)   
 [Designdetails – Artikelverfolgungszeilenfenster-Seite](design-details-item-tracking-lines-window.md)

