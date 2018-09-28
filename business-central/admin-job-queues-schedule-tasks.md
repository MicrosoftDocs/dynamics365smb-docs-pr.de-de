---
title: "Vorgehensweise: Planen der Ausführung eines Berichts | Microsoft Docs"
description: "Geplante Aufgaben sind von der Aufgabenwarteschlange verwaltet. Diese Projektausführungsberichte und Codeunits. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: fae1b2937a3c06fc947dd3dbec529826322d035c
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a>Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung
Die Aufgabenwarteschlangen in [!INCLUDE[d365fin](includes/d365fin_md.md)] ermöglichen es Benutzern, bestimmte Berichte und Codeunits zu planen und auszuführen. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden. So kann es beispielsweise empfehlenswert sein, den Bericht **Verkäufer - Verkäuferstatistik** wöchentlich auszuführen, um jede Woche die Verkaufserfolge eines Verkäufers im Auge zu haben, während die Codenit  **Service-E-Mail-Warteschlange** verarbeiten" täglich ausgeführt wird, um sicherzustellen, dass ausstehende, serviceauftragsbezogene E-Mails rechtzeitig an die entsprechenden Debitoren versendet werden.  

## <a name="add-jobs-to-the-job-queue"></a>Fügen Sie Projekte der Aufgabenwarteschlange hinzu
Im Fenster **Projektwarteschlangeneinträge** sind alle aktuellen Aufgabenwarteschlangenposten aufgelistet. Wenn Sie eine neue Projektwarteschlange hinzufügen, die Sie planen möchten, müssen Sie die Informationen über die Art des Objekts, das Sie ausführen möchten, angeben, wie der Name und die Objekt-ID, die Sie ausführen möchten. Sie können auch Parameter hinzufügen, um das Verhalten eines Aufgabenwarteschlangenpostens festzulegen. So können Sie beispielsweise einen Parameter hinzufügen, um nur gebuchte Verkaufsaufträge zu senden. Sie benötigen die entsprechende Berechtigung zum Ausführen des jeweiligen Berichts oder der jeweiligen Codeunit, da ansonsten beim Ausführen der Projektwarteschlange ein Fehler auftritt.  

Optional im Feld **Kategorienfilter für Aufgabenwarteschlange** Feld, Sie wählen einen Filter, der gelten soll. Aufgabenwarteschlangenkategorien können verwendet werden, um Projekte in der Liste zu gruppieren.

[!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch aktiviert die Projekte entsprechend den angegebenen Plänen für jeden Aufgabenwarteschlangenposten. Sie können einen Projektwarteschlangenposten auch manuell beginnen, beenden und aktivieren.

### <a name="log-files"></a>Transaktionsprotokoll
Die Fehler werden im Fenster **Aufgabenwarteschlangen-Protokolleinträge** aufgeführt, das Sie im Menüband zugreifen können. Sie können auch Aufgabenwarteschlangenfehler beheben. Die Daten, die beim Ausführen einer Aufgabenwarteschlange generiert werden, werden an der Datenbank gespeichert.  

### <a name="background-posting-with-job-queues"></a>Buchen im Hintergrund mit Aufgabenwarteschlangen
Aufgabenwarteschlangen sind ein effektives Werkzeug, um die Ausführung von Geschäftsprozessen im Hintergrund zu planen. Ein Beispiel hierfür ist eine Instanz, in der mehrere Benutzer versuchen, Verkaufsaufträge gleichzeitig zu buchen, aber nur ein Auftrag gleichzeitig verarbeitet werden kann. Indem Sie eine Buchungsroutine im Hintergrund erstellen, können Sie die Buchungen in eine Warteschlange zur Bearbeitung im Hintergrund einreihen.  

 Alternativ können Sie Buchungen zu bestimmten Betriebszeiten planen, wenn es für Ihre Organisation hilfreich ist. Beispielsweise kann es in Ihrem Unternehmen sinnvoll sein, bestimmte Routinen dann auszuführen, wenn ein Großteil der Dateneingaben für einen Arbeitstag abgeschlossen wurde. Sie können dieses erreichen, indem Sie die oben Aufgabenwarteschlange auf Batch-Beitragsberichte des Ausführens verschiedene, wie **Aufträge stapelbuchen** **Verk. Rechnungen stapelbuchen** die **Verk.Gutschriften stapelbuchen** festlegen.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt die Hintergrundbuchung für die folgenden Belegarten:  

-   Vertrieb: Verkaufsauftrag, Verkaufsreklamation, Gutschrift, Rechnung  

-   Einkauf: Bestellung, Verkaufsreklamation, Gutschrift, Rechnung  

 Wenn die Aufgabenwarteschlange den Verkaufsauftrag nicht buchen kann, wird der Status auf **Fehler** geändert, und der Verkaufsauftrag wird der Liste von Verkaufsaufträgen hinzugefügt, die der Benutzer verarbeiten muss.  

> [!NOTE]  
>  Wenn Sie einen Beleg für die Buchung planen und den Buchungsvorgang starten, wird die Buchungsroutine automatisch das Timeout eines Aufgabenwarteschlangenpostens innerhalb von zwei Stunden konfigurieren, wenn die Buchungsroutine, aus beliebigen Grund aufhört zu reagieren.  

Sie richten diese mithilfe der Projektwarteschlange im Fenster **Debitoren & Verkauf Einr.** oder im Fenster **Kreditoren & Einkauf**, fest. Im Inforegister **Hintergrundbuchung** wählen Sie das Kontrollkästchen **Beitrags-Belege über Aufgabenwarteschlange** und füllen Sie die entsprechenden Informationen ein. Hier können Sie das Feld **Aufgabenwarteschlange - Kategoriencode** verwenden, um die Aufgabenwarteschlangenposten mit diesem Code auszuführen. Wenn Sie diese Kategorie auswählen, können Sie die **Verkauf buchen** Kategorie nutzen, die alle Aufträge filtert, die mit einer Projektwarteschlange übereinstimmen, die denselben Kategoriencode hat.  

> [!IMPORTANT]  
>  Wenn Sie einen Beleg an einen Drucker senden und der Drucker ein Dialogfeld anzeigt, wie eine Anforderung für Anmeldeinformationen oder eine Warnung über geringe Druckertinte, wird der Beleg gebucht, aber nicht gedruckt. Die entsprechenden Aufgabenwarteschlangenposten überschreiten letztendlich die Zeit und das Feld **Status** ist auf **Fehler** festgelegt. Entsprechend empfiehlt es sich, dass Sie kein Druckersetup verwenden, das Aktivität mit der Anzeige von Druckerdialogfeldern in Verbindung mit Hintergrundbuchung benötigt.  

## <a name="use-the-my-job-queue-part"></a>Nutzen Sie den Teil Meine Aufgabenwarteschange
Der **Meine Aufgabenwarteschlange**-Teil zeigt die Aufgabenwarteschlangenposten an, die ein Benutzer gestartet hat, die jedoch noch nicht abgeschlossen sind. Standardmäßig ist dieser Teil nicht sichtbar, Sie müssen ihn also Ihrem Rollencenter hinzufügen. Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).  

