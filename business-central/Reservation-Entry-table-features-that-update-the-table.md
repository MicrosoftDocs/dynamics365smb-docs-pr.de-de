---
title: Tabelle „Reservierungseintrag“ – Features zum Aktualisieren der Tabelle „Reservierungseintrag“ | Microsoft Docs
description: Hier erhalten Sie Hinweise zum Verständnis und zur Behebung von Dateninkonsistenzproblemen in der Tabelle „Reservierungseintrag“.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Reservierungseintragstabelle – Einführung

Dieses technische Whitepaper bietet Anleitungen zum Verständnis und zur Behebung von Dateninkonsistenzproblemen in der Tabelle  *Reservierungseintrag*  (Tabelle 337) Microsoft Dynamics NAV. Der erste Teil ist eine Einführung in die Funktionen, die Daten in dieser Tabelle generieren oder ändern. Darüber hinaus werden mehrere Felder in der Tabelle  *Reservierungseintrag*  abgedeckt, die im Zusammenhang mit diesen Funktionen hervorzuheben sind. Der zweite Teil zeigt anhand von Beispielen, wie Einträge in der Tabelle  *Reservierungseintrag*  erzeugt, gelöscht oder geändert werden, wenn Transferaufträge verarbeitet oder Planungsfunktionen ausgeführt werden.

Die Tabelle  *Reservierungseintrag*  wird zum Verarbeiten und Speichern von Informationen zu Reservierungen, Artikelverfolgung und Auftragsverfolgung verwendet.

Bei der Handhabung der Artikelverfolgung mit Teilbuchung arbeitet die Tabelle mit der Tabelle  *Verfolgungsspezifikation*  (Tabelle 336) zusammen. Vom Benutzer auf der Seite  **Artikelverfolgungszeilen**  eingegebene Daten werden in einer temporären Version der Tabelle 336 erstellt und beim Schließen der Seite in Tabelle 337 und in die Tabelle mit den Verfolgungsspezifikationen übernommen.

Generell hängen die in der Tabelle  *Reservierungseintrag*  generierten Daten davon ab, welche Funktionen Sie verwenden und welche Parameter Sie für das Element Karte ausgewählt haben. Diese beinhalten:

- Richtlinie zur Auftragsverfolgung
- Reservierungsbedingungen
- Planungsfunktionen ausgeführt
- Nachbestellungs- und Fertigungspolitik
- Planungsparameter zum Artikel oder zur Lagereinheit Karte
- Artikelverfolgung

## Funktionen zum Aktualisieren der Reservierungseintragstabelle

### Richtlinie zur Auftragsverfolgung

Wenn das Feld  **Bestellverfolgungsrichtlinie** für einen Artikel auf Keine gesetzt ist, Microsoft Dynamics NAV werden nie Reservierungseinträge in der Tabelle  *Reservierungseintrag*  erstellt, es sei denn, der Änderungsplan oder Neuplan, die Reservierung oder die Artikelverfolgung wird ausgeführt. Darüber hinaus können Sie auch ohne aktivierte Auftragsverfolgung Reservierungseinträge haben, wenn Sie die Richtlinien „Auftragsfertigung“ oder „Auftragsmontage“ verwenden.

Sie können die  **Richtlinie zur Auftragsverfolgung**  auf „Keine“ setzen, wenn Sie keine sofortige Verfolgung einer Nachfrage im Hinblick auf ein Angebot oder umgekehrt benötigen. Die Nachverfolgung des Angebots im Hinblick auf die Nachfrage wird durch die Auftragsnachverfolgungsfunktion oder die Planungs-Engine übernommen. Wir empfehlen, die Auftragsverfolgung nicht zusammen mit der Planungsfunktion zu verwenden.

Wenn Sie das Feld  **Richtlinie zur Auftragsverfolgung**  auf „Nur Verfolgung“ setzen, Microsoft Dynamics NAV werden immer Einträge in Tabelle 337 erstellt, wenn für den Artikel eine Bestellung erstellt wird. Der  **Reservierungsstatus**  in Tabelle 337 ist jedoch nicht immer strikt auf „Verfolgung“ gesetzt. Stellen Sie sich folgendes Szenario vor:

> [!NOTE]  
> Das Arbeitsdatum ist für alle Beispiele auf den 23.01.2014 (TT.MM.JJJJ) festgelegt. 
  
1. Erstellen Sie einen Artikel, bei dem das Feld  **Bestellverfolgungsrichtlinie**  auf „Nur Sendungsverfolgung“ eingestellt ist.  
1. Erstellen Sie eine Bestellung. Microsoft Dynamics NAV erstellt einen Reservierungseintrag mit dem  **Reservierungsstatus** Überschuss, da der Einkaufsbestellung noch keine Nachfrage zugeordnet ist.
1. Erstellen Sie einen Auftrag. Microsoft Dynamics NAV erstellt jetzt einen weiteren Reservierungseintrag mit dem  **Reservierungsstatus** „Tracking“.

Der in Schritt 2 erstellte  **Reservierungsstatus** wird auf „Tracking“ aktualisiert; dies geschieht  Microsoft Dynamics NAV automatisch. Dieses Konzept wird dynamisches Tracking genannt.
Indem das Feld  **Bestellverfolgungsrichtlinie**  des Artikels auf „Nur Verfolgung“ gesetzt wird, kann ein Endbenutzer die Bestellverfolgungsfunktion nutzen, um sich einen Überblick darüber zu verschaffen, welchem Vorrat die Nachfrage zugeordnet ist und umgekehrt.

> [!NOTE]  
> Die Tracking-Funktionalität ersetzt nicht die Planungsfunktionalität, die alle Artikel, Bedarfe und Vorräte gemeinsam berücksichtigt, um optimale Planungsvorschläge zur Optimierung des Kundenservice und zum Ausgleich der Lagerbestände bereitzustellen.

### Reservierungsbedingungen

Eine Reservierung besteht aus einem Datensatzpaar in der Tabelle  *Reservierungseintrag*  mit einem  **Reservierungsstatus** der Reservierung, die dieselbe Eintragsnummer haben. Bei einem Datensatz ist das positive Feld aktiviert und dieser verweist auf die Versorgung. Im anderen Datensatz ist das Feld  **Positiv**  nicht aktiviert und verweist auf die Nachfrage. Die Felder  **Quellentyp**,  **Quellen-Referenznr.** und  **Quellen-ID**  markieren die Reservierung verknüpfen zwischen Nachfrage und Angebot.

Die Information im Feld  **Quelltyp**  ist die Tabelle, auf die sich das Feld  **Reservierungseintragsnr.**  bezieht. Handelt es sich beispielsweise um einen (negativen) Bedarfseintrag, könnte es sich um die Tabelle  *Verkaufsauftrag*  (Tabelle 37) oder die  *Planungskomponente*  (Tabelle 99000829) handeln.

Das Feld  **Quell-ID**  enthält die ID des Dokuments in der Tabelle, auf die durch den Quelltyp verwiesen wird.

