---
title: Exemplarische Vorgehensweise für grundlegende Jobs
description: Dieser Artikel führt Sie durch mehrere Kernprozesse im Projektmanagement.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---
# <a name="walkthrough-of-basic-jobs"></a>Exemplarische Vorgehensweise für grundlegende Jobs

Diese exemplarische Vorgehensweise demonstriert mehrere Kernprozesse:

- Jobaufgaben zu Jobs hinzufügen
- Erfassung von Zeit- und Materialaufwand zu einem Auftrag
- Fakturieren eines Projekts

## <a name="adding-a-job-task-to-a-job"></a>Eine Jobaufgabe zu einem Job hinzufügen

### <a name="scenario"></a>Szenario

Simon, der Projektmanager, möchte so viel Zeit wie möglich damit verbringen, den Kunden in die Verwendung von Espressomaschinen zu schulen, und zwar zu einer separaten Aufgabe im Rahmen der Installation einer kommerziellen Maschine vor Ort.

### <a name="steps"></a>Schritte

1. Erstellen Sie die Jobaufgabe  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
    2. Wählen Sie den Auftrag *J00010*.
    3. Wählen Sie im Bereich **Aufgaben** die Aktion **Neue Zeile**.  Geben Sie die folgenden Werte ein:
 
    |Aufg. Nr.|Description|Aufg. Art|
    |------------|-----------|-------------|  
    |220|Debitorenschulung|Buchen|

2. Einrücken der Projektaufgaben
   1. Suchen Sie im Bereich „Aufgaben“ nach der Aktion **Auftragsaufgaben einrücken**
   2. Bestätigen Sie, dass Sie Aufgaben einrücken möchten, indem Sie **Ja** auswählen.

### <a name="results"></a>Ergebnisse

 - Jetzt können Zeit und Kosten für die neue Arbeitsaufgabe erfasst werden

## <a name="record-time-and-material-expenses-to-a-job"></a>Datensätze für Zeit- und Materialaufwand zu einer Stelle

### <a name="scenario-1"></a>Szenario

Edgin, der Techniker, der die Maschine installiert, muss für die Abrechnung seine Zeit und die bei der Installation verwendeten Materialien für den Auftrag erfassen.  Er hat bereits die Reise- und Materialkosten hinzugefügt und muss nun noch die Zeit hinzufügen, um den Mitarbeitern den Umgang mit der Maschine beizubringen.

### <a name="steps-1"></a>Schritte

1. Erstellen Sie die zusätzlichen Erfassungspositionen

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  
    2. Wählen Sie den Stapel *CONTOSO*.  Sie sehen mehrere Zeilen mit Ressourcen- und Artikeltypen, die die verwendete Zeit (für den Techniker und das Fahrzeug) und die verwendeten Materialien (Maschine und Zubehör) widerspiegeln.
    3. Erstellen Sie eine neue Zeile. Geben Sie die folgenden Werte ein:
 
    |Einzelvorgangsnr.|Aufg. Nr.|Typ|Nr.|Description|Menge|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Ressource|EDGIN|Debitorenschulung|0|

2. Geben Sie den Zeit- und Kostenaufwand an
   1. Wählen Sie die Aktion **Buchen**
   2. Bestätigen Sie, dass Sie die Zeilen buchen möchten, indem Sie **Ja** auswählen.

### <a name="results-1"></a>Ergebnisse

 - Auftragshauptbucheinträge und Ressourcenhauptbucheinträge des Typs *Verwendung* wird erstellt
 - Es werden Artikelposten erstellt, um den Lagerbestand negativ anzupassen
 - Auf der Auftragskarte spiegeln die Kosten und Preise im Bereich „Aufgaben“ die neuen Salden wider, die auf die Rechnungsstellung warten
 - Auf der Jobkarte werden in der Infobox „Jobdetails“ die Gesamtpreise angezeigt

## <a name="creating-a-sales-invoice-for-a-job"></a>Erstellen einer Verkaufsrechnung für einen Auftrag

### <a name="scenario-2"></a>Szenario
Simon muss eine Rechnung erstellen und buchen, die zusammen mit dem Zeit- und Kostenaufwand für den Auftrag an den Kunden gesendet werden soll.

### <a name="steps-2"></a>Schritte
1. Verkaufsrechnung erstellen

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
    2. Wählen Sie in der Liste der Aufträge die Aktion **Projektverkaufsrechnung erstellen**.
    3. Stellen Sie den Filter **Projektnr.** auf *J00010*.
    4. Klicken Sie auf **OK**, um die Verkaufsrechnung zu erstellen.  Sie erhalten eine Bestätigung darüber, wie viele Rechnungen erstellt wurden

2. Buchen Sie die Zeit- und Spesenrechnung
   1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
   2. Wählen Sie die letzte Rechnung aus, um sie zur Überprüfung zu öffnen.
   3. Wählen Sie die Aktion **Buchen**.

### <a name="results-2"></a>Ergebnisse

 - Auftragshauptbucheinträge und Ressourcenhauptbucheinträge des Typs *Verkauf* wird erstellt
 - Auf der Auftragskarte spiegeln die Kosten und Preise im Bereich „Aufgaben“ die neuen fakturierten Salden wider
 - Auf der Auftragskarte werden in der Infobox „Auftragsdetails“ die Gesamtsummen der Preise im Abschnitt „Fakturierter Preis“ angezeigt
