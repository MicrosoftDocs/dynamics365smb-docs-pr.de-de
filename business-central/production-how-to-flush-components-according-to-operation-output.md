---
title: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren
description: Für Artikel, die mit der Rückwärtsbuchungsmethode erstellt wurden, ist das Standardverhalten, Komponentenverbrauch zu berechnen und zu buchen, wenn Sie den Status eines freigegebenen Fertigungsauftrags in Erledigt ändern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d1448b9105426103d70abfb820bd38b6adb41db8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779253"
---
# <a name="flush-components-according-to-operation-output"></a>Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren
Sie können verschiedene Buchungsmethoden definieren, um die Registrierung des Verbrauchs von Komponenten zu automatisieren. 

Wenn beispielsweise ein Fertigungsauftrag, 800 Meter zu produzieren, 8 Kilogramm einer Komponente benötigt, dann werden, wenn Sie 200 Meter buchen, wie ausgegeben, 2 Kilogramm automatisch als Verbrauch gebucht. 

Diese Funktionalität ist aus folgenden Ursachen nützlich:  

- **Lagerwert ermitteln**

    Wertposten für Istmeldungen und Verbräuche werden beim Fortschritt des Fertigungsauftrags erstellt. Ohne Verbindungscodes erhöht sich der Lagerwert, wenn Ausstoß registriert wird, und vermindert sich später, wenn der Wert des Komponentenverbrauchs zusammen mit dem beendeten FA gebucht wird.  
- **Lager - Verfügbarkeit**

    Mit allmählicher Verbrauchsbuchung wird die Verfügbarkeit von Komponenten aktueller, was wichtig ist, um die interne Balance zwischen Bedarf und Vorrat aufrechtzuerhalten. Ohne Verbindungscodenummern glauben möglicherweise andere, die Bedarf für die Komponente haben, dass sie verfügbar ist, solange eine verzögerte Verbrauchsbuchung dafür aussteht.  
- **Just-in-Time**

    Mit der Möglichkeit, Produkte an Debitorenanfragen anzupassen, können Sie Abfall minimieren, indem Sie sicherstellen, dass Arbeits- und Systemänderungen nur eintreten, wenn es erforderlich ist.  

Sie können dies durch Kombination der Rückwärtsbuchen und der Verbindungscodes erreichen, sodass die Menge, die je Arbeitsgang geleert wird, zur aktuellen Isteffektivität des abgeschlossenen Arbeitsgangs proportional ist. Für Artikel, die mit der Rückwärtsbuchungsmethode erstellt wurden, ist das Standardverhalten, Komponentenverbrauch zu berechnen und zu buchen, wenn Sie den Status eines freigegebenen Fertigungsauftrags in **Erledigt** ändern. Wenn Sie auch Verbindungscodes definieren, dann erfolgt die Berechnung und Buchung, wenn jeder Arbeitsgang beendet ist, und die Menge, die tatsächlich im Arbeitsgang verbraucht wurde, wird gebucht. Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Bearbeiten** aus.  
3.  Wählen Sie im Inforegister **Beschaffung** im Feld **Buchungsmethode** die Option **Rückwärts** aus.  

    > [!NOTE]  
    >  Wählen Sie **Kommiss. + Rückwärts** aus, wenn die Komponente in einem Lagerplatz verwendet wird, der für die gesteuerte Einlagerung und Kommissionierung eingerichtet ist.  