Die **Quellen-Referenz-Nr.** Enthält eine Referenznummer für die Zeile, die die Reservierung **Laufnr.**  bezieht sich auf. Wenn sich der Eintrag auf eine Verkaufs- oder Einkaufszeile, eine Journalzeile oder eine Anforderungszeile bezieht, werden die Informationen in diesem Feld aus dem **Linie Nr.** Feld Wenn es sich auf einen Eintrag in der Tabelle  *Artikelposten*  (Tabelle 32) bezieht, werden die Informationen in diesem Feld aus dem Feld  **Postennr.**  der Tabelle  *Artikelposten*  kopiert.

Wenn Sie die Reservierungsrichtlinienoption „Immer“ in Kombination mit der Auftragsverfolgung verwenden, sind beide normalerweise synchron. Wenn jedoch die Reservierung entfernt wird oder das Eingangsdatum der Lieferung über das Bedarfsfälligkeitsdatum hinaus verschoben wird, wird die Auftragsverfolgung entfernt. Möglicherweise wird auch eine Fehlermeldung angezeigt, in der Microsoft Dynamics NAV gefragt wird, was mit bestehenden Reservierungen geschehen soll. Dieses Szenario wird im folgenden Beispiel veranschaulicht:

1. Erstellen Sie ein neues Element mit dem Namen COMP. Legen Sie die folgenden Felder fest:
  - **Nachschubsystem**: Einkauf
  - **Richtlinie zur Auftragsverfolgung**: Nur Sendungsverfolgung
  - **Reservieren**: Immer
2. Erstellen Sie ein zweites Element namens FG. Legen Sie die folgenden Felder fest:
  - **Nachschubsystem**: Produktionsauftrag
  - **Richtlinie zur Auftragsverfolgung**: Nur Sendungsverfolgung
  - **Reservieren**: Immer
3. Erstellen Sie ein zweites Element namens FG. Legen Sie die folgenden Felder fest:
  - **Artikel**: COMP
  - **Menge pro**: 1
4. Zertifizieren Sie die Produktionsstücklistennummer BOM FG und ordnen Sie sie dem Artikel FG zu.
5. Erstellen Sie eine Bestellung. Legen Sie die folgenden Felder fest:
  - **Artikel**: COMP
  - **Menge**: 10
  - **Standortcode**: BLAU
  - **Voraussichtliches Eingangsdatum**: 24.01.2014
6. Erstellen Sie einen Auftrag. Legen Sie die folgenden Felder fest:
  - **Versanddatum**: 14.02.2014
  - **Standortcode**: BLAU
  - **Artikel**: COMP
  - **Menge**: 10

> [!NOTE]  
> Zwischen Einkaufs- und Verkaufsauftrag wurde eine automatische Reservierung durchgeführt. Darüber hinaus wurde eine Auftragsverfolgung zwischen Einkaufs- und Verkaufsaufträgen erstellt.

7. Erstellen Sie einen manuell freigegebenen Produktionsauftrag. Legen Sie die folgenden Felder fest:
  - **Artikel**: 14.02.2014
  - **Menge**: 10
  - **Standort**: BLAU
  - **Fälligkeitsdatum**: 01.02.2014
8. Wählen Sie auf der Registerkarte  **Startseite**  in der Gruppe „Prozess“ die Option  **Produktionsauftrag aktualisieren**.
9. Öffnen Sie die Komponentenliste und suchen Sie nach dem Artikel COMP.

> [!NOTE]  
> Es wird keine Reservierung oder Auftragsverfolgung durch Microsoft Dynamics NAV erstellt. Der Grund dafür ist, dass für den in Schritt 6 erstellten Verkaufsauftrag bereits eine Reservierung vorliegt.

Angenommen, der Artikel wird aus geschäftlichen Gründen für den in Schritt 7 erstellten freigegebenen Fertigungsauftrag dringender benötigt. Als nächstes Abbrechen wir in den folgenden Schritten die Reservierung aus dem in Schritt 6 erstellten Verkaufsauftrag und beachten, wie die Auftragsverfolgung gehandhabt wird.

10. Suchen Sie den Verkaufsauftrag für Artikel COMP aus Schritt 6 und Abbrechen der Reservierung.
11. Öffnen Sie die Bestellung aus Schritt 5 und beachten Sie, dass jetzt eine Auftragsverfolgung zwischen der Bestellung und der aus dem freigegebenen Fertigungsauftrag benötigten Komponente erstellt wird.
12. Erstellen Sie die Reservierung zwischen der benötigten Komponente aus dem freigegebenen Fertigungsauftrag und der Lieferung aus der Bestellung in Schritt 5 neu.

> [!NOTE]  
> Die Reservierung wird nicht neu erstellt und muss manuell Fertig werden.

13. Ändern Sie das Feld  **Voraussichtliches Eingangsdatum**  im Kopf der Bestellung unter Schritt 5 vom 24.01.2014 in den 05.02.2014.

Microsoft Dynamics NAV wird die folgende Warnmeldung angezeigt:

   Für diese Bestellung bestehen Reservierungen. Diese Reservierungen werden storniert, wenn durch diese Änderung ein Datenkonflikt entsteht. Möchten Sie fortfahren?

14. Wählen Sie Ja. Suchen Sie in der Bestellung nach Reservierungs- und Auftragsverfolgungseinträgen.

> [!NOTE]  
> Die bestehende Reservierung wird storniert und muss manuell neu erstellt werden. Der Auftrag ist jedoch dynamisch und wurde neu erstellt, um zwischen der Einkaufsbestellung und dem Verkaufsauftrag zu bestehen. Microsoft Dynamics NAV  Der Grund hierfür ist, dass der Bedarf des freigegebenen Fertigungsauftrags (01.02.2014) vor dem voraussichtlichen Liefertermin liegt.

Damit ist die Demonstration des Zusammenspiels zwischen der Nutzung automatischer Reservierungen und der Auftragsverfolgung abgeschlossen. Die Beispiele zeigen auch, was passiert, wenn Sie Fälligkeitsdaten ändern, und welche Fehlermeldung bei einem Reservierungskonflikt ausgelöst wird.

### Planung berechnet

Bei der Planung Fertig mithilfe der Auftragsplanung, des Anforderungsarbeitsblatts oder des Planungsarbeitsblatts werden Einträge in der Tabelle  *Reservierungseintrag*  generiert, wobei das Feld  **Reservierungsstatus**  auf Verfolgung, Reservierung oder Überschuss gesetzt ist. Es sollte immer ein passendes Paar mit derselben Eintragsnummer aus positivem und negativem Wert im Feld  **Menge (Basis)**  vorhanden sein, wenn der Status „Verfolgung“ oder „Reservierung“ lautet. Das Feld  **Quelltyp**  entspricht dem Bedarfstyp, also Tabelle 37 für die negative Menge und einer Planungstabelle, z. B. Tabelle 246, für die positive Menge. Das Feld  **Quell-ID**  lautet PLANNING.

Im Falle eines nicht zugewiesenen Angebots oder Bedarfs wird das Feld  Microsoft Dynamics NAV Reservierungsstatus **auf „Überschuss“ gesetzt.**  Beispielsweise kann der Reservierungsstatus „Überschuss“ festgelegt werden, wenn der vorhandene Lagerbestand unter der Sicherheitsbestandsmenge liegt oder die Nachfrage mit der Prognose verknüpft ist.

