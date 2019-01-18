---
title: Arbeiten mit eingehenden Belegen| Microsoft Docs
description: "Sie können eingehende externe Unternehmensbelege, wie Zahlungseingänge oder PDF-Dateien verwalten, OCR-Aufgaben verwalten und Dateien in elektronische Belege und Datensätze umwandeln."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 989fff07cb0608b8dbf6611a39163fc3cfe31459
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="incoming-documents"></a>Eingehende Belege
Einige Geschäftstransaktionen werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] nicht von Anfang an erfasst. Stattdessen geht ein externes Geschäftsdokument in Ihrem Unternehmen als E-Mail-Anhang oder Papierkopie ein, die Sie in eine Datei scannen. Dieses ist typisch für Einkäufe, wo solche Eingangsbelege Zahlungseingänge für Aufwendungen oder kleine Einkäufe darstellen.

Mithilfe eines externen OCR-Dienstes (optische Zeichenerkennung) können Sie aus PDF- oder Bilddateien, die die Eingangsbelege darstellen, elektronische Belege generieren, die dann in Project '[!INCLUDE[d365fin](includes/d365fin_md.md)]' in Belegdatensätze konvertiert werden können.

Auf der Seite **Eingehende Belege** können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren eingehender Belege, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden. Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten.

Die Verarbeitung von Eingangsbelegen kann aus den folgenden Hauptaktivitäten bestehen:

* Erfassen Sie die externen Belege in Project '[!INCLUDE[d365fin](includes/d365fin_md.md)]', indem Sie mithilfe einer der folgenden Methoden Zeilen auf der Seite **Eingehende Belege** anlegen:
  * Manuell, mithilfe von einfachen Funktionen, entweder von einem PC oder von einem mobilen Gerät aus, auf eine der folgenden Arten:
    * Verwenden Sie die Schaltfläche **Aus Datei erstellen** und füllen Sie dann die entsprechenden Felder auf der Seite **Eingehender Beleg** aus. Die Datei wird automatisch angehängt.  
    * Verwenden Sie die Schaltfläche **Neu**, füllen Sie dann die entsprechende Felder auf der Seite **Eingehender Beleg** aus und hängen Sie die betreffende Datei an.
    * Auf einem Tablet oder einem Telefon verwenden Sie die Schaltfläche **Von Kamera erstellen**, um einen neuen Eingangsbelegsdatensatz zu erstellen, und senden das Bild dann beispielsweise an den OCR-Dienst.
  * Automatisch, indem Sie den Beleg vom OCR-Dienst als ein elektronisches Dokument empfangen, nachdem Sie die zugehörige PDF- oder Bilddatei per E-Mail an den OCR-Dienst gesendet haben. Das Inforegister **Finanzinformationen** wird automatisch auf der Seite **Eingehender Beleg** ausgefüllt.
* Nutzen Sie den OCR-Dienst zur Umwandlung von PDF- oder Bilddateien in elektronische Belege die in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Belegdatensätze konvertiert werden können.
* Erstellen Sie neue Belege oder eine Fibu Buch.-Blattzeilen aus einem eingehenden Belegdatensatz, indem sie die Informationen so eingeben, wie sie in den eingehenden Belegen stehen.
* Fügen Sie eingehender Belege zu Einkaufs- und Verkaufsbelegen jeden möglichen Status hinzu, einschließlich der resultierenden Kreditor, Debitor- und Sachposten, die aus dem Buchen resultieren.
* Zeigen Sie Eingangsbelege und deren Anhänge aus Einkaufs- und Verkaufsbelegen oder Posten an, oder finden Sie alle Sachposten ohne Eingangsbelege auf der Seite **Kontenplan**.

| An | Siehe |
| --- | --- |
| Richten Sie die Funktion für Eingangsbelege und den OCR-Dienst ein. |[Einrichten von eingehenden Belegen](across-how-setup-income-documents.md) |
| Erstellen Sie eingehende Belegdatensätze, fügen Sie Dateien hinzu, nutzen Sie OCR, um PDF-Dateien in elektronische Belege umzuwandeln, konvertieren Sie elektronische Belege in Belegdatensätze, überwachen Sie eingehende Belegdatensätze aus gebuchten Verkaufs- und Einkaufsbelegen. |[Eingehende Belege verarbeiten](across-process-income-documents.md) |

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

