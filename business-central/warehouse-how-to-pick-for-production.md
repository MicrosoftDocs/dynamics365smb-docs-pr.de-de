---
title: 'Kommissionierung oder Umlagerung von Artikeln für Produktion, Montage oder Projekte in Grund-Lagerkonfigurationen'
description: 'Wenn Ihr Lagerort eine Verarbeitung der Kommissionierung, aber keine Versandverarbeitung erfordert, verwenden Sie die Seite Lagerkommissionierungen, um die Kommissionierung der Komponenten zu erfassen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Kommissionierung für Produktion, Montage oder Projekte in Grund-Lagerkonfigurationen

Wie Sie Ihre Komponenten für Produktion, Projekte oder Montageaufträge kommissionieren, hängt davon ab, wie Ihr Lagerort eingerichtet wurde. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).

Aktivieren Sie in einer Basislagerkonfiguration für den ausgehenden Fluss (Kommissionierung) die Schalter **Kommissionierung erfordern** aber deaktivieren den Schalter **Warenausgang erforderlich** auf der Seite **Lagerortkarte** für den Lagerort.

Verwenden Sie folgende Belege für interne Arbeitsgänge:

* Lagerkommissionierung
* Lagerbestandsumlagerung

## <a name="inventory-picks"></a>Lagerkommissionierungen

* Wenn Sie eine Lagerkommissionierung für einen internen Vorgang erfassen, wie etwa Produktion oder einen Auftrag, wird der Verbrauch der kommissionierten Komponenten gleichzeitig gebucht.
* Der Schalter **Lagerplatz erforderlich** auf der Seite **Lagerortkarte** ist optional.
* Wenn Sie Lagerkommissionierungen verwenden, definiert das Feld **Lagerplatzcode** in der Komponentenzeile eines Fertigungsauftrags oder den Auftragsplanungszeilen den *Entnahme*-Lagerplatz. Beim Buchen des Verbrauchs werden die Komponenten im Entnahme-Lagerplatz verringert.

## <a name="inventory-movements"></a>Lagerbestandsumlagerungen

* Lagerbestandsumlagerungen erfordern, dass Sie den Schalter **Lagerplatz erforderlich** auf der Seite **Lagerplatzcode** für den Lagerplatz aktivieren.
* Lagerbestandsumlagerungen funktionieren nur mit Produktionsauftragskomponentenzeilen und Montageauftragszeilen.
* Wenn Sie eine Lagerbestandsumlagerung für einen internen Vorgang registrieren, erfassen Sie nur die physische Umlagerung der Komponenten an einen Lagerplatz im Arbeitsgangbereich. Sie posten keinen Verbrauch.
* Wenn Sie Lagerbestandsumlagerungen verwenden, definiert das Feld **Lagerplatzcode** in Komponentenzeilen eines Fertigungsauftrags den *Platzieren*-Lagerplatz im Arbeitsgangbereich. Der Lagerplatz ist der Ort, an dem die Lagermitarbeiter die Komponenten ablegen müssen.
* Erfassen Sie den Verbrauch der kommissionierten Komponenten separat, indem Sie ein Verbrauchsjournal oder einen Montageauftrag buchen.

>[!NOTE]
> Auch wenn der Schalter **Entnahme erforderlich** deaktiviert ist, können Sie ein **Lagerentnahmedokument** verwenden. Lagerkommissionierungsdokumente ähneln Dokumente für **Bestandskommissionierung**. Dies ist nützlich, wenn Sie Entnahmen in Vorgängen verwenden und in ausgehenden Lagerflüssen versenden möchten.

### <a name="production"></a>Produktion

Verwenden Sie **Bestandskommissionierungsdokumente** für die Kommissionierung von Produktionskomponenten im Fluss zur Produktion.

