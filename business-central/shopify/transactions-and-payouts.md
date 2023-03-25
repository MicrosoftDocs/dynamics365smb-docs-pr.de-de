---
title: Synchronisieren und Transaktionen und Auszahlungen
description: Legen Sie den Import von Transaktionen und Auszahlungen aus Shopify fest und führen Sie ihn aus.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30124, 30125, 30130, 30131, 30132, 30133, 30134,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Transaktionen und Auszahlungen

Wenn ein Kunde seinen Checkout im Online-Shop abschließt, werden die Informationen zu Zahlungen als **Transaktion** gespeichert. Mit der Bestellung können mehrere Transaktionen verknüpft sein, z. B. wenn ein Kunde eine Geschenkkarte verwendet, um einen Teil der Kosten zu bezahlen, und dann eine Kreditkarte oder PayPal für den Restbetrag verwendet.

Wenn Sie Shopify Zahlung als Zahlungsanbieter verwenden, dann können Sie neben Informationen über Gelder, die der Kunde vom Zahlungsanbieter erhalten hat, auch Auszahlungen von Shopify auf Ihr Bankkonto sehen.

## Transaktionen

Die Zahlungstransaktionen, die in Shopify stattfinden, werden mit den Aufträgen synchronisiert und können auf der Seite **Shopify Aufträge** eingesehen werden.

Um alle Transaktionen zu überprüfen, wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1 öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") aus, geben Sie **Transaktionen** ein, und wählen Sie den entsprechenden Link aus.

