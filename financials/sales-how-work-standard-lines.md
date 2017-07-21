---
title: "Einrichten und Verwenden von Standardzeilen für Wiederverkäufe und -einkäufe| Microsoft Docs"
description: "Sie können Verkaufszeilen und Einkaufszeilen einrichten, die Sie häufig machen und diese dann in Verkaufs- und Einkaufsbelegen einfügen, um die Zeilen mit Standardinformationen schnell auszufüllen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a>Vorgehensweise: Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen
Wenn Sie häufiger Verkaufs- und Einkaufszeilen mit ähnlichen Daten erstellen müssen, können Sie die Standardzeilen einrichten, die Sie in wiederkehrenden Verkaufs- und Einkaufsbelegen, z. B. für wiederkehrende Ersatzaufträge benötigen.  

Der folgende Ablauf zeigt, wie man Standardverkaufszeilen einrichtet. Es geht auf ähnliche Weise für Standardeinkaufszeilen.  

## <a name="to-set-up-standard-sales-lines"></a>So richten Sie eine Standard-Verkaufszeile ein  
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Standardverkaufscode** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Standardverkaufszeile** die Aktion **Neu** aus.  
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Im Inforegister **Zeilen** können Sie Informationen in die Felder eingeben, um Verkaufszeilen vorzubereiten, die die Standardzeilen widerspiegeln, von der Sie erwarten, wiederkehrende Zeilen in Einkaufsbelegen zu verwenden.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Um auf einer Verkaufsrechnung Standardverkaufszeilen einfügen
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Rechnung** ein und wählen den zugehörenden Link aus.
2. Öffnen Sie die Verkaufsrechnung, in die Sie eine oder mehrere Standard-Verkaufszeilen einfügen möchten.
3. Wählen Sie die **Wiederkehrende Verkaufszeilen abrufen** Aktion aus.
4. Im Fenster **Wiederkehrende Verkaufszeilen** wählen Sie die Suchschaltfläche im Feld **Code**, und wählen einen Satz von Standardverkaufszeilen aus.
5. Wählen Sie die Schaltfläche **OK**, um die Standardverkaufszeilen in die Rechnung einzufügen, in die Sie Informationen verwenden ist beim oder bearbeiten können.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Vorgehensweise: Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufscodes erstellen
Alternativ können Sie **Wiederkehrende Verkaufsrechnung erstellen** verwenden. Sie können mit der -Stapelverarbeitung Verkaufsrechnungen gemäß Standardverkaufscodes erstellen, die den Debitoren zugeordnet sind und Buchungsdaten enthalten, die innerhalb der Gültigkeitszeiträume liegen, die Sie im Standardverkaufscode festgelegt haben.

Im Fenster **Wiederkehrende Verkaufszeilen** können Sie auch eine Einzugsmethode und ein Lastschrift-Mandat angeben. Die Verkaufsrechnung, die mit **Wiederkehrende Verkaufsrechn. erstellen** erstellt werden Batchauftrag umfasst dann die Informationen, die benötigt werden, die Zahlung der Verkaufsrechnungen mit Abbuchung SEPA zu erfassen. Weitere Informationen finden Sie unter Einziehen von Zahlungen mit Abbuchung SEPA.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Wiederkehrende Verkaufsrechnung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Im Fenster **Wiederkehrende Verkaufsrechn. erstellen** füllen Sie die Felder je nach Bedarf aus.
3. In dem Feld **Code** geben Sie den Code der Standardverkaufscode ein, die einem Debitor zugewiesen sind, für den Verkaufsrechnungen erstellen möchten.
4. Wählen Sie die Schaltfläche **OK** aus.

Verkaufsrechnungen werden für die Debitoren mit dem angegebenen Standard-Debitorenvertriebscode und allen angegebenen Direkteinzugsinformationen zur Buchung am angegebenen Datum erstellt.

## <a name="see-also"></a>Siehe auch  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

