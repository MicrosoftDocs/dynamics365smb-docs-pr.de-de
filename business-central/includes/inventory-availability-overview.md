---
author: brentholtorf
ms.topic: include
ms.date: 09/11/2023
ms.author: bholtorf
---

Steigern Sie die Effizienz in Ihrem Lager mit genauen Echtzeitinformationen über Faktoren, die sich auf die verfügbaren Mengen auswirken können. Beispiel: 

* Lagerbestände
* Lagerorte
* Verarbeitungsphasen
* Unter Quarantäne gestellte Elemente
* Reservierungen

Informationen zur Artikelverfügbarkeit können Sie den folgenden Quelldokumenten entnehmen:

* Verkaufsaufträge
* Fertigungsaufträge
* Montageaufträge
* Aufträge

Die Informationen berücksichtigen auch andere Faktoren, die die Verfügbarkeit beeinflussen. Zum Beispiel spezielle Lagerplätze, verschlossene Lagerplätze und Artikel, die nicht zur Kommissionierung verfügbar sind. Beispielsweise können Artikel reserviert sein oder auf Einlagerungs- oder Versandvorgänge warten. Auf der Seite **Zusammenfassung der Kommissionierung** können Sie die Elemente überprüfen, die [!INCLUDE [prod_short](prod_short.md)] nicht in die Kommissionierbelege aufgenommen und die erforderlichen Maßnahmen ergriffen.

> [!NOTE]
> Für diese Funktion müssen Sie die Funktion **Gezielte Einlagerung und Kommissionierung** für die Standorte aktivieren, die Sie in Ihrem Kommissionierungsprozess verwenden.

### <a name="set-up-previews"></a>Vorschauversionen einrichten

Um Details darüber zu erhalten, was kommissioniert wird und was nicht, aktivieren Sie den Schalter **Zusammenfassung anzeigen (gesteuerte Einlagerung und Kommissionierung)** auf den Anforderungsseiten **Logistik Herk. - Beleg erst.** oder **Warenausgang - Kommiss. erst.**.

### <a name="determine-the-quantity-you-can-pick"></a>Bestimmen Sie die Menge, die Sie auswählen können

Auf Zeilen auf der Seite **Zusammenfassung der Lagerkommissionierung erstellen** zeigt das Feld **Bewegungsmenge (Basis)** an, welche und wie viele Elemente vorhanden sind und [!INCLUDE [prod_short](prod_short.md)] versuchte zu entnehmen. Die Infobox **Zusammenfassung** bietet weitere Details.

Für einfache Untersuchungen bietet die **Entnehmbare Menge** genügend Informationen geben. Das Feld zeigt an, wie viele Artikel verfügbar sind. Wenn die kommissionierbare Menge geringer ist als erwartet, untersuchen Sie den Lagerplätzeinhalt.

Die **Kommissionierbare Menge** ist die maximale Menge, die [!INCLUDE [prod_short](prod_short.md)] für die Kommissionierung berücksichtigt werden kann. Diese Menge besteht aus Artikeln in kommissionierbaren Lagerplätzen. Die Menge schließt Mengen aus, die sich in gesperrten oder dedizierten Lagerplätzen befinden, oder Artikel, die in Lagerkommissionierbelegen kommissioniert werden. Wenn für den Artikel, den Sie kommissionieren möchten, eine Artikelverfolgung erforderlich ist, werden gesperrte Chargen- oder Seriennummern, die in kommissionierbaren Lagerplätzen gespeichert sind, von der kommissionierbaren Menge ausgeschlossen.

Wenn die kommissionierbare Menge von der Menge in kommissionierbaren Lagerplätzen abweicht, liegt möglicherweise ein Problem vor. Durchsuchen Sie den Lagerplatzinhalt, um blockierte Lagerplätze oder Mengen in aktiven Dokumenten zu finden.

