---
title: Wie Sie Serviceartikel erstellen
description: 'Lesen Sie über die verschiedenen Möglichkeiten, wie Sie in Business Central Serviceartikel erstellen können, zum Beispiel innerhalb eines Serviceauftrags oder beim Versand von Artikeln.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-service-items"></a>Serviceartikel erstellen

In [!INCLUDE[prod_short](includes/prod_short.md)], berücksichtigt der Begriff "Serviceartikel" Lagerhilfsmittel oder Artikel, die Service benötigen. Wenn Sie einen Serviceauftrag erstellen, geben Sie den Artikeln die Anforderungsdienst an. Im Verkaufsauftrag können Sie einen Serviceartikel für einen Artikel im Lagerbestand oder in einer Serviceartikelgruppe verknüpfen.

Wenn Sie einen Serviceartikel für Servicearbeiten empfangen, der nicht erfasst ist, kann dieser als Serviceartikel angelegt werden. Es gibt mehrere Möglichkeiten dazu: Beispielsweise können Sie einen Serviceartikel unter **Serviceartikel** oder als Teil eines anderen Prozesses erstellen, etwa bei der Arbeit mit einem Serviceauftrag.

## <a name="to-create-a-service-item"></a>So erstellen Sie einen Serviceartikel

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceartikel** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>So erstellen Sie Serviceartikel in Serviceaufträgen

Wenn Sie Artikel für Servicearbeiten erhalten, können Sie diese als Serviceartikel auf der Seite **Serviceauftrag** oder **Serviceangebot** anlegen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceaufträge** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Aktion **Serviceartikel erstellen**.  

    Eine Nummer wird dem Serviceartikel zugeordnet und eine Serviceartikelkarte wird erstellt. Das Feld **Serviceartikelnr.** wird mit der Nummer des neuen Serviceartikels ausgefüllt.

## <a name="to-create-a-service-item-when-shipping-items"></a>So erstellen Sie Serviceartikel bei Artikellieferungen

Wenn Sie Artikel liefern, indem Sie entweder Verkaufsaufträge oder Verkaufsrechnungen buchen, werden die gelieferten Artikel unter folgender Bedingung automatisch als Serviceartikel erfasst. Die Artikel müssen zu einer Serviceartikelgruppe mit aktiviertem Kontrollkästchen **Serviceartikel erstellen** gehören. Wenn die Artikel über auf der Seite "Artikelverfolgungszeilen" erfasste Seriennummern verfügen, werden diese Informationen beim Erstellen der Serviceartikel automatisch in das Feld **Seriennr.** der Serviceartikelkarte kopiert.  

Im folgenden Verfahren wird gezeigt, wie bei Artikellieferungen in Verkaufsaufträgen Serviceartikel erstellt werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den entsprechenden Verkaufsauftrag.  
3. Wählen Sie die Aktion **Buchen** oder **Buchen und drucken** aus.  
4. Wählen Sie **Warenausgang** oder die **Liefern und fakturieren** Aktion aus.  
5. Es werden automatisch Serviceartikel für die Artikel im Auftrag erstellt, sofern diese einer Serviceartikelgruppe angehören, die zum Erstellen von Serviceartikeln eingerichtet wurde. Wenn auf der Seite **Artikelverfolgungszeilen** spezielle Seriennummern erfasst wurden, werden diese den Serviceartikeln zugeordnet.  

> [!NOTE]  
> Wenn es sich bei dem Artikel um eine Stückliste handelt und die Stückliste entfaltet wurde, werden die entfalteten Stücklistenartikel wie normale Artikel behandelt. Serviceartikel werden gemäß der Bedingung für Serviceartikelgruppen und optional gemäß der Bedingung für Seriennummern erstellt. Weiterhin werden diese Artikel, wenn ein Serviceartikel für einen entfalteten Stücklistenartikel erstellt wird, der aus anderen Stücklistenkomponenten besteht, als Serviceartikelkomponenten für den entfalteten Stücklistenserviceartikel erstellt.  
>
> Wenn es sich bei dem Artikel um eine nicht entfaltete Stückliste handelt, wird ein Serviceartikel gemäß der Bedingung für Serviceartikelgruppen und optional gemäß der Bedingung für Seriennummern erstellt.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>So fügen Sie die Grundgebühr für einen Serviceartikel ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceaufgaben** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Artikel-Arbeitsblatt** aus.
3. Wählen Sie auf dem Inforegister Zeilen die relevante **Aktion** aus, und wählen Sie dann **Funktinone**und dann **Grundgebühr** einfügen.  

    Eine Servicezeile der Art **Kosten** wird mit der Grundgebühr eingefügt. Die Grundgebühr bezieht sich auf den ausgewählten Serviceartikel.

## <a name="block-items-item-variants-or-specific-service-items"></a>Artikel, Artikelvarianten oder bestimmte Serviceartikel blockieren

Sie können verhindern, dass Artikel, Artikelvarianten oder Serviceartikel in Servicemanagementtransaktionen wie Serviceverträgen, Serviceaufträgen und Servicerechnungen verwendet werden. Dies kann nützlich sein, wenn Sie die Verfügbarkeit einiger Artikel oder Serviceartikel zu Servicezwecken einschränken möchten, beispielsweise aufgrund von eingestelltem Support, begrenztem Lagerbestand oder vertraglichen Vereinbarungen.

Um die Verwendung eines Artikels oder einer Artikelvariante in Servicemanagementtransaktionen zu blockieren, aktivieren Sie den Schalter **Service blockiert** auf der Seite **Artikelkarte**, **Artikelvarianten** und **Artikelvariantenkarte**. Sie können dieses Feld auch auf der Seite **Artikelvorlage** festlegen und es wird in die Artikel kopiert, die aus dieser Vorlage erstellt wurden.

