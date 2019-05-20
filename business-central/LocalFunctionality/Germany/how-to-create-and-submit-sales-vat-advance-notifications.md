---
title: Vorgehensweise beim Erstellen und Senden von Umsatzsteuervoranmeldungen
description: In Business Central können Sie die Umsatzsteuervoranmeldungsdatei elektronisch an das ELSTER-Portal übermitteln. Sie können die Umsatzsteuervoranmeldungsdatei elektronisch an das Finanzamt übertragen, nachdem Sie den errechneten Steuerbetrag und die Bemessungsgrundlage geprüft haben.
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
ms.openlocfilehash: e8756130644620fcc37b441514b3ce963520a357
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246593"
---
# <a name="create-and-submit-sales-vat-advance-notifications"></a>Gewusst wie: Erstellen und Senden von Umsatzsteuervoranmeldungen
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie die Umsatzsteuervoranmeldungsdatei elektronisch an das ELSTER-Portal übermitteln. Sie können die Umsatzsteuervoranmeldungsdatei elektronisch an das Finanzamt übertragen, nachdem Sie den errechneten Steuerbetrag und die Bemessungsgrundlage geprüft haben.  

## <a name="to-create-an-xml-document-for-sales-vat-advance-notification"></a>So erstellen Sie ein XML-Dokument für Umsatzsteuervoranmeldung  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”") aus, und geben Sie **Umsatzsteuervoranmeldungsliste** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Auf der Seite **Umsatzsteuervoranmeldungsliste** auf der Registerkarte Aktionen, wählen Sie **Neu** aus.  
3.  Füllen Sie auf der Seite **MwSt-Voranmeldungskarte** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |------------------------------------|---------------------------------------|  
    |**Ansprechpartner für Finanzamt**|Die Kontaktperson für das Finanzamt in Ihrer Organisation.|  
    |**Telefonnummer Kontakt**|Telefonnummer der Kontaktperson.|  
    |**Kontakt-E-Mail**|E-Mail-Adresse der Kontaktperson.|  

5.  Wählen Sie die Aktion **XML-Datei erstellen** aus.  
6.  Im Batchauftrag **MwSt.-Voranmeldung erstellen** im Inforegister **Optionen**, im Feld **XML-Datei**, wählen Sie **Erstellen** oder **Erstellen und anzeigen** aus.  
7.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-submit-an-xml-document-for-sales-vat-advance-notification"></a>So übermitteln Sie ein XML-Dokument für Umsatzsteuervoranmeldung  

1.  Auf der Seite **Umsatzsteuervoranmeldungsliste** wählen Sie den Beleg aus, den Sie an ELSTER senden möchten.  
2.  Wählen Sie die Aktion **XML-Datei übermitteln** aus.  

Die XML-Datei wird an ELSTER übermittelt.  

## <a name="see-also"></a>Siehe auch  
 [Elektronische Übermittlung der Umsatzsteuervoranmeldungen an ELSTER](electronic-submission-of-sales-vat-advance-notifications-to-elster.md)   
 [Gewusst wie: Einrichten von Umsatzsteuervoranmeldungen für ELSTER](how-to-set-up-sales-vat-advance-notifications-for-elster.md)