Die Tabelle  *Nicht verfolgte Planungselemente*  (Tabelle 99000855) enthält Informationen zu nicht verfolgten Mengen, die angezeigt werden, wenn der Benutzer auf der Seite zur Auftragsverfolgung eine Suche durchführt, um nicht verfolgte Mengen anzuzeigen, oder ein Warnsymbol im Planungsarbeitsblatt auswählt. Die Tabelle enthält Einträge, die eine nicht verfolgte Überschussmenge im Auftragstrackingnetzwerk berücksichtigen.

Diese Posten werden während der Planung erzeugt und zeigen die Herkunft der Überschussmenge ohne Bedarfsverursacher in den Bedarfsverursacherzeilen. Die folgende Herkunft ist für den Überschuss ohne Bedarfsverursacher möglich:

- Absatzplanung
- Rahmenbestellungen
- Sicherheitsbestand
- Minimalbestand
- Maximalbestand
- Bestellmenge
- Maximale Losgröße
- Minimale Losgröße
- Losgrößenrundungsfaktor
- Toleranz (% der Losgröße)

In der Tabelle  *Reservierungseintrag*  gibt es ebenso wie bei Einkaufs-, Umlagerungs- und Produktionsaufträgen ein Feld  **Planungsflexibilität** . Dieses Optionsfeld definiert, ob der durch diese Beschaffungsaufträge dargestellte Vorrat beim Berechnen von Aktionsmeldungen vom Planungssystem berücksichtigt wird. Wenn das Feld die Option „Unbegrenzt“ enthält, berücksichtigt das Planungssystem die Zeile bei der Berechnung von Aktionsmeldungen. Wenn das Feld die Option „Keine“ enthält, ist die Zeile fest und unveränderlich, und das Planungssystem berücksichtigt die Zeile bei der Berechnung von Aktionsmeldungen nicht. Die Funktion wird in der Tabelle  *Reservierungseintrag*  über das gleichnamige Feld verwaltet.

### Nachbestellungs- und Fertigungspolitik

Wenn eine Planungsfunktion für einen Artikelsatz ausgeführt wird, bei dem die Nachbestellrichtlinie auf „Bestellung“ eingestellt ist, Microsoft Dynamics NAV werden in der Tabelle *Reservierungseintrag* Einträge mit dem Reservierungsstatus vom Typ „Reservierung“ statt „Verfolgung“ erstellt.

Die Felder  **Quelltyp**  und  **Quell-ID**  werden wie andere Neuordnungsrichtlinien behandelt. Allerdings wird im Feld  **Bindung**  in der Tabelle  *Reservierungseintrag* „Order-to-Order“ eingetragen. Microsoft Dynamics NAV 

Das Feld  **Bindung**  wird ausgefüllt, um Beschaffungsaufträge zu steuern, die an einen bestimmten Bedarf gebunden sind, beispielsweise Fertigungsaufträge, die direkt aus einem Verkaufsauftrag erstellt werden. Das Feld zeigt „Auftrag-zu-Auftrag“ an, wenn der Eintrag speziell an eine Nachfrage oder ein Angebot gebunden ist (Automatische Reservierung). Die Nachfrage kann sich auf den Umsatz oder den Bedarf an Komponenten beziehen.

### Artikelverfolgung und Interessentenreservierungserfassung

Der Reservierungsstatus des potenziellen Kunden kann  Microsoft Dynamics NAV in der Tabelle  *Reservierungseintrag*  erstellt werden, wenn Sie keine Auftragsnetzwerkeinheiten verwenden, d. h. keine Auftragsverfolgung. Beispielsweise können Sie in einer Verbrauchserfassungszeile der Komponente eine Artikelverfolgung zuordnen. Wenn für den Artikel jedoch bereits eine Auftragsverfolgung durchgeführt wird, Microsoft Dynamics NAV können weitere Reservierungseinträge für potenzielle Kunden erstellt werden. Dies wird im BEISPIEL 2 zu Überweisungsaufträgen im zweiten Teil dieses Dokuments veranschaulicht.

Wenn Sie die Seite  **Artikelverfolgungszeilen**  anzeigen oder ändern, wird der gesamte Inhalt der Tabelle  *Sendungsverfolgungsspezifikation*  (Tabelle 336) und der Tabelle  *Reservierungseintrag*  in einer temporären Version der Tabelle 336 angezeigt. Dadurch ist sichergestellt, dass auf historische und aktive Artikelverfolgungsdaten als Einheit zugegriffen wird.

Reservierungen lassen sich in zwei Kategorien einteilen: Unspezifische Reservierungen, bei denen Chargen- und Seriennummern zum Zeitpunkt der Reservierung nicht angegeben werden, und Spezifische Reservierungen, bei denen Sie bestimmte Chargen- oder Seriennummern aus dem Lagerbestand reservieren.

Bei einer unspezifischen Reservierung ist das Feld  **Lot-Nr.** oder  **Seriennr.**  im Feld  **Eintragsnr.**  der Tabelle 337 leer und verweist auf die Nachfrage (z. B. den Verkauf). Aufgrund der Struktur der Reservierungslogik in  Microsoft Dynamics NAV müssen, wenn Sie eine unspezifische Reservierung für einen artikelverfolgten Artikel im Lager vornehmen,  Microsoft Dynamics NAV trotzdem Auswählen spezifische Artikelposten zum Reservieren vorhanden sein.

Da die Artikelposten die Artikelverfolgungsinformationen enthalten, reserviert die Reservierung indirekt bestimmte Chargen- oder Seriennummern, auch wenn der Benutzer dies nicht beabsichtigt hat. Beim Late Binding werden jedoch weiterhin Reservierungen für bestimmte Einträge vorgenommen, beim Posten wird dann jedoch ein Umordnungsmechanismus verwendet. Microsoft Dynamics NAV  Microsoft Dynamics NAV 

Weitere Informationen finden Sie in den  Microsoft Dynamics NAV technischen Whitepapers unter „Zusätzliche Ressourcen“ am Ende dieses Dokuments.

### Felder „Quellsubtyp“, „Unterdrückte Aktionsmeldung“, „Anpassung der Aktionsmeldung“ und „Stornierung nicht zulassen“

In diesem Abschnitt werden die Felder  **Quelluntertyp**,  **Unterdrückte Aktionsmeldung**,  **Anpassung der Aktionsmeldung** und  **Stornierung nicht zulassen**  in der Tabelle  *Reservierungseintrag*  beschrieben. Es werden Szenarien bereitgestellt, um die Verwendung der Felder  **Unterdrückte Aktionsmeldung**,  **Anpassung der Aktionsmeldung**  und  **Stornierung nicht zulassen**  zu demonstrieren. Das Feld  **Anpassung der Aktionsnachricht**  wird für die Auftragsverfolgungsrichtlinienfunktion „Sendungsverfolgung und Aktionsnachricht“ verwendet. Das Feld  **Stornierung nicht zulassen**  wird in  Microsoft Dynamics NAV 2013 für die Funktion „Assembly-to-Order“ verwendet.

#### Herkunftsunterart

Das Feld  **Quell-Subtyp**  gibt an, auf welchen Quell-Subtyp sich der Reservierungseintrag bezieht. Wenn sich der Eintrag auf eine Einkaufs- oder Verkaufszeile bezieht, wird das Feld aus dem Feld  **Dokumentenart**  in der Zeile kopiert. Wenn es sich auf eine Journalzeile bezieht, wird das Feld aus dem Feld  **Buchungsart**  in der Journalzeile kopiert.

