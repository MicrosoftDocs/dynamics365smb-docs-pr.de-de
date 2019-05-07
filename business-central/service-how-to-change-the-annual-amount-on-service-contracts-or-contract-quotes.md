---
title: 'Vorgehensweise: Ändern des Betrags "Zu fakturieren (Jahr)" von Serviceverträgen oder Vertragsangeboten | Microsoft Docs'
description: Gibt den Betrag an, der jährlich für den Servicevertrag oder das Vertragsangebot fakturiert wird.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: adb6cb718f0f63eb5b12b62f1d40f1d8ea0c70d1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "915917"
---
# <a name="change-the-annual-amount-on-service-contracts-or-contract-quotes"></a>Ändern des jährlichen Betrags für Serviceverträgen oder Vertragsangebote
Sie können den Betrag "Zu fakturieren (Jahr)" des Servicevertrags oder Vertragsangebots ändern, um den jährlich fakturierten Betrag zu korrigieren.  

## <a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote"></a>So ändern Sie den Betrag "Zu fakturieren (Jahr)" eines Servicevertrags oder Vertragsangebots  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceverträge** oder **Servicevertragsangebote** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie den Vertrag oder das Vertragsangebot aus.  
3. Wählen Sie die Aktionen **Vertrag öffnen** aus, um den Vertrag oder das Vertragsangebot zwecks Bearbeitung zu öffnen.  
4. Wählen Sie das Kontrollkästchen **Nicht ausgegl. Betr. zulassen** aus, wenn Sie den jährlichen Betrag ändern und die Differenz manuell in den Vertragszeilen ausgleichen möchten. Falls Sie das nicht möchten, deaktivieren Sie das Kontrollkästchen, um die Differenz in den Vertragszeilen automatisch ausgleichen zu lassen, wenn Sie den jährlichen Betrag ändern.  
5. Ändern Sie den Inhalt des Feldes **Zu fakturieren (Jahr)**. Sie können keinen Servicevertrag zu unterzeichnen, d. h., in einen Servicevertrag umzuwandeln, wenn Sie mit einem Servicevertragsangebot arbeiten oder einen Servicevertrag zu sperren, wenn der Betrag "Zu fakturieren (Jahr)" negativ ist. Wenn Sie den Betrag "Zu fakturieren (Jahr)" auf Null setzen, sollte der Wert im Feld **Fakturierungsintervall** **Keine** betragen, wenn Sie den Vertrag unterzeichnen oder sperren.  
6. Abhängig davon, ob das Kontrollkästchen **Nicht ausgegl. Betr. zulassen** aktiviert ist, rufen Sie die manuelle oder die automatische Verteilung der Differenz der jährlichen Beträge auf. Die Vertragszeilen werden so aktualisiert, dass der Wert des Feldes **Berech. zu fakturieren (Jahr)** gleich dem neuen Betrag ist.  

## <a name="distributing-differences-between-new-and-calculated-annual-amounts"></a>Verteilen von Differenzen zwischen neuen und berechneten jährlichen Beträgen
Wenn Sie den jährlichen Betrag für einen Servicevertrag oder ein Servicevertragsangebot ändern, müssen Sie u. U. die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag auf die Vertragszeilen verteilen. Es gibt drei Möglichkeiten, Beträge zu verteilen:

* Gleichmäßige Verteilung  
* Verteilung nach Zeilenbetrag  
* Verteilung nach DB

### <a name="even-distribution"></a>Gleichmäßige Verteilung
Wenn Sie den jährlichen Betrag für den Servicevertrag oder das Servicevertragsangebot ändern, müssen Sie u. U. die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag auf die Vertragszeilen verteilen. Die gleichmäßige Verteilung ist eine der automatischen Verteilungsmethoden, die Ihnen dabei helfen kann, die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag gleichmäßig auf die Zeilenbeträge der Vertragszeilen zu verteilen. Im Folgenden wird diese Methode beschrieben:  

1. Die Differenz zwischen dem neuen Betrag **Zu fakturieren (Jahr)** und dem **Berech. zu fakturieren (Jahr)** wird durch die Anzahl der Vertragszeilen im Servicevertrag oder Serviceangebot geteilt.  
2. Der **Zeilenbetrag** wird aktualisiert, indem das Ergebnis des vorherigen Schrittes hinzuaddiert wird.  
3. Der Inhalt der Felder **Zeilenrabattbetrag**, **Zeilenrabatt %** und **DB** wird hinsichtlich des neuen Werts im Feld **Zeilenbetrag** wie folgt aktualisiert:   
    * Zeilenrabattbetrag = Zeilenwert - Zeilenbetrag.  
    * Zeilenrabatt % = Zeilenrabattbetrag / Zeilenwert * 100.  
    * DB = Zeilenbetrag – Zeileneinstandspreis.  

 Die Schritte werden für jede Vertragszeile wiederholt.  

#### <a name="example"></a>Beispiel  
Das Feld **Nicht ausgegl. Betr. zulassen** ist nicht im Servicevertrag aktiviert, wenn dieser drei Vertragszeilen mit folgenden Daten enthält.  

|Artikel|Zeileneinstandspreis|Zeilenwert|Zeilenrabatt %|Zeilenrabattbetrag|Zeilenbetrag|DB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|30,00|40,00|0.00|0.00|40,00|10,00|  
|Artikel 2|40,00|50.00|10,00|5.00|45.00|5.00|  
|Artikel 3|50.00|70.00|10,00|7.00|63.00|13.00|  

Das Feld **Zu fakturieren (Jahr)** entspricht dem Wert des Feldes **Berech. zu fakturieren (Jahr)**, das immer der Summe der Zeilenbeträge entspricht. In diesem Fall entspricht es 40 + 45 + 63 = 148.  

Wenn Sie den **Betrag zu fakturieren (Jahr)** auf 139 ändern, wird der Betrag berechnet, der zu jedem Feld **Zeilenbetrag** addiert werden sollte. Dieser Betrag wird berechnet, indem die Differenz aus dem neuen Wert **Zu fakturieren (Jahr)** und dem Wert **Berech. zu fakturieren (Jahr)** durch die Anzahl der Vertragszeilen im Servicevertrag geteilt wird. In diesem Fall entspricht es (139 - 148) / 3 = -3. Dann wird die zuletzt berechnete Zahl zum Feld **Zeilenbetrag** hinzugefügt, und die Felder **Zeilenrabatt %**, **Zeilenrabattbetrag** und **DB** werden mithilfe der Formeln im oben beschriebenen Verfahren aktualisiert.  

Zum Schluss werden die Vertragszeilen die folgenden Daten enthalten.  

|Artikel|Zeileneinstandspreis|Zeilenwert|Zeilenrabatt %|Zeilenrabattbetrag|Zeilenbetrag|DB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|30,00|40,00|7.50|3.00|37.00|7.00|  
|Artikel 2|40,00|50.00|16.00|8.00|42.00|2.00|  
|Artikel 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### <a name="distribution-based-on-line-amount"></a>Verteilung nach Zeilenbetrag
Wenn Sie den jährlichen Betrag für den Servicevertrag oder das Servicevertragsangebot ändern, müssen Sie u. U. die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag auf die Vertragszeilen verteilen. Die Verteilung basierend auf dem Zeilenbetrag ist eine der automatischen Verteilungsmethoden, die Ihnen dabei helfen kann, die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag auf die Zeilenbeträge der Vertragszeilen zu verteilen. Die Verteilung wird proportional zu dem Anteil vorgenommen, den der Zeilenbetrag am berechneten Betrag fakturieren (Jahr) hat. Die folgende Übersicht über Verteilungsschritte für Vertragszeilen beschreibt die Grundidee dieser Methode:  

1. Der Zeilenbetragsprozentanteil wird wie folgt berechnet: Der Inhalt des Felds **Zeilenbetrag** wird in allen Vertragszeilen durch die Werte des Felds **Berech. zu fakturieren (Jahr)** dividiert.  
2. Der Wert des Felds **Zeilenbetrag** wird aktualisiert, indem die Differenz zwischen dem neuen und dem berechneten jährlich zu fakturierenden Betrag hinzuaddiert wird, dann wird mit dem Zeilenbetragsprozentanteil multipliziert.  
3. Der Inhalt der Felder **Zeilenrabattbetrag**, **Zeilenrabatt %** und **DB** wird hinsichtlich des neuen Werts im Feld **Zeilenrabattbetrag** wie folgt aktualisiert:  

    * Zeilenrabattbetrag = Zeilenwert - Zeilenbetrag  
    * Zeilenrabatt % = Zeilenrabattbetrag / Zeilenwert * 100  
    * DB = Zeilenbetrag - Zeileneinstandspreis  

### <a name="distribution-based-on-line-amount"></a>Verteilung nach Zeilenbetrag
Wenn Sie den jährlichen Betrag für den Servicevertrag oder das Servicevertragsangebot ändern, müssen Sie u. U. die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag auf die Vertragszeilen verteilen. Die Verteilung basierend auf dem Zeilenbetrag ist eine der automatischen Verteilungsmethoden, die Ihnen dabei helfen kann, die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag auf die Zeilenbeträge der Vertragszeilen zu verteilen. Die Verteilung wird proportional zu dem Anteil vorgenommen, den der Zeilenbetrag am berechneten Betrag fakturieren (Jahr) hat. Die folgende Übersicht über Verteilungsschritte für Vertragszeilen beschreibt die Grundidee dieser Methode:  

