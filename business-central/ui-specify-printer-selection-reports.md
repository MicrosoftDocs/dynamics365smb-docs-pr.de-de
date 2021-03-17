---
title: Einrichten von Berichten, um auf bestimmte Druckern zu drucken | Microsoft Docs
description: Weitere Informationen zum Definieren eines Druckers für eine Bericht und zur Nutzung der Druckerauswahlseite.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 59e3efb3800b309203c77f566bf909f92d7e0882
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390631"
---
# <a name="set-up-printers"></a>Einrichten von Druckern
Da [!INCLUDE[prod_short](includes/prod_short.md)] ein Cloud-Service ist, kann er keine lokalen Drucker erreichen, die mit den Rechnern der Benutzer verbunden sind. Sie kann jedoch mit Cloud-fähigen Druckern verbunden werden. In der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)] wird ein Cloud-Drucker namens **E-Mail-Drucker** als Erweiterung installiert und ist nach der Ersteinrichtung einsatzbereit.

Wenn ein Cloud-Drucker nicht installiert und eingerichtet ist oder wenn ein installierter Drucker ausfällt, werden beim Drucken standardmäßig die Druckoptionen des Browsers verwendet. Dies wird durch diesen Wert im Feld **Drucker** auf der Berichtsanforderungsseite angezeigt: *(keines, wird vom Browser behandelt)*.

Auf der Seite **Druckerverwaltung** sehen Sie die Drucker, die eingerichtet sind. Wenn Sie einen oder mehrere Drucker eingerichtet haben, können Sie die Seite **Druckerauswahlen** öffnen, um für Ihr Benutzerkonto einzurichten, welche spezifischen Berichte mit welchem Drucker gedruckt werden sollen.