#### Ereignismeldung unterdrückt

Das Feld  **Unterdrückte Aktionsmeldung**  zeichnet auf, wenn eine vorhandene Lieferung bereits teilweise verarbeitet wurde, z. B. wenn eine Einkaufsbestellung bereits teilweise eingegangen ist oder für einen Produktionsauftrag Verbrauchswerte gebucht wurden.

Wenn die Planung ausgeführt wird,  Microsoft Dynamics NAV markiert es dieses Feld und setzt das Feld  **Reservierungseintragsstatus**  auf *Überschuss8. Zur Veranschaulichung dient folgendes Beispiel:

1. Öffnen Sie Artikel 80001. Legen Sie die folgenden Felder fest:
  - **Nachbestellrichtlinie**: Lot für Lot
  - **Reservieren**: Optional
  - **Richtlinie zur Auftragsverfolgung**: Keine
2. Erstellen Sie einen Auftrag. Legen Sie die folgenden Felder fest:
  - **Artikel**: 80001
  - **Standort**: Leer/Keiner
  - **Menge**: 10
  - **Versanddatum**: 15.02.2014
3. Öffnen Sie die  **Anforderungsarbeitsblätter**  und führen Sie den Stapelverarbeitungsauftrag  **Plan berechnen**  für Artikel 80001 aus.
  - **Startdatum**: 23.01.2014
  - **Enddatum**: 01.03.2014
4. Es wird ein Planungsvorschlag gegeben, die Menge 10 mit einer neuen Bestellung und dem  **Fälligkeitsdatum** 15.02.2014 aufzufüllen.
5. Wählen Sie auf der Registerkarte  **Aktionen**  in der Gruppe Funktionen die Option  **Aktion ausführen** Nachricht aus, um eine Bestellung mit dem  **Voraussichtlichen Eingangsdatum** 15.02.2014 anzulegen.
6. Öffnen Sie die Bestellung von Schritt 5 und setzen Sie die  **Zu empfangende Menge**  auf 2 und buchen Sie nur den Empfang.
7. Öffnen Sie den Verkaufsauftrag von Schritt 2 und ändern Sie das  **Versanddatum** auf den 10.02.2014.
8. Öffnen Sie die  **Anforderungsarbeitsblätter**  und führen Sie  **Plan berechnen** für Artikel 80001 aus.
  - **Startdatum**: 23.01.2014
  - **Enddatum**: 01.03.2014
9. Es wird ein Planungsvorschlag gegeben, die Menge 8 mit einer neuen Bestellung und dem  **Fälligkeitsdatum** 02.10.2014 aufzufüllen.

Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung angezeigt.

Eintrag Nr. 28 in Tabelle 337 hat den Reservierungsstatus „Verfolgung“, um mit dem vorhandenen Bestand übereinzustimmen, der im Artikelposten 318 für 2 Einheiten erfasst ist, und mit der ausstehenden Nachfrage in der Verkaufsauftragstabelle 37. Der nachfolgende Eintrag Nr. 29 hat ebenfalls den Reservierungsstatus „Verfolgung“ und verknüpft die verbleibende Menge von 8 Einheiten zwischen dem Bedarf in der Verkaufsauftragstabelle 37 und dem vorgeschlagenen Angebot in der Anforderungszeilentabelle 246.

Eintrag Nr. 30 ist die vorhandene, teilweise empfangene Einkaufsbestellung mit der Menge 2. Dies führt dazu, dass das Feld  **Reservierungsstatus**  „Überschuss“ lautet und das Feld  Microsoft Dynamics NAV Menge (Basis) **auf** 8 *(Restbetrag) gesetzt wird. Zudem wird das Feld* Unterdrückte Aktionsmeldung **aktiviert.** 

#### Ereignismeldungsjustierung

Im Feld  **Aktionsnachrichtenanpassung**  wird die Änderung auf der Angebotsseite der Auftragsverfolgung angezeigt, die sich ergibt, wenn Sie die zugehörigen Aktionsnachrichten akzeptieren. Ein Wert wird hier nur dann angezeigt, wenn die Funktionen sowohl für die Auftragsverfolgung als auch für Aktionsmeldungen aktiv sind (Auftragsverfolgungsrichtlinie auf Verfolgung und Aktionsmeldung eingestellt). Der Wert wird basierend auf den Daten in der Tabelle  *Action Message Entry*  (Tabelle 99000849) berechnet. Zur Veranschaulichung dient folgendes Beispiel:
1. Öffnen Sie Punkt 80002. Legen Sie das folgende Feld fest:
 - **Richtlinie zur Auftragsverfolgung**: Sendungsverfolgung und Aktionsmeldung.
2. Erstellen Sie einen Auftrag. Legen Sie die folgenden Felder fest:
  - **Artikel**: 80002
  - **Standort**: BLAU
  - **Menge**: 100
3. Öffnen Sie die Seite  **Auftragsplanung**  und führen Sie den Stapelverarbeitungsauftrag  **Plan berechnen**  aus.
4. Auswählen den Verkaufsauftrag von Schritt 2 und führen Sie den Stapelverarbeitungsauftrag  **Aufträge erstellen**  aus.
5. Ändern Sie im Verkaufsauftrag von Schritt 2 das Feld  **Menge**  von 100 in 105.
Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung angezeigt.
6. Für Eintrag Nr. 34 ist das Feld  **Aktionsnachrichtenanpassung**  in Tabelle 337 für 5 Einheiten mit Reservierungsstatus „Überschuss“ aktiviert. Da der Verkaufsauftrag bei Schritt 5 erhöht wurde, Microsoft Dynamics NAV wurde diese Reservierung erstellt, da mehr Vorrat benötigt wird.
7. Öffnen Sie die Seite  **Planungsarbeitsblätter**  und wählen Sie auf der Registerkarte  **Start**  in der Gruppe  **Prozess**  die Option  **Aktionsmeldungen abrufen**. Microsoft Dynamics NAV schlägt vor, die Bestellmenge von 100 auf 105 zu erhöhen.

#### Keine Stornierung zulassen

Das Feld  **Stornierung nicht zulassen**  gibt an, dass der Reservierungseintrag den verknüpfen zwischen einer Verkaufsauftragszeile und einem Montageauftrag darstellt. Sie können diese Reservierung nicht löschen, da sie erforderlich ist, um die Synchronisierung beizubehalten, die bei der Zusammenstellung eines Artikels auf Bestellung erfolgt. Zur Veranschaulichung dient folgendes Beispiel:

1. Erstellen Sie eine Bestellung. Legen Sie die folgenden Felder fest:
  - **Basismaßeinheit**: STK
  - Alle standardmäßigen Buchungsgruppen
  - **Nachschubsystem**: Montage
  - **Montagerichtlinie**: Assemble-to-Order
  - **Richtlinie zur Auftragsverfolgung**: Nur Sendungsverfolgung
2. Erstellen Sie ein neues Element mit dem Namen „Assemble COMP“. Legen Sie die folgenden Felder fest:
  - **Basismaßeinheit**: STK
  - Alle standardmäßigen Buchungsgruppen
  - **Nachschubsystem**: Einkauf
  - **Richtlinie zur Auftragsverfolgung**: Nur Sendungsverfolgung
