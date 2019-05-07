---
title: 'Gewusst wie: MwSt.-Berichte erstellen'
description: Verschiedene Arten von MwSt.-Erklärungen können basierend auf Anforderungen konfiguriert werden. Wenn Sie dann eine MwSt buchen müssen, können Sie sie auf der Seite MwSt Bericht erstellen und dann im elektronischen Format exportieren, das an die Anforderungen des ELMA5 Formats sich anpaßt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 40a98ad916a55cfbe606f04bee92d777479c2929
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "937716"
---
# <a name="create-vat-reports"></a>Erstellen von MwsT-Berichten.
Verschiedene Arten von MwSt.-Erklärungen können basierend auf Anforderungen konfiguriert werden. Wenn Sie dann eine MwSt buchen müssen, können Sie sie auf der Seite **MwSt Bericht** erstellen und dann im elektronischen Format exportieren, das an die Anforderungen des ELMA5 Formats sich anpaßt.  

## <a name="to-create-a-vat-report"></a>Einen MwSt.-Bericht erstellen:  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **MwSt-Bericht** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Füllen Sie im Inforegister **Allgemein** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nr.**|Geben Sie die Nummer der Erklärung an.<br /><br /> Je nach Art der Erklärung und der Konfiguration in Ihrem Unternehmen können Sie die automatisch generierte Nummer verwenden, eine andere Nummernserie auswählen oder eine andere Nummer manuell eingeben.|  
    |**MwSt.-Berichtstyp**|Wählen Sie die entsprechende MwSt Berichtstyp aus. Die Standardeinstellung ist **Standard**. Wenn der Bericht eine Aktualisierung auf ein existierendes Bericht ist, wählen Sie **Korrektur** aus.|  
    |**Handelstyp**|Geben Sie die Art des Handels an, den der Bericht beschreibt. Der Standardwert ist **Verkauf**. Andere Optionen sind **Einkäufe** oder **Beides**.|  
    |**Startdatum**|Geben Sie das Startdatum der Berichtsperiode an.|  
    |**Enddatum**|Geben Sie das Enddatum des Erklärungszeitraums an.|  
    |**EU-Waren/-Dienstleistungen**|Geben Sie an, ob der Bericht sich auf **Waren**, **Dienste** oder beides bezieht. Der Standardwert ist **Beides**.|  
    |**Berichtsperiodentyp**|Geben Sie den Zeitraum an, den der Bericht umfasst:<br /><br /> -   Monat<br />-   Quartal<br />-   Jahr<br />-   Zwei-Monatlich|  
    |**Berichtsperiodennummer**|Geben Sie die Nummer der Mehrwertsteuerperiode an.|  
    |**Berichtsjahr**|Gibt das Jahr an, das der MwSt.-Bericht abdeckt.|  
    |**Verarbeitungsdatum**|Gibt das Datum an, an dem der MwSt.-Bericht erstellt wurde.|  

3.  Füllen Sie im Inforegister **Genehmigen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Bereich zum Abzeichnen**|Gibt den Ort an, an dem der MwSt.-Bericht unterzeichnet wurde.|  
    |**Datum des Abzeichnens**|Gibt das Datum an, an dem der MwSt.-Bericht unterzeichnet wurde.|  
    |**Unterzeichnet von Mitarbeiter Nr.**|Geben Sie die Nummer des Mitarbeiters an, der den MwSt-Bericht aus der Lookupliste unterschrieben hat.|  
    |**Erstellt von Mitarbeiter Nr.**|Geben Sie die Nummer des Mitarbeiters an, der den MwSt-Bericht aus der Lookupliste erstellt hat.|  

4.  Jetzt müssen Sie die Mehrwertsteuerposten importieren, die in dieser MwSt.-Erklärung enthalten sein müssen.  
5. Wählen Sie die Aktion **Mahnungszeile vorschlagen**.  

Dadurch werden der Seite MwSt-Einträge hinzugefügt. Sie können optional für jede Zeile im Feld **Betrag** ein Drilldown durchführen, um die Mehrwertsteuerposten anzuzeigen, aus denen die Zeile resultiert.  

Nachdem Sie die MwSt.-Erklärung erstellt haben, müssen Sie sie an die Steuerbehörden übermitteln.  

## <a name="to-submit-a-vat-report"></a>Einen MwSt.-Bericht übermitteln:  

1.  Wählen Sie auf der Seite **MwSt-Bericht** die Aktion **Freigabe** aus.  
2.  Bestätigen Sie, dass Sie den Bericht freigeben möchten.  

    [!INCLUDE[d365fin](../../includes/d365fin_md.md)] prüft, ob die MwSt.-Erklärung korrekt eingerichtet ist. Wenn die Prüfung fehlschlägt, werden die Fehler auf der Seite **MwSt-Bericht Fehlerprotokoll** angezeigt, sodass Sie entsprechende Änderungen vornehmen können. Beispielsweise wird ein Fehler angezeigt, wenn Sie versuchen, eine Standard-MwSt.-Erklärung freizugeben, aber Sie der Erklärung noch keine Zeilen hinzugefügt haben.  

    Wenn Sie eine MwSt.-Erklärung als freigegeben kennzeichnen, ist sie nicht mehr editierbar. Wenn Sie die Erklärung ändern müssen, nachdem Sie sie als freigegeben gekennzeichnet haben, müssen Sie sie zuerst erneut öffnen.  

3.  Wählen Sie auf der Registerkarte die Aktion **Exportieren**, um einen MwSt-Bericht aus EU- Ausfuhr-Listendaten im Format ELMA5 zu erstellen. Speichern Sie eine Kopie des Berichtes, der den gewünschten Namen hat, der durch ELMA5 angegeben ist.  

    Sie können die Erklärung jetzt an die Steuerbehörden senden.  

4.  Wählen Sie die Akltion **Als Übermittelt markieren** aus.  

## <a name="see-also"></a>Siehe auch  
 [Zu korrigierender MwSt.-Bericht](how-to-correct-vat-reports.md)   
 [Richten Sie die MwSt.-Berichte ein.](how-to-set-up-vat-reports.md)
