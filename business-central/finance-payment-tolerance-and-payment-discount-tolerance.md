---
title: Zahlungstoleranz und Skontotoleranz | Microsoft Docs
description: Sie können Zahlungstoleranz einrichten, um eine Rechnung zu schließen, wenn die Zahlung nicht vollständig den Betrag der Rechnung umfasst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c2669d830ab95e5cd0c20240ae776175a2db9f6a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380027"
---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Mit Zahlungstoleranzen und Skontotoleranzen arbeiten
Sie können eine Zahlungstoleranz einrichten, um eine Rechnung zu schließen, wenn die Zahlung nicht vollständig den Betrag der Rechnung umfasst. Beispielsweise sind Zahlungstoleranzen in der Regel für kleine Beträge vorgesehen, deren Korrektur mehr kosten würde als deren Akzeptanz. Die eingerichtete Skontotoleranz erlaubt Ihnen, Skonto nach Ablauf des Skontodatums zu gewähren.  

Sie können Zahlungstoleranzen verwenden, sodass für jeden Restauftragsbetrag eine festgelegte maximale Zahlungstoleranz definiert wird. Wenn die Zahlungstoleranz erfüllt wird, dann wird der Zahlungsbetrag analysiert. Wenn der Zahlungsbetrag eine Unterzahlung ist, wird der ausstehende Betrag durch die Unterzahlung vollständig geschlossen. Für den Zahlungsposten wird ein detaillierter Debitorenposten gebucht, sodass in dem ausgeglichenen Rechnungsposten kein Restbetrag offen bleibt. Wenn der Zahlungsbetrag eine Überzahlung ist, wird für den Zahlungsposten wird ein neuer detaillierter Debitorenposten gebucht, sodass in dem Zahlungsposten kein Restbetrag offen bleibt.

Sie können Skototoleranzen verwenden, sodass bei Gewährung eines Skontos nach Ablauf des Skontodatums dieses immer entweder auf das Skontokonto oder das Zahlungstoleranzkonto gebucht wird.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Anwenden der Zahlungstoleranz auf mehrere Belege  
Ein einzelner Beleg hat dieselben Zahlungstoleranzen, egal ob er alleine oder mit anderen Belegen ausgeglichen wird. Das Akzeptieren eines verspäteten Skontos, wenn Sie Zahlungstoleranz auf mehrere Belegen anwenden, tritt automatisch für jeden Beleg auf, für den die folgende Regel gilt:  

*Skontodatum < Zahlungsdatum (des markierten Postens) <= Zahlungstoleranzdatum*  

