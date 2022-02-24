---
title: Aktualisieren von Währungswechselkursen | Microsoft Docs
description: Verfolgen Sie Beträge in verschiedenen Währungen mithilfe der Währungscodes, und lassen Sie mithilfe von Business Central die Wechselkurse der gebuchte Posten mit einer Fremdleistung anpassen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 252636417dab633b8b95a15f206d1be82fc78a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183188"
---
# <a name="update-currency-exchange-rates"></a>Währungswechselkurse aktualisieren
Da die Anzahl der Länder, in denen Unternehmen Geschäftsbeziehungen unterhalten, ständig wächst, wird es immer wichtiger, dass Finanzdaten in mehreren Währungen erfasst und angezeigt werden können. Sie müssen für jede Währung, die Sie verwenden, einen Währungscode einrichten, wenn Sie in anderen Währungen als Ihrer Mandantenwährung verkaufen oder einkaufen, Forderungen oder Verbindlichkeiten haben oder in unterschiedlichen Währungen buchen.

In der Anwendung wird die Finanzbuchhaltung in der Mandantenwährung (MW) eingerichtet. Eine weitere Währung, der ein aktueller Wechselkurs zugewiesen ist, wird als zusätzliche Währung eingerichtet. Wird eine zweite Währung als [!INCLUDE[d365fin](includes/d365fin_md.md)] Berichtswährung festgelegt, werden Beträge automatisch für jeden Sachposten und weitere Posten, wie zum Beispiel MwSt.-Posten, in der Mandantenwährung und der Berichtswährung erfasst. Weitere Informationen finden Sie unter [Zusätzliche Berichtswährung einrichten](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Regulieren von Wechselkursen
Da sich Wechselkurse ständig ändern, müssen weitere Währungsentsprechungen im System in regelmäßigen Abständen reguliert werden. Werden diese Regulierungen nicht durchgeführt, sind Beträge, die aus fremden (oder zusätzlichen) Währungen umgerechnet und in der Mandantenwährung in der Finanzbuchhaltung gebucht wurden, möglicherweise irreführend. Darüber hinaus müssen Tagesposten, die vor der Eingabe eines Tageswechelkurses in der Anwendung gebucht werden, aktualisiert werden, nachdem der Tageswechselkurs eingegeben wurde.

Die Stapelverarbeitung **Wechselkurse regulieren** dient zur manuellen Regulierung der Wechselkurse gebuchter Kreditoren-, Debitoren- und Bankkontoposten. Berichtswährungsbeträge in Sachposten können hiermit ebenfalls aktualisiert werden. Sie können die Wechselkurse von der Anwendung eines Services automatisch anpassen lassen. Weitere Informationen finden Sie unter [So richten Sie einen Währungswechselkurs-Service ein](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### <a name="effect-on-customers-and-vendors"></a>Auswirkung auf Debitoren und Kreditoren
Für Debitoren- und Kreditorenkonten reguliert der Batchauftrag die Währung unter Verwendung des Wechselkurses, der zum Zeitpunkt des im Batchauftrag angegebenen Buchungsdatums gültig ist. Die Stapelverarbeitung berechnet die Differenzen für die einzelnen Währungssalden und bucht die Beträge auf das Sachkonto, das im Feld **Kursgewinn unrealisiert Kto.** oder im Feld **Kursverlust unrealisiert Kto.** auf der Seite **Währungen** angegeben ist. Gegenposten werden automatisch auf die Debitoren- und Kreditorensammelkonten in der Finanzbuchhaltung gebucht.

Die Stapelverarbeitung bearbeitet alle offenen Debitoren- und Kreditorenposten. Wenn es eine Wechselkursdifferenz für einen Posten gibt, erzeugt die Stapelverarbeitung einen neuen detaillierten Debitoren- oder Kreditorenposten, der den Regulierungsbetrag des Debitoren- oder Kreditorenpostens wiedergibt.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensionen in Debitoren- und Kreditorenposten
Den Differenzposten werden die Dimensionen von den Debitoren-/Kreditorenposten zugewiesen. Die Differenzen werden pro Kombination von Dimensionswerten gebucht.

### <a name="effect-on-bank-accounts"></a>Auswirkungen auf Bankkonten
Für Bankkonten reguliert der Batchauftrag die Währung unter Verwendung des Wechselkurses, der zum Zeitpunkt des im Batchauftrag angegebenen Buchungsdatums gültig ist. Die Stapelverarbeitung berechnet die Differenzen für jedes Bankkonto mit einem Währungscode und bucht die Beträge auf das Sachkonto, das im Feld **Kursgewinn realisiert Kto.** oder im Feld **Kursverlust realisiert Kto.** der Tabelle **Währungen** angegeben ist. Gegenposten werden automatisch auf die Banksachkonten gebucht, die in den Bankkontenbuchungsgruppen angegeben sind. Die Stapelverarbeitung erzeugt einen Posten pro Währung pro Buchungsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensionen in Bankposten
Den Differenzposten für das Sachkonto des Bankkontos und für das Gewinn- und Verlustkonto werden die Vorgabedimensionen des Bankkontos zugewiesen.

### <a name="effect-on-gl-accounts"></a>Auswirkungen auf Sachkonten
Wenn Sie in einer Berichtswährung buchen, kann die Stapelverarbeitung neue Sachposten für Wechselkursregulierungen zwischen Mandantenwährung und Berichtswährung erstellen. Die Stapelverarbeitung berechnet die Differenzen für jeden Sachposten und reguliert den Sachposten abhängig vom Inhalt des Felds **Kursregulierung** für jedes Sachkonto.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensionen in Sachposten
Den Differenzposten werden die Vorgabedimensionen der Konten zugewiesen, auf die sie gebucht werden.

> [!Important]
> Bevor Sie den Batchauftrag aufrufen können, müssen Sie die Wechselkurse eingeben, die zum Regulieren der Fremdwährungssalden verwendet werden. Dies erfolgt auf der Seite **Währungswechselkurse**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>So richten Sie einen Währungswechselkurs-Service ein
Sie können einen externen Service verwenden, um Ihre Währungswechselkurse wie FloatRates auf dem neuesten Stand zu halten.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Währungswechselkurs-Dienste** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Währungswechselkurs-Service** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie das Kontrollkästchen **Aktiviert**, um den Service zu aktivieren.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Um Währungswechselkurse über einen Service zu aktualisieren
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Währungen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die **Aktualisieren von Wechselkursen** Aktion aus.

Der Wert im Feld **Wechselkurs** wird auf der Seite **Währung** mit dem aktuellen Währungswechselkurs aktualisiert.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch
[Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md)  
[Abschlussjahre und -perioden](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
