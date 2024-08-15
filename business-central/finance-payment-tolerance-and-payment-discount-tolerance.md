---
title: Zahlungstoleranz und Skontotoleranz
description: 'Dieser Artikel erklärt, wie Sie Zahlungstoleranz einrichten können, um eine Rechnung zu schließen, wenn die Zahlung nicht vollständig den Betrag der Rechnung umfasst.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '118, 314, 395'
ms.date: 07/05/2024
ms.service: dynamics-365-business-central
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Mit Zahlungstoleranzen und Skontotoleranzen arbeiten

Sie können eine Zahlungstoleranz einrichten, um eine Rechnung zu schließen, wenn die Zahlung nicht vollständig den Betrag der Rechnung umfasst. Beispielsweise sind Zahlungstoleranzen in der Regel für kleine Beträge vorgesehen, deren Korrektur mehr kosten würde als deren Akzeptanz. Die eingerichtete Skontotoleranz erlaubt Ihnen, Skonto nach Ablauf des Skontodatums zu gewähren.  

Sie können Zahlungstoleranzen verwenden, sodass für jeden Restauftragsbetrag eine festgelegte maximale Zahlungstoleranz definiert wird. Wenn die Zahlungstoleranz erfüllt wird, dann wird der Zahlungsbetrag analysiert. Wenn der Zahlungsbetrag eine Unterzahlung ist, wird der ausstehende Betrag durch die Unterzahlung vollständig geschlossen. Für den Zahlungsposten wird ein detaillierter Debitorenposten gebucht, sodass in dem ausgeglichenen Rechnungsposten kein Restbetrag offen bleibt. Wenn der Zahlungsbetrag eine Überzahlung ist, wird für den Zahlungsposten wird ein neuer detaillierter Debitorenposten gebucht, sodass in dem Zahlungsposten kein Restbetrag offen bleibt.

Sie können Skototoleranzen einrichten, sodass bei Gewährung eines Rabatts nach Ablauf des Skontodatums dieses immer auf ein Skonto- oder ein Zahlungstoleranzkonto gebucht wird.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Anwenden der Zahlungstoleranz auf mehrere Belege

Ein einzelner Beleg hat dieselben Zahlungstoleranzen, egal ob er alleine oder mit anderen Belegen ausgeglichen wird. Das Akzeptieren eines verspäteten Skontos, wenn Sie Zahlungstoleranz auf mehrere Belegen anwenden, tritt automatisch für jeden Beleg auf, für den die folgende Regel gilt:  

*Skontodatum < Zahlungsdatum (des markierten Postens) <= Zahlungstoleranzdatum*  

