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
# <a name="couple-and-synchronize-records-manually"></a>Datensätze manuell koppeln und synchronisieren
Dieses Thema beschreibt, wie man einen oder mehrere Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Datensätzen in Common Data Service oder [!INCLUDE[crm_md](includes/crm_md.md)] koppelt. Durch das Koppeln der Datensätze können Sie Common Data Service-Informationen aus [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen und umgekehrt. Die Kopplung ermöglicht Ihnen außerdem, Daten zwischen den Datensätzen zu synchronisieren. Sie können vorhandene Datensätze koppeln, oder Sie erstellen und koppeln neue Datensätze.

> [!Note]
> Die Kopplung und Synchronisierung von Daten ist nur verfügbar, wenn Ihr Systemadministrator eine Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Common Data Service oder [!INCLUDE[crm_md](includes/crm_md.md)] hergestellt hat. Eine schnelle Art dies sicherzustellen ist, die Karte **Debitor** zu öffnen und nach der **Kopplung einrichten**-Aktion zu suchen. Wenn die Aktion verfügbar ist, sind die Apps verbunden.   

## <a name="video-example"></a>Video-Beispiel

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>So koppeln Sie einen Datensatz  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten. Zum Beispiel den die Debitor- oder Kontaktkarte.  

    Sie können auch einfach die Listenseite öffnen und den Datensatz auswählen, den Sie koppeln möchten.  

2.  Wählen Sie die **Kopplung einrichten**-Aktion aus.  
3.  Füllen Sie die Felder aus, und wählen Sie dann **OK** aus.  

## <a name="to-synchronize-a-single-record"></a>So synchronisieren Sie einen einzelnen Datensatz  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten. Zum Beispiel den die Debitor- oder Kontaktkarte.  
2.  Wählen Sie die **Jetzt synchronisieren**-Aktion aus.  
3.  Wenn ein Datensatz in eine Richtung synchronisiert werden kann, wählen Sie die Option, die die Richtung der Datenaktualisierung angibt, und wählen Sie dann **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>So synchronisieren Sie einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] aus  
1.  Öffnen Sie in [!INCLUDE[crm_md](includes/crm_md.md)] das Formular für den Datensatz, den Sie koppeln möchten. Zum Beispiel das Formular „Kontokarte“ oder „Kontaktkarte“.  
2.  Wählen Sie die Aktion **[!INCLUDE[d365fin](includes/d365fin_md.md)]** in der Multifunktionsleiste, um den Datensatz automatisch zu öffnen und zu koppeln.

> [!Note]
> Sie können einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] nur dann automatisch synchronisieren, wenn **Synchronisieren nur gekoppelte Datensätze** deaktiviert ist und die Synchronisierungsrichtung auf der Seite **Integrationstabellenzuordnung** für den Datensatz auf Bidirektional oder Von Integrationstabelle eingestellt ist. Weitere Informationen finden Sie unter [Zuordnen der zu synchronisierenden Tabellen und Felder](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>So synchronisieren Sie mehrere Datensätze  
1.  Öffnen Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] die Listenseite für den Datensatz, beispielsweise die Listenseiten "Debitoren" oder "Kontakte".  
2.  Wählen Sie die Datensätze aus, die Sie synchronisieren möchten, und wählen Sie die Aktion **Jetzt synchronisieren** aus.  
3.  Wenn Datensätze in eine Richtung synchronisiert werden können, wählen Sie die Option, die die Richtung angibt, und wählen Sie dann **OK**.  

## <a name="see-also"></a>Siehe auch  
[Verwenden von Dynamics 365 Sales von Business Central](marketing-integrate-dynamicscrm.md)