Wenn ein Artikel oder eine Artikelvariante für den Service blockiert ist, steht er auf den folgenden Seiten nicht zur Auswahl:

- Servicezeile (außer bei Servicegutschriften, bei denen Sie eine Benachrichtigung sehen, dass der Artikel oder die Variante blockiert, aber für diesen Dokumenttyp zulässig ist)
- Serviceartikel
- Servicevertragszeile
- Standardservicezeile

Wenn Sie manuell eine blockierte Artikelnummer oder Variante eingeben, erhalten Sie eine Fehlermeldung mit der Meldung „Das Feld enthält einen Wert, der in der zugehörigen Tabelle nicht gefunden werden kann.“

Wenn Sie außerdem über Serviceverträge, Servicevertragsangebote oder Serviceaufträge verfügen, die blockierte Serviceartikel oder Artikelvarianten enthalten, können Sie die folgenden Aktionen nicht verwenden:

- **Sperren** oder **Vertrag abschließen** auf der Seite **Servicevertragsangebot**.
- **Vertrag sperren**, **Vertrag unterzeichnen**, **Vertragsserviceaufträge erstellen** oder **Vertragsrechnungen erstellen** auf der Seite **Servicevertrag**.
- **Auftrag erstellen** auf der Seite **Serviceangebot**.
- **Für Warenausgang freigeben** oder **Buchen** auf der Seite **Serviceauftrag**.
- **Buchen** auf der Seite **Servicerechnung**.

### <a name="block-a-service-item"></a>Serviceartikel blockieren

Um die Verwendung eines Serviceartikels in Servicemanagementtransaktionen zu sperren, wählen Sie auf der Seite **Serviceartikelkarte** im Feld **Blockiert** eine der folgenden Optionen aus:

- **Servicevertrag**: Blockieren Sie die Verwendung des Serviceartikels in Serviceverträgen und Servicevertragsangeboten, jedoch nicht in Serviceaufträgen oder anderen Servicebelegen.
- **Alle**: Blockieren Sie die Verwendung des Serviceartikels in Servicemanagementtransaktionen, darunter Serviceverträgen, Serviceaufträgen und anderen Servicebelegen.

Wenn eine Serviceartikel blockiert ist, ist dieser auf folgenden Seiten nicht mehr auswählbar:

- Servicevertragszeile (falls für einen oder alle Serviceverträge blockiert)
- Serviceartikelzeile (außer Servicegutschriften, wenn für alle blockiert)

Wenn Sie manuell eine Serviceartikelnummer für einen blockierten Serviceartikel eingeben, wird die Fehlermeldung „Das Feld enthält einen Wert, der in der zugehörigen Tabelle nicht gefunden werden kann.“ angezeigt.

Wenn Sie außerdem über Serviceverträge, Servicevertragsangebote oder Serviceaufträge verfügen, die blockierte Serviceartikel enthalten, können Sie die folgenden Aktionen nicht verwenden:

- **Sperren** und **Vertrag abschließen** auf der Seite **Servicevertragsangebot** (falls für einen oder alle Serviceverträge blockiert).
- **Vertrag sperren**, **Vertrag unterschreiben** oder **Debitor wechseln** auf der Seite **Servicevertrag** (falls für einen oder alle Serviceverträge blockiert).
- **Auftrag erstellen** für das **Serviceangebot** (falls für alle blockiert).
- **Für Warenausgang freigeben** oder **Buchen** unter **Serviceauftrag** (wenn für alle blockiert). Wenn Serviceauftragsbelege mehrere Servicepositionen enthalten und einige blockiert sind und andere nicht, können Sie nicht blockierte Zeilen freigeben und buchen. Überlegen Sie, ob Sie den Schalter **Ein Serviceartikel pro Auftrag** auf der Seite **Serviceverwaltungseinrichtung** aktivieren möchten.
- **Buchen** auf der Seite **Servicerechnung** (falls für alle blockiert).

Sie können die blockierten Serviceartikel auch anzeigen, indem Sie einen Filter auf die folgenden Berichte anwenden:

- Serviceartikel (Bericht 5935)
- Serviceartikel – Garantie abgelaufen (Bericht 5937)
- Service-DB (Serviceartikel) (Bericht 5938)

### <a name="data-upgrade"></a>Datenupgrade

Diese Funktion erfordert keine zusätzliche Einrichtung. Wenn Sie jedoch Ihr [!INCLUDE [prod_short](includes/prod_short.md)] aktualisieren, beachten Sie Folgendes:

- Wenn Sie Artikel, Artikelvarianten oder Artikelvorlagen haben, bei denen der Umschalter **Verkäufe blockiert** eingeschaltet ist, wird das Feld **Dienst gesperrt** während des Upgrades auch für diese Datensätze aktiviert. Dadurch wird sichergestellt, dass die vorhandene Logik zur Blockierung von Verkäufen auch für Servicemanagementtransaktionen gilt.
- Für Daten werden nur Upgrades ausgeführt, wenn Sie in Ihrem Unternehmen über mindestens einen Serviceartikel verfügen, also die Servicemanagementfunktionalität nutzen und das Daten-Upgrade benötigen. Wenn Sie keine Serviceartikel haben, wird die Datenaktualisierung übersprungen und der Umschalter **Dienst gesperrt** ist standardmäßig für alle Artikel, Artikelvarianten und Artikelvorlagen deaktiviert.

## <a name="see-also"></a>Siehe auch

[Serviceartikel und Serviceartikelkomponenten einrichten](service-how-setup-service-items.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Service](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