3. Öffnen Sie das Element „Assemble FG“, wählen Sie auf der Registerkarte  **Navigieren**  in der Gruppe  **Montage/Produktion**  die Option  **Montage** und anschließend  **Montage-Stückliste**. Legen Sie in der Montagestückliste die folgenden Felder fest:
  - **Typ**: Artikel
  - **Nr.**: COMP zusammenbauen
  - **Menge pro**: 1 Wählen Sie die Schaltfläche **OK** .
4. Öffnen Sie ein Artikeljournal und erhöhen Sie den Bestand von Assemble COMP auf die Menge 10 am Lagerplatz BLAU und buchen Sie die Journalzeile.
5. Erstellen Sie einen Auftrag. Legen Sie die folgenden Felder fest:
  - **Artikel**: FG zusammenbauen
  - **Standort**: BLAU
  - **Menge**: 1 Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung dargestellt.

Eintrag Nr. 82 weist den Reservierungsstatus „Überschuss“ auf, da 9 Einheiten der Assembler-Komponente auf Lager sind und kein Bedarf besteht. Bei Eintrag Nr. 84 handelt es sich um Reservierungseinträge, die die Nachfrage in Tabelle 901 des  *Fließbands*  verfolgen, und deren Lieferung im Artikelposten 346.

Eintrag Nr. 86 enthält eine verbindliche Bestellung mit Reservierungsstatus „Reservierung“. Darüber hinaus ist das Feld  **Stornierung nicht zulassen**  aktiviert, da die Montagerichtlinie für den Artikel „Montage FG“ auf „Auftragsmontage“ eingestellt ist. Schließlich wird das Feld  **Planungsflexibilität**  auf Keine gesetzt, da Microsoft Dynamics NAV die Planungslogik das Löschen der Reservierung nicht zulässt.

#### Verfügbare Menge zum Kommissionieren und Reservierungen

Das Feld  **Reservierte Kommissionier- und Versandmenge**  in Tabelle 337, das in Versionen vor  Microsoft Dynamics NAV 2013 vorhanden ist, steuert die Artikelverfügbarkeit in einem verwalteten Lager. In jeder Installation der Lagerverwaltung sind Artikelmengen sowohl als Lagereinträge als auch als Artikelposten vorhanden. Microsoft Dynamics NAV  Diese beiden Eintragsarten enthalten unterschiedliche Informationen darüber, wo Artikel vorhanden sind und ob diese verfügbar sind. Lagerplatzposten definieren die Verfügbarkeit eines Artikels nach Lagerplatz und Lagerplatzart, was als Lagerplatzinhalt bezeichnet wird. Artikelposten definieren die Verfügbarkeit eines Artikels durch ihre Reservierung auf ausgehenden Belegen. Im Kommissionierungsalgorithmus gibt es eine spezielle Funktion zum Berechnen der Menge, die zur Kommissionierung verfügbar ist, wenn der Behälterinhalt mit Reservierungen gekoppelt ist. Der Kommissionierungsalgorithmus subtrahiert Mengen, die für andere ausgehende Dokumente reserviert sind, Mengen auf vorhandenen Kommissionierungsdokumenten und Mengen, die kommissioniert, aber noch nicht versendet oder verbraucht wurden. Das Ergebnis wird im Feld  **Zur Kommissionierung verfügbare Menge**  auf der Seite  **Kommissionierarbeitsblatt**  angezeigt, wo das Feld dynamisch berechnet wird. Der Wert wird auch berechnet, wenn ein Benutzer Lagerentnahmen direkt aus ausgehenden Dokumenten wie Verkaufsaufträgen, Produktionsverbrauch oder ausgehenden Übertragungen erstellt.

*Zum Kommissionieren verfügbare Menge = Menge in Kommissionierbehältern – Menge bei Kommissionierungen und Bewegungen – (reservierte Menge in Kommissionierbehältern + reservierte Menge bei Kommissionierungen und Bewegungen).*

Das folgende Beispiel veranschaulicht, wie der Wert in der zur Kommissionierung verfügbaren Menge in  Microsoft Dynamics NAV berechnet wird:

1. Erstellen Sie einen neuen Artikel mit dem Namen „Lagerartikel“. Legen Sie die folgenden Felder fest:
  - **Basismaßeinheit**: STK
  - Alle standardmäßigen Buchungsgruppen
  - **Nachschubsystem**: Einkauf
  - **Reserverichtlinie**: Immer
  - **Richtlinie zur Auftragsverfolgung**: Nur Sendungsverfolgung
2. Erstellen Sie eine Bestellung für den Lieferanten 60000. Legen Sie die folgenden Felder fest:
  - **Artikel**: Lagerartikel
  - **Standort**: WEISS
  - **Menge**: 100
3. Geben Sie die Bestellung frei und erstellen Sie den Lagereingang.
4. Buchen Sie den Lagereingang und registrieren Sie die Einlagerung für die Menge 100.
5. Erstellen Sie eine zweite Bestellung für Lieferant 60000. Legen Sie die folgenden Felder fest:
  - **Artikel**: Lagerartikel
  - **Standort**: WEISS
  - **Menge**: 10
6. Geben Sie die Bestellung frei und erstellen Sie den Lagereingang.
7. Buchen Sie NUR den Lagerschein. Erfassen Sie die Lagereinlagerung nicht.
8. Erstellen Sie einen Auftrag. Legen Sie die folgenden Felder fest:
  - **Artikel**: Lagerartikel
  - **Standort**: WEISS
  - **Menge**: 10. Die reservierte Menge wird automatisch auf 10 festgelegt, da die Reserverichtlinie auf „Immer“ eingestellt ist.
9. Erstellen Sie einen Auftrag. Legen Sie die folgenden Felder fest:
  - **Artikel**: Lagerartikel
  - **Standort**: WEISS
  - **Menge**: 100. Die reservierte Menge wird automatisch auf 100 gesetzt, da die Reserverichtlinie auf „Immer“ eingestellt ist.
10. Geben Sie den ersten Verkaufsauftrag von Schritt 8 frei und erstellen Sie einen Lagerversand.
11. Geben Sie den Lagerversand frei und wählen Sie auf der Registerkarte  **Aktionen** die Option  **Kommissionierung erstellen**.
Die folgende Fehlermeldung wird angezeigt: *Nichts zu verarbeiten.*
  Der Grund dafür ist, dass die zum Kommissionieren verfügbare Menge Null ist. Dies wird wie folgt berechnet: Lagerbestand = 110 Verfügbare Menge zur Kommissionierung = 100

> [!NOTE]  
> Die Menge im Einlagerungs- oder Empfangsbehälter ist nicht zur Kommissionierung verfügbar.
   
   Die für Verkaufsaufträge reservierte Gesamtmenge beträgt 110. Zur Kommissionierung verfügbare Menge = 100 – 110 = null.

Wenn die Lagereinlagerung in Schritt 7 registriert ist, ermöglicht dies die Erstellung der Lagerkommissionierung in Schritt 11. In Versionen vor  Microsoft Dynamics NAV 2013 wird das Feld „Reservierte  **Kommissionier- und Versandmenge** “ in Tabelle 337 mit der Reservierung für Menge 10 ausgefüllt.

