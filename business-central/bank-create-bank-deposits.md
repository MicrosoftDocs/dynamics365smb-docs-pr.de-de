---
title: Bankeinzahlungen erstellen
description: 'Sie können Einzahlungen vornehmen, um einen Transaktionsdatensatz zu pflegen, der Informationen enthält, die auf ausstehende Rechnungen und Gutschriften angewendet werden können.'
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Bankeinzahlungen erstellen
> [!NOTE]
> Die Möglichkeit zum Erstellen von Bankeinzahlungen ist in Business Central 2022 Veröffentlichungszyklus 1 für viele Länder-/Regionsversionen neu. Wenn Sie Business Central in den Vereinigten Staaten, Kanada oder Mexiko vor dieser Version verwendet haben, verwenden Sie möglicherweise die früheren Funktionen. Sie können fortfahren, die neuen Funktionen werden die alten jedoch in einer zukünftigen Version ersetzen. Ihr Administrator kann zur Seite **Funktionsverwaltung** navigieren und die Option **Funktionsupdate: Standardisierte Bankabstimmung und Einzahlungen** aktivieren, um die in diesem Artikel beschriebenen neuen Funktionen zu verwenden.  

Verwenden Sie die Seite **Bankeinzahlungen**, um Einzahlungen als einzelnes Dokument zu registrieren, das einen oder mehrere Posten auf einem Bankkonto bucht. Bankeinzahlung werden in der Regel verwendet, um Bareinzahlungen zu registrieren. Die Seite „Bankeinzahlungen“ ist im Menü **Zahlungsmanagement** im Rollencenter „Geschäftsführer“ und in anderen Rollencentern verfügbar, die sich auf das Zahlungsmanagement beziehen.

Beträge auf Bankeinlagen können aus mehreren Quellen stammen:

* Verkäufe unter Verwendung eines Sachkontos für Umsätze
* Debitorenzahlungen
* Barrückerstattungen von Kreditoren oder Barzahlungen an sie 

Bankeinzahlungszeilen enthalten Informationen zu einzelnen Einzahlungen, z. B. Schecks von Debitoren. Die Summe der Beträge in den Zeilen muss den Gesamtbetrag der Einzahlung ergeben.

Nachdem Sie die Einzahlungsinformationen und -zeilen ausgefüllt haben, müssen Sie sie buchen. Durch die Buchung werden die relevanten Sachkonten aktualisiert. Zu diesen Sachkonten gehören der Sachposten sowie die Bank-, Debitoren- und Kreditorenposten. Gebuchte Einzahlungen werden zur späteren Referenz auf der Seite **Gebuchte Bankeinzahlungen** gespeichert.

Der Bericht **Bankeinzahlung** zeigt Debitoren- und Kreditoreneinzahlungen mit dem ursprünglichen Einzahlungsbetrag, dem noch offenen Einzahlungsbetrag und dem angewendeten Betrag an. Der Bericht zeigt auch den gesamten gebuchten Einzahlungsbetrag an, der abgestimmt werden soll.

## Bevor Sie beginnen
Bevor Sie Bankeinzahlungen verwenden können, müssen einige Dinge eingerichtet werden. Sie müssen eine Nummernserien- und Fibu Buch.-Blattvorlage bereithalten. Sie sollte außerdem angeben, ob Bankeinzahlungsbeträge als Abschlag gebucht werden sollen. D. h. als Summe aller Beträge in den Einzahlungszeilen. Andernfalls wird jede Zeile als einzelner Posten gebucht. Das Buchen einer Einzahlung als einzelner Bankposten kann den Bankabgleich vereinfachen.

### Nummernserien und Abschlagseinzahlungen
Sie müssen eine Nummernserie für Bankeinzahlungen einrichten und dann die Serie im Feld **Bankeinzahlungsnr.** auf der Seite **Debitoren & Verkauf Einr.** angeben. Weitere Informationen finden Sie unter [Nummernserie erstellen](ui-create-number-series.md). 

