---
title: Exemplarische Vorgehensweise für Serviceverträge für Serviceartikel
description: Dieser Artikel führt Sie durch verschiedene Szenarios mit Serviceartikeln und Verträgen.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Exemplarische Vorgehensweise für Serviceverträge für Serviceartikel

Diese exemplarische Vorgehensweise demonstriert mehrere Kernprozesse:

- Erstellung von Serviceartikeln durch den Verkauf
- Erstellen und Fakturieren eines Servicevertrags
- Erstellen eines Serviceauftrags für einen Servicevertrag
- Weisen Sie eine Ressource basierend auf Fähigkeit und Zone zu
- Vervollständigen Sie den Zeiteintrag für den Serviceauftrag
- Buchen und fakturieren Sie den Vertragsserviceauftrag

## Erstellung von Serviceartikeln

### Szenario  

Susan, die Auftragsbearbeiterin, gibt einen Debitorenauftrag auf, in dem ein Artikel verkauft wird, der für die Generierung eines Serviceartikels konfiguriert ist.  

### Schritte

1. Überprüfen Sie, ob für **Artikel** **Serviceartikelgruppe** ausgewählt ist.
   
    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.  
    2. Wählen Sie den Artikel *S-100* aus und öffnen Sie ihn.
    3. Überprüfen Sie den Wert im Feld **Serviceartikelgruppe**.
       
2. Buchen Sie den **Verkaufsauftrag**, um den Serviceartikel für den Debitoren zu erstellen.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
    2. Wählen Sie den Auftrag für Debitor 10000 aus. Die externe Bestellnr. ist *SVC-1*.
    3. Wählen Sie die Aktion **Buchen**, um den Artikel an den Debitor zu versenden.

### Ergebnisse

- Für Debitor 10000 wird ein Serviceartikel erstellt

##  Fakturierung eines Servicevertrags

### Szenario

Charles, der Servicemanager, erstellt dann einen Servicevertrag, um regelmäßige Wartungsbesuche in Rechnung zu stellen.

3. Erstellen Sie den **Servicevertrag** für den neuen Serviceartikel
    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Serviceverträge** ein und wählen Sie dann den zugehörigen Link.
    2. Wählen Sie die Aktion **Neu**.  
    3. Wählen Sie im Bestätigungsdialogfeld **Ja**, um einen Vertrag mithilfe einer Vorlage zu erstellen. 
    4. Wählen Sie *Nicht vorausbezahlter Vertrag - Monatlich*.
    5. Geben Sie im Inforegister „Service“ im **Serviceauftragstyp** **MAINTEN** ein.
    6. Geben Sie in den Zeilen die folgenden Informationen ein:

    |Serviceartikelnr.|Zeilenwert|  
    |----------------|----------|  
    |SV000001|6000|

    7. Um den Vertrag zu unterzeichnen, wählen Sie die Aktion **Vertrag unterschreiben**.
    8. Wählen Sie **Ja**, um die Erstellung einer Servicerechnung zu bestätigen. Sie erhalten eine Bestätigungsnachricht mit der Servicerechnungsnummer.

3. Buchen Sie die Servicerechnung
   1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicerechnungen** ein und wählen Sie dann den zugehörigen Link.
   2. Suchen Sie die Servicerechnung und wählen Sie die Aktion **Buchen** aus.

### Ergebnisse

- Es wird ein unterzeichneter Servicevertrag mit Hauptbucheinträgen erstellt
- Eine gebuchte Servicerechnung wird erstellt

## Einen Serviceauftrag für einen Servicevertrag erstellen und Ressourcen zuweisen

### Szenario  

Charles, der Servicemanager, erstellt die Serviceaufträge für reguläre Wartungsaufträge im Rahmen des Servicevertrags und überprüft dann die Einsatzplanung, um sie zuzuweisen.

### Schritte

1. Führen Sie die Serviceaufträge aus, welche die Verpflichtungen aktiver Serviceverträge erfüllen.
   1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aufträge für Verträge erst erstellen** ein, und wählen Sie dann den zugehörigen Link.
   2. Geben Sie das Anfangs- und Enddatum des Monats in die Felder „Startdatum“ und „Enddatum“ im Inforegister „Optionen“ ein
   3. Wählen Sie **OK**, um die Erstellung eines Serviceauftrags zu bestätigen. Sie erhalten eine Bestätigungsnachricht mit der Anzahl der erstellten Serviceaufträge.

2. Überprüfen Sie die Bestellungen, die auf die Zuweisung warten, über die Einsatzplanung
   1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einsatzplanung** ein und wählen Sie den zugehörigen Link.
   2. Die Einsatzplanung zeigt alle offenen Serviceaufträge zusammen mit der **Nr. der Zuordnungen** um anzuzeigen, ob die Serviceaufträge einer Ressource zugewiesen wurden.
   3. Wählen Sie die Aktion **Dokumente anzeigen**, um einen Serviceauftrag zu öffnen.  Sie sehen, dass in der Infobox „Serviceartikelzeilen“ angezeigt wird, welche Ressourcen über die nötigen Kenntnisse für die Arbeit mit diesem Artikel verfügen.

3. Dem Serviceauftrag eine Ressource zuweisen
   1. Wählen Sie im Serviceauftrag die Zeilenaktion **Ressourcen zuweisen** aus.
   2. Geben Sie die folgenden Informationen für die Zuteilung der Ressourcen ein

    |Serviceartikelnr.|Ressourcennr.|Zuordnungsdatum|Zugeordnete Stunden|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|h|0|

    3. Die Zuordnung wird in den Status „Aktiv“ geändert.
    4. Wenn Sie die Einsatzplanung aktualisieren, wird **Nr. der Zuordnungen** für den Serviceauftrag von 0 auf 1 geändert.

### Ergebnisse

- Für die Serviceverträge werden Serviceaufträge erstellt
- Die Serviceaufträge werden einer Ressource zugewiesen, um die Arbeit abzuschließen

## Vervollständigen Sie die Zeiterfassung für den Serviceauftrag und buchen Sie ihn

### Szenario  

Die Servicefachkraft registriert seine Zeit direkt im Serviceauftrag und kennzeichnet den Auftrag dann als abgeschlossen.

> [!NOTE]
> Die Zeiterfassung für Serviceaufträge kann über Arbeitszeitnachweise erfasst werden. Weitere Informationen finden Sie unter [Link zur Arbeitszeittabelle, wenn dieser Hinweis sinnvoll ist].

### Schritte

1. Suchen Sie den Serviceauftrag und geben Sie die Zeit in die Servicezeile ein
   1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Serviceaufträge** ein und wählen Sie dann den zugehörigen Link.
   2. Suchen Sie den Serviceauftrag, für den Sie die Zeit eingeben möchten.
   3. Wählen Sie die Zeilenaktion **Servicezeilen**.
   4. Geben Sie die folgenden Informationen ein

    |Typ|Anz.|Menge|Mge. zu verbrauchen|
    |----|---|--------|--------|   
    |Ressource|RESOURCE1|2|2|

2. Buchen Sie auf dem Serviceauftrag den Verbrauch
   1. Wählen Sie die Aktion **Buchen**, um den Serviceauftrag abzuschließen. Wählen Sie die Aktion **Versenden und verbrauchen**, und wählen Sie dann **OK**.

### Ergebnisse

- Es werden Serviceposten erstellt, die dem Serviceartikel, dem Servicevertrag und der Ressource zugeordnet sind

## Siehe auch

[Einführung in Contoso Coffee-Demodaten](../../contoso-coffee/contoso-coffee-intro.md)  
[Informationen zu Fertigungsaufträgen](../../production-about-production-orders.md)