Die folgende Abbildung stammt aus Microsoft Dynamics NAV 2009 R2.

## Abbildungen anhand von Transportaufträgen und Planung

### Umlagerungsaufträge

Wenn Sie Transferaufträge verwenden und der Artikel versendet, aber nicht vollständig empfangen wurde, erhalten Sie in der Tabelle  *Reservierungseintrag*  den Reservierungsstatus „Überschuss“. Der Standortcode ist der Transferzielort.

Die **Quellen-Referenz-Nr.** Das Feld wird aus der letzten Zeileneintragsnummer + der Zeileneintragsnummer des Artikels in der gebuchten Transferlieferung berechnet.

Wenn die Auftragsverfolgung aktiviert ist und kein Bedarf (Verkaufsauftrag oder Verbrauch) vorliegt, Microsoft Dynamics NAV werden in Tabelle 337 zwei Einträge mit dem Reservierungsstatus „Überschuss“ erstellt. Einer bezieht sich auf die  *Transferzeile* Tabelle 5741 und der andere auf die Artikelpostentabelle 32.

Dies wird im ersten Beispiel demonstriert.

#### Beispiel 1

1. Öffnen Sie die Artikel 80003 und 80004 und setzen Sie das Feld  **Tracking-Richtlinie**  auf  *Nur Tracking*. Belassen Sie die anderen Felder in der Standardeinstellung.
2. Öffnen Sie ein Artikeljournal, erhöhen Sie den Bestand dieser Artikel auf jeweils 10 am Lagerplatz ROT und buchen Sie die Journalzeilen.
3. Erstellen Sie einen Transferauftrag vom Standort ROT nach BLAU für diese beiden Artikel: Artikel 80003 in Transferauftragszeile 10000 und Artikel 80004 in der zweiten Zeile 20000, beide für 10 Einheiten.
4. Buchen Sie nur den Versandteil des Transportauftrags ohne Lagerfunktionen.
In der nachfolgenden Abbildung ist die gebuchte Transfersendung dargestellt.
Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung angezeigt.
5. Vergleichen Sie die Ergebnisse der gebuchten Transfersendung mit den Einträgen in Tabelle 337.

In der folgenden Tabelle wird beschrieben, was in bestimmten Feldern gegenüber dem Reservierungseintrag 40 geschieht.

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Reservierungsstatus**|Überschuss, da Artikel 80003 mit Auftragsverfolgung eingerichtet ist, aber kein Bedarf besteht.|  
|**Lagerortcode**|Überweisung an Codestelle BLAU.|  
|**Herkunftsart**|Transferlinientabelle 5741.|  
|**Quell-ID**|Belegnummer des Überweisungsauftrags: 1011.|
|**Quelle Ref.-Nr.**|Gesamtzahl der Zeilen 20000 + Zeilennr. 10000 gegen Artikel 80003 = 30000.|

Die Erklärung für die folgenden Felder im Reservierungseintrag 43 lautet wie folgt.

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Reservierungsstatus**|Überschuss, da Artikel 80003 mit Auftragsverfolgung eingerichtet ist, aber kein Bedarf besteht.|  
|**Lagerortcode**|Der Transportort EIGENES LOG ist der Ort, an dem sich der Artikel befindet.|  
|**Herkunftsart**|Artikelpostentabelle 32.|  
|**Quelle Ref.-Nr.**|Der offene Artikelposten Nummer 322.|

#### Beispiel 2

Das nächste Beispiel veranschaulicht, was passiert, wenn eine Komponente zwischen Standorten übertragen wird, gleichzeitig aber zwischen Bedarf und verfügbarem Angebot überwacht wird. Dabei werden die Komponenten vom Standort ROT nach BLAU transferiert und im Rahmen eines freigegebenen Fertigungsauftrags verbraucht. Die Komponente verwendet Auftragsverfolgung, Auftragsplanung und Artikelverfolgung.

Das Beispiel hebt den erkannten Fluss in Tabelle 337 in Bezug auf die Felder  **Reservierungsstatus**,  **Standortcode**,  **Quelltyp**,  **Quell-ID**,  **Quell-Referenznummer** und Art der  **Bindung** hervor.

1. Setzen Sie auf der Seite  **Fertigungseinrichtung**  das Feld  **Komponenten am Standort**  auf ROT.
2. Erstellen Sie eine neue Artikelkomponente. Legen Sie die folgenden Felder fest:
  - **Basismaßeinheit**: STK
  - Alle standardmäßigen Buchungsgruppen
  - **Nachschubsystem**: Einkauf
  - **Fertigungsrichtlinie**: Lagerfertigung
  - **Richtlinie zur Auftragsverfolgung**: Nur Sendungsverfolgung
  - **Artikelverfolgungscode**: LOTALL
3. Erhöhen Sie mithilfe des Artikeljournals den Bestand für die Artikelkomponente am Standort ROT auf 100 Einheiten. Legen Sie die folgenden Chargennummern fest:
  - Losnummer Los A, Menge 30
  - Losnummer Los B, Menge 70
4. Ein neues Produkt erstellen. Legen Sie die folgenden Felder fest:
  - **Basismaßeinheit**: STK
  - Alle standardmäßigen Buchungsgruppen
  - **Nachschubsystem**: Produktion
  - **Fertigungsrichtlinie**: Lagerfertigung
  - **Richtlinie zur Auftragsverfolgung**: Nur Sendungsverfolgung
5. Erstellen Sie eine **Produktionsstückliste** mit 1 Menge pro Artikelkomponente.
6. Ordnen Sie die Produktionsstückliste dem produzierten Artikel zu.
7. Erstellen Sie einen Auftrag. Legen Sie die folgenden Felder fest:
  - **Artikel**: Produziert
  - **Standort**: BLAU
  - **Menge**: 100
8. Wählen Sie auf der Registerkarte  **Aktionen**  des Verkaufsauftrags in der Gruppe  **Planen** die Option  **Planung**  aus, um einen verknüpften freigegebenen Fertigungsauftrag für den Verkaufsauftrag zu erstellen.
9. Öffnen Sie den freigegebenen Fertigungsauftrag/Komponentenbedarf und beachten Sie, dass der Standort auf ROT eingestellt ist.
Der Grund hierfür ist, dass die Option  **Komponenten am Standort**  im  **Fertigungs-Setup** Karte ROT ist.
Der produzierte Artikel wird am Standort BLAU ausgegeben.

Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung angezeigt.

##### Reservierungseinträge mit den Nummern 55 und 56

Für den Komponentenbedarf für Los A bzw. Los B werden Auftragstrackingverknüpfungen vom Bedarf in Tabelle 5407 (Fertigungsauftragskomponente) zum Vorrat in Tabelle 32 (Artikelposten) erstellt. Der **Reservierungsstatus**  Das Feld enthält Tracking für alle vier Einträge, um anzuzeigen, dass diese dynamische Auftragsverfolgung zwischen Angebot und Nachfrage verknüpft ist.

Der Bedarf in Tabelle 5407 (Fertigungsauftragskomponente) ist mit der Quell-ID des freigegebenen Fertigungsauftrags 101006 verknüpft. Die Versorgung in Tabelle 32, Artikelposten, ist mit der Quellenreferenznummer verknüpft. Dabei handelt es sich um die Artikelpostennummern 325 und 326, unter denen die Einheiten vorhanden sind.

