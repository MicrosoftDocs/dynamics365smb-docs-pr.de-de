---
title: Exemplarische Vorgehensweise für grundlegende Jobs
description: Dieser Artikel führt Sie durch mehrere Kernprozesse im Projektmanagement.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Exemplarische Vorgehensweise für grundlegende Jobs

Diese exemplarische Vorgehensweise demonstriert mehrere Kernprozesse:

- Projekten Projektaufgaben hinzufügen
- Ausgaben für Zeit und Material zu einem Projekt erfassen
- Ein Projekt fakturieren

## Eine Projektaufgabe hinzufügen

### Szenario  

Simon, der Projektmanager, möchte erfassen, wie lange es gedauert hat, der Kundschaft den Umgang mit der Espressomaschine beizubringen. Simon möchte in dem Projekt eine separate Aufgabe für die Installation einer professionellen Maschine am Kundenstandort nutzen.

### Schritte

1. Erstellen Sie die Projektaufgabe.

    1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.  
    2. Wählen Sie den Auftrag *J00010*.
    3. Wählen Sie im Bereich **Aufgaben** die Aktion **Neue Zeile** ein und geben Sie dann die folgenden Werte ein:
 
    |Projektaufgabennr.|Description|Projektaufgabentyp|
    |------------|-----------|-------------|  
    |220|Debitorenschulung|Buchen|

2. Rücken Sie die Projektaufgaben ein.
   1. Suchen Sie im Bereich „Aufgaben“ nach der Aktion **Projektaufgaben einrücken**.
   2. Bestätigen Sie mit **Ja**, dass Sie die Aufgaben einrücken möchten.

### Ergebnisse

 - Jetzt können Zeit und Kosten für die neue Projektaufgabe erfasst werden

## Zeit- und Materialaufwand für ein Projekt erfassen

### Szenario  

Edgin, der Techniker, der die Maschine installiert, muss für die Abrechnung die Zeit und die bei der Installation verwendeten Materialien für den Auftrag erfassen. Edgin hat bereits die Fahrt- und Materialkosten hinzugefügt und muss nun noch die Zeit hinzufügen, um den Mitarbeitenden den Umgang mit der Maschine beizubringen.

### Schritte

1. Erstellen Sie die zusätzlichen Projektbuchungsblattzeilen.

    1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Projekterfassungen** ein und wählen Sie dann den zugehörigen Link aus.  
    2. Wählen Sie den Stapel *CONTOSO*. Sie sehen mehrere Zeilen mit Ressourcen- und Artikeltypen, die die verwendete Zeit (für den Techniker und das Fahrzeug) und die verwendeten Materialien (Maschine und Zubehör) widerspiegeln.
    3. Erstellen Sie eine neue Zeile und geben Sie dann die folgenden Werte ein:
 
    |Projektnr.|Projektaufgabennr.|Typ|Anz.|Description|Menge|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Ressource|EDGIN|Debitorenschulung|0|

2. Geben Sie den Zeit- und Kostenaufwand an.
   1. Wählen Sie die Aktion **Buchen**.
   2. Bestätigen Sie mit **Ja**, dass Sie die Zeilen buchen möchten.

### Ergebnisse

- Es werden Projekt- und Ressourcenhauptbuchposten vom Typ *Verwendung* erstellt.
- Es werden Artikelposten erstellt, um den Lagerbestand nach unten zu korrigieren.
- Auf der Projektkarte spiegeln die Kosten und Preise im Bereich „Aufgaben“ die neuen Salden wider, die auf die Rechnungsstellung warten.
- Auf der Projektkarte werden in der Infobox „Projektdetails“ die Gesamtpreise angezeigt.

## Eine Verkaufsrechnung für ein Projekt erstellen

### Szenario  

Simon muss eine Rechnung erstellen und buchen, die zusammen mit dem Zeit- und Kostenaufwand für das Projekt an die Kundschaft gesendet werden soll.

### Schritte

1. Erstellen Sie die Verkaufsrechnung.

    1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.  
    2. Wählen Sie in der Liste der Aufträge die Aktion **Projektverkaufsrechnung erstellen** aus.
    3. Legen Sie den Filter **Projektnr.** auf *J00010* fest.
    4. Gehen Sie auf **OK**, um die Verkaufsrechnung zu erstellen. Sie erhalten eine Bestätigung darüber, wie viele Rechnungen erstellt wurden.

2. Buchen Sie die Zeit- und Ausgabenrechnung.

   1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
   2. Wählen Sie die letzte Rechnung aus, um sie zur Überprüfung zu öffnen.
   3. Wählen Sie die Aktion **Buchen**.

### Ergebnisse

- Projekt- und Ressourcenhauptbucheinträge vom Typ *Verkauf* werden erstellt.
- Auf der Projektkarte spiegeln die Kosten und Preise im Bereich „Aufgaben“ die neuen fakturierten Salden wider.
- Auf der Projektkarte werden in der Infobox „Projektdetails“ die Gesamtsummen der Preise im Abschnitt „Fakturierter Preis“ angezeigt.
