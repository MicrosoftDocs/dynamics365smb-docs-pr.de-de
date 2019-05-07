---
title: Fehlermeldungen des ElsterTransferHandler
description: Wenn Business Central Umsatzsteuervoranmeldungen übermittelt, können Fehler auftreten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
redirect_url: how-to-set-up-and-export-sales-vat-advance-notifications.md
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1d829fbffa0e2e7a1b596997b992aea6607a9804
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935872"
---
# <a name="error-messages-of-the-elstertransferhandler"></a>Fehlermeldungen des ElsterTransferHandler
Wenn [!INCLUDE[d365fin](../../includes/d365fin_md.md)] Umsatzsteuervoranmeldungen übermittelt, können Fehler auftreten.  

Wenn beispielsweise die Konfigurationsdatei für die Microsoft.Dynamics.ElsterTransferHandler.dll-Assembly nicht den richtigen Anzeigenamen des öffentlichen Zertifikats enthält, gibt das ELSTER-Portal den Fehler 3400 zurück, und [!INCLUDE[d365fin](../../includes/d365fin_md.md)] zeigt die entsprechende Fehlermeldung an.  

## <a name="error-messages"></a>Fehlermeldungen  
In der folgenden Tabelle sind die Fehlermeldungen aufgelistet, die das ELSTER-Portal an [!INCLUDE[d365fin](../../includes/d365fin_md.md)] übermittelt.  

|**Fehlernummer**|**Beschreibung**|  
|----------------------|-------------------------------------------|  
|1000|ELSTER kann den Absender nicht als [!INCLUDE[d365fin](../../includes/d365fin_md.md)] identifizieren. Die Microsoft.Dynamics.ElsterTransferHandler.dll-Assembly kann nur mit Microsoft Dynamics-Produkten verwendet werden.|  
|2000|Es konnte beim Übermitteln von Daten keine Verbindung zu den OFD-Servern hergestellt werden. Dies kann ein Problem mit Ihrer Netzwerkverbindung sein. Prüfen Sie Ihre Netzwerkkonfiguration, oder versuchen Sie es zu einem späteren Zeitpunkt erneut.|  
|2100|Die XML-Datei konnte nicht gesendet werden, da die Verbindung unerwartet unterbrochen wurde.|  
|2200|Es konnte beim Empfangen von Daten keine Verbindung zu den OFD-Servern hergestellt werden. Dies kann ein Problem mit Ihrer Netzwerkverbindung sein. Prüfen Sie Ihre Netzwerkkonfiguration, oder versuchen Sie es zu einem späteren Zeitpunkt erneut.|  
|2300|Das Antwortdokument konnte nicht empfangen werden, da die Verbindung unerwartet unterbrochen wurde.|  
|3000|ELSTER konnte nicht auf das benutzerspezifische Zertifikat zugreifen. Sie müssen sich vergewissern, dass das Zertifikat richtig installiert ist.|  
|3100|Sie haben ein Dokument übermittelt, haben aber keinen Zugriff auf den Zertifikatspeicher. Sie müssen sich vergewissern, dass das Zertifikat richtig installiert ist.|  
|3200|Das benutzerspezifische Zertifikat konnte nicht gefunden werden. Sie müssen sich vergewissern, dass das Zertifikat richtig installiert ist.|  
|3300|Das angegebene Zertifikat weist keinen privaten Schlüssel auf, oder das Kennwort für den privaten Schlüssel ist falsch. Sie müssen sich vergewissern, dass das Zertifikat richtig installiert ist.|  
|3400|Das öffentliche Zertifikat der OFD konnte nicht geöffnet werden. Sie müssen sich vergewissern, dass das Zertifikat richtig installiert ist.|  
|4000|Das Antwortdokument konnte nicht entschlüsselt werden, da der private Schlüssel nicht mit dem öffentlichen Schlüssel übereinstimmt, der für die Verschlüsselung verwendet wurde.|  
|4100|Das Antwortdokument konnte nicht entschlüsselt werden. Die Daten wurden während der Übermittlung möglicherweise beschädigt. Sie müssen das Dokument erneut senden.|  
|5000|Das Dokument konnte nicht komprimiert werden. Dies kann auf einen Mangel an Speicherplatz auf dem Computer zurückzuführen sein, oder dass das Betriebssystem den Komprimierungsprozess beendet hat. Sie müssen das Dokument erneut senden.|  
|5100|Das Dokument konnte nicht dekomprimiert werden. Sie müssen das Dokument erneut senden.|  
|6000|Der Proxyserver antwortet nicht. Sie müssen sicherstellen, dass die Einrichtung von Umsatzsteuervoranmeldungen in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] korrekt ist.|  
|6100|Der Benutzer ist nicht dazu in der Lage, eine Verbindung mit dem Server herzustellen. Sie müssen sicherstellen, dass die Einrichtung von Umsatzsteuervoranmeldungen in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] korrekt ist.|  
|6200|Der Benutzer konnte nicht auf dem Proxyserver registriert werden. Sie müssen sicherstellen, dass die Einrichtung von Umsatzsteuervoranmeldungen in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] korrekt ist.|  
|7000|Die Daten konnten nicht signiert werden, da das konfigurierte Zertifikat nicht zum Signieren von Daten verwendet werden kann. Sie müssen sicherstellen, dass die Einrichtung von Umsatzsteuervoranmeldungen in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] korrekt ist.|  
|7100|Das XML-Dokument konnte nicht signiert werden. Dies kann auf einen Mangel an Speicherplatz auf dem Computer zurückzuführen sein, oder dass das Betriebssystem den Komprimierungsprozess beendet hat.|  
|9000|Ein Fehler ist aufgetreten, als das ELSTER-Portal versuchte, die Konfiguration des Zertifikats zu lesen. Sie müssen den Inhalt des generierten XML-Dokuments prüfen.|  

## <a name="see-also"></a>Siehe auch  
 [ELSTER-Übermittlung – Übersicht](elster-transmission-overview.md)   
 [Gewusst wie: Einrichten von Umsatzsteuervoranmeldungen für ELSTER](how-to-set-up-sales-vat-advance-notifications-for-elster.md)