> [!NOTE]  
> Das Feld **Chargennr.** ist auf den Bedarfszeilen leer, da die Chargennummern nicht auf den Komponentenzeilen des freigegebenen Fertigungsauftrags angegeben sind.

##### Reservierungseintrag mit Nummer 57

Aus dem Verkaufsbedarf in Tabelle 37 (Verkaufszeile) wird eine Auftragsverfolgung verknüpfen für den Vorrat in Tabelle 5406 (Produktionsauftragszeile) erstellt. Das Feld  **Reservierungsstatus**  enthält „Reservierung“ und das Feld  **Verbindlich**  enthält „Bestellung-zu-Bestellung“. Dies liegt daran, dass der freigegebene Fertigungsauftrag speziell für den Verkaufsauftrag generiert wurde und verknüpft bleiben muss, im Gegensatz zu Auftragstrackingverknüpfungen mit dem Reservierungsstatus „Tracking“, die dynamisch erstellt und geändert werden.

> [!NOTE]  
> Das Feld  **Verbindlich**  kann auch  *Auftragsfertigung*  enthalten, wenn „Auftragsfertigung“ als Fertigungsrichtlinie und/oder „Bestellung“ als Nachbestellrichtlinie verwendet wird.

10. An dieser Stelle im Szenario zeigen werden die 100 Einheiten der Komponente mithilfe eines Transferauftrags vom ROTEN Standort zum BLAUEN Standort übertragen.

Auswählen Los A und Los B für die Sendung.

Buchen Sie die gesamte ausstehende Menge NUR als „Gesendet“.

> [!NOTE]  
> Am Standort ROT können Komponenten verbraucht werden, für das Beispiel zur Veranschaulichung des Ablaufs von Reservierungseinträgen werden die Einheiten jedoch manuell an den Standort BLAU übertragen.

Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung dargestellt.

##### Reservierungseinträge mit den Nummern 55 und 56

Die Auftragsverfolgungseinträge für die beiden Chargen der Komponente, die den Bedarf in Tabelle 5407 widerspiegeln, werden vom Reservierungsstatus „Verfolgung“ in „Überschuss“ geändert. Der Grund besteht darin, dass Vorräte, mit denen vorher eine Verknüpfung hergestellt wurde (in Tabelle 32), von der Lieferung des Umlagerungsauftrags verwendet wurden. Echter Überschuss, wie in diesem Fall, spiegelt überschüssigen Vorrat oder Bedarf wider, der nicht nachverfolgt wird. Es handelt sich um einen Hinweis auf ein Ungleichgewicht im Auftragsnetzwerk, das, sofern es nicht dynamisch behoben wird, eine Aktionsmeldung durch das Planungssystem generiert.

##### Reservierungseintragsnummern 59 bis 63

Da die beiden Chargen der Komponente im Umlagerungsauftrag als geliefert, aber nicht als empfangen gebucht sind, weisen alle zugehörigen positiven Auftragstrackingeinträge den Reservierungstyp „Überschuss“ auf, was bedeutet, dass sie keinen Bedarfen zugeordnet sind. Für jede Chargennummer bezieht sich ein Eintrag auf die Tabelle 5741 (Transferzeile) und ein Eintrag auf den Artikelposten am Transportort, an dem sich die Artikel jetzt befinden.

Tabelle 5741,  **Übertragungszeile**, ist der Quelltyp. **Quell-ID** ist die Transferauftragsbelegnummer 1012 und **Quell-Referenznummer.** Beträgt 20000 = 10000 + 10000, wie in Beispiel 1 beschrieben. Der Standort ist für den Transferortcode auf BLAU eingestellt.

Die verbleibenden zwei Einträge mit  **Reservierungsstatus** Überschuss haben Tabelle 32,  **Artikelposten**, als Quelltyp und  **Quellreferenznr.** 328 und 330, einschließlich ihrer Chargennummern, die sich derzeit am Transitort OUT LOG befinden.

11. Buchen Sie den ausstehenden Überweisungsauftrag als „Empfangen“.

Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung dargestellt.

Die Auftragsverfolgungseinträge ähneln jetzt den ersten zeigen im Szenario, bevor der Transferauftrag nur als „Versendet“ gebucht wurde, außer dass die Einträge für die Komponente jetzt den Reservierungsstatus „Überschuss“ anstelle von „Verfolgung“ haben. Dies liegt daran, dass der Komponentenbedarf immer noch am Standort ROT liegt, was sich darin widerspiegelt, dass das Feld  **Standortcode**  in der Komponentenzeile des Fertigungsauftrags ROT enthält, wie im Einrichtungsfeld  **Komponenten am Standort**  festgelegt.

Der Vorrat, der diesem Bedarf zuvor zugewiesen wurde, wurde an den BLAUEN Standort übertragen und kann jetzt nicht vollständig nachverfolgt werden, es sei denn, der Komponentenbedarf in der Fertigungsauftragszeile wird auf den BLAUEN Standort geändert. Dies wird in den letzten beiden Reservierungseinträgen mit den ausgefüllten Losnummern aufgezeichnet, wobei das Feld  **Quellentyp** Tabelle 32 ist und die  **Quellen-Referenznr.** Das Feld sind die Artikelposten 333 und 334.

12. Ändern Sie in der dem freigegebenen Fertigungsauftrag zugeordneten Komponentenliste den Standort für die Komponente auf BLAU.

12. Öffnen Sie das  **Verbrauchs Buch.-Blatt** und führen Sie die Stapelverarbeitung  **Verbrauch berechnen** aus.
Weisen Sie Los A die Menge 30 und Los B die Menge 70 zu.

Schließen Sie das Formular zur Artikelverfolgung.

Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung dargestellt.

##### Reservierungseinträge mit den Nummern 68 und 69

Da der Komponentenbedarf auf den Lagerort BLAU geändert wurde und der Vorrat als Artikelposten am Lagerort BLAU verfügbar ist, werden nun alle Auftragstrackingeinträge für die beiden Chargennummern vollständig verfolgt, was durch den Reservierungsstatus von Tracking angezeigt wird. Die Chargennummern werden im Feld  **Chargennr.**  nicht gegenüber dem Bedarf in Tabelle 5406,  **Fertigungsauftragszeile** eingetragen, da wir im freigegebenen Fertigungsauftrag keine Chargennummern für die Komponente angegeben haben.

##### Reservierungseinträge mit den Nummern 70 und 71

Einträge mit Reservierungsstatus Interessent werden in Tabelle 337 erzeugt. Dies liegt daran, dass der Komponente im Verbrauchsjournal beide Chargennummern zugeordnet sind, das Journal jedoch nicht gebucht wurde.

Damit ist der Abschnitt abgeschlossen, in dem beschrieben wird, wie Auftragstrackingeinträge in der Tabelle  **Reservierungseintrag**  generiert, geändert und gelöscht werden, wenn mehrere Funktionen in Kombination mit Transferaufträgen verwendet werden.

### Planung berechnet

