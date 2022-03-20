---
title: Koppeln und Synchronisieren (enthält Video)
description: Die Synchronisierung einer Integrationstabellenzuordnung ermöglicht die Datensynchronisierung in allen Datensätzen in einer Tabelle in Business Central und der Dynamics 365 Sales-Tabellen, die gekoppelt sind.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.search.form: 6250
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: 4caf32bb0c7b4471809d8af3b899329c571d144f
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381590"
---
# <a name="coupling-and-synchronizing-records-between-dataverse-and-business-central"></a>Datensätze zwischen Dataverse und Business Central koppeln und synchronisieren

Dieses Thema beschreibt, wie man einen oder mehrere Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] mit Datensätzen in Dataverse oder [!INCLUDE[crm_md](includes/crm_md.md)] koppelt. Durch das Koppeln der Datensätze können Sie Dataverse-Informationen aus [!INCLUDE[prod_short](includes/prod_short.md)] anzeigen und umgekehrt. Die Kopplung ermöglicht Ihnen außerdem, Daten zwischen den Datensätzen zu synchronisieren. Sie können vorhandene Datensätze koppeln, oder Sie erstellen und koppeln neue Datensätze.

> [!Note]
> Die Kopplung und Synchronisierung von Daten ist nur verfügbar, wenn Ihr Systemadministrator eine Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Dataverse oder [!INCLUDE[crm_md](includes/crm_md.md)] hergestellt hat. Eine schnelle Art dies sicherzustellen ist, die Karte **Debitor** zu öffnen und nach der **Kopplung einrichten**-Aktion zu suchen. Wenn die Aktion verfügbar ist, sind die Apps verbunden.   

## <a name="video-example"></a>Video-Beispiel
Dieses Video zeigt die Kopplung und Synchronisierung von Daten im Rahmen einer Integration in [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>So koppeln Sie einen Datensatz  
1.  In [!INCLUDE[prod_short](includes/prod_short.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten. Zum Beispiel den die Debitor- oder Kontaktkarte.  

    Sie können auch einfach die Listenseite öffnen und den Datensatz auswählen, den Sie koppeln möchten.  

2.  Wählen Sie die **Kopplung einrichten**-Aktion aus.  
3.  Füllen Sie die Felder aus, und wählen Sie dann **OK** aus.  

## <a name="to-synchronize-a-single-record"></a>So synchronisieren Sie einen einzelnen Datensatz  
1.  In [!INCLUDE[prod_short](includes/prod_short.md)] öffnen Sie die Karte für den Datensatztyp, den Sie koppeln möchten. Zum Beispiel den die Debitor- oder Kontaktkarte.  
2.  Wählen Sie die **Jetzt synchronisieren**-Aktion aus.  
3.  Wenn ein Datensatz in eine Richtung synchronisiert werden kann, wählen Sie die Option, die die Richtung der Datenaktualisierung angibt, und wählen Sie dann **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>So synchronisieren Sie einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] aus  
1.  Öffnen Sie in [!INCLUDE[crm_md](includes/crm_md.md)] das Formular für den Datensatz, den Sie koppeln möchten. Zum Beispiel das Formular „Kontokarte“ oder „Kontaktkarte“.  
2.  Wählen Sie die Aktion **[!INCLUDE[prod_short](includes/prod_short.md)]** in der Multifunktionsleiste, um den Datensatz automatisch zu öffnen und zu koppeln.

> [!Note]
> Sie können einen einzelnen Datensatz von [!INCLUDE[crm_md](includes/crm_md.md)] nur dann automatisch synchronisieren, wenn **Synchronisieren nur gekoppelte Datensätze** deaktiviert ist und die Synchronisierungsrichtung auf der Seite **Integrationstabellenzuordnung** für den Datensatz auf Bidirektional oder Von Integrationstabelle eingestellt ist. Weitere Informationen finden Sie unter [Zuordnen der zu synchronisierenden Tabellen und Felder](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>So koppeln Sie mehrere Datensätze mithilfe der abgleichsbasierten Kopplung

Sie können die zu synchronisierenden Daten für eine Entität, z.B. einen Debitor oder einen Kontakt, angeben, indem Sie Datensätze auf der Grundlage von Übereinstimmungen koppeln. Sie können die Übereinstimmungen verfeinern, indem Sie bei der Suche zwischen Groß- und Kleinschreibung unterscheiden und jeder Übereinstimmung eine Priorität zuweisen. Wenn keine Übereinstimmung gefunden wird, können Sie auch angeben, dass Sie die Entität in Dataverse erstellen möchten. Weitere Informationen finden Sie unter [Anpassen der abgleichsbasierten Kopplung](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

1. Öffnen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die Listenseite für den Datensatz, beispielsweise die Listenseiten "Debitoren" oder "Kontakte".
2. Wählen Sie die Aktion **Abgleichsbasierte Kopplung**.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>So synchronisieren Sie mehrere Datensätze  
1.  Öffnen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die Listenseite für den Datensatz, beispielsweise die Listenseiten "Debitoren" oder "Kontakte".  
2.  Wählen Sie die Datensätze aus, die Sie synchronisieren möchten, und wählen Sie die Aktion **Jetzt synchronisieren** aus.  
3.  Wenn Datensätze in eine Richtung synchronisiert werden können, wählen Sie die Option, die die Richtung angibt, und wählen Sie dann **OK**.  

## <a name="uncoupling-records"></a>Kopplung von Datensätzen aufheben
Sie können einen oder mehrere Datensätze von Listenseiten oder der Seite **Fehler bei der Synchronisierung gekoppelter Daten** durch Auswahl einer oder mehrerer Zeilen und Auswahl von **Kopplung löschen** entkoppeln. Sie können auch alle Kupplungen für eine oder mehrere Tabellenzuordnungen auf der Seite **Zuordnungen der Integrationstabelle** entfernen.

## <a name="see-also"></a>Siehe auch  
[Verwenden von Dynamics 365 Sales von Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]