In diesem Teil können Sie die Dokumente einsehen, die verarbeitet oder in die Warteschlange eingereiht werden und für die Ihre ID im Feld **Zugewiesene Benutzer-ID** angegeben ist. Dieser Teil hilft Ihnen bei der Nachverfolgung aller Projektwarteschlangenposten, einschließlich derer, die sich auf die Hintergrundbuchung beziehen. Dieser Teil informiert Sie auf einen Blick darüber, ob bei der Buchung eines Belegs ein Fehler aufgetreten ist, oder ob ein Projektwarteschlangenposten einen Fehler enthält. Mit diesem Teil können Sie auch eine Buchung stornieren, wenn diese nicht ausgeführt wird.  

## <a name="security"></a>Sicherheit  
Aufgabenwarteschlangenposten werden auf Basis von Berechtigungen ausgeführt. Diese Berechtigungen müssen die Ausführung des Berichts oder der Codeunit ermöglichen.  

Wenn eine Aufgabenwarteschlange manuell aktiviert wird, wird sie mit den Anmeldeinformationen des Benutzers ausgeführt. Wenn eine Aufgabenwarteschlange über NAS aktiviert wird, wird sie mit den Anmeldeinformationen der Serverinstanz ausgeführt. Wenn ein Projekt ausgeführt wird, wird es mit den Anmeldeinformationen der Aufgabenwarteschlange ausgeführt, mit der das Projekt aktiviert wird. Jedoch muss der Benutzer, der den Aufgabenwarteschlangenposten erstellt hat, auch über Berechtigungen verfügen. Wenn ein Projekt in einer Benutzersession ausgeführt wird (zum Beispiel bei der Hintergrundbuchung), wird es mit den Anmeldeinformationen des Benutzers ausgeführt, der dieses Projekt erstellt hat.  

> [!IMPORTANT]  
>  Wenn Sie den SUPER-Zugriffsrechtsatz der Demolizenz für [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, sind Sie und Ihre Benutzer zum Ausführen aller Objekte berechtigt. In diesem Fall ist der Zugriff für jeden Benutzer nur durch Berechtigungen für Daten beschränkt.  

## <a name="using-job-queues-effectively"></a>Effektive Verwendung von Aufgabenwarteschlangen  
Der Aufgabenwarteschlangenposten hat viele Felder, deren Zweck darin besteht, Parameter in die Codeunit zu übertragen, die Sie für die Ausführung mit einer Aufgabenwarteschlange festgelegt haben. Dies bedeutet auch, dass Codeunits, die über die Aufgabenwarteschlange ausgeführt werden sollen, beim Warteschlangenposten als Parameter im **OnRun**-Trigger angegeben werden müssen. Dies gewährleistet ein zusätzliches Maß an Sicherheit, da so Benutzer über die Aufgabenwarteschlange keine beliebigen Codeunits ausführen können. Wenn der Benutzer Parameter einem Bericht weiterleiten muss, besteht hierfür die einzige Möglichkeit darin, die Berichtsausführung in eine Codeunit einzubinden, die anschließend die Eingabeparameter analysiert und in den Bericht einfügt, bevor dieser ausgeführt wird.  

## <a name="see-also"></a>Siehe auch  
[Verwaltung](admin-setup-and-administration.md)  
[Einrichten von Business Central](setup.md)  

