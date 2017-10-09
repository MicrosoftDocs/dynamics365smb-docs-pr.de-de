---
title: "Sie können einen Bericht planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird | Microsoft Docs"
description: Erfahren Sie mehr zum Eingeben eines Berichts in eine Aufgabenwarteschlange und das Planen der Verarbeitung an einem bestimmten Datum und Uhrzeit.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: badcdee3dfa5bec3c2462149989cf9d4fb5af2a0
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-reports"></a>Arbeiten mit Berichten
Ein Bericht stellt Informationen auf Basis eines bestimmten Satz an Kriterien zusammen und unterteilt die Informationen in ein einfach zu lesendes, druckbares Format. Es gibt viele Berichte, auf die Sie im Zuge der Anwendung zugreifen können. Die Berichte stellen in der Regel Informationen proportional zu dem Kontext der Seite bereit, auf der Sie sich befinden. Beispielsweise der **Debitor** für die Seite Berichte Top 10 Debitoren und die Verkaufsstatistik und mehr.

Sie können Berichte auf der Registerkarte **Berichte** über ausgewählte Seiten finden, oder Sie können die Suche verwenden, um Berichte nach Namen zu finden. Wenn Sie einen Bericht öffnen, wird eine Seite dargestellt, mit der Sie bestimmte Informationen definieren können (Optionen und Filter), die Sie im Bericht integrieren möchten. Beispielsweise abhängig vom Bericht, können Sie eines bestimmten Datumsbereichs einem bestimmten Datensatz, beispielsweise Debitor oder Sortierreihenfolge festlegen.

## <a name="previewing-a-report"></a>So zeigen Sie eine Berichtvorschau an:
Wählen Sie **Vorschau**, um den Bericht im Internetbrowser anzuzeigen. Anzeigen auf einem Bereich des Berichts, um ihn auf der Menüleiste anzuzeigen.  

![Berichtsvorschausymbolleiste](media/report_viewer.png "Berichtsvorschausymbolleiste")

Verwenden der Menüleiste:

-   Navigieren durch Seiten
-   Ein- und Ausblenden
-   An das Fenster anpassen
-   Text auswählen

    Sie können Text aus einem Bericht kopieren und fügen diesen dann an einem anderen Ort oder in [!INCLUDE[d365fin](includes/d365fin_md.md)] Microsoft Word ein.  Mithilfe einer Maus beispielsweise drücken und halten Sie, wo Sie beginnen möchten, und fahren dann mit der Maus, um einen oder mehrere Begriffe, Sätze oder Absätze auszuwählen. Sie können die rechte Maustaste drücken dann **Kopieren** auswählen. Sie können dann den ausgewählten Text kopieren.
-   Beleg verschieben

    Sie können den sichtbaren Bereich des Berichts in beliebiger Richtung verschieben, daher können Sie weitere Bereiche oder den Bericht anzeigen. Dies ist hilfreich, wenn Sie gezoomt haben, um Details anzuzeigen.  Mithilfe der Maus beispielsweise drücken und halten Sie die Maustaste an einem beliebigen Ort in der  Berichtsvorschau und bewegen Sie dann Ihre Maus.

-   Download in eine PDF-Datei auf Ihrem Computer oder Netzwerk.


## <a name="saving-a-report"></a>Speichern des Berichts
Sie können einen Bericht in ein PDF-Dokument, Microsoft Word Dokument oder Microsoft Excel-Dokument speichern, indem Sie **Senden an** auswählen, und anschließend Ihre Auswahl treffen. 

## <a name="ScheduleReport"></a>Planen der Ausführung eines Berichts
Sie können einen Bericht planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird. Geplante Berichte werden in der Projektwarteschlange eingegeben und zu der geplanten Zeit verarbeitet, wie vergleichbare andere Aufträge auch. Sie können auswählen, ob Sie den verarbeiteten Bericht speichern möchten, beispielsweise als Excel-, Word- oder PDF-Datei, ihn auf einem ausgewählten Drucker auszugeben, oder ihn nur zu verarbeiten. Wenn Sie wählen, den Bericht in eine Datei zu speichern, wird der verarbeitete Bericht an den **Berichts-Eingang** auf Ihrer Startseite gesendet, wo Sie ihn anzeigen können.

Sie können einen Bericht planen, wenn Sie einen Bericht öffnen. Sie wählen **Plan** aus und Sie geben die Informationen wie Drucker und Zeit und Datum ein. Der Bericht wird der Aufgabenwarteschlange hinzugefügt und zum angegebenen Zeitpunkt ausgeführt. Wenn der Bericht verarbeitet ist, wird das Element aus der Aufgabenwarteschlange entfernt. Wenn Sie den verarbeiteten Bericht in einer Datei gespeichert haben, ist er im **Berichts-Eingang** verfügbar.

## <a name="PrintReport"></a>Berichte drucken
Wenn Sie einen Bericht drucken möchten, müssen Sie den Bericht als PDF-, Word- oder Excel-Dokument zuerst herunterladen, indem Sie die Schaltfläche **Senden an** auswählen. Jetzt können Sie entweder das PDF-Dokument sofort öffnen und es drucken, oder speichern Sie es, um später zu drucken.

## <a name="using-saved-settings"></a>Gespeicherte Einstellungen nutzen
Ein Bericht kann einen oder mehrere Eiunträge im Feld **Gespeicherte Einstellungen** enthalten. *Gespeicherte Einstellungen* sind im Allgemeinen eine vordefinierte Gruppe von Optionen und Filter, die Sie z. B. für Bericht anwenden können, bevor Sie den Bericht auf eine Datei in der Vorschau sehen oder buchen. Die Verwendung von gespeicherten Einstellungen ist eine schnelle und zuverlässige Art, Berichte zu erstellen, die die richtigen Daten enthalten.

Der gespeicherte Einstellungseintrag mit der Bezeichnung **Zuletzt verwendete Optionen und Filter** ist immer verfügbar. Dieser Posten setzt den Bericht mit den Optionen und Filtern, die Sie beim letzten Mal verwendet haben, als Sie den Bericht betrachteten.

>[!NOTE]
>Als Administrator können Sie die gespeicherten Einstellungen für Berichte für alle Benutzer erstellen und verwalten. Weitere Informationen finden Sie unter [Verwaltung von gespeicherten Einstellungen in Berichten](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Ändern des Layouts und des Layouts eines Berichts
Ein Berichtslayout steuert, was in einem Bericht angezeigt wird, wie er angeordnet wird und wie er formatiert ist. Wenn Sie zu einem anderen Layout wechseln möchten, finden Sie Informationen unter [Vorgehensweise: Ändern Sie, das Layout derzeit auf einem Bericht verwendet wird](ui-how-change-layout-currently-used-report.md). Oder, wenn Sie Ihr eigenes Berichtslayout anpassen möchten gehen Sie zu [Vorgehensweise: Erstellen und bearbeiten von benutzerdefinierten Berichtslayouts](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Siehe auch
[Angeben der Druckerauswahl für Berichte](ui-specify-printer-selection-reports.md)  
[Verwaltung von Berichts- und Beleg-Layouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

