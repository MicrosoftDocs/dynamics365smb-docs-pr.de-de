---
title: Arbeitspläne erstellen
description: 'Diese Artikel gibt einen Überblick über die verschiedenen Möglichkeiten, Arbeitspläne zu erstellen, einschließlich der erforderlichen Voraussetzungen und wie Sie Arbeitsplan-Verknüpfungen erstellen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '99000764, 99000765, 99000766, 99000767, 99000794, 99000796, 99000798, 99000806, 99000808, 99000810, 99000817, 99000834, 99000835, 99000836, 99000837, 99000840, 99000841, 99000844, 99000845'
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# <a name="create-routings"></a>Arbeitspläne erstellen

Produktionsbetriebe verwenden Arbeitspläne, um den Produktionsablauf zu definieren.

Der Arbeitsplan ist auch die Basis für die Prozessplanung, Kapazitätsplanung und zur Dokumentation der Fertigung.  

Was Fertigungsstücklisten für die Arbeitspläne sind, sind Artikel beim Fertigungsendartikel. Im Arbeitsplan sind Stammdaten enthalten, die die Verarbeitungsanforderungen für bestimmte Fertigungsartikel erfassen. Nachdem ein Fertigungsauftrag für einen Artikel erstellt wurde, steuert dessen Arbeitsplan die Planung der Arbeitsgänge, die auf der Seite **FA-Arbeitsplan** unter dem Fertigungsauftrag dargestellt werden.  

Bevor Sie einen Arbeitsplan erstellen können, müssen die folgenden Einrichtungen verfügbar sein:  

- Artikelkarten wurden für übergeordnete Artikel erstellt, die an der Fertigung teilnehmen. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).
- Die Ressourcen sind eingerichtet. Weitere Informationen finden Sie unter [Arbeitsplatzgruppen und Arbeitsplätze einrichten](production-how-to-set-up-work-and-machine-centers.md)

## <a name="to-create-a-routing"></a>So erstellen Sie ein Routing

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitspläne** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie im Feld **Typ** eine der folgenden Optionen aus:
   - **Serie** zum Berechnen des Fertigungsarbeitsplans abhängig vom Eintrag im **Arbeitsgangnr.**- Feld  
   - Wählen Sie die Option **Parallel**, um die Arbeitsgänge abhängig vom Eintrag im Feld **Nächste Arbeitsgangnr.** zu berechnen. Feld  
5. Wenn Sie den Arbeitsplan bearbeiten möchten, setzen Sie das Feld **Status** auf **Neu** oder **In Entwicklung**.  

    So füllen Sie die Arbeitsplanzeilen aus
6. Im Feld **Vorherige Arbeitsgangnr.** geben Sie die Nummer des ersten Arbeitsgangs ein, z. B. **10**.  
7. Geben Sie im Feld **Art** die verwendete Ressourcenart an, z. B. **Arbeitsplatzgruppe**.  
8. Geben Sie im Feld **Nr.** die zu verwendende Ressource oder geben Sie sie im Feld ein.  
9. Geben Sie im Feld **Verbindungscode** einen Code für die Verbindung der Komponente mit einem bestimmten Arbeitsgang ein. Weitere Informationen finden Sie unter [So erstellen Sie einen Arbeitsplanlink](production-how-to-create-routings.md#to-create-routing-links).
10. Geben Sie in den Feldern **Bearbeitungszeit** und **Rüstzeit** die benötigte Dauer zum Ausführen des Arbeitsgangs ein.

     > [!NOTE]
     > Die Rüstzeit wird pro Fertigungsauftrag berechnet, wobei die Bearbeitungszeit pro Fertigungsartikel berechnet wird.  

11. Geben Sie im Feld **Gleichzeitig zu belasten** an, wie viele Einheiten der ausgewählten Ressource verwendet werden, um den Vorgang auszuführen. Beispielsweise halbiert sich die Bearbeitungszeit, wenn zwei Personen einem Verpackungsarbeitsgang zugeordnet werden.  
12. Füllen Sie weitere Zeilen für alle Arbeitsgänge aus, die für die Fertigung des betreffenden Artikels erforderlich sind.  
13. Wenn Sie aus einem vorhandenen Arbeitsplan kopieren möchten, klicken Sie auf **Arbeitsplan kopieren**, um vorhandene Zeilen auszuwählen.  
14. Um den Arbeitsplan zu aktivieren, wählen Sie im Feld **Status** Option **Zertifiziert** aus.  
15. Sie können den neuen Arbeitsplan an die Karte des betreffenden Fertigungsartikels anhängen, indem das Feld **Arbeitsplan-Nr.** ausgefüllt wird. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).  