Wenn ein Drucker eingerichtet und bestimmten Berichten zugeordnet ist, drucken Sie einen Bericht, indem Sie auf der Berichtsanforderungsseite die Schaltfläche **Drucken** wählen. Weitere Informationen finden Sie unter [Drucken eines Berichts](ui-work-report.md#PrintReport).

### <a name="sizing-print-jobs"></a>Größe von Druckaufträgen anpassen
Das Drucken in der Cloud ist für Dokumente mit einer angemessenen Größe vorgesehen. Die meisten Clouddienste, einschließlich PrintNode und HP ePrint, sind auf 10 MB pro Auftrag begrenzt. Wenn Sie größere Berichte drucken müssen, müssen Sie diese möglicherweise in mehrere Ausdrucke aufteilen.

## <a name="to-set-up-a-printer"></a>So richten Sie einen Drucker ein
Auf der Seite **Druckerverwaltung** sehen Sie die eingerichteten Drucker, und Sie können auf die Seite **Einstellungen** für jeden Drucker zugreifen, um eine vorhandene Einrichtung zu bearbeiten oder einen neuen Drucker einzurichten.

Die folgende Prozedur beschreibt die Einrichtung des vorhandenen Druckers **E-Mail-Drucker**, bei dem es sich um eine vorinstallierte Erweiterung handelt.

> [!NOTE]
> Um den E-Mail-Druck zu verwenden, muss die E-Mail-Funktionalität eingerichtet werden. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Druckerverwaltung** ein, und wählen Sie dann den entsprechenden Link.
2. Markieren Sie die Zeile für den Drucker **E-Mail-Drucker** und wählen Sie dann die Aktion **Druckereinstellungen bearbeiten**.
3. Füllen Sie auf der Seite **Einstellungen** die Felder wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Sie müssen das geeignete Papierformat für einen Drucker manuell auswählen, da keine lokalen Drucker- oder Benutzereinstellungen gespeichert werden können.
    >
    > Beachten Sie, dass die E-Mail-Drucker-Erweiterung standardmäßig auf **A4** Papierformat eingestellt ist, was z.B. in Nordamerika nicht geeignet ist.
4. Um einen Drucker zu Ihrem Standarddrucker zu machen, wählen Sie auf der Seite **Druckerverwaltung** das Modul **Als mein Standarddrucker festlegen**.

### <a name="privacy-notice"></a>Datenschutzhinweis
Wenn Sie die E-Mail-Drucker-Erweiterung verwenden, dann werden alle oder einige Druckaufträge an die E-Mail-Adresse gesendet, die Sie bei der Konfiguration des Druckers angegeben haben. Wir empfehlen dringend, dass eine eindeutige E-Mail-ID an ein Druckergerät gebunden wird, das nur die offiziellen Dienste des Hardware-Herstellers nutzt, wie z.B. HP ePrint, KonicaMinolta EveryonePrint oder Epson Email Print.

Sie müssen alle erforderlichen Datenschutzvorkehrungen treffen, einschließlich der Sicherstellung, dass die E-Mail-Drucklösung über ordnungsgemäß konfigurierte Berechtigungen, Datenschutzeinstellungen und Aufbewahrungsrichtlinien verfügt. Es liegt in Ihrer Verantwortung, eine korrekte, verifizierte und funktionsfähige E-Mail-Adresse anzugeben. Weitere Informationen finden Sie unter [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>So wählen Sie aus, welche Drucker welche Berichte drucken

Auf der Seite **Druckerwahlen** können Sie für Ihr Benutzerkonto einstellen, welche Berichte von welchem Drucker gedruckt werden. Dies ist nützlich, wenn Sie mit verschiedenen Berichten arbeiten, die aufgrund ihrer Platzierung in der Firma oder ihrer Ausgabemöglichkeiten unterschiedliche Drucker erfordern.

> [!IMPORTANT]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort kann die Seite **Druckerauswahl** nur für Drucker verwendet werden, die durch Druckerweiterungen definiert sind. Sie kann nicht für lokale Drucker verwendet werden.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Druckerverwaltung** ein und wählen Sie dann den entsprechenden Link. Alternativ können Sie auf der Seite **Druckerverwaltung** einen Drucker auswählen und dann die Aktion **Druckerauswahl** wählen.
2. Wählen Sie die Aktion **Neu**, um eine Druckerauswahl für einen bestimmten Bericht hinzuzufügen.
3. Füllen Sie die Felder nach Bedarf aus.

Der angegebene Bericht ist jetzt so eingerichtet, dass er standardmäßig auf dem ausgewählten Drucker gedruckt wird.

> [!NOTE]
> Wenn Sie den betreffenden Bericht drucken, können Sie diese Einstellung außer Kraft setzen, indem Sie auf der Anforderungsseite **Druckeinstellungen** einen anderen Drucker auswählen.

> [!NOTE]
> Wenn Sie auf der Seite **Druckerauswahl** keinen Bericht für einen bestimmten Drucker einrichten, wird er auf dem Standarddrucker der Firma gedruckt, wie er auf der Seite **Druckerverwaltung** definiert ist.

Sie oder der Administrator können auch die Seite **Druckerauswahl** verwenden, um andere Varianten des Druckens für Benutzer und Berichte zu definieren. Die folgende Tabelle beschreibt die Kombination von Werten zur Angabe verschiedener Druckeinstellungen für einen Bericht.

|Aktion                                                 |Stellen Sie die folgenden Werte ein                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Einen Bericht für alle Benutzer auf einem bestimmten Drucker ausdrucken |Geben Sie Werte in den Feldern **Berichts-ID** und **Druckername** an und lassen Sie das Feld **Benutzer-ID** leer.|
|Drucken aller Berichte auf einem bestimmten Drucker für einen bestimmten Benutzer|Geben Sie Werte in die Felder **Benutzer-ID** und **Druckername** ein und lassen Sie das Feld **Berichts-ID** leer.|
|Legen Sie den Standarddrucker für alle Berichte fest|Geben Sie einen Wert in das Feld **Druckername** ein und lassen Sie die Felder **Benutzer-ID** und **Berichts-ID** leer.|
|Drucken eines bestimmten Berichts auf dem Standarddrucker des Benutzers|Geben Sie einen Wert in das Feld **Berichts-ID** ein und lassen Sie die Felder **Druckername** und **Benutzer-ID** leer.|
|Drucken eines bestimmten Berichts auf einem bestimmten Drucker für einen bestimmten Benutzer|Geben Sie Werte in allen drei Feldern an.|

> [!NOTE]
> Spezifischere Druckerauswahlen haben Vorrang vor einer allgemeineren Druckerauswahl. Zum Beispiel hat eine Druckerauswahl, die Werte in den Feldern **Benutzer-ID**, **Berichts-ID** und **Druckername** hat, Vorrang vor einer Druckerauswahl, die leere Einträge in den Feldern **Benutzer-ID** oder **Berichts-ID** hat.

## <a name="see-also"></a>Siehe auch
[Berichte drucken](ui-work-report.md#PrintReport)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ausführen von Stapelverarbeitungen](ui-how-run-batch-jobs.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]