1. Der Zeilenbetragsprozentanteil wird wie folgt berechnet: Der Inhalt des Felds **Zeilenbetrag** wird in allen Vertragszeilen durch die Werte des Felds **Berech. zu fakturieren (Jahr)** dividiert.  
2. Der Wert des Felds **Zeilenbetrag** wird aktualisiert, indem die Differenz zwischen dem neuen und dem berechneten jährlich zu fakturierenden Betrag hinzuaddiert wird, dann wird mit dem Zeilenbetragsprozentanteil multipliziert.  
3. Der Inhalt der Felder **Zeilenrabattbetrag**, **Zeilenrabatt %** und **DB** wird hinsichtlich des neuen Werts im Feld **Zeilenrabattbetrag** wie folgt aktualisiert:  

    * Zeilenrabattbetrag = Zeilenwert - Zeilenbetrag  
    * Zeilenrabatt % = Zeilenrabattbetrag / Zeilenwert * 100  
    * DB = Zeilenbetrag - Zeileneinstandspreis  

Die Schritte werden für jede Vertragszeile wiederholt.  

#### <a name="example"></a>Beispiel  
Das Feld **Nicht ausgegl. Betr. zulassen** ist nicht im Servicevertrag aktiviert, wenn dieser drei Vertragszeilen mit folgenden Daten enthält.  

|Artikel|Zeileneinstandspreis|Zeilenwert|Zeilenrabatt %|Zeilenrabattbetrag|Zeilenbetrag|DB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|15.00|17.00|3.00|0.51|25.00|1.49|  
|Artikel 2|20,00|23.00|"Keine"|0.00|55.10|3.00|  
|Artikel 3|24.00|27.00|3.00|0.81|112.70|2.19|  

Das Feld **Zu fakturieren (Jahr)** entspricht dem Wert des Felds **Berech. zu fakturieren (Jahr)**, das immer der Summe der Zeilenbeträge entspricht. In diesem Fall entspricht es 16,49 + 23,00 + 26,19 = 65,68.  

Wenn Sie den Wert von **Zu fakturieren (Jahr)** auf 60 ändern, werden die DB-Prozentsatzanteile für jede Vertragszeile berechnet:  

* Artikel 1 – 5 / (5 + 5,1 +12,7) = 0,2193 %  
* Artikel 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Artikel 3 – 12.7 / (5 + 5,1 +12,7) = 0,557 %  

Der Wert des Felds **Zeilenbetrag** wird in jeder Vertragszeile aktualisiert. Dabei wird folgende Formel verwendet: Zeilenbetrag + Differenz zwischen dem neuen und dem berechneten Betrag zu fakturieren (Jahr) * Prozentanteil des Beitrags. Danach werden die Felder **Zeilenrabattbetrag**, **Zeilenrabatt %** und **DB** aktualisiert, indem die Formeln aus den o. a. Schritten verwendet werden.  

Zum Schluss werden die Vertragszeilen die folgenden Daten enthalten.  

|Artikel|Zeileneinstandspreis|Zeilenwert|Zeilenrabatt %|Zeilenrabattbetrag|Zeilenbetrag|DB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|15.00|17.00|11.41|1.94|15.06|0.06|  
|Artikel 2|20,00|23.00|8.65|1.99|21.01|1.01|  
|Artikel 3|24.00|27.00|11.37|3.07|23.93|-0,07|  -   Zeilenrabatt % = Zeilenrabattbetrag / Zeilenwert * 100  

#### <a name="example"></a>Beispiel  
Das Feld **Nicht ausgegl. Betr. zulassen** ist nicht im Servicevertrag aktiviert, wenn dieser drei Vertragszeilen mit folgenden Daten enthält.  

|Artikel|Zeileneinstandspreis|Zeilenwert|Zeilenrabatt %|Zeilenrabattbetrag|Zeilenbetrag|DB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|15.00|17.00|3.00|0.51|25.00|1.49|  
|Artikel 2|20,00|23.00|"Keine"|0.00|55.10|3.00|  
|Artikel 3|24.00|27.00|3.00|0.81|112.70|2.19|  

Das Feld **Zu fakturieren (Jahr)** entspricht dem Wert des Felds **Berech. zu fakturieren (Jahr)**, das immer der Summe der Zeilenbeträge entspricht. In diesem Fall entspricht es 16,49 + 23,00 + 26,19 = 65,68.  

Wenn Sie den Wert von **Zu fakturieren (Jahr)** auf 60 ändern, werden die DB-Prozentsatzanteile für jede Vertragszeile berechnet:  

* Artikel 1 – 5 / (5 + 5,1 +12,7) = 0,2193 %  
* Artikel 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Artikel 3 – 12.7 / (5 + 5,1 +12,7) = 0,557 %  