4.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Routings** ein, und wählen Sie dann den zugehörigen Link.  
5.  Definieren Sie Verbindungscodes für jeden Arbeitsgang, der die Komponente verbraucht. Weitere Informationen finden Sie unter [Arbeitspläne erstellen ](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Verwenden Sie nicht dieselbe Routing-Routing-Verbindung für verschiedene Vorgänge im Routing, da dies zur Registrierung des Verbrauchs von Komponenten für jeden verknüpften Vorgang führt.  
6.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Fertigungsstückliste** ein und wählen Sie dann den entsprechenden Link.  
7.  Definieren Sie Verbindungscodes von jeder Instanz der Komponente zu dem Arbeitsgang, in dem sie verbraucht wird.

Der Verbrauch wird automatisch gebucht, wenn Sie die Ausgabe registrieren. Weitere Informationen finden Sie unter [Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Buchungsmethode

In der folgenden Tabelle werden die verfügbaren Optionen für die Buchungsmethode beschrieben, die Sie auf **Artikel**-Karten und **Lagerhaltungsdaten**-Karten festlegen.

|Option|Beschreibung|
|------------|-------------|  
|Manuell|Erfordert, dass Sie den Verbrauch manuell im FA-Verbrauchs Buch eingeben und buchen.|
|Vorwärts|Bucht Verbräuche automatisch entsprechend den Fertigungsauftragskomponentenzeilen. <br><br>Standardmäßig tritt die Buchung des Komponentenverbrauchs auf, wenn Sie den Status eines Fertigungsauftrags auf **Freigegeben** ändern. Wenn Sie jedoch das Feld **Verbindungscode** in den Fertigungsauftragskomponentenzeilen verwenden, dann erfolgt das Buchen pro Arbeitsgang, wenn der Arbeitsgang beginnt. Weitere Informationen finden Sie unter [Gewusst wie: Arbeitspläne erstellen](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Hinweis**<br>Für Vorausbuchung basiert die entsprechende Buchung, die Sie mit Verbindungscodes erhalten, auf der erwarteten Menge, die in der Komponentenzeile definiert ist. Informationen zu Arbeitsgang-spezifischen Buchungen basierend auf der Isteffektivität finden Sie in der Beschreibung für **Rückwärts** in diesem Thema.<br><br>Wenn der Lagerort oder die Ressourcen, für die diese Komponente verbraucht werden, mit einer Standardlagerplatzstruktur eingerichtet werden, wird der Artikel vom **Off. Fert.-Ber.-Lagerpl.-Code** verbraucht. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Wichtig** <br>Vorausbuchung tritt auch auf, wenn Sie auf **Aktualisieren** auf einem freigegebenen Fertigungsauftrag klicken, der von Grund auf neu erstellt wurde. In diesen direkt erstellten und freigegebenen Fertigungsaufträgen können Sie keine Lagerplatzinformationen ändern, da die Fertigungsauftragskomponentenzeilen generiert werden, wenn Sie den Auftrag aktualisieren, der Komponenten gleichzeitig vorwärts bucht. Wenn Sie Lagerplatzinformationen über Fertigungsauftragskomponentenzeilen ändern möchten, bevor die Vorausbuchung auftritt, muss dieser Auftrag mit dem *geplanten* oder *fest geplanten* Status erstellt werden.|
|Rückwärts|Berechnet und bucht Verbräuche automatisch entsprechend den Fertigungsauftragskomponentenzeilen.<br><br> Standardmäßig tritt die Berechnung und Buchung des Komponentenverbrauchs auf, wenn Sie den Status eines freigegebenen Fertigungsauftrags auf **Beendet** ändern. Wenn Sie jedoch das Feld **Verbindungscode** in den Fertigungsauftragskomponentenzeilen verwenden, dann erfolgt das Berechnen und Buchen beim Beenden jedes Arbeitsgangs.<br><br> **Hinweis** <br>Das Rückwärtsbuchen und die Verbindungscodes können zusammengefasst werden, sodass die Menge, die je Arbeitsgang geleert wird, zur aktuellen Isteffektivität dieses Arbeitsgangs proportional ist. Weitere Informationen finden Sie unter [Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](#to-flush-components-according-to-operation-output).<br><br> Wenn der Lagerort oder der Arbeitsplatz, für die diese Komponente verbraucht werden, mit einer Standardlagerplatzstruktur eingerichtet werden, wird der Artikel vom **Off. Fert.-Ber.-Lagerpl.-Code** verbraucht.|
|Kommiss. + Vorwärts|Das gleiche gilt für die Vorausbuchungsmethode, mit der Ausnahme, dass dies nur für Lagerorte funktioniert, die gesteuerte Einlagerung und Kommissionierung verwenden.<br><br> Verbrauch wird aus dem Lagerort berechnet und gebucht, der im Feld **Fert.-Bereitst.-Lagerplatzcode** im Lagerplatz oder dem Arbeitsplatz definiert wird, nachdem die Komponente aus dem Lager kommissioniert wurde.<br><br> **Hinweis** <br>Wenn eine Komponente mit der Kommissionierungs- + Vorausbuchungsmethode eingerichtet wird, kann sie keinen Verbindungscode für einen Arbeitsgang haben, der mit der Vorausbuchungsmethode eingerichtet wurde. Die Komponente wird dann automatisch geleert, wenn der Arbeitsgang beginnt, was das Anfordern der Kommissionierungsaktivität unmöglich macht.|
|Kommiss. + Rückwärts|Das gleiche gilt für die Rückwärtsbuchungsmethode, mit der Ausnahme, dass dies nur für Lagerorte funktioniert, die gesteuerte Einlagerung und Kommissionierung verwenden.<br><br> Verbrauch wird aus dem Lagerort berechnet und gebucht, der im Feld **Fert.-Bereitst.-Lagerplatzcode** im Lagerplatz oder dem Arbeitsplatz definiert wird, nachdem die Komponente aus dem Lager kommissioniert wurde.|

## <a name="see-also"></a>Siehe auch

[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planung](production-planning.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