> [!NOTE]  
> Denken Sie daran, die Standardkosten des Artikels anhand der **Artikelkarte** neu zu berechnen. Wählen Sie die Aktion **Produktion**, die Aktion **Standardkosten berechnen** und anschließend die Aktion **Alle Ebenen** aus.  

## <a name="to-create-routing-links"></a>So erstellen Sie einen Arbeitsplanlink

Sie können Arbeitsplanverbindungen von Komponenten mit speziellen Vorgängen erstellen, um deren Zuordnung auch dann beizubehalten, wenn die Fertigungsstückliste oder der Arbeitsplan geändert werden. Außerdem wird die zeitlich optimierte Buchung von Komponenten durch Verbindungen vereinfacht, und zwar zu Beginn des spezifischen verknüpften Arbeitsgangs und nicht bei Freigabe des vollständigen Fertigungsauftrags. Weitere Informationen finden Sie unter [Komponenten nach Vorgangsausgabe buchen](production-how-to-flush-components-according-to-operation-output.md).  

Ein weiterer wichtiger Vorteil besteht darin, dass verknüpfte Komponenten und Arbeitsgänge in einer logischen Vorgangsstruktur angezeigt werden, wenn Sie die Seite **Produktionsprotokoll** für Istmeldungen und Verbrauchsbuchungen verwenden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitspläne** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den Arbeitsplan mit den Arbeitsgängen, die Sie verbinden möchten.  

    Stellen Sie sicher, dass der Arbeitsplanstatus **In Entwicklung** ist.  

3. Wählen Sie im entsprechenden Arbeitsgang im Feld **Verbindungscode** einen Code aus.  
4. Fügen Sie ggf. verschiedene Verbindungscodes mit anderen Arbeitsgängen im Arbeitsplan hinzu.  

    > [!NOTE]  
    > Der gleiche Verbindungscode sollte nicht in verschiedenen Arbeitsgängen eines Arbeitsplans verwendet werden, da dabei möglicherweise eine Komponente fehlerhaft mit zwei verschiedenen Arbeitsgängen verknüpft wird, so dass sie zweimal verbraucht würde.  
    >
    > Es empfiehlt sich, den Verbindungscode nach dem Arbeitsgang zu benennen, um entsprechend spezifische Verbindungscodes zu erstellen.

5. Setzen Sie den Arbeitsplanstatus auf **Zertifiziert**.  

    Verbindungscodes werden nun Arbeitsplänen zugeordnet. Als Nächstes müssen Sie die tatsächliche Verbindung erstellen, indem Sie die gleichen Codes spezifischen Komponenten in der entsprechenden Fertigungsstückliste zuordnen.  

6. Öffnen Sie die **Fertigungsstückliste** mit den Komponenten, die Sie mit den obigen Arbeitsgängen verbinden möchten. Weitere Informationen finden Sie unter [Produktionsstücklisten erstellen](production-how-to-create-production-boms.md).
7. Stellen Sie sicher, dass der Status der Stückliste **In Entwicklung** ist.  
8. Klicken Sie auf der entsprechenden Zeile der Fertigungsstückliste in das Feld **Verbindungscode**, und wählen Sie den Code, den Sie dem entsprechenden Arbeitsgang zugeordnet haben.  
9. Fahren Sie mit dem Hinzufügen von Verbindungscodes zu anderen Komponenten fort. Dies muss den eindeutigen Arbeitsgängen und deren Verwendung entsprechen.  
10. Setzen Sie den Status der Fertigungsstückliste auf **Zertifiziert**.  

    > [!NOTE]  
    > Einen vorhandenen Fertigungsauftrag müssen Sie zuerst aktualisieren, um die Verbindungen aktivieren zu können. Weitere Informationen finden Sie unter [Fertigungsaufträge erstellen](production-how-to-create-production-orders.md).  

