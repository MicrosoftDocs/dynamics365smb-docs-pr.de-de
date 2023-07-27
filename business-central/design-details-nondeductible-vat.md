---
title: "Designdetails\_– nicht abzugsfähige MwSt."
description: 'Dieser Artikel enthält Informationen zur nicht abzugsfähigen Mehrwertsteuer (MwSt.), die von einem Käufer zu zahlen ist, aber nicht von seiner eigenen Mehrwertsteuerschuld des Käufers abgezogen werden kann.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
---

# Designdetails: Nicht abzugsfähige MwSt.

Bei der nicht abzugsfähigen Mehrwertsteuer (MwSt.) handelt es sich um die Mehrwertsteuer, die von einem Käufer zu zahlen ist, aber nicht von seiner eigenen Mehrwertsteuerschuld des Käufers abgezogen werden kann. Da es schwierig sein kann, zu wissen, wo und wie ein Artikel verwendet wird, müssen Sie sich an die örtlichen Steuerbehörden in Ihrem Land oder Ihrer Region wenden, um herauszufinden, ob ein bestimmter Prozentsatz der MwSt. abzugsfähig ist. Auch wenn Sie wissen, dass ein bestimmter Prozentsatz der MwSt. nicht abzugsfähig ist, gibt es unterschiedliche Modelle für den Umgang mit nicht abzugsfähigen Beträgen im Zusammenhang mit **Artikeln** und **Anlagen**.

## Voraussetzungen für die Nutzung der nicht abzugsfähigen MwSt.

Gehen Sie wie folgt vor, um die nicht abzugsfähige MwSt. zu verwenden und zu buchen.

1. Wählen Sie auf der Seite **MwSt.-Einrichtung** **Nicht abzugsfähige MwSt. aktivieren** aus, um das Feature zu aktivieren.
2. Wählen Sie auf der Seite **MwSt.-Buchungseinrichtung** aus, welche MwSt.-Buchungsgruppen die nicht abzugsfähige MwSt. verwenden können.

## Beispiele

Für die folgenden Beispiele ist die nicht abzugsfähige MwSt. aktiviert und die folgende Einrichtung ist abgeschlossen:

- Das Feld **MwSt.-Produktbuchungsgruppe** ist auf **NDVAT** eingestellt.
- Gehen Sie auf der Seite **MwSt.-Buchungseinrichtung** wie folgt vor:

    - **NDVAT** wird als MwSt.-Produktbuchungsgruppe und **INLAND** als MwSt.-Geschäftsbuchungsgruppe festgelegt.
    - Der Wert **MwSt.-Kennzeichen** muss eindeutig sein.
    - Das Feld **MwSt. %** ist auf **25**.
    - Das Feld **Nicht abzugsfähige MwSt. zulassen** ist auf **Zulassen** eingestellt.
    - Das Feld **Nicht abzugsfähige MwSt. %** ist auf **100** eingestellt.
    - Das Feld **MwSt.-Berechnungsart** ist auf **Normale MwSt.** eingestellt.
    - Es sind nur das Umsatzsteuerkonto und das Vorsteuerkonto konfiguriert.

In allen Beispielen werden Artikel und Anlagen verwendet, bei denen die MwSt.-Produktbuchungsgruppe **NDVAT** lautet.

### Artikel

Für einen neuen Artikel ist **NDVAT** als MwSt.-Produktbuchungsgruppe festgelegt. Im Einkaufsbeleg sind **Menge** = **1** und **EK-Preis ohne MwSt.** = **1.000,00**.

Unabhängig von der verwendeten Option sind die Ergebnisse bei **MwSt.-Posten** dieselben.

| Belegtyp | Typ | Basis | Betrag | Nicht abziehbare MwSt. Basis | Nicht abzugsfähiger MwSt. Betrag |
|---|---|---|---|---|---|
| Fakturieren | Einkauf | 0.00 | 0.00 | 1,000.00 | 250.00 |

Die Details werden in den **Werteinträgen** angezeigt.

> [!NOTE]
> Sie können das Feld **Für Artikelkosten verwenden** auf der Seite **MwSt.-Einrichtung** aktivieren.

#### Die Verwendung für Artikelkosten ist nicht aktiviert

| Artikelpostenart | Postenart | Einstandsbetrag (tatsächl.) | Artikelpostenmenge |
|---|---|---|---|
| Einkauf | Direkte Kosten | 1,000.00 | 0 |

#### Die Verwendung für Artikelkosten ist aktiviert

| Artikelpostenart | Postenart | Einstandsbetrag (tatsächl.) | Artikelpostenmenge |
|---|---|---|---|
| Einkauf | Direkte Kosten | 1,250.00 | 0 |

### Anlagen

Für eine neue Anlage ist das Anschaffungskostenkonto so eingestellt, dass **NDVAT** als MwSt.-Produktbuchungsgruppe verwendet wird. Im Einkaufsbeleg sind **Menge** = **1** und **EK-Preis ohne MwSt.** = **1.000,00**.

Unabhängig von der verwendeten Option sind die Ergebnisse bei **MwSt.-Posten** dieselben.

| Belegtyp | Typ | Basis | Betrag | Nicht abziehbare MwSt. Basis | Nicht abzugsfähiger MwSt. Betrag |
|---|---|---|---|---|---|
| Fakturieren | Einkauf | 0.00 | 0.00 | 1,000.00 | 250.00 |

Die Details werden in den **Anlagenposten** angezeigt.

> [!NOTE]
> Sie können das Feld **Für Anlagenkosten verwenden** auf der Seite **MwSt.-Einrichtung** aktivieren.

#### Die Verwendung für Anlagenkosten ist nicht aktiviert

| Belegtyp | Anlagenbuchungsart | Betrag | MwSt.- Betrag |
|---|---|---|---|
| Fakturieren | Anschaffungskosten | 1,000.00 | 250.00 |

#### Die Verwendung für Anlagenkosten ist aktiviert

| Belegtyp | Anlagenbuchungsart | Betrag | MwSt.- Betrag |
|---|---|---|---|
| Fakturieren | Anschaffungskosten | 1,000.00 | 250.00 |
| Fakturieren | Anschaffungskosten | 250.00 | 0.00 |

## Siehe auch

[Nicht absetzbare MwSt. einrichten](finance-setup-nondeductible-vat.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
