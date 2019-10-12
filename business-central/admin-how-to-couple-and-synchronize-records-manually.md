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
# <a name="couple-and-synchronize-records-manually"></a>Datensätze manuell koppeln und synchronisieren
In diesem Thema wird beschrieben, wie mindestens ein Datensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppelt werden. Durch das Koppeln der Datensätze können Sie [!INCLUDE[crm_md](includes/crm_md.md)]-Informationen aus [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen und umgekehrt. Die Kopplung ermöglicht Ihnen außerdem, Daten zwischen den Datensätzen zu synchronisieren. Sie können vorhandene Datensätze koppeln, oder Sie erstellen und koppeln neue Datensätze.

> [!Note]
> Das Koppeln und Synchronisieren von Daten mit [!INCLUDE[crm_md](includes/crm_md.md)] ist nur verfügbar, wenn Ihr Systemadministrator eine Verbindung zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt hat. Eine schnelle Art dies sicherzustellen ist, die Karte **Debitor** zu öffnen und nach der **Kopplung einrichten**-Aktion zu suchen. Wenn die Aktion verfügbar ist, sind die Apps verbunden.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>So koppeln Sie einen Datensatz  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten. Zum Beispiel den die Debitor- oder Kontaktkarte.  

    Sie können auch einfach die Listenseite öffnen und den Datensatz auswählen, den Sie koppeln möchten.  

2.  Wählen Sie die **Kopplung einrichten**-Aktion aus.  
3.  Füllen Sie die Felder aus, und wählen Sie dann **OK** aus.  

## <a name="to-synchronize-a-single-record"></a>So synchronisieren Sie einen einzelnen Datensatz  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten. Zum Beispiel den die Debitor- oder Kontaktkarte.  
2.  Wählen Sie die **Jetzt synchronisieren**-Aktion aus.  
3.  Falls ein Datensatz sowohl von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)] als auch von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert werden kann, wählen Sie die Option, die der Richtung der Datenaktualisierung entspricht, und wählen Sie dann die Schaltfläche **OK** aus.  

## <a name="to-synchronize-multiple-records"></a>So synchronisieren Sie mehrere Datensätze  
1.  Öffnen Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] die Listenseite für den Datensatz, beispielsweise die Listenseiten "Debitoren" oder "Kontakte".  
2.  Wählen Sie die Datensätze aus, die Sie synchronisieren möchten, und wählen Sie die Aktion **Jetzt synchronisieren** aus.  
3.  Falls Datensätze sowohl von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)] als auch von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert werden kann, wählen Sie die Option, die der Richtung der Datenaktualisierung entspricht, und wählen Sie dann die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
[Verwenden von Dynamics 365 Sales von Business Central](marketing-integrate-dynamicscrm.md)