Für einen Lagerort, der Lagerplätze verwendet, können Sie den Fluss zur Produktion erweitern, indem Sie **Lagerbestandsumlagerungsbelege** verwenden. Lagerbestandsumlagerungen sind besonders nützlich für die Komponentenbuchung. Weitere Informationen darüber, wie der Komponentenverbrauch aus Fert.-Bereitst.- oder Off. Fert.-Ber.-Lagerplätzen gebucht wird, finden Sie unter [Buchungen von Produktionskomponenten in einer Basislagerkonfiguration](#flushing-production-components-in-a-basic-warehouse-configuration).

### <a name="assembly"></a>Montage

Verwenden Sie **Lagerbestandsumlagerungsdokumente** , um Montagekomponenten in den Montagebereich umzulagern.

> [!NOTE]
> Dokumente für **Lagerbestandsumlagerungen** erfordern Lagerplätze.

[!INCLUDE [prod_short](includes/prod_short.md)] unterstützt Lagermontage und Auftragsmontage-Typen von Montageflüssen. Weitere Informationen zur Auftragsmontage im ausgehenden Lagerfluss finden Sie unter [Handhabung von Auftragsmontageartikeln mit Bestandskommissionierung](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="project-management"></a>Projektmanagement

Verwenden Sie Dokumente für **Lagerbestandskommissionierung** für die Kommissionierung von Auftragskomponenten im Fluss zum Produktionsmanagement.

Für Lagerorte, die Lagerplätze verwenden, können Sie den Fluss mit **Lagerbestandsumlagerungsbelegen** zu Aufträgen erweitern.

> [!NOTE]
> Die Möglichkeit, Komponenten für Auftragsplanungslinien auszuwählen, wurde hinzugefügt[!INCLUDE[d365fin](includes/d365fin_md.md)] 2022 Veröffentlichungswelle 2. Um die Funktion zu verwenden, muss Ihr Administrator **Funktion Aktualisieren: Lagerbestand und Lagerkommissionierungen von Aufträgen aus aktivieren** auf der Seite **Funktionsverwaltung** aktivieren.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] verwendet den Wert im Feld **Verbleibende Menge** in der Auftragsplanungszeile, wenn es Bestandsentnahmen erstellt. Um Bestandsentnahmen für Aufträge zu verwenden, müssen Sie den Schalter **Nutzungslink anwenden** auf der Seite **Projektkarte** Seite für das Projekt umschalten. Auf diese Weise können Sie die Nutzung anhand Ihres Plans verfolgen. Wenn Sie den Schalter nicht einschalten, bleibt die Restmenge bei **0** und die Bestandsauswahl wird nicht erstellt. Weitere Informationen finden Sie unter [Projektverbrauch-Nachverfolgung einrichten](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking)

## <a name="pick-or-move-for-production-assembly-and-projects-in-a-basic-warehouse-configuration"></a>Kommissionierung oder Umlagerung für Produktion, Montage und Aufträge in einer Basislagerkonfiguration

Sie können eine Lagerkommissionierung oder Bestandumlagerung auf drei Arten erstellen:  

* Aus dem Herkunftsbeleg selbst.  
* Für mehrere Herkunftsbelege gleichzeitig, indem Sie einen Batchauftrag verwenden.  
* In zwei Schritten. Geben Sie den Herkunftsbeleg frei, um den Herkunftsbeleg kommissionierbereit zu machen. Erstellen Sie die Bestandskommissionierung oder -umlagerung aus den Dokumenten **Bestandskommissionierung** oder **Lagerbestandsumlagerung**. Die Bestandskommissionierung oder -umlagerung basieren auf dem Herkunftsbeleg.  

### <a name="to-create-an-inventory-pick-from-the-source-document"></a>Eine Lagerkommissionierung vom Herkunftsbeleg aus erstellen

1. Wählen Sie im Herkunftsbeleg, bei dem es sich um einen Produktionsauftrag oder einen Auftrag handeln kann, die Aktion **Lagereinlagerung/Kommissionierung erstellen** aus.  
2. Aktivieren Sie das Kontrollkästchen **Lagerkomm. erst.**.
3. Wählen Sie die Schaltfläche **OK**.

### <a name="to-create-an-inventory-movement-from-the-source-document"></a>Eine Lagerbestandsumlagerung vom Herkunftsbeleg aus erstellen

1. Wählen Sie im Herkunftsbeleg, bei dem es sich um einen Produktionsauftrag, Montageauftrag oder einen Auftrag handeln kann, die Aktion **Lagereinlagerung/Kommissionierung erstellen** aus.  
2. Aktivieren Sie das Kontrollkästchen **Lagerbestandsumlagerung erstellen**.
3. Wählen Sie die Schaltfläche **OK**.

### <a name="to-create-multiple-inventory-picks-or-movements-with-a-batch-job"></a>Mehrere Bestandskommissionierungen oder -umlagerungenmit einem Batchauftrag erstellen

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Erstelle Invt. Einlagern/Kommissionieren/Umlagern** ein, und wählen Sie dann den zugehörigen Link.  
2. Verwenden Sie im Inforegister **Erwartete Lagerbewegung** die Felder **Herkunftsbeleg** und **Herkunftsnr.**, um Filter auf Arten von Belegen oder Bereiche von Belegnummern zu setzen. Beispielsweise könnten Sie Kommissionierungen nur für Fertigungsaufträge erstellen.
3. Aktivieren Sie auf dem Inforegister **Optionen** die Schalter **Lagerkomm. erst.** oder **Lagerbestandsumlagerung erstellen**.
4. Wählen Sie die Schaltfläche **OK**.

### <a name="to-create-inventory-picks-or-movements-in-two-steps"></a>So erstellen Sie Lagerbestandskommissionierung oder -umlagerungen in zwei Schritten

Um Komponenten für Herkunftsbelege in zwei Schritten zu kommissionieren oder zu verschieben, müssen Sie den Herkunftsbeleg freigeben, um es für die Entnahme bereit zu machen. Die Freigabe von Herkunftsbelegen für interne Arbeitsgänge geschieht auf die folgenden Arten.  

|Herkunftsbeleg|Freigabeverfahren|  
|---------------------|--------------------|  
|Produktionsauftrag|Ändern Sie auf der Seite **Geplanter Produktionsauftrag** den Status eines Auftrags in **Freigegeben** oder verwenden Sie die Seite **Freigegebener Produktionsauftrag**, um einen freigegebenen Produktionsauftrag zu erstellen.|  
|Montageauftrag|Ändern des Status eines Montageauftrags auf **Freigegeben**.|
|Aufträge | Ändern Sie den Status eines Auftrags auf **Offen**, oder erstellen Sie sofort einen Auftrag mit dem Status Offen.|  

Ein Lagermitarbeiter, der der Kommissionierung von Artikeln zugeordnet ist, kann einen Lagereinlagerungsbeleg für den Herkunftsbeleg erstellen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Geben Sie **Lagerbestandskommissionierungen** oder **Lagerbestandsumlagerung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Wählen Sie im Feld **Herkunftsbeleg** die Art des Herkunftsbelegs aus, für den die Einlagerung ist.

    > [!NOTE]
    > Sie können Dokumente für **Lagerbestandskommissionierung** nicht für die Kommissionierung von Montagekomponenten verwenden.
4. Wählen Sie im Feld **Herkunftsnr.** den Herkunftsbeleg aus.  
5. Oder wählen Sie die Aktion **Herkunftsbeleg holen** aus, um den Beleg aus einer Liste von eingehenden Herkunftsbelegen auszuwählen, die zur Kommissionierung am Lagerort bereit sind.  
6. Wählen Sie die Schaltfläche **OK**, um die Kommissionierungs- oder Umlagerungszeilen gemäß dem ausgewählten Herkunftsbeleg auszufüllen.  

## <a name="to-record-the-inventory-pick"></a>So erfassen Sie die Lagerbestandskommissionierung

1. Öffnen Sie auf der Seite **Lagerbestandskommissionierung** das Dokument, für das eine Kommissionierung erfasst werden soll.  
2. Im Feld **Lagerplatzcode** auf den Kommissionierungszeilen der Lagerplatz, bei dem der Artikel aus dem Lagerplatz kommissioniert werden muss, an dem der Artikel verfügbar ist. Sie können den Lagerplatz bei Bedarf ändern.
3. Führen Sie die Kommissionierung durch und geben Sie dann die kommissionierte Menge in das Feld **Bewegungsmenge** ein.

    Wenn Sie die Artikel für eine Zeile aus mehr als einem Lagerplatz kommissionieren müssen, beispielsweise, da ein Lagerplatz nicht die gesamte Menge enthält, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.  
4. Wählen Sie die Aktion **Buchen**.  

Folgendes passiert während des Buchungsprozesses:

* Buchen Sie den Verbrauch der kommissionierten Herkunftsbelegzeilen.
* Wenn der Lagerort Lagerplätze verwendet, erzeugt der Buchungsvorgang Lagerplatzposten, um die Änderungen an der Lagerplatzmenge zu buchen.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="to-record-the-inventory-movement"></a>So erfassen Sie die Lagerbestandsumlagerung

1. Öffnen Sie auf der Seite **Lagerbestandsumlagerung** das Dokument, für das eine Umlagerung erfasst werden soll.  
2. Geben Sie im Feld **Lagerplatzcode** auf den Umlagerungszeilen wird der Lagerplatz, aus dem kommissioniert wird, basierend auf dem Standardlagerplatz und der Verfügbarkeit des Artikels vorgeschlagen. Sie können den Lagerplatz bei Bedarf ändern.  
3. Führen Sie die Umlagerung durch und geben Sie dann die umgelagerte Menge in das Feld **Bewegungsmenge** ein. Die Werte in den Zeilen "Entnahme" und "Einlagerung" müssen gleich sein. Andernfalls kann die Lagerplatzumlagerung nicht gebucht werden.

    Wenn Sie die Artikel für eine Zeile aus mehr als einem Lagerplatz entnehmen müssen, beispielsweise, da ein Lagerplatz nicht die gesamte Menge enthält, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.  
4. Wählen Sie die Aktion **Lagerbestandsumlagerung registrieren** aus.  

Folgendes passiert während des Buchungsprozesses:

* Die Lagerplatzposten geben jetzt an, dass die Komponenten an den Lagerplätzen vorhanden sind, die in den Auftragszeilen des Herkunftsbelegs angegeben sind. Beispielsweise der Montageauftrag, die Produktionskomponente oder die Auftragsplanungszeile.

>[!NOTE]
> Anders als beim Umlagern von Komponenten mit Lagerbestandkommissionierungen, wird Verbrauch nicht gebucht, wenn Sie eine Lagerbestandsumlagerung erfassen. Sie erfassen den Verbrauch in einem separaten Schritt, indem Sie den Herkunftsbeleg buchen.

## <a name="flushing-production-components-in-a-basic-warehouse-configuration"></a>Buchen von Produktionskomponenten in einer Basislagerkonfiguration

Die Buchungsmethoden beeinflussen den Fluss der Komponenten in der Produktion. Weitere Informationen finden Sie unter [Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md). Abhängig von der von Ihnen gewählten Buchungsmethode können Sie Komponenten für die Produktion auf folgende Weise kommissionieren:

* Verwenden Sie ein **Lagerbestandskommissionierungs**-Dokument , um die Kommissionierung für Artikel aufzuzeichnen, die die **Manuelle** Buchungsmethode verwenden. Wenn Sie eine Lagerkommissionierung erfassen, wird der Verbrauch der kommissionierten Komponenten gebucht. 
* Verwenden Sie ein **Lagerbestandsumlagerungsbeleg** mit einem Verweis auf ein Herkunftsbeleg, um Kommissionierungen für Komponenten zu erfassen, die die **manuelle** Buchungsmethode verwenden. Den Verbrauch müssen Sie separat anmelden. Weitere Informationen finden Sie unter [Produktionsverbrauch mit Stapelverarbeitung buchen](production-how-to-post-consumption.md). 
* Verwenden Sie ein **Lagerbestandsumlagerungsbeleg** mit einem Verweis auf ein Herkunftsbeleg, um Kommissionierungen für Komponenten zu erfassen, die die Buchungsmethode **Kommissionieren + Vorwärts**, **Kommissionieren + Rückwärts** verwenden. Der Verbrauch der Komponenten erfolgt automatisch, wenn Sie entweder den Status des Produktionsauftrags ändern oder einen Vorgang starten oder beenden. Alle benötigten Komponenten müssen verfügbar sein. Andernfalls stoppt das Buchen geleerten Verbrauchs für diese Komponente.
* Verwenden Sie einen **Lagerbestandsumlagerungs**-Beleg ohne eine Referenz, um einen Herkunftsbeleg oder andere Methoden, um die Umlagerung von Komponenten aufzuzeichnen, die die Buchungsmethode **Vorwärts** oder **Rückwärts** verwenden. Der Verbrauch der Komponenten erfolgt automatisch, wenn Sie entweder den Status des Produktionsauftrags ändern oder einen Vorgang starten oder beenden. Alle benötigten Komponenten müssen verfügbar sein. Andernfalls stoppt das Buchen geleerten Verbrauchs für diese Komponente. Weitere Informationen finden Sie unter [Interne Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="example"></a>Beispiel

Sie haben einen Fertigungsauftrag für 15 STÜCK des Artikels SP-SCM1004. Einige der Artikel auf der Komponentenliste müssen manuell in ein FA-Verbrauchs Buch.-Blatt gebucht werden, und andere Artikel können mithilfe der **Kommiss. + Rückwärts**-Buchungsmethode automatisch kommissioniert und gebucht werden.  

Die folgenden Schritte bieten ein Beispiel für die Aktionen, die von verschiedenen Personen genutzt werden, und die entsprechende Reaktionen:  

1. Der Fertigungsbereichsvorgesetzte gibt den Fertigungsauftrag frei. Artikel mit der Buchungsmethode **Vorwärts** und keiner Arbeitsplanverknüpfung werden vom Off. Fert.-Ber.-Lagerplatz. abgezogen.  
2. Der Fertigungsleiter wählt die Aktion **Lagereinlagerung/Kommissionierung/Umlagerung erstellen** für den Produktionsauftrag aus und aktiviert die Schalter **Lagerkomm. erst.** und **Lagerbestandsumlagerung erstellen**. Ein Beleg für Lagerbestandskommissionierung wird für Artikel mit der Buchungsmethode **Manuell** erstellt und eine Lagerbestandsumlagerung wird für Artikel mit den Buchungsmethoden **Kommissionierung + Rückwärts** und **Kommissionierung + Vorwärts** erstellt.
3. Der Lagermanager weist einem Lagermitarbeiter die Kommissionierungen und Umlagerungen zu.
4. Der Lagermitarbeiter kommissioniert die Artikel aus den jeweiligen Lagerplätzen und platziert sie im Fert.-Bereitst.-Lagerplatzcode oder in der Lagerbestandsumlagerung. Der Lagerplatz, kann der Lagerplatz eine Arbeitsplatzgruppe oder eines Arbeitsplatzes sein.  
5. Der Lagermitarbeiter bucht die Kommissionierung. Die Menge wird von den Lagerplätzen abgezogen.
6. Der Lagermitarbeiter bucht die Umlagerung. Die Menge wird von den Kommissionierungslagerplätzen abgezogen und dem Verbrauchslagerplatz hinzugefügt. Das Feld **Menge kommissioniert** auf der Komponentenliste für alle kommissionierten Artikel wird aktualisiert.  
7. Der Maschinist informiert den Produktionsleiter, dass die Endartikel fertig sind.  
8. Der Fertigungsleiter verwendet die Ausgabeerfassung oder die Produktionserfassung, um die Istmeldung zu buchen. Die Menge der Komponentenartikel, die die Buchungsmethoden **Kommissionieren + Vorwärts** oder **Kommissionieren + Rückwärts** mit Arbeitsplanlinks verwenden, wird vom Fert.-Bereitst.-Lagerplatz abgezogen.
9. Der Produktionsleiter ändert den Status des Fertigungsauftrags zu **Beendet**. Die Menge der Komponenten, die die Buchungsmethode **Rückwärts** verwenden, wird vom Off. Fert.-Ber.-Lagerplatz.abgezogen, und die Menge der Komponenten, die die Buchungsmethode **Kommiss. + Rückwärts** verwenden wird vom Fert.-Bereitst.-Lagerplatz abgezogen und kein Arbeitsplanlink wird vom Fert.-Bereitst.-Lagerplatzcode abgezogen.  

 Die folgende Abbildung zeigt, wann das Feld **Lagerplatzcode** auf der Komponentenliste entsprechend Ihrer Lagerort- oder Arbeitsplatzeinrichtung gefüllt wird.  

:::image type="content" source="media/binflow.png" alt-text="Übersicht, wann und wie das Feld Lagerplatz ausgefüllt wird.":::

## <a name="see-also"></a>Siehe auch

[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