Diese Regel bestimmt auch, um zu ermitteln, ob Warnungen angezeigt werden, wenn Sie Zahlungstoleranz auf mehrere Belege anwenden. Die Skontotoleranzwarnung wird für jeden Posten angezeigt, der die Datumskriterien erfüllt. Weitere Informationen finden unter [Beispiel 2 – Toleranzberechnungen für mehrere Belege](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

Sie können eine Warnung anzeigen, die auf verschiedenen Toleranzsituationen basiert.  

- Der erste Warnungstext bezieht sich auf die Skontotoleranz. Sie werden darüber informiert, dass Sie einen verspäteten Skonto akzeptieren können. Sie können auswählen, ob Toleranz für das Skontodatum akzeptiert werden soll.  
- Der zweite Warnungstext bezieht sich auf die Zahlungstoleranz. Sie werden darüber informiert, dass alle Posten geschlossen werden können, da die Differenz innerhalb der maximalen Zahlungstoleranz der ausgeglichenen Posten liegt. Sie können auswählen, ob Toleranz für die Zahlungssumme akzeptiert werden soll.

> [!NOTE]
> Durch Aktivieren der Warnmeldung können Sie auswählen, wie Zahlungen innerhalb der Toleranz verarbeitet werden sollen. Wenn Sie die Meldung nicht aktivieren und eine Toleranzstufe angegeben ist, werden Rechnungen mit Beträgen, die innerhalb der Toleranz liegen, automatisch geschlossen. Sie können den Restbetrag dann nicht mehr offen lassen. 

Weitere Informationen finden Sie unter [So aktivieren oder deaktivieren Sie die Zahlungstoleranzwarnung](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings). 

## <a name="to-set-up-tolerances"></a>Toleranzen einrichten:

Die Zahlungstoleranz für Tage und Beträge erlaubt Ihnen, eine Rechnung zu schließen, auch wenn die Zahlung nicht vollständig den Betrag der Rechnung umfasst. Zum Beispiel wegen Skontoüberschreitung, Warenabzug oder wegen eines kleinen Fehlers. Dieses Prinzip gilt auch für Gutschriften und Erstattungen.  

Um diese Toleranz einzurichten, müssen Sie verschiedene Toleranzkonten einrichten, das Skontokonto und die Zahlungstoleranzbuchungsmethode spezifizieren und die Stapelverarbeitung **Zahlungstoleranz ändern** laufen lassen.  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Allgemeine Buchungsmatrixeinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Seite **Buchungsmatrix Einrichtung**. Richten Sie ein Haben- und ein Soll-Verkaufszahlungstoleranzkonto sowie ein Haben- und ein Soll-Einkaufszahlungstoleranzkonto ein.  
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Debitorenbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.    
4. Öffnen Sie die Seite **Debitorenbuchungsgruppen**. Richten Sie ein Haben- und ein Soll-Zahlungstoleranzkonto ein. Weitere Informationen finden Sie unter [Einrichten von Buchungsgruppen](finance-posting-groups.md).  
5. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kreditorenbuchungseinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
6. Öffnen Sie die Seite **Debitorenbuchungsgruppen**. Richten Sie ein Haben- und ein Soll-Zahlungstoleranzkonto ein.  
7. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
8. Öffnen Sie die Seite **Finanzbuchhaltung Einrichtung**.  
9. Füllen Sie auf dem Inforegister  **Anwendung**  die Felder  **Zahlungsrabatt-Toleranzbuchung**,  **Zahlungsrabatt-Karenzzeit**  und  **Zahlungstoleranzbuchung**  aus.   
10. Wählen Sie die Aktion **Zahlungstoleranz ändern** aus.

    > [!NOTE]
    > Wenn Sie **Auf Älteste Anwenden** im Feld **Anwendungsverfahren** auf der Seite **Debitorenkarte** auswählen, bucht [!INCLUDE[prod_short](includes/prod_short.md)] Zahlungstoleranzen nicht automatisch, selbst wenn sie innerhalb der festgelegten Schwellen auf der Seite **Finanzbuchhaltungs-Einrichtung** liegen. [!INCLUDE[prod_short](includes/prod_short.md)] geht davon aus, dass die Einstellung "Auf Älteste anwenden" angibt, dass der Debitor (oder Sie als Debitor Ihres Kreditors) ein Konto bei Ihnen hat, auf das er regelmäßig den Saldo zahlt. Daher sollten Restbeträge nicht durch das Buchen eines Zahlungstoleranzeintrags entfernt werden.

11. Füllen Sie auf der Seite  **Zahlungstoleranz ändern**  die Felder  **Zahlungstoleranz %**  und  **Max. Zahlungstoleranzbetrag**  aus und wählen Sie dann die Schaltfläche  **OK** .

> [!IMPORTANT]  
> Sie haben jetzt nur die Toleranz für die Mandantenwährung eingerichtet. Wenn [!INCLUDE[prod_short](includes/prod_short.md)] Toleranzen auf Zahlungen, Gutschriften und Erstattungen in Fremdwährungen gewähren soll, müssen Sie die Stapelverarbeitung **Zahlungstoleranz ändern** mit einem Wert im Feld **Währungscode** aufrufen.  

> [!NOTE]  
> Zum Erhalten einer Zahlungstoleranzwarnung jedes Mal, wenn Sie einen Ausgleich innerhalb der Toleranz buchen, müssen Sie die Zahlungstoleranzwarnung aktivieren. Weitere Informationen finden Sie unter [So aktivieren oder deaktivieren Sie die Zahlungstoleranzwarnung](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).  
>
> Um die Toleranz für einen Debitor oder Kreditor zu deaktivieren, müssen Sie auf der Debitoren- oder Kreditorenkarte Toleranzen blockieren. Weitere Informationen finden unter [Zahlungstoleranz für Debitoren sperren](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).  
>
> Wenn Sie eine Toleranz einrichten, prüft [!INCLUDE[prod_short](includes/prod_short.md)] auch, ob es offene Posten gibt, und berechnet die Toleranz für diese Posten.

> [!IMPORTANT]  
> Wenn Sie das Feld **An Zahlungsrabatt anpassen** auf der Seite **Einrichtung der MwSt.-Buchung** aktivieren, gilt der MwSt.-Betrag als es bezieht sich auf die Beträge **Zahlungstoleranzen** und **Zahlungsrabatte** , und die Mehrwertsteuer wird für beide Transaktionsbeträge reduziert, wenn Sie existieren. Das System kann nicht so konfiguriert werden, dass es die Mehrwertsteuersenkung nur für eine Transaktionsart verwendet.  

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>So aktivieren oder deaktivieren Sie die Zahlungstoleranzwarnungen

Die Zahlungstoleranzwarnung erscheint, wenn Sie einen Ausgleich mit einem Saldo innerhalb der erlaubten Toleranz buchen. Sie können dann wählen, wie Sie den Saldo buchen und dokumentieren wollen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Aktivieren Sie auf der Seite **Finanzbuchhaltung einrichten** im Inforegister **Anwendung** den Schalter **Zahlungstoleranzwarnung**, um die Warnung zu aktivieren. Deaktivieren Sie den Schalter, um die Warnung zu deaktivieren.  

> [!NOTE]  
> Die Standardoption der Seite **Zahlungstoleranzwarnung** ist **Restbetrag offen lassen**. Die Standardoption der Seite **Skontotoleranzwarnung** ist **Überzogenes Skonto nicht akzeptieren**.

## <a name="to-block-payment-tolerance-for-customers"></a>Zahlungstoleranz für Debitoren sperren:

Die Standardeinrichtung für die Zahlungstoleranz ist zulässig. Sperren Sie auf der entsprechenden Debitoren- oder Kreditorenkarte die Toleranz, um eine Zahlungstoleranz für einen bestimmten Kreditor oder Debitor zu sperren. Anhand der folgenden Schritte wird die Vorgehensweise für einen Debitor beschrieben: Die Schritte sind für einen Kreditor ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kunde** oder **Kreditor** ein und wählen Sie dann den zugehörigen Link.  
2. Aktivieren Sie auf dem Inforegister **Zahlungen** das Kontrollkästchen **Zahlungstoleranz sperren**.  

> [!NOTE]  
> Sind für einen Debitor oder Kreditor offene Posten vorhanden, müssen Sie zuerst die Zahlungstoleranz aus den offenen Posten entfernen.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Beispiel 1 – Toleranzberechnungen für einen einzelnen Beleg

Im Folgenden wird anhand von Beispielszenarien gezeigt, welche Toleranzberechnungen und Buchungen sich in verschiedenen Situationen ergeben.  

Die Seite **Sachkontoeinrichtung** enthält die folgende Einrichtung:

- Skontozahlungstoleranzperiode:    5T  
- Maximale Zahlungstoleranz. 5  

Szenarien mit Alternative A oder B bedeuten:  

- **A** – In diesem Fall wurde die Skontotoleranzwarnung ausgeschaltet ODER der Benutzer hat die Warnung aktiviert und sich entschieden, den verspäteten Skonto zu erlauben (d. h. den Saldo als Zahlungstoleranz zu buchen).  
- **B** – In diesem Fall hat der Benutzer die Warnung aktiviert und sich entschieden, den überzogenen Skonto nicht zu erlauben (d. h. den Saldo als Restbetrag zu belassen).  

|—|Inv.|Skonto|Max. Zahlungstoleranz|Skontodatum|Skontotoleranz – Datum|Zahlungsdatum|Zahlung|Toleranzart|Alle Posten geschlossen|Skontotoleranz GL/CL|Maximale Zahlungstoleranz GL/CL|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1.000|20|5|15.01.2003|01/20/03|<=15.01.03|985|PaymentTolerance|Ja|0|-5|  
|2|**1,000**|**20**|**5**|**15.01.2003**|**01/20/03**|**<=15.01.03**|**980**|**Keine**|**Ja**|**0**|**0**|  
|3|1.000|20|5|15.01.2003|a|<=15.01.03|975|PaymentTolerance|Ja|0|5|  
|4A|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|1005|PaymentDiscountTolerance|Nein, 25 in der Zahlung|20/-20|0|  
|5A|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|1000|PaymentDiscountTolerance|Nein, 20 in der Zahlung|20/-20|0|  
|6A|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|995|PaymentDiscountTolerance|Nein, 15 in der Zahlung|20/-20|0|  
|4B|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|1005|PaymentTolerance|Ja|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15.01.2003**|**01/20/03**|**16.01.2003 – 20.01.03**|**1000**|**Keine**|**Ja**|**0**|**0**|  
|6B|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|995|PaymentTolerance|Ja|0|5|  
|7|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|985|PaymentDiscountTolerance & PaymentTolerance|Ja|20/-20|-5|  
|8|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|980|PaymentDiscountTolerance|Ja|20/-20|0|  
|9|1.000|20|5|15.01.2003|01/20/03|16.01.2003 – 20.01.03|975|PaymentDiscountTolerance & PaymentTolerance|Ja|20/-20|5|  
|10|1.000|20|5|15.01.2003|01/20/03|>20.01.03|1005|PaymentTolerance|Ja|0|-5|  
|**11**|**1,000**|**20**|**5**|**15.01.2003**|**01/20/03**|**>20.01.03**|**1000**|**Keine**|**Ja**|**0**|**0**|  
|12|1.000|20|5|15.01.2003|01/20/03|>20.01.03|995|PaymentTolerance|Ja|0|5|  
|13|1.000|20|5|15.01.2003|01/20/03|>20.01.03|985|"Keine"|Nein, 15 in der Rech.|0|0|  
|14|1.000|20|5|15.01.2003|01/20/03|>20.01.03|980|"Keine"|Nein, 20 in der Rech.|0|0|  
|15|1.000|20|5|15.01.2003|01/20/03|>20.01.03|975|"Keine"|Nein, 25 in der Rech.|0|0|  

### <a name="payment-range-diagrams"></a>Zahlungsbereichsdiagramme

Bezugnehmend auf das Szenario, sind die Zahlungszeiträume wie folgt:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Zahlungsdatum <=15.01.03 (Szenarien 1-3)

Restbetrag gemäß  

Normale Ausgleichsvorschriften  

![Einzelzahlungstoleranzregeln 1.](media/singlePmtTolRules_Pre1503.gif "Einmahlzahlungstoleranz-Regeln 1")  

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Zahlung zwischen dem 16.01.2003 und 20.01.2003 (Szenarien 4-9)

Restbetrag gemäß  

Normale Ausgleichsvorschriften  

![Einzelzahlungstoleranzregeln 2.](media/singlePmtTolRules_GracePeriod.gif "Einmahlzahlungstoleranz-Regeln 2")  

(1) Wenn die Zahlung in diese Bereiche fällt, können alle Anwendungseinträge mit oder ohne Toleranz abgeschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Zahlungsdatum liegt nach dem 20.01.03 (Szenarien 10-15)

Restbetrag gemäß  

Normale Ausgleichsvorschriften  

![Einzelzahlungstoleranzregeln 3.](media/singlePmtTolRules_Post0120.gif "Einmalzahlungstoleranz-Regeln 3")  

(1) Wenn die Zahlung in diese Bereiche fällt, können alle Anwendungseinträge mit oder ohne Toleranz abgeschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Beispiel 2 – Toleranzberechnungen für mehrere Belege

Im Folgenden wird anhand von Beispielszenarien gezeigt, welche Toleranzberechnungen und Buchungen sich in verschiedenen Situationen ergeben. Die Beispiele beschränken sich auf die Szenarien, die dazu führen, dass alle Posten geschlossen werden.  

Die Seite **Sachkontoeinrichtung** enthält die folgende Einrichtung:
- Skontotoleranzperiode:     5T  
- Maximale Zahlungstoleranz                 5  

Szenarien mit Alternative A, B, C oder D bedeuten Folgendes:  

- **A** – In diesem Fall wurde die Skontotoleranzwarnung ausgeschaltet oder der Benutzer hat die Warnung aktiviert und sich entschieden, den verspäteten Skonto in jeder Rechnung zu erlauben (d. h. als Toleranz auszubuchen).  
- **B** – In diesem Fall hat der Benutzer die Warnung aktiviert und sich entschieden, den verspäteten Skonto in keiner Rechnung zu erlauben.  
- **C** – In diesem Fall hat der Benutzer die Warnung aktiviert und sich entschieden, den verspäteten Skonto in der ersten Rechnung zu erlauben, in der zweiten jedoch nicht.  
- **D** – In diesem Fall hat der Benutzer die Warnung aktiviert und sich entschieden, den verspäteten Skonto in der ersten Rechnung nicht zu erlauben, jedoch in der zweiten.  

|—|Inv.|Skonto|Max. Zahlungstoleranz|Skontodatum|Skontotoleranz – Datum|Zahlungsdatum|Zahlung|Toleranzart|Alle Posten geschlossen|Skontotoleranz GL/CL|Maximale Zahlungstoleranz GL/CL|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|<=15.01.03|1920|PaymentTolerance|Ja|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**<=15.01.03**|**1910**|**Keine**|**Ja**|**0**<br /><br /> **0**|0 <br />0|  
|3|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|<=15.01.03|1900|PaymentTolerance|Ja|0<br /><br /> 0|5 <br />5|  
|4B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1980|PaymentTolerance|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/16/03 01/17/03**|**1970**|**Keine**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1960|PaymentTolerance|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1920|PaymentDiscountTolerance & PaymentTolerance|Ja|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1910|PaymentDiscountTolerance|Ja|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/16/03 01/17/03|1900|PaymentDiscountTolerance & PaymentTolerance|Ja|60/60|5 <br />5|  
|10B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|2010|PaymentTolerance|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/18/03 01/20/03**|**2000**|**Keine**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1990|PaymentTolerance|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1980|PaymentDiscountTolerance & PaymentTolerance|Ja|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1970|PaymentDiscountTolerance|Ja|0/0<br /><br /> 30/-30|0 <br />0|  
|15T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1960|PaymentDiscountTolerance & PaymentTolerance|Ja|0/0<br /><br /> 30/-30|5 <br />5|  
|16T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1950|PaymentDiscountTolerance & PaymentTolerance|Ja|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1940|PaymentDiscountTolerance|Ja|60/-60<br /><br /> 0/0|0 <br />0|  
|18T|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1930|PaymentDiscountTolerance & PaymentTolerance|Ja|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1920|PaymentDiscountTolerance & PaymentTolerance|Ja|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1910|PaymentDiscountTolerance|Ja|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/18/03 01/20/03|1900|PaymentDiscountTolerance & PaymentTolerance|Ja|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|2010|PaymentTolerance|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**01/21/03 01/22/03**|**2000**|**Keine**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|1990|PaymentTolerance|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|1980|PaymentDiscountTolerance & PaymentTolerance|Ja|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|1970|PaymentDiscountTolerance|Ja|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|01/21/03 01/22/03|1960|PaymentDiscountTolerance & PaymentTolerance|Ja|0/0<br /><br /> 30/30|5 <br />5|  
|28|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|>22.01.03|2010|PaymentTolerance|Ja|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.2003** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**>22.01.03**|**2000**|**Keine**|**Ja**|**0**|**0**|  
|30|1.000 <br />1.000|60 <br />30|5 <br />5|15.01.2003 <br />17.01.2003|01/20/03 <br />01/22/03|>22.01.03|1990|PaymentTolerance|Ja|0|5|  

### <a name="payment-range-diagrams-1"></a>Zahlungsbereichsdiagramme

Bezugnehmend auf das Szenario, sind die Zahlungszeiträume wie folgt:  

#### <a name="1-payment-date-011503-scenarios-1-3-1"></a>(1) Zahlungsdatum <=15.01.03 (Szenarien 1-3)

Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules_Pre1503.gif" alt-text="Mehrfachzahlungstoleranz-Regeln 1A":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Zahlung zwischen dem 16.01.2003 und 17.01.2003 (Szenarien 4-9)

Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv1-2.gif" alt-text="Mehrfachzahlungstoleranz-Regeln 2":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Zahlung zwischen dem 18.01.2003 und 20.01.2003 (Szenarien 10-21)

Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv1.gif" alt-text="Mehrfachzahlungstoleranz-Regeln 3":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Zahlung zwischen dem 21.01.03 und 22.01.03 (Szenarien 22-27)

Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules_GracePeriodInv2.gif" alt-text="Mehrfachzahlungstoleranz-Regeln 4":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Zahlungsdatum liegt nach dem 22.01.2003 (Szenarien 28-30)

Restbetrag gemäß  

Normale Ausgleichsvorschriften  

:::image type="content" source="media/multiplePmtTolRules_Post0122.gif" alt-text="Mehrfachzahlungstoleranz-Regeln 5":::

(1) Fällt die Zahlung in diesen Zeitraum, können alle Ausgleichsposten mit oder ohne Toleranz geschlossen werden.  

(2) Fällt die Zahlung in diesen Bereich, können nicht alle Posten geschlossen werden, auch nicht mit Toleranz.

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