Wenn Sie Einzahlungen als Pauschalbeträge und nicht als einzelne Zeilen buchen möchten, aktivieren Sie auch auf der Seite **Debitoren & Verkauf Einrichtung** die Umschaltfläche **Bankeinzahlungen als Abschlag buchen**. Wird die Buchung einer Einzahlung als Pauschalbetrag gebucht, wodurch ein Posten für den vollen Betrag der Einzahlung erstellt wird, kann der Bankabgleich vereinfacht werden.

### Fibu Buch.-Blattvorlagen für Bankeinzahlungen
Sie müssen auch eine Fibu Buch.-Blattvorlage für Einzahlungen erstellen. Fibu Buch.-Blätter werden verwendet, um Posten auf Bank-, Debitoren-, Kreditoren-, Anlagen- und Hauptbuchkonten zu buchen. Die Buch.-Blattvorlagen passen das Fibu Buch.-Blatt an Ihren Arbeitszweck an. Das heißt, die Buch.-Blattvorlage enthält genau die Felder, die Sie benötigen. 

Die Einzahlungen sind Zahlungseingänge, sodass Sie Ihre Nummernserie für Zahlungseingangs Buch.-Blätter wiederverwenden können. Wenn Sie zwischen Einträgen von Bankeinzahlungen und Zahlungseingangs Buch.-Blättern unterscheiden müssen, verwenden Sie alternativ eine andere Nummernserie.