Diese Regel gilt auch, um zu ermitteln, ob Warnungen angezeigt werden, wenn Sie Zahlungstoleranz auf mehrere Belege anwenden. Die Skontotoleranzwarnung wird für jeden Posten angezeigt, der die Datumskriterien erfüllt. Weitere Informationen finden unter [Beispiel 2 – Toleranzberechnungen für mehrere Belege](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

Sie können eine Warnung anzeigen, die auf verschiedenen Toleranzsituationen basiert.  

- Der erste Warnungstext bezieht sich auf die Skontotoleranz. Sie werden darüber informiert, dass Sie einen verspäteten Skonto akzeptieren können. Sie können auswählen, ob Toleranz für das Skontodatum akzeptiert werden soll.  
- Der zweite Warnungstext bezieht sich auf die Zahlungstoleranz. Sie werden darüber informiert, dass alle Posten geschlossen werden können, da die Differenz innerhalb der maximalen Zahlungstoleranz der ausgeglichenen Posten liegt. Sie können auswählen, ob Toleranz für die Zahlungssumme akzeptiert werden soll.

> [!NOTE]
> Durch Aktivieren der Warnmeldung können Sie auswählen, wie Zahlungen innerhalb der Toleranz verarbeitet werden sollen. Wenn Sie die Meldung nicht aktivieren und eine Toleranzstufe angegeben ist, werden Rechnungen mit Beträgen, die innerhalb der Toleranz liegen, automatisch geschlossen. Sie können den Restbetrag dann nicht mehr offen lassen. 

Weitere Informationen finden Sie unter [So aktivieren oder deaktivieren Sie die Zahlungstoleranzwarnung](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings). 

## <a name="to-set-up-tolerances"></a>Toleranzen einrichten:  
Toleranz auf Tage und Beträge erlaubt Ihnen, eine Rechnung auszugleichen, selbst wenn die Zahlung nicht vollständig den Rechnungsbetrag abdeckt, sei es aufgrund eines überschrittenen Skontodatums, weil Waren abgezogen wurden oder aufgrund eines kleineren Fehlers. Dies gilt auch für Gutschriften und Erstattungen.  

Um diese Toleranz einzurichten, müssen Sie verschiedene Toleranzkonten einrichten, das Skontokonto und die Zahlungstoleranzbuchungsmethode spezifizieren und die Stapelverarbeitung **Zahlungstoleranz ändern** laufen lassen.  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Buchungsmatrix** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie die Seite **Buchungsmatrix Einrichtung**. Richten Sie ein Haben- und ein Soll-Verkaufszahlungstoleranzkonto sowie ein Haben- und ein Soll-Einkaufszahlungstoleranzkonto ein.  
3. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitorenbuchungsgruppen** ein und wählen Sie dann den entsprechenden Link.    
4. Öffnen Sie die Seite **Debitorenbuchungsgruppen**. Richten Sie ein Haben- und ein Soll-Zahlungstoleranzkonto ein. Weitere Informationen finden Sie unter [Einrichten von Buchungsgruppen](finance-posting-groups.md).  
5. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kreditorenbuchungsmatrix** ein und wählen Sie dann den entsprechenden Link.  
6. Öffnen Sie die Seite **Debitorenbuchungsgruppen**. Richten Sie ein Haben- und ein Soll-Zahlungstoleranzkonto ein.  
7. Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Finanzbuchhaltungs-Einrichtung** ein und wählen Sie dann den entsprechenden Link.  
8. Öffnen Sie die Seite **Finanzbuchhaltung Einrichtung**.  
9. Füllen Sie auf dem Inforegister **Ausgleich** die Felder **Skontotoleranzbuchung**, **Skontotoleranzperiode** und **Zahlungstoleranzbuchung** aus.   
10. Wählen Sie die Aktion **Zahlungstoleranz ändern** aus.
11. Füllen Sie die Seite **Zahlungstoleranz ändern** die Felder **Zahlungstoleranz %** und **Max- Zahlungstoleranzbetrag** und bestätigen Sie dann mit **OK**.

> [!IMPORTANT]  
>  Sie haben jetzt nur die Toleranz für die Mandantenwährung eingerichtet. Wenn [!INCLUDE[prod_short](includes/prod_short.md)] Toleranzen auf Zahlungen, Gutschriften und Erstattungen in Fremdwährungen gewähren soll, müssen Sie die Stapelverarbeitung **Zahlungstoleranz ändern** mit einem Wert im Feld **Währungscode** aufrufen.  

> [!NOTE]  
>  Wenn Sie jedes Mal eine Zahlungstoleranzwarnung erhalten möchten, wenn Sie einen Ausgleich innerhalb der Toleranz buchen, müssen Sie die Zahlungstoleranzwarnung aktivieren. Weitere Informationen finden Sie unter [So aktivieren oder deaktivieren Sie die Zahlungstoleranzwarnung](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>   
>  Um die Toleranz für einen Debitor oder Kreditor zu deaktivieren, müssen Sie auf der Debitoren- oder Kreditorenkarte Toleranzen blockieren. Weitere Informationen finden unter [Zahlungstoleranz für Debitoren sperren](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>   
>  Wenn Sie eine Toleranz einrichten, prüft [!INCLUDE[prod_short](includes/prod_short.md)] auch, ob es offene Posten gibt, und berechnet die Toleranz für diese Posten.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>So aktivieren oder deaktivieren Sie die Zahlungstoleranzwarnungen
Die Zahlungstoleranzwarnung erscheint, wenn Sie einen Ausgleich mit einem Saldo innerhalb der erlaubten Toleranz buchen. Sie können dann wählen, wie Sie den Saldo buchen und dokumentieren wollen.    
1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Finanzbuchhaltungs-Einrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Aktivieren Sie auf der Seite **Finanzbuchhaltung einrichten** im Inforegister **Anwendung** den Schalter **Zahlungstoleranzwarnung**, um die Warnung zu aktivieren. Deaktivieren Sie den Schalter, um die Warnung zu deaktivieren.  

> [!NOTE]  
>  Die Standardoption der Seite **Zahlungstoleranzwarnung** ist **Restbetrag offen lassen**. Die Standardoption der Seite **Kontotoleranzwarnung** ist **Überzogenes Skonto nicht akzeptieren**.

## <a name="to-block-payment-tolerance-for-customers"></a>Zahlungstoleranz für Debitoren sperren:  
Die Standardeinrichtung für die Zahlungstoleranz ist zulässig. Um eine Zahlungstoleranz für einen bestimmten Kreditor oder Debitor zu sperren, müssen Sie auf der entsprechenden Debitoren- oder Kreditorenkarte die Toleranz sperren. Wie dies für einen Debitoren stattfindet, wird im Folgendem beschrieben: Die Schritte sind für einen Kreditor ähnlich.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kunde** oder **Lieferant** ein und wählen Sie dann den entsprechenden Link.  
2. Aktivieren Sie auf dem Inforegister **Zahlungen** das Kontrollkästchen **Zahlungstoleranz sperren**.  

> [!NOTE]  
>  Sind für einen Debitor oder Kreditor offene Posten vorhanden, müssen Sie zuerst die Zahlungstoleranz aus den offenen Posten entfernen.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Beispiel 1 – Toleranzberechnungen für einen einzelnen Beleg
Im Folgenden wird anhand von Beispielszenarien gezeigt, welche Toleranzberechnungen und Buchungen sich in verschiedenen Situationen ergeben.  

Die Seite **Sachkontoeinrichtung** enthält die folgende Einrichtung:
- Skontozahlungstoleranzperiode:    5T  
- Maximale Zahlungstoleranz. 5  

Szenarien mit Alternative A oder B bedeuten Folgendes:  

- **A** – In diesem Fall wurde die Skontotoleranzwarnung ausgeschaltet ODER der Benutzer hat die Warnung aktiviert und sich entschieden, den verspäteten Skonto zu erlauben (d. h. den Saldo als Zahlungstoleranz zu buchen).  
- **B** – In diesem Fall hat der Benutzer die Warnung aktiviert und sich entschieden, den überzogenen Skonto nicht zu erlauben (d. h. den Saldo als Restbetrag zu belassen).  

|—|Inv.|Skonto|Max. Zahl.-Tol.|Skontodatum|Skontotol. Datum|Zahlungsdatum|Zahl.-|Toleranzart|Alle Posten geschlossen|Skontotol. Skontotoleranz|Zahl.-Tol. G/L|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1.000|20|5|15.01.2003|01/20/03|<=15.01.03|985|Zahl.-Tol.|Ja|0|-5|  
|2|**1,000**|**20**|**5**|**15.01.2003**|**01/20/03**|**<=15.01.03**|**980**|**Keine**|**Ja**|**0**|**0**|  
|3|1.000|20|5|15.01.2003|c|<=15.01.03|975|Zahl.-Tol.|Ja|0|5|  
|4A|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|1005|Skontotoleranz|Nein, 25 in der Zahl.|20/-20|0|  
|5A|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|1000|Skontotoleranz|Nein, 20 in der Zahl.|20/-20|0|  
|6A|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|995|Skontotoleranz|Nein, 15 in der Zahl.|20/-20|0|  
|4B|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|1005|Zahl.-Tol.|Ja|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15.01.2003**|**01/20/03**|**16.01.2003 – 20.01.03**|**1000**|**Keine**|**Ja**|**0**|**0**|  
|6B|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|995|Zahl.-Tol.|Ja|0|5|  
|7|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|985|Skontotol. & Zahl.-Tol.|Ja|20/-20|-5|  
|8|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|980|Skontotoleranz|Ja|20/-20|0|  
|9|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|975|Skontotol. & Zahl.-Tol.|Ja|20/-20|5|  
|10|1.000|20|5|15.01.2003|01/20/03|>20.01.03|1005|Zahl.-Tol.|Ja|0|-5|  
|**11**|**1,000**|**20**|**5**|**15.01.2003**|**01/20/03**|**>20.01.03**|**1000**|**Keine**|**Ja**|**0**|**0**|  
|12|1.000|20|5|15.01.2003|01/20/03|>20.01.03|995|Zahl.-Tol.|Ja|0|5|  
|13|1.000|20|5|15.01.2003|01/20/03|>20.01.03|985|"Keine"|Nein, 15 in der Rech.|0|0|  
|14|1.000|20|5|15.01.2003|01/20/03|>20.01.03|980|"Keine"|Nein, 20 in der Rech.|0|0|  
|15|1.000|20|5|15.01.2003|01/20/03|>20.01.03|975|"Keine"|Nein, 25 in der Rech.|0|0|  

### <a name="payment-range-diagrams"></a>Zahlungsbereichsdiagramme  
Bezugnehmend auf das o. g. Szenario, sind die Zahlungszeiträume wie folgt:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Zahlungsdatum <=15.01.03 (Szenarien 1-3)  
Restbetrag gemäß  

Normale Ausgleichsvorschriften  

![Einmalzahlungstoleranz-Regeln 1](media/singlePmtTolRules(Pre1503).gif "Einmahlzahlungstoleranz-Regeln 1")  

(1) Fällt die Zahlung in diesen Zeitraum, können alle Posten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Zeitraum, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Zahlung zwischen dem 16.01.2003 und 20.01.2003 (Szenarien 4-9)  
Restbetrag gemäß  

Normale Ausgleichsvorschriften  

![Einmalzahlungstoleranz-Regeln 2](media/singlePmtTolRules(GracePeriod).gif "Einmahlzahlungstoleranz-Regeln 2")  

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Zeitraum, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Zahlungsdatum liegt nach dem 20.01.03 (Szenarien 10-15)  
Restbetrag gemäß  

Normale Ausgleichsvorschriften  

![Einmalzahlungstoleranz-Regeln 3](media/singlePmtTolRules(Post0120).gif "Einmalzahlungstoleranz-Regeln 3")  

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Zeitraum, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Beispiel 2 – Toleranzberechnungen für mehrere Belege
Im Folgenden wird anhand von Beispielszenarien gezeigt, welche Toleranzberechnungen und Buchungen sich in verschiedenen Situationen ergeben. Die Beispiele beschränken sich auf die Szenarien, die dazu führen, dass alle Posten geschlossen werden.  

Die Seite **Sachkontoeinrichtung** enthält die folgende Einrichtung:
- Skontotoleranzperiode:     5T  
- Maximale Zahlungstoleranz                 5  

Szenarien mit Alternative A, B, C oder D bedeuten Folgendes:  

- **A** – In diesem Fall wurde die Skontotoleranzwarnung ausgeschaltet ODER der Benutzer hat die Warnung aktiviert und sich entschieden, den verspäteten Skonto in jeder Rechnung zu erlauben (d. h. als Toleranz auszubuchen).  
- **B** – In diesem Fall hat der Benutzer die Warnung aktiviert und sich entschieden, den verspäteten Skonto in keiner Rechnung zu erlauben.  
- **C** – In diesem Fall hat der Benutzer die Warnung aktiviert und sich entschieden, den verspäteten Skonto in der ersten Rechnung zu erlauben, in der zweiten jedoch nicht.  
- **D** – In diesem Fall hat der Benutzer die Warnung aktiviert und sich entschieden, den verspäteten Skonto in der ersten Rechnung nicht zu erlauben, jedoch in der zweiten.  

|—|Inv.|Skonto|Max. Zahl.-Tol.|Skontodatum|Skontotol. Datum|Zahlungsdatum|Zahl.-|Toleranzart|Alle Posten geschlossen|Skontotol. Skontotoleranz|Zahl.-Tol. G/L|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|<=15.01.03|1920|Zahl.-Tol.|Ja|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**<=15.01.03**|**1910**|**Keine**|**Ja**|**0**<br /><br /> **0**|0 <br />0|  
|3|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|<=15.01.03|1900|Zahl.-Tol.|Ja|0<br /><br /> 0|5 <br />5|  
|4B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1980|Zahl.-Tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/16/03 01/17/03**|**1970**|**Keine**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1960|Zahl.-Tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1920|Skontotol. & Zahl.-Tol.|Ja|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1910|Skontotoleranz|Ja|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1900|Skontotol. & Zahl.-Tol.|Ja|60/60|5 <br />5|  
|10B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|2010|Zahl.-Tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/18/03 01/20/03**|**2000**|**Keine**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1990|Zahl.-Tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1980|Skontotol. & Zahl.-Tol.|Ja|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1970|Skontotoleranz|Ja|0/0<br /><br /> 30/-30|0 <br />0|  
|15T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1960|Skontotol. & Zahl.-Tol.|Ja|0/0<br /><br /> 30/-30|5 <br />5|  
|16T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1950|Skontotol. & Zahl.-Tol.|Ja|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1940|Skontotoleranz|Ja|60/-60<br /><br /> 0/0|0 <br />0|  
|18T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1930|Skontotol. & Zahl.-Tol.|Ja|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1920|Skontotol. & Zahl.-Tol.|Ja|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1910|Skontotoleranz|Ja|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1900|Skontotol. & Zahl.-Tol.|Ja|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|2010|Zahl.-Tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/21/03 01/22/03**|**2000**|**Keine**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|1990|Zahl.-Tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|1980|Skontotol. & Zahl.-Tol.|Ja|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|1970|Skontotoleranz|Ja|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|1960|Skontotol. & Zahl.-Tol.|Ja|0/0<br /><br /> 30/30|5 <br />5|  
|28|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|>22.01.03|2010|Zahl.-Tol.|Ja|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**>22.01.03**|**2000**|**Keine**|**Ja**|**0**|**0**|  
|30|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|>22.01.03|1990|Zahl.-Tol.|Ja|0|5|  

### <a name="payment-range-diagrams"></a>Zahlungsbereichsdiagramme  
Bezugnehmend auf das o. g. Szenario, sind die Zahlungszeiträume wie folgt:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Zahlungsdatum <=15.01.03 (Szenarien 1-3)  
Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules(Pre1503).gif" alt-text="Mehrfachzahlungstoleranz-Regeln 1A":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Zahlung zwischen dem 16.01.2003 und 17.01.2003 (Szenarien 4-9)  
Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules(GracePeriodInv1-2).gif" alt-text="Mehrfachzahlungstoleranz-Regeln 2":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Zahlung zwischen dem 18.01.2003 und 20.01.2003 (Szenarien 10-21)  
Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules(GracePeriodInv1).gif" alt-text="Mehrfachzahlungstoleranz-Regeln 3":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Zahlung zwischen dem 21.01.03 und 22.01.03 (Szenarien 22-27)  
Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules(GracePeriodInv2).gif" alt-text="Mehrfachzahlungstoleranz-Regeln 4":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Zahlungsdatum liegt nach dem 22.01.2003 (Szenarien 28-30)  
Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules(Post0122).gif" alt-text="Mehrfachzahlungstoleranz-Regeln 5":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Zeitraum, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.

## <a name="see-also"></a>Siehe auch  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]