Das Feld **Menge im Lager** zeigt die Gesamtmenge an, die Sie in Ihrem Lager vorfinden, wenn Sie eine physische Zählung durchführen. Von diesem Feld aus können Sie einen Drilldown zu den Lagerbucheinträgen durchführen. Wenn das Feld eine Menge anzeigt, die geringer ist als die Menge in der **Menge in kommissionierbaren Lagerplätzen**, liegt eine Abweichung zwischen Lager- und Bestandsmengen vor. Verwenden Sie in diesem Fall die Aktion **Lageranpassung berechnen** auf der Seite **Artikelbuch.-Blatt** und erstellen Sie dann die Lagerkommissionierung wieder.

Das folgende Bild zeigt die maximale Menge, die für die Kommissionierung berücksichtigt wird.

:::image type="content" source="../media/pickable-qty.png" alt-text="Maximale Menge, die für die Kommissionierung berücksichtigt wird.":::

**Legende**

|Brief  |Description  |
|---------|---------|
|P     |Lagerplätze mit Inhalt vom Typ Kommissionierung         |
|T     |Lagerplätze mit Inhalt vom Typ „Auswahl“, die als „Dedizierte Lagerplätze“ markiert sind        |
|A     |Lagerplätze mit Inhalt vom Typ „Auswahl“ in den aktiven Dokumenten (wie eine andere Auswahl)       |
|T     |Lagerplätze mit Inhalt vom Typ „Kommissionieren“ mit Artikeln mit gesperrter Sendungsverfolgung         |
|B     |Lagerplätze mit Inhalt der Art Pick mit gesperrtem Ausgang         |
|O     |Andere Lagerplätze         |

### <a name="reservations"></a>Reservierungen

Wenn für den kommissionierten Artikel Reservierungen vorhanden sind, wird die Berechnung fortgesetzt. Die Idee dahinter ist, dass der reservierte Bedarf eine höhere Priorität hat als der nicht reservierte Bedarf, was bedeutet, dass die Kommissionierung für den nicht reservierten Bedarf die spätere Kommissionierung für den reservierten Bedarf nicht verhindern sollte.

Um zu überprüfen, ob Ihre Menge einen Bedarf decken kann, vergleichen Sie den Wert **Auswählbare Menge** in der **Zusammenfassung** Infobox mit dem Wert im Feld **Bewegungsmenge (Basis)** auf den Zeilen.

Reservierungen finden Sie im Bereich **Insgesamt reservierte Menge im Lager**. Reservierte Mengen, die bereits kommissioniert wurden und zum Versand, zur Verwendung oder zum Verbrauch bereit sind, haben keinen Einfluss auf die Verfügbarkeit. Im Feld **Reservierte Menge in Kommissionier-/Ausgangslagerplätzen** wird diese Menge angezeigt.

Das Feld **Verfügbare Menge ohne Lieferungslagerplatz** zeigt die verfügbare Menge an, mit Ausnahme der Mengen, für die Folgendes gilt:

* Sie sind bereits für den Versand ausgewählt.
* Sie befinden sich in gesperrten Artikelchargen oder Seriennummern.
* Sie liegen in verstopften Behältern.

Diese Mengen sind möglicherweise verfügbar, aber Sie können sie möglicherweise noch nicht auswählen. Sie könnten sich noch im Wareneingangs-, Lager- oder Qualitätssicherungsbereich befinden. Sie können sie in den Kommissionierbereich verschieben, indem Sie ein Einlagerungs- oder Umlagerungsarbeitsblatt bearbeiten.

Der Unterschied zwischen **Verfügbare Menge ohne Lieferungslagerplatz** und der reservierten Menge im Lager ist die Menge verfügbar, die zur Entnahme verfügbar ist, ohne dass sich dies auf den reservierten Bestand auswirkt.

### <a name="other-details"></a>Sonstige Details

Wenn Artikel eine Artikelverfolgung erfordern, können Sie die Menge auch in gesperrten Chargen oder Seriennummern finden, was zu folgenden Reduzierungen führt:

* Die kommissionierbare Menge
* Verfügbare Menge, ohne den Transportplatz
* Die reservierte Menge im Lager 

Wenn Sie denselben Artikel für mehrere Quelldokumente oder -zeilen kommissionieren, was auch bei der Kommissionierung von Seriennummern der Fall ist, werden auch Informationen zu Kommissionierungen für andere Zeilen angezeigt, da dadurch die kommissionierbare Menge reduziert wird.