Sie müssen außerdem einen Batchauftrag für die Vorlage erstellen. Um einen Batchauftrag zu erstellen, wählen Sie auf der Seite **Fibu Buch.-Blattvorlagen** die Aktion **Chargen** aus. Weitere Informationen finden Sie unter [Buch-Blattvorlagen und Stapel nutzen](ui-work-general-journals.md#use-journal-templates-and-batches).

## Dimensionen in Bankeinzahlungszeilen
Die Zeilen in der Bankeinzahlung verwenden automatisch die Standarddimensionen, die Sie in den Feldern **Abteilungscode** und **Debitorengruppencode** angegeben haben. Wenn Sie **Debitor** oder **Kreditor** im Feld **Kontotyp** auswählen, ersetzen die für den Debitor oder Kreditor angegebenen Dimensionen die Standardwerte. Die Dimensionen in den Zeilen können bei Bedarf geändert werden.

> [!TIP]
> Dimensionen in Zeilen werden gemäß „Standarddimension Prioritäten“ festgelegt. Zeilendimensionen haben Vorrang vor Kopfzeilendimensionen. Um Konflikte zu vermeiden, können Sie Regeln erstellen, die die Verwendung einer Dimension in Abhängigkeit von der Quelle priorisieren. Wenn Sie die Priorisierung von Dimensionen ändern möchten, können Sie ihre Prioritäten auf der Seite **Standarddimensionsprioritäten** ändern. Weitere Informationen finden Sie unter [Prioritäten für Standarddimensionen einrichten](finance-dimensions.md#to-set-up-default-dimension-priorities).

## Bankeinzahlung erstellen
1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankeinzahlungen** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie **Neu** aus, um die Seite **Bankdepot** zu öffnen. 
3. Wählen Sie die Fibu Buch.-Blattvorlage aus, die Sie für Bankeinzahlungen erstellt haben.  

    > [!NOTE]
    > Wenn die Fibu Buch.-Blattvorlage mehr als einen Stapel enthält, werden Sie aufgefordert, einen auszuwählen.

4. Wählen Sie im Feld **Bankkontonr.** das Bankkonto aus, auf das Sie den Betrag einzahlen möchten.

    > [!TIP]
    > Sie können überprüfen, ob Sie die Einzahlung auf das richtige Konto erfolgt, indem Sie die Hauptbucheinträge für das ausgewählte Bankkonto mithilfe der Aktionen **Kontokarte** und **Bankposten** suchen. Zum Beispiel, um zu ermitteln, ob ähnliche Einzahlungen auf das Konto getätigt wurden.

5. Geben Sie im Feld **Einzahlungsgesamtbetrag** den Gesamtbetrag der Einzahlung ein. Diese Summe muss die Summe der Beträge aller Zeilen sein.
6. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    Das Datum im Feld **Buchungsdatum** und die Dimensionen in den Felder **Abteilungscode** und **Debitorengruppencode** werden den Zeilen zugewiesen, die Sie für die Bankeinzahlung erstellen. Diese können bei Bedarf geändert werden. 

7. Je nachdem, ob Sie das Bankguthaben pauschal oder jede Zeile einzeln ins Bank-/Sachkonto buchen möchten, aktivieren oder deaktivieren Sie den Umschalter **Als Abschlag buchen**. Die Standardeinstellung erfolgt über denselben Umschalter auf der Seite **Einkäufe und Verkäufe einrichten**.

    > [!NOTE]
    > Das Feld **Währungscode** zeigt die Währung an, die für das von Ihnen ausgewählte Bankkonto festgelegt ist. Sie können keine andere Währung auswählen.

8. Erstellen Sie im Inforegister **Zeilen** für jede Barzahlung, die Sie tätigen möchten, eine neue Zeile.
9. Geben Sie im Feld **Kontotyp** an, woher die Zahlung stammt. Für Bankeinzahlungen lautet der Typ in der Regel **Debitor** oder **Kreditor**. 

    > [!NOTE]
    > Sie können auch eine Barzahlung an einen Kreditor registrieren. Wählen Sie dazu **Kreditor** aus, und geben Sie dann den Zahlungsbetrag als negative Zahl im Feld **Habenbetrag** der Zeile ein. 

10. Geben Sie im Feld **Belegnr.** die Belegnummer der Rechnung ein, aus der der Habenbetrag stammt. Sie können für jede Zeile eine Belegnummer oder für alle Zeilen dieselbe Nummer verwenden.

    > [!TIP]
    > In der Regel müssen Sie das Feld **Belegtyp** für Finanzbuchungen nicht ausfüllen. Wenn Sie beispielsweise Bargeld aus einem Tagesverkauf einzahlen, lassen Sie das Feld leer. Wenn Sie Bargeld aus einer Debitorenzahlung einzahlen, wählen Sie **Zahlung** aus.

11. Wenn Sie eine Barzahlung für eine bestimmte Debitorenrechnung tätigen, wählen Sie die Aktion **Einträge anwenden** aus, und geben Sie dann im Feld **Ausgleichs-ID** die Rechnungsnummer ein. 
12. Wenn Sie bereit sind, die Bankeinzahlung zu buchen, wählen Sie die Aktion **Buchen** aus.

    > [!TIP]
    > Bevor Sie die Einzahlung buchen, können Sie die Aktion **Testbericht** verwenden, um Ihre Daten zu überprüfen. Der Bericht zeigt an, ob Probleme vorliegen, z. B. fehlende Daten, die eine Buchung verhindern.  

## Suchen gebuchter Bankeinzahlungen
Auf der Seite **Gebuchte Bankeinzahlungen** sind die bisherigen Einzahlungen Ihres Unternehmens aufgelistet. In der Liste können Sie die Kommentare und Dimensionen überprüfen, die für die Einzahlungen angegeben wurden. Sie können die Bankeinzahlung öffnen, um weitere Details anzuzeigen, und von dort aus weitere Untersuchungen durchführen. Sie können beispielsweise die Aktion „Posten suchen“ auswählen, um die gebuchten Bankposten anzuzeigen. Über den Bankposten können Sie den entsprechenden Hauptbucheintrag suchen.

Wenn Sie alle Hauptbucheinträge für die gebuchten Einzahlungszeilen suchen möchten, wechseln Sie zur Seite **Fibujournal**, und verwenden Sie die Aktion **Sachposten**. Dort finden Sie alle Sachposteneinträge, einschließlich der Einträge für Debitoren und Kreditoren.

## Stornieren einer gebuchten Bankeinzahlung
Um eine gebuchte Einzahlung zu stornieren, wechseln Sie zur Seite **Fibujournale**, suchen Sie das Journal für die Einzahlung, und wählen Sie dann die Aktion **Journal stornieren** aus.

> [!NOTE]
> Sie können nur ein Journal stornieren, das einen einzelnen Postentyp enthält. Das heißt, das Journal darf nur Debitorenposten oder Kreditorenposten enthalten, jedoch nicht beides. Wenn ein Journal beides enthält, müssen Sie die Einzahlung manuell stornieren.      

## Weitere Informationen
[Finanzen](finance.md)  
[Einrichten von Finanzen](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



