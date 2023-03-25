---
title: 'Artikel in Lager umlagern, die gesteuerte Einlagerung und Kommissionierung verwenden'
description: 'In diesem Artikel wird erläutert, wie Sie Artikel an Lagerplätzen umlagern, die eine gesteuerte Einlagerung und Kommissionierung verwenden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
---

# Artikel in erweiterten Lagerkonfigurationen umlagern, die gesteuerte Einlagerung und Kommissionierung verwenden

Sie können Artikel ohne einen Bedarf aus einem Herkunftsbeleg zwischen Lagerplätzen umlagern. Beispielsweise möchten Sie dies möglicherweise im Rahmen der folgenden Aktivitäten tun:

* Reorganisieren Ihres Lagers.
* Artikel in einen Inspektionsbereich bringen.
* Entnehmen Sie Artikel vorübergehend aus den Kommissionierungslagerplätzen, um z. B. als Vorführartikel in einer Verkaufspräsentation zu dienen.
* Lagern Sie zusätzliche Artikel in den Produktionsbereich für Komponenten um, die mit einigen Buchungsmethoden konfiguriert wurden.
* Lagern Sie produzierte oder montierte Artikel aus dem Produktions- oder Montagebereich ins Lager um.
* Lagern Sie Artikel aus dem Massenlagerbereich in Lagerplätze um, die Sie für die Kommissionierung verwenden.

Wie Sie Artikel für die Produktion umlagern, hängt davon ab, wie Ihr Lagerort eingerichtet wurde. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).

In Lagerkonfigurationen, in denen der Schalter **Gezielte Kommissionierung und Einlagerung** für Lagerorte aktiviert ist, können Sie ungeplante Umlagerungen auf den folgenden Seiten registrieren:  

* Lagerplatzumlagerungsarbeitsblatt
* Lagerinterne Kommissionierung
* Lagerinterne Einlagerung
* Logistik Umlagerungs Buch.-Blatt

Die Seiten **Umlagerungsarbeitsblatt**, **Lagerinterne Kommissionierung** und **Lagerinterne Einlagerung** funktionieren auf die gleiche Weise. Verwenden Sie die Seiten, um Lageraktivitäten für Lagermitarbeiter vorzubereiten. Der Unterschied liegt in der erweiterten Funktionalität, die mit jeder Seite verbunden ist, und den verschiedenen Arten von Lageraktivitäten, die wahrscheinlich von verschiedenen Mitarbeitern durchgeführt werden:

* Mit dem Umlagerungsarbeitsblatt können Sie hochrangige Kommissionierungslagerplätze mit Artikeln aus anderen Lagerplätzen füllen
* Einlagerungen verwenden Einlagerungsvorlagen
* Kommissionierung verwendet die Lagerplatzränge und -verfügbarkeit

## Lagerplatzumlagerungsarbeitsblatt

### Um Artikel mit dem Lagerplatzumlagerungsarbeitsblatt umzulagern

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Arbeitsblatt für Lagerplatzumlagerungen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder in den Arbeitsblattzeilen manuell aus oder verwenden Sie eine der folgenden Aktionen, um die Zeilen automatisch auszufüllen:

    * **Lagerplatzinhalt holen** füllt die Arbeitsblattzeilen mit dem Inhalt des Lagerplatzes oder der Lagerplätze, die Sie festlegen.
    * **Lagerplatzauffüllung berechnen** verwendet die Lagerplatzprioritäten, um eine Auffüllung der Lagerplätze mit höheren Prioritäten aus denen mit niedrigeren Prioritäten vorzuschlagen.

    > [!NOTE]  
    > Wenn der Artikel die Kriterien in der folgenden Liste erfüllt, sind die Felder **Von Zone** und **Von Lagerplatz** leer. [!INCLUDE [prod_short](includes/prod_short.md)] berechnet, von wo die Artikel umgelagert werden sollen, nur wenn Sie die Aktion **Umlagerung erstellen** verwenden.  
    >  
    > * Der Artikel weist ein Ablaufdatum auf.  
    > * Der Schalter **Gemäß FEFO kommissionieren** ist für den Lagerort aktiviert.  
    > * Sie verwenden die Funktio **Lagerplatzauffüllung berechnen**.  

3. Wählen Sie die Aktion **Umlagerung erstellen**, um die Umlagerung zu erstellen. Sobald die Umlagerung fertig gestellt ist, können Sie sie registrieren.  