Der Wert des Felds **Zeilenbetrag** wird in jeder Vertragszeile aktualisiert. Dabei wird folgende Formel verwendet: Zeilenbetrag + Differenz zwischen dem neuen und dem berechneten Betrag zu fakturieren (Jahr) * Prozentanteil des Beitrags. Danach werden die Felder **Zeilenrabattbetrag**, **Zeilenrabatt %** und **DB** aktualisiert, indem die Formeln aus den o. a. Schritten verwendet werden.  

Zum Schluss werden die Vertragszeilen die folgenden Daten enthalten.  

|Artikel|Zeileneinstandspreis|Zeilenwert|Zeilenrabatt %|Zeilenrabattbetrag|Zeilenbetrag|DB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|15.00|17.00|11.41|1.94|15.06|0.06|  
|Artikel 2|20,00|23.00|8.65|1.99|21.01|1.01|  
|Artikel 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### <a name="distribution-based-on-profit"></a>Verteilung nach DB
Wenn Sie den jährlichen Betrag für den Servicevertrag oder das Servicevertragsangebot ändern, müssen Sie u. U. die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag auf die Vertragszeilen verteilen. Die Verteilung basierend auf dem DB ist eine der automatischen Verteilungsmethoden, die Ihnen dabei helfen kann, die Differenz zwischen dem neuen und dem berechneten jährlichen Betrag auf die Zeilenbeträge der Vertragszeilen zu verteilen. Die Verteilung wird gemäß dem Anteil des DB am Gesamtvertragsdeckungsbeitrag oder Vertragsangebotsdeckungsbeitrag vorgenommen. Die folgende Übersicht über Verteilungsschritte für Vertragszeilen beschreibt die Grundidee dieser Methode:  

1. Der DB %-Anteil wird wie folgt berechnet: Der Inhalt des Felds **DB** wird durch die Summe aller Feldwerte **DB** aller Vertragszeilen geteilt.  
2. Der **Zeilenbetrag** wird aktualisiert, indem die Differenz zwischen dem neuen und dem berechneten Betrag zu fakturieren (Jahr) hinzuaddiert wird, dann wird mit dem DB-Prozentanteil multipliziert.  
3. Der Inhalt der Felder Zeilenrabattbetrag, Zeilenrabatt % und DB wird hinsichtlich des neuen Werts im Feld **Zeilenbetrag** wie folgt aktualisiert:  

    * Zeilenrabattbetrag = Zeilenwert - Zeilenbetrag  
    * Zeilenrabatt % = Zeilenrabattbetrag / Zeilenwert * 100  
    * DB = Zeilenbetrag - Zeileneinstandspreis  

#### <a name="example"></a>Beispiel  
Das Feld **Nicht ausgegl. Betr. zulassen** ist nicht im Servicevertrag aktiviert, wenn dieser drei Vertragszeilen mit folgenden Daten enthält.  

|Artikel|Zeileneinstandspreis|Zeilenwert|Zeilenrabatt %|Zeilenrabattbetrag|Zeilenbetrag|DB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|20,00|25.00|0.00|0.00|25.00|5.00|  
|Artikel 2|50.00|58.00|5.00|2.90|55.10|5.10|  
|Artikel 3|100.00|115.00|2.00|2.30|112.70|12.70|  

Das Feld **Zu fakturieren (Jahr)** entspricht dem Wert des Feldes **Berech. zu fakturieren (Jahr)**, das immer der Summe der Zeilenbeträge entspricht. In diesem Fall entspricht es 25,00 + 55,10 + 112,70 = 192,80.  

 Wenn Sie den Wert von **Zu fakturieren (Jahr)** auf 180 ändern, werden die DB-Prozentsatzanteile für jede Vertragszeile berechnet:  

* Artikel 1 – 5 / (5 + 5,1 +1 2,7) = 0,2193 %  
* Artikel 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Artikel 3 – 12.7 / (5 + 5,1 +12,7) = 0,557 %  

Der Wert des Felds **Zeilenbetrag** wird in jeder Vertragszeile aktualisiert. Dabei wird folgende Formel verwendet: Zeilenbetrag + Differenz zwischen dem neuen und dem berechneten Betrag zu fakturieren (Jahr) * Prozentanteil des Beitrags. Danach werden die Felder **Zeilenrabattbetrag**, **Zeilenrabatt %** und **DB** aktualisiert, indem die Formeln von Schritt 3 aus den o. a. Schritten verwendet werden.  

Zum Schluss werden die Vertragszeilen die folgenden Daten enthalten.  

|Artikel|Zeileneinstandspreis|Zeilenwert|Zeilenrabatt %|Zeilenrabattbetrag|Zeilenbetrag|DB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|20,00|25.00|11.24|2.81|22.19|2.19|  
|Artikel 2|50.00|58.00|9.93|5.76|52.24|2.24|  
|Artikel 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## <a name="see-also"></a>Siehe auch  
[Erstellen von Serviceverträgen und Servicevertragsangeboten](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
