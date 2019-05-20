---
title: ELSTER-Übermittlung – Übersicht
description: Wenn ein Benutzer eine Umsatzsteuervoranmeldung von Business Central an das Onlineportal „Elektronische Steuererklärungen (ELSTER)” übermittelt, verarbeitet die Microsoft.Dynamics.ElsterTransferHandler-Assembly das Dokument und übermittelt es dann an ELSTER.
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
ms.openlocfilehash: bf3a9c6b3869ab510376939b48b7452f03cdd4af
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1237947"
---
# <a name="elster-transmission-overview"></a>ELSTER-Übermittlung – Übersicht
Wenn ein Benutzer eine Umsatzsteuervoranmeldung von [!INCLUDE[d365fin](../../includes/d365fin_md.md)] an das Onlineportal „Elektronische Steuererklärungen (ELSTER)” übermittelt, verarbeitet die Microsoft.Dynamics.ElsterTransferHandler-Assembly das Dokument und übermittelt es dann an ELSTER. Im nächsten Abschnitt werden technische Aspekte der Übermittlung von Dokumenten an ELSTER beschrieben.  

## <a name="process-overview"></a>Prozess – Überblick  

1.  Innerhalb des Programms werden alle relevanten Daten erfasst und in ein XML-Dokument geschrieben, das einem von der Oberfinanzdirektion (OFD) vorgegebenen Schema entspricht. Dieses Dokument enthält Steuerdaten sowie Informationen zu dem Unternehmen und der Person, die diese Steuerdaten übermittelt.  
2.  Nachdem dieses Dokument erfolgreich erstellt wurde, wird es um Konfigurationsinformationen (Proxyserver, Zertifikate usw.) erweitert, die von Microsoft.Dynamics.ElsterTransferHandler benötigt werden.  
3.  Das vollständige Dokument wird an Microsoft.Dynamics.ElsterTransferHandler übergeben. Die Assembly führt eine weitere Verarbeitung der Daten aus (Verschlüsselung, Komprimierung, Signatur) und sendet diese an einen der Server der OFD.  

    Sie können die Servern der OFD auf der Seite **Elektronische Umsatzsteuererklärung – Einrichtung** angeben. Weitere Informationen finden Sie unter [Gewusst wie: Einrichten von Umsatzsteuervoranmeldungen für ELSTER](how-to-set-up-sales-vat-advance-notifications-for-elster.md).  

4.  Die Daten werden vom Server der OFD empfangen und verarbeitet, und ein Antwortdokument wird zurückgesendet.  
5.  Das Antwortdokument wird von Microsoft.Dynamics.ElsterTransferHandler empfangen, entschlüsselt und dekomprimiert und als XML-Dokument an [!INCLUDE[d365fin](../../includes/d365fin_md.md)] zurückgegeben. Sie können dann die Antworten auf der Seite **MwSt.-Übertragungsprotokollposten** anzeigen.  

## <a name="process-details"></a>Verarbeiten von Details  
Die Microsoft.Dynamics.ElsterTransferHandler-Assembly ist für die Aufbereitung vor der Übermittlung an die OFD sowie die Verarbeitung des Antwortdokuments vor der Rückgabe an das Programm zuständig.  

## <a name="compression"></a>Komprimierung  
Das verwendete Komprimierungsverfahren ist GZIP. Eine Komprimierungsmethode, die Datenintegrität anhand einer Redundanzprüfung gewährleistet. Weitere Informationen finden Sie unter [System.IO.Compression.GZipStream](https://go.microsoft.com/fwlink/?LinkId=200710) in MSDN-Bibliothek. Bestimmte Teile der Dokumente werden mithilfe des GZIP-Verfahrens komprimiert.  

Das Antwortdokument wird ebenfalls mithilfe dieses Verfahrens komprimiert. Der Handler muss die Daten vor der Rückgabe an die Anwendung dekomprimieren.  

## <a name="encryption"></a>Verschlüsselung  
Der Standard, der für Verschlüsselung verwendet wird, lautet PKCS#7v1.5. Weitere Informationen finden Sie unter [System.Security.Cryptography.Pkcs.EnvelopedCms](https://go.microsoft.com/fwlink/?LinkId=200708) in der MSDN-Bibliothek. Mit diesem Verfahren werden nicht nur die Daten, sondern auch Empfängerinformationen in Form eines Zertifikats von der OFD verschlüsselt. Diese Verschlüsselung basiert auf einer asymmetrischen Methode, durch das sichergestellt ist, dass die Daten nur vom Empfänger entschlüsselt werden können. Die Daten werden mit einem Teil des Zertifikats verschlüsselt, der öffentlich zugänglich ist (PublicKey), und können ausschließlich mit dem nicht öffentlichen Teil des Zertifikats (PrivateKey) entschlüsselt werden. Darüber hinaus müssen die Empfängerinformationen aus der Verschlüsselung dem Empfängerzertifikat entsprechen. Dadurch ist sichergestellt, dass die Daten nur von der OFD entschlüsselt werden können.  

Bei der Antwort wird dasselbe Verfahren verwendet. Zusammen mit den übertragenen Daten empfängt die OFD den öffentlichen Teil des Benutzerzertifikats, der zum Verschlüsseln des Antwortdokuments verwendet wird. Dadurch ist sichergestellt, dass das Antwortdokument nur vom Empfänger entschlüsselt werden kann.  

Um die verschlüsselten Daten in einer textbasierten XML-Datei zu übertragen, müssen sie Base64-codiert werden. Mit dieser Methode werden binäre Daten in Textform dargestellt.  

## <a name="signature"></a>Unterschrift  
Für die Signatur der Daten wird eine Methode gemäß der standardmäßigen XML-DSig verwendet. Weitere Informationen finden Sie unter [System.Security.Cryptography.Xml.SignedXml](https://go.microsoft.com/fwlink/?LinkId=200709) in der MSDN-Bibliothek. Bei diesem Verfahren wird eine Signatur auf das gesamte Dokument oder einen Teil des Dokuments angewendet, der mit einem Zertifikat verschlüsselt wird. Bei Verwendung dieser Verschlüsselung (auch mit einer asymmetrischen Methode) ist die Zuordnung zu einem bestimmten registrierten Benutzer durch die OFD möglich. Auf diese Weise kann die Datenintegrität sichergestellt und die Identität des Absenders anhand der Signatur ermittelt werden.  

Die Integrität ist dadurch sichergestellt, dass bei einer Änderung des Dokuments nach dem Signieren die Signatur ungültig wird und die Daten von der OFD zurückgewiesen werden.  

Die Identität des Absenders wird durch eine Zuordnung des Zertifikats zu einem registrierten Benutzer festgestellt. Es wird geprüft, ob das Zertifikat gültig ist, gesperrt ist oder andere Unregelmäßigkeiten festgestellt wurden.  

## <a name="see-also"></a>Siehe auch  
 [Fehlermeldungen des ElsterTransferHandler](error-messages-of-the-elstertransferhandler.md)   
 [Elektronische Übermittlung der Umsatzsteuervoranmeldungen an ELSTER](electronic-submission-of-sales-vat-advance-notifications-to-elster.md)   
 [Gewusst wie: Einrichten von Umsatzsteuervoranmeldungen für ELSTER](how-to-set-up-sales-vat-advance-notifications-for-elster.md)