Wenn Sie eine Zuordnung von Zahlungsformen konfiguriert haben, wird dem erstellten Beleg ein Zahlungsformen-Code zugewiesen. Erfahren Sie mehr unter [Zuordnung von Zahlungsmethoden](#payment-method-mapping).

## Auszahlungen

Wenn Ihr Store Shopify Payment verwendet, erhalten Sie Zahlungen über **Shopify Payouts**, wenn ein Debitor mit Shopify Payments und beschleunigten Checkouts bezahlt.

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1 öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie Auszahlungen synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Auszahlungen synchronisieren** aus.

Um alle Auszahlungen zu überprüfen, wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") aus, geben Sie **Auszahlungen** ein, und wählen Sie den entsprechenden Link aus.

**Auszahlungen** dienen nur zu Informationszwecken und wirken sich nicht auf das Hauptbuch oder das Bankbuch aus, können jedoch hilfreich sein, wenn Sie Ihren Kontoauszug bearbeiten.

## Zuordnung der Zahlungsform

Zum Ausfüllen des Felds **Zahlungsformcode** für Verkaufsbelege, die automatisch aus Shopify importiert wurden, müssen Sie **Zuordnung der Zahlungsform** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie eine Zuordnung definieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung der Zahlungsform** aus.
4. Geben Sie in die Felder **Gateway** und **Kreditkartenfirma** den Namen der Zahlungsmethode aus Shopify ein. Der Datensatz wird automatisch erstellt, wenn Sie Shopify-Bestellungen importieren.
5. Geben Sie den **Zahlungsformcode** mit der entsprechenden Zahlungsform in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.
6. Legen Sie die **Priorität** für den Fall fest, dass der Kunde mehrere Zahlungsmittel verwendet. Im Verkaufsbeleg wird die Zahlungsform mit der höchsten Priorität ausgewählt. Wenn beide Zahlungsformen dieselbe Priorität aufweisen, wird die Zahlungsform mit dem höchsten Betrag verwendet.

> [!NOTE]  
> Wenn die entsprechende Zahlungsmethode in [!INCLUDE[prod_short](../includes/prod_short.md)] über **Guth. Kontotyp** und **Guth. Konto-Nr.** ausgefüllt sind, erstellt das System beim Buchen der Rechnung eine Ausgleichsbuchung der Art *Zahlung* und wendet sie auf die Art *Rechnung* im Debitor-Sachkonto an.

## Anwendungsfälle
  
Parteien:

* Käufer - Person, die Waren im Online Store Shopify kauft.
* Händler - Ihre Firma.
* Zahlungsanbieter - Firma, die die Verarbeitung von Zahlungen für Sie übernimmt. Das kann Shopify Payments oder eine dritte Partei sein.

### Wie das Geld fließt

Der Käufer kauft Waren im Online Store. Der letzte Schritt ist die Verarbeitung der Zahlung.

>[!NOTE]
> Dieses Beispiel deckt nicht die Fälle ab, in denen die Zahlung außerhalb der Shopify-Kasse abgeschlossen wird, was für B2B-Szenarien gilt.
  
Der Käufer zahlt mit Kreditkarte, PayPal oder einer lokalen Zahlungsmethode wie MobilePay in Dänemark. Der Zahlungsanbieter zieht den gesamten Betrag vom Käufer ein. In diesem Moment wird das Geld des Käufers an den Zahlungsanbieter überwiesen.

Je nach Zahlungsanbieter kann der Händler dieses Geld auf seinem Konto beim Zahlungsanbieter sehen - sowohl die erhaltenen Beträge als auch die abgezogenen Provisionen. Zahlungsanbieter nehmen oft eine Provision von jeder Transaktion, und in einigen Fällen können sie auch eine feste Gebühr verlangen.
  
Je nach Zahlungsanbieter löst der Händler entweder manuell eine Überweisung des Geldes auf sein Bankkonto (Auszahlung) aus oder dies geschieht automatisch innerhalb eines bestimmten Zeitraums - einmal pro Tag, einmal pro Monat usw.
  
Je nach Bank kann der Händler diese eingehende Transaktion auf seinem Bankkonto über Online-Banking oder im Bankauszug sehen.

Es gibt mehrere Optionen, wie Sie Transaktionen mit dem Schweregrad [!INCLUDE[prod_short](../includes/prod_short.md)] behandeln können
  
### Option 1: Eingehende Überweisungen auf das Bankkonto mit den Originalrechnungen abstimmen
  
Der Händler importiert einen Verkaufsauftrag in [!INCLUDE[prod_short](../includes/prod_short.md)] und bucht Geb. Verkaufslieferungen und Rechnungen.

Ergebnis: Das System erstellt eine **Sachkonto-Buchung** vom Typ *Rechnung* mit dem vollen Betrag, **Öffnen** ist auf Ja festgelegt. Der **Restbetrag** ist gleich dem Rechnungsbetrag.

Der Händler importiert den Bankauszug über das Zahlungsabstimmungs Buch.-Blatt.

Probleme:

1. Kann schwierig sein, wenn es mehrere Rechnungen (und Gutschriften), aber eine Auszahlung vom Zahlungsanbieter mit einem Pauschalbetrag gibt.
2. Die Beträge stimmen in der Regel aufgrund der Provisionen nicht überein. Sie können Zahlungstoleranzen oder/und Zahlungsrabatte verwenden, um Gebühren zu handhaben.

### Option 2: Stimmen Sie eingehende Überweisungen auf ein Bankkonto mit einem Zwischenkonto ab, das Geld beim Zahlungsanbieter darstellt.
  
Der Händler importiert einen Verkaufsauftrag in [!INCLUDE[prod_short](../includes/prod_short.md)] und bucht Geb. Verkaufslieferungen und Rechnungen.
  
Ergebnis: Das System erstellt einen Debitor-Sachkonto-Eintrag vom Typ **Rechnung** mit dem vollen Betrag und **Öffnen** ist auf Ja festgelegt. Der **Restbetrag** ist gleich dem Rechnungsbetrag.

Da der Verkaufsauftrag jedoch einen Zahlungsartencode hat, bei dem die **Bal. Kontotyp** und **Bal. Konto-Nr.** ausgefüllt sind, erstellt das System automatisch einen weiteren Debitor-Sachkonto-Eintrag der Art **Zahlung** und wendet ihn auf den zuvor erstellten Debitor-Sachkonto-Eintrag an.

>[!NOTE]
> Das System füllt das Feld Code der Zahlungsmethode auf der Grundlage der Zuordnung der Zahlungsmethode. Erfahren Sie mehr unter [Zuordnung von Zahlungsmethoden](#payment-method-mapping).
  
Sie können Ausgleichskonten für Zahlungsformen auf zwei Arten definieren:

* **Bal. Kontotyp**, festgelegt auf *Bank*, und **Gegenkonto-Nr.** geben Sie das spezielle Bankkonto ein, das Ihr Konto beim Zahlungsanbieter darstellt.
* **Gegenkontotyp** festgelegt auf *Sachkonto** und **Gegenkontonr.** geben Sie das Sachkonto ein, das Ihr Konto beim Zahlungsanbieter repräsentiert.

Es ist sinnvoll, ein Bankkonto zu verwenden, wenn der Zahlungsanbieter eine Art Kontoauszug exportiert, den Sie in das Zahlungsausgangs Buch.-Blatt importieren können.

Der Händler importiert den Bankauszug über das Zahlungsabstimmungs Buch.-Blatt. Die eingehende Auszahlung kann verarbeitet werden:

* als Überweisung von einer anderen Bank. Wenn die Überweisung einige Tage dauert oder einen Währungsumtausch beinhaltet, sollten Sie ein Interimssachkonto verwenden.
* als Differenz auf dem Sachkonto, das Ihr Konto beim Zahlungsanbieter darstellt.
  
Der verbleibende Saldo auf dem Sachkonto oder Bankkonto, das Ihr Konto beim Zahlungsanbieter darstellt, kann als “Gebühren/Provisionen„ abgeschrieben werden.

Probleme:

1. Sie können mehrere Sach- oder Bankkonten erstellen, wenn Sie mit mehreren Zahlungsanbietern zu tun haben. Verkaufsaufträge in [!INCLUDE[prod_short](../includes/prod_short.md)] unterstützen jedoch nur einen Zahlungsartencode, was es schwierig macht, Fälle zu behandeln, in denen ein Käufer mehrere Zahlungsarten für eine Bestellung verwendet.

## Siehe auch

[Einstieg in den Konnektor für Shopify](get-started.md)  