### So registrieren Sie die Lagerplatzumlagerung:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerplatzumlagerungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den Umlagerungsbeleg, um zu registrieren:  
3. Geben Sie in Zeilen **Bereich** an, wo, welche und bis wann der fragliche Artikel umgelagert wird, indem Sie Werte in den Feldern **Zonencode**, **Lagerplatzcode**, **Bewegungsmenge** oder **Fälligkeitsdatum** auswählen.  
4. Geben Sie in den Zeilen **Lagerentnahme** im Feld **Bewegungsmenge** die Menge des Lagerplatzinhalts ein, die Sie umlagern möchten. Sie können dieses Feld nur auf **Lagerentnahme**-Zeilen bearbeiten. 

    > [!NOTE]
    > Wenn Sie die Artikel für eine Zeile in mehr als einem Lagerplatz kommissionieren oder platzieren müssen, beispielsweise, da der freie Lagerplatz voll ist, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.
 
5. Um alle vorgeschlagenen Mengen zu registrieren, die im Feld **Menge** angegeben sind, wählen Sie die Aktion **Bewegungsmenge autom. ausfüllen** aus.  
6. Wählen Sie die Aktion **Registrieren** aus.  

> [!NOTE]  
> Für Lagerorte, die gesteuertes Einlagern und Kommissionieren verwenden, können Sie Artikel in Lagerplätzen des Typs **EINGANG** nicht manuell verschieben, da sie noch nicht als verfügbarer Bestand betrachtet werden. Sie müssen die Artikel in diesen Lagerplätzen einlagern, bevor sie für Umlagerungen verfügbar sind.

## Interne Kommissionierung  