Bei Verwendung von Planungsfunktionen, d. h. des  **Anforderungsarbeitsblatts**, des  **Planungsarbeitsblatts** oder der  **Auftragsplanung**, können Reservierungseinträge in der  **Reservierungseintrag** Tabelle 337 je nach Planungsvorschlag der Logik in  Microsoft Dynamics NAV geändert oder hinzugefügt werden. Beispiel 3 verwendet **Nachbestellrichtlinie**  Bestellen Sie mit **Fertigungspolitik**  Einzelanfertigung für einen produzierten Artikel. Die Komponente verwendet **Nachbestellrichtlinie**  Feste Nachbestellmenge.

#### Beispiel 3

1. Im **Fertigungseinrichtung**  Karte, **Komponente am Standort**  ist ROT aus dem vorherigen Beispiel.
2. Erstellen Sie ein neues übergeordnetes Element-Element 70061. Legen Sie die folgenden Felder fest:
  - **Basismaßeinheit**: STK
  - Alle standardmäßigen Buchungsgruppen
  - **Nachschubsystem**: Produktionsauftrag
  - **Fertigungspolitik** : Auftragsfertigung
  - **Nachbestellrichtlinie** : Befehl
  - **Rücklagenpolitik** : Optional
  - **Sendungsverfolgung** : Keiner
3. Neues Komponentenelement 70062 erstellen. Legen Sie die folgenden Felder fest:
  - **Basismaßeinheit**: STK
  - Alle standardmäßigen Buchungsgruppen
  - **Nachschubsystem** : Kaufen
  - **Nachbestellrichtlinie** : Feste Nachbestellmenge
  - **Rücklagenpolitik** : Optional
  - **Richtlinie zur Auftragsverfolgung**: Keine
  - **Sicherheitsbestandsmenge**: 10
  - **Neu anordnen zeigen**: 25
  - **Nachbestellmenge**: 50
4. Erstellen Sie eine neue Produktionsstückliste und geben Sie das Komponentenelement 70062 mit der Menge pro 1 an.
Weisen Sie die Produktionsstückliste dem Artikel 70061 übergeordnetes Element zu.
5. Erstellen Sie einen Auftrag. Legen Sie die folgenden Felder fest:
  - **Artikel**: Feste Nachbestellmenge
  - **Standort**: ROT
  - **Menge**: 40
  - **Versanddatum**: 15.02.2014
6. Öffnen Sie die Seite  **Planungsarbeitsblätter**  und führen Sie den Stapelverarbeitungsauftrag  **Neuplan berechnen**  aus.
  - **MPS/MRP**: aktiviert
  - **Startdatum**: 23.01.2014
  - **Enddatum**: 01.03.2014
  - Filtern Sie nach Artikeln 70061 und 70062
  - Keine Vorhersage

Nachfolgend werden Planungsvorschläge gegeben.

Der erste Planungsvorschlag besteht darin, einen neuen geplanten Fertigungsauftrag zu erstellen, um den ausstehenden Bedarf des Verkaufsauftrags für Menge 40 des übergeordnetes Element-Artikels 70061 zu decken. Überprüfen Sie die Auftragsverfolgung und Microsoft Dynamics NAV sie zeigt Ihnen den ausstehenden Verkaufsauftrag. Die Auftragsverfolgung wird aktiviert, wenn sie von der Planungs-Engine generiert wird.

Die zweite Zeile soll den Lagerbestand über die Neuordnung zeigen (25) bringen. Unter Berücksichtigung der Nachbestellmenge (50) wird von der Planungslogik eine Menge von 50 Einheiten vorgeschlagen. Die dritte Zeile dient dazu, den Lagerbestand auf den Sicherheitsbestand (10) zu bringen.

Die vierte Zeile dient der Bestandsauffüllung, wenn der Verkaufsauftrag versandt wird. Zu diesem Zeitpunkt beträgt der Lagerbestand 20 und liegt somit unter der Nachbestellungsnummer zeigen. Als Ergebnis schlägt die Planungsmaschine vor, unter Berücksichtigung der Nachbestellmenge 50 zusätzliche Komponenten zu kaufen. Dies ist eine nicht nachverfolgte Menge, daher wird diese im  *Reservierungseintrag* Tabelle 337 mit dem Reservierungsstatus „Überschuss“ gekennzeichnet.

Die Statusinformationen in Tabelle 337 werden in der folgenden Abbildung dargestellt.

Das Feld  **Reservierungsstatus**  lautet „Reservierung“ und es wird eine Order-to-Order-Bindung erstellt. Der Grund hierfür liegt darin, dass die Artikelherstellungsrichtlinie auf „Auftragsfertigung“ lautet und die Nachbestellrichtlinie auf „Bestellung“ eingestellt ist. Wenn einer der beiden auf „Bestellung“ eingestellt ist, lautet der Reservierungsstatus „Reservierung“ statt „Verfolgung“ und die Bindung wird auf „Bestellung zu Bestellung“ eingestellt.

Der Bedarf von 40 Einheiten gegenüber dem Feld  **Quell-ID**  hat die Verkaufsauftragsnummer 1005 und der Quelltyp ist  *Verkaufszeile* Tabelle 37. Der Reservierungseintrag wird mit dem Planungsvorschlag, Quelle Ref.-Nr., abgeglichen. 10000, Quell-ID ist PLANUNG und Quelltyp ist  *Anforderungszeile* Tabelle 246. Es besteht also ein Gleichgewicht zwischen der Nachfrage aus dem Verkaufsauftrag und dem vom Planungsmodul vorgeschlagenen Angebot.

##### Reservierungseintragsnummern 73 und 74

Durch Ausführen des Stapelverarbeitungsauftrags „Plan berechnen“ werden die nächsten vier Einträge mit einem Reservierungsstatus „Verfolgung“ aufgrund der Einstellung der Nachbestellrichtlinie „Feste Nachbestellmenge“ für die Komponente generiert. Der Bedarf für das Bauteil 70062 wird durch die angegebenen Planungsvorschläge aufgefüllt, Bezugsquellen-Nr. 20000 und 30000, mit der Quell-ID „PLANUNG“ und dem Quelltyp aus der  *Anforderungszeile* Tabelle 246. Der Komponentenbedarf wird erstellt, um die Nachfrage nach dem Artikel 70061 übergeordnetes Element für die Gesamtmenge (Basis) 40 zu erfüllen. Als Ergebnis dieser Nachfrage hat das Feld  **Quell-Produktionsauftragszeile**  den Wert 10000, mit Quelltyp die  *Komponentenbedarf* Tabelle 99000829.

Der Reservierungsstatus ist nicht „Überschuss“, da eine Auftragsverfolgung zwischen der Nachfrage nach übergeordnetes Element Artikel 70061 und der Versorgung mit Komponentenartikel 70062 besteht.

##### Reservierungseintragsnummern 75 und 76

Die letzten beiden Einträge weisen den Reservierungsstatus „Überschuss“ auf, da es sich hierbei um nicht nachverfolgte Mengen handelt, die im Planungsarbeitsblatt in Bezug auf die Nachbestellparameter „Nachbestell-Nr. zeigen“ und „Nachbestellmenge“ generiert werden.

## Siehe auch  
[Designdetails: Artikelverfolgungsdesign](design-details-item-tracking-design.md)  
[Designdetails: Ausgleich von Nachfrage und Angebot](design-details-balancing-demand-and-supply.md)  
[Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]