Die ausgewählten Komponenten werden nun mit den ausgewählten Arbeitsgängen verknüpft, wenn ein Fertigungsauftrag anhand der Fertigungsstückliste und des betreffenden Arbeitsplans erstellt oder aktualisiert wird. Dieser Link ist auf der Seite **FA-Komponenten** unter dem Fertigungsauftrag sichtbar. Sie können die Verbindungscodes jederzeit entfernen und hinzufügen.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Personal, Werkzeug und Prüfmaßnahmen den Arbeitsplanvorgängen zuweisen

Wenn Sie Personal mit besonderen Fähigkeiten, speziellem Wissen oder speziellen Qualifikationen für diesen Arbeitsgang benötigen, können Sie dieses Personal hier zuordnen. Darüber hinaus können Sie Werkzeugen Qualitätsanforderungen dem Arbeitsgang zuweisen. Hier wird beschrieben, wie Personal zugewiesen wird. Die Schritte sind für andere Arten Arbeitsgangsinformationen ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitspläne** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den entsprechenden Arbeitsplan.  
3. Im Inforegister **Zeilen** wählen Sie die Zeile aus, die Sie bearbeiten möchten, und wählen Sie dann die Aktion **Vorgänge** und **Personal** aus.  
4. Füllen Sie die Felder auf der Seite **Arbeitsgang Personal** aus.  
5. Wählen Sie die Schaltfläche **OK**, um die Seite zu verlassen. Die eingegebenen Werte werden kopiert und dem Arbeitsgang zugeordnet.  

## <a name="to-create-a-new-version-of-a-routing"></a>So erstellen Sie eine Version eines Arbeitsplans

Das Versionsprinzip ermöglicht Ihnen, mehrere Versionen eines Arbeitsplans zu verwalten. Die Struktur der Arbeitsplanversion entspricht der Struktur der Arbeitspläne, bestehend aus dem Arbeitsplanversionskopf und den Arbeitsgängen. Das Startdatum definiert den Hauptunterschied.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Arbeitspläne** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den zu kopierende Arbeitsplan, und wählen Sie die **Versionen** Aktion aus.  
3. Wählen Sie auf der Seite **Arbeitsgangversion** die Aktion **Neu** aus.
4. Geben Sie im Feld **Versionscode** eine eindeutige Kennung der Version ein. Sie können beliebige Kombinationen von Ziffern und Buchstaben verwenden.  

    Die neu erstellte Version erhält automatisch den Status **Neu**.  
5. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
6. Um Arbeitsgangszeilen zu erstellen, wählen Sie die erste leere Zeile, und füllen Sie dann **Arbeitsgangnr.** aus Füllen Sie das Feld Arbeitsgangnr. entsprechend der Reihenfolge der Arbeitsgänge aus.

    Die Arbeitsgänge sind in der Reihenfolge der Arbeitsgangnummern aufsteigend sortiert. Um später Änderungen durchführen zu können, empfehlen wir Ihnen die Auswahl angemessener Schrittweiten. Das **Nächste Arbeitsgangnr.** -Feld bezieht sich auf den nächsten Arbeitsgang im Arbeitsplan.

7. Wenn die Arbeitsplanversion eingerichtet haben, wählen Sie im Feld **Status** die Option **Zertifiziert** aus.

## <a name="see-also"></a>Siehe auch

[Produktionsstücklisten erstellen](production-how-to-create-production-boms.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Fertigung](production-manage-manufacturing.md)  
[Planung](production-planning.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