### So erstellen Sie eine interne Kommissionierung  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Whse. Interne Kommissionierung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie die **Felder Nr.** Felder **Lagerortcode** und **Nach Lagerplatzcode** im Inforegister **Allgemein**. Das Feld **Nach Lagerplatzcode** legt den Lagerplatz fest, in dem Sie die entnommenen Artikel platzieren wollen. Für die Produktion wäre dieser Lagerplatz der Fertigungsbereitstellungslagerplatz oder der Off. Fert.-Ber.-Lagerplatz. Für andere Zwecke müssen Sie einen „Lagerplatzcode“ einer Lagerplatzart auswählen, die nicht für Kommissionierungen genutzt werden, am besten einen Warenausgangs-, Zwischen- oder Speziallagerplatz.  
4. Wählen Sie einen Artikel im Feld **Artikelnr.** und tragen Sie die Mengen ein, die Sie kommissionieren möchten.  
5. Wählen Sie die Aktion **Kommissionierung erstellen** aus. Jetzt ist eine Kommissionieranweisung fertig und kann von einem Lagermitarbeiter ausgeführt werden. Wählen Sie alternativ die Aktion **Freigeben** und erstellen Sie Warenkommissionierungen mit der Seite **Kommissionierungsarbeitsblatt**. Mehr über Kommissionierungsarbeitsblätter erfahren Sie unter [Kommissionierungsdokumente in großen Mengen mit dem Kommissionierungsarbeitsblatt erstellen](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Sobald die Kommissionierung fertig gestellt ist, können Sie sie registrieren.  

### So registrieren Sie die Warenkommissionierung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kommissionierungen** ein und wählen Sie dann den zugehörigen Link.  

    Um an einer bestimmten Kommissionierung zu arbeiten, wählen Sie die Kommissionierung in der Liste aus, oder filtern Sie die Liste, um die Kommissionierungen zu finden, die Ihnen zugeordnet wurden.  
2. Wenn das Feld **Zugewiesene Benutzer-ID** leer ist, geben Sie gegebenenfalls Ihre ID ein, um sich zu identifizieren.  
3. Kommissionieren Sie die Artikel.  

    Da das Lager mit gesteuerter Einlagerung und Kommissionierung eingerichtet wurde, bestimmen Lagerplatzränge die Lagerplätze für die Kommissionierung. Die Lagerplätze werden in den Kommissionierungszeilen vorgeschlagen. Die Anweisungen enthalten mindestens zwei separate Zeilen für jede der Aktionen Entnahme und Einlagerung.  

4. Nachdem Sie die Kommissionierung ausgeführt und die Artikel in den Ausgangsbereich oder den Ausgangslagerplatz eingelagert haben, wählen Sie die Aktionen **Kommissionierung registrieren** aus.  

## Interne Einlagerung  

### So erstellen Sie eine interne Einlag.-Anforderung  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerinterne Einlagerungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie die **Felder Nr.** und **Lagerortcode** aus.
4. Tragen Sie für jeden Artikel, der ins Lager eingelagert werden soll, eine Zeile ein. Die Felder **Artikelnummer** und **Menge** sind Pflichtfelder.

    > [!NOTE]  
    > Wenn Sie einen Artikel im Feld **Artikelnr.** auswählen, wird die Seite **Lagerplatzinhalte** anstelle der Seite **Artikel** angezeigt. Diese Seite wird geöffnet, da Sie einen Artikel einlagern, der einem bestimmten Lagerplatz zugewiesen ist – *Lagerplatzinhalt* – und nicht nur einen Artikel. Außerdem wissen Sie bereits, aus welchem Lagerplatz der Artikel entnommen werden soll. Wenn Sie das Feld **Von Lagerplatzcode** ausgefüllt haben, wird der Lagerplatzinhalt nach diesem Wert gefiltert.

5. Um die Zeilen mit dem gesamten oder dem gefilterten Inhalt der Lagerplätze des Lagerorts zu füllen, wählen Sie die Aktion **Lagerplatzinhalt abrufen** aus.  
6. Wählen Sie die Aktion **Einlagerung erstellen** aus. Jetzt ist eine Einlagerungsanweisung für einen Lagermitarbeiter fertig. Wählen Sie alternativ die Aktion **Freigeben**, um Wareneinlagerungen mit der Seite **Einlagerungsarbeitsblatt** zu erstellen. Mehr über Einlagerungsarbeitsblätter erfahren Sie unter [Einlagerungsbelege in großen Mengen mit dem Einlagerungsarbeitsblatt erstellen](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Sobald die Einlagerung fertig gestellt ist, können Sie sie registrieren.  

### So registrieren Sie eine Wareneinlagerung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einlagerungen** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Wareneinlagerung, die für die Bearbeitung bereit ist.  
3. Geben Sie bei Bedarf Ihre Benutzerkennung ein, wenn Sie mit der Arbeit an einer Einlagerung beginnen.  

    Um den Einlagerungsprozess zu optimieren, können Sie die Einlagerungspositionen nach verschiedenen Kriterien sortieren. Zum Beispiel nach Artikel, Regalnummer oder Fälligkeitsdatum.

    * Wenn die Zeilen der Art Entnahme und Einlagerung einer Wareneingangszeile nicht direkt aufeinander folgen, Sie dies aber wünschen, sortieren Sie die Zeilen, indem Sie **Artikel** im Feld **Sortiermethode** auswählen.  
    * Wenn die Lagerplatzränge das physische Layout des Lagers widerspiegeln, verwenden Sie die Sortiermethode **Lagerplatzrang**, um die Arbeit um die Lagerplatzlagerorte zu organisieren.  

4. Führen Sie die Einlagerung durch.

    Jede interne Einlagerungszeile ist zu mindestens zwei Zeilen in der Einlagerung geworden.  

    * Die erste Zeile mit dem Feld **Entnahme** im Feld **Aktionsart** zeigt an, wo sich die Artikel im Wareneingangsbereich befinden. Sie können die Zone und den Lagerplatz in dieser Zeile nicht ändern.  
    * Die nächste Zeile, mit **Einlagerung** im Feld **Aktionsart** zeigt an, wo die Artikel im Lager eingelagert werden müssen. Wenn Sie eine große Menge an Artikeln in einer Wareneingangszeile erhalten, müssen Sie die Artikel möglicherweise in mehrere Lagerplätze einlagern und es gibt eine Zeile der Art Einlagerung für jeden Lagerplatz.  

5. Wenn Sie alle Artikel so in die Lagerplätze eingelagert haben, wie es die Anweisungen vorsehen, wählen Sie die Aktion **Einlagerung registrieren** aus.  

## So registrieren Sie eine Umlagerung, die bereits stattgefunden hat

Wenn Sie die Tatsache registrieren müssen, dass Artikel bereits ohne Einlagerung, Kommissionierung oder Umlagerung auf andere Lagerplätze umgelagert wurden, können Sie die Seite **Whse. Umlagerungs Buch.-Blatt** verwenden, um die Umlagerung zu registrieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Whse. Umlagerungs Buch.-Blatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder **Artikelnr.**, **Von Zonencode**, **Von Lagerplatzcode**, **Nach Zonencode** und **Nach Lagerplatzcode** aus.  
3. Wählen Sie die Aktion **Registrieren** aus.  

## Siehe verwandte [Microsoft Schulungen](/training/modules/manage-internal-warehouse-processes/)

## Weitere Informationen

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
