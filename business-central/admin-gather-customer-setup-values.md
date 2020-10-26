---
title: Debitoren-Einrichtungswerte sammeln | Microsoft Docs
description: Verwenden Sie den Einrichtungsfragebogen, um Ihre Implementierungsarbeitslast zu verringern, indem Sie die Aufgabe des Einrichtens neuer Mandanten rationalisieren. Sie können den Einrichtungsfragebogen in Business Central erstellen und Ihrem Debitor als Excel (.xlsx) oder XML-Datei zur Verfügung stellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 77534395d868b1ea82317c32aaed0e70d222e1e1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911480"
---
# <a name="gather-customer-setup-values"></a>Sammeln von Einrichtungswerten für Debitoren
Verwenden Sie den Einrichtungsfragebogen, um Ihre Implementierungsarbeitslast zu verringern, indem Sie die Aufgabe des Einrichtens neuer Mandanten rationalisieren. Sie können den Einrichtungsfragebogen in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen und Ihrem Debitor als Excel (.xls) oder XML-Datei zur Verfügung stellen.  

Sie können alle Vorgabewerte in einem Fragebogen ändern, um sie an die Anforderungen des Debitors anzugleichen.  

> [!TIP]  
>  Weitere Informationen zum Definieren von Einrichtungswerten auf den Beschaffungsplanungsgebieten, siehe [Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md).  

Wenn Ihr Debitor den Fragebogen ausgefüllt hat, importieren Sie die Datei in den neuen Mandanten [!INCLUDE[d365fin](includes/d365fin_md.md)] des Debitors. Sie und Ihr Debitor validieren die Antworten aus dem Fragebogen, bevor Sie ihn für das Unternehmen anwenden.

## <a name="to-create-a-configuration-questionnaire"></a>So erstellen Sie einen benutzerdefinierten Konfigurationsfragebogen
Sie können einen Fragebogen verwenden, um den Umfang und die Anforderungen der Konfiguration zu bestimmen. Sie können eine neue Befragung erstellen oder ändern eine bestehende Befragung ändern, indem Sie auch neue Fragen oder Fragenbereiche hinzufügen.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company informtion. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 Sie können Fragebögen nur für Setup-Typ-Tabellen erstellen. Beispielsweise können Sie das Werkzeug verwenden, um Informationen auf den folgenden Seiten bereitzustellen:  

-   Unternehmensdaten  
-   Anlageneinrichtung  
-   Finanzbuchhaltung Einrichtung  
-   Lagereinrichtung  
-   Montageeinrichtung
-   Produktion Einrichtung  
-   Kreditoren und Einkauf Einr.  
-   Marketingeinrichtung  
-   Service Einrichtung  
-   Debitoren und Verkauf Einr.  
-   Logistik Einrichtung  

> [!NOTE]  
>  Um eine vollständige Liste von Einrichtungstabellen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Einrichtung** ein und wählen Sie dann den zugehörigen Link aus. Um den Umfang der Migration von Daten zu ermitteln, verwenden Sie Migrationsfunktionen. Weitere Informationen finden Sie unter [Gewusst wie: Debitorendaten zusammenführen](admin-migrate-customer-data.md).  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationsfragebogen** ein, und wählen Sie den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** .   
3. Geben Sie auf der Seite **Konfigurationsfragebogen** im Feld **Code** Folgendes ein... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Wählen Sie die **Fragen-Bereiche** Aktion aus. Die Seite **Fragenbereiche** wird geöffnet.  
4. Wählen Sie die Aktion **Neu** aus. Die Seite **Fragenbereiche konfigurieren** wird geöffnet.  
5. Wählen Sie im Feld **Tabellen-ID** die ID der Tabelle aus, für die Sie Daten erfassen möchten. Das Feld **Tabellennamen** wird automatisch ausgefüllt.  
6. Wählen Sie die **Fragen aktualisieren** Aktion aus. Jedes Feld in der Tabelle wird der Befragung mit einem Fragezeichen hinter seiner Beschriftung hinzugefügt.

Sie können die Beschriftung neu formulieren, um zu verdeutlichen, wie die Frage beantwortet werden soll. Beispielsweise können Sie ein Feld mit der Bezeichnung "Name" so bearbeiten, dass seine Beschriftung "Wie ist der Name von zu erfassende Daten" <data being collected>  lautet. Sie können aucn eine Anleitung im Feld **Referenz** angeben, einschließlich einer URL auf einer Seite angeben, die zusätzliche Informationen angibt.  

Bei Bedarf können Sie Fragen auch löschen, die nicht im Fragebogen berücksichtigt werden sollen.  

> [!NOTE]  
>  Das Feld **Antwort-Optionen** beschreibt die Art und das Format der geeigneten Antwortdaten. Das Feld **Antworten** enthält vom Benutzer bereitgestellte Informationen.  
>   
>  Bei Bedarf können Sie im Feld **Antworten** auch Standardantworten definieren. Diese Werte werden standardmäßig für benutzerdefinierte Einrichtungen verwendet. Jedoch kann die Person, die den Fragebogen ausfüllt, die Antwort ändern und aktualisieren.  

## <a name="to-complete-the-configuration-questionnaire"></a>Vorgehensweise: Abschließen des Konfigurationsfragebogens
Verwenden Sie den Einrichtungsfragebogen, um eine detaillierte Erörterung der speziellen Anforderungen des Debitors zu strukturieren und zu dokumentieren. Verwenden Sie sie auch, um Einrichtungsdaten vom Debitoren zu erfassen, um die relevanten [!INCLUDE[d365fin](includes/d365fin_md.md)]-Einrichtungstabellen, wie die Finanzbuchhaltung, die Lagerbestandsdaten und die Debitoren zu konfigurieren.  

> [!NOTE]  
>  Sie können auch einen eigenen Einrichtungsfragebogen erstellen, der ihre speziellen Bedürfnisse erfüllt.  

1. Wählen Sie im Feld Mandanten den gewünschten Mandanten aus, für dten.en Sie den Fragebogen beenden möchten.
2. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationsfragebogen** ein, und wählen Sie dann den zugehörigen Link.  
3. Wählen Sie die Befragung für Unternehmen, und wählen die **In Excel exportieren** Aktion, optional die **In XML exportieren** Aktion aus.
4. Lassen Sie den Mandanten den Konfigurationsfragebogen ausfüllen, indem Sie die Antworten in die Excel-Arbeitsmappe eingeben. Es gibt Arbeitsblätter für jeden der Fragenbereiche, die für die Befragung erstellt wurden.   
5. Speichern Sie die Excel-Arbeitsmappe als *XML-Daten* . Wählen Sie die **Aus XML importieren** Aktion aus, und wählen Sie die XLSX-Datei mit der Antworten des Debitors aus.
6. Klicken Sie auf der Registerkarte Start in der Gruppe Vorgang auf **Fragenbereiche** , um die Validierung und die Anwendung der Antworten auf den Einrichtungsfragebogen zu starten.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>So füllen Sie einen Fragebogen aus dem Konfigurationsarbeitsblatt aus  
Das nächste Verfahren ist eine alternative Möglichkeit für den Zugriff auf Konfigurationsfragebögen. Dabei wird davon ausgegangen, dass das Konfigurationspaket, das Sie bereitgestellt haben, Fragebögen enthält.  

1. Nachdem Sie ein Konfigurationspaket importiert haben, öffnen Sie das Konfigurationsarbeitsblatt.  
2. Für jede Tabelle, für ein Fragenbereich vorhanden ist, wählen Sie die **Fragen** Aktion aus. Die Fragebogenseite wird geöffnet.  
3. Beantworten Sie die Fragen, und wählen Sie die **Antworten übernehmen** Aktion aus.  
4. Wählen Sie die Schaltfläche **OK** , um den Fragebogen zu schließen.

## <a name="to-validate-the-configuration-questionnaire"></a>Vorgehensweise: Überprüfen des Konfigurationsfragebogens
Es ist wichtig, dass der Konfigurationsfragebogen geprüft wird, bevor Sie ihn auf das [!INCLUDE[d365fin](includes/d365fin_md.md)]-Format anwenden. Damit prüfen Sie auch, ob die Datenformatierung während des Imports aus Excel beibehalten wurde.  

Ein typischer Validierungsvorgang ist die Prüfung, ob keine Textzeichenfolgen in Datumsfelder eingegeben wurden. Dieser Reviewprozess ist notwendig, da das Format der Antwort im Fragebogen nicht automatisch überprüft wird, wenn die Funktion **Antworten übernehmen** ausgeführt wird.  

> [!NOTE]  
>  Im Allgemeinen ist die Konfiguration des Einrichtungsfragebogens nur ein manueller Prozess. Es gibt jedoch Prüfungen für regionale Formatierungsinkonsistenzen. Darüber hinaus erhalten Sie Fehler, wenn die Struktur Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank nicht der Struktur der Migrationsdatenbank entspricht.  

1. Auf der Seite **Konfigurationsfragebogen** wählen Sie den gewünschten Fragebogen aus, und wählen Sie die **Fragenbereiche** Aktion aus.  
2. Öffnen Sie den relevanten Fragebogenbereich aus.  
3. Prüfen Sie für jede Frage, dass der Wert im Feld **Antwort** dem Format entspricht, das im Feld **Antwortoptionen** bereitgestellt wird. Prüfen Sie etwa, dass die Adresse eines Mandanten im Textformat ist.  
4. Wenn Sie Fehler finden, können Sie Korrekturen in Excel vornehmen; dazu exportieren Sie den Fragebogen und importieren ihn anschließend wieder. Alternativ können Sie Fehler auch direkt in [!INCLUDE[d365fin](includes/d365fin_md.md)] korrigieren, während Sie die Antworten auf der Seite **Fragenbereich konfigurieren** prüfen.  
5. Wiederholen Sie diese Schritte für jeden Fragenbereich.  

Nachdem Sie Ihre Prüfung abgeschlossen haben, sind die Daten bereit, um zur Datenbank ausgeglichen werden.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Anwenden von Antworten aus dem Konfigurationsfragebogen
Nachdem Sie und Informationen aus einem Konfigurationsfragebogen importiert und validiert haben, können Sie die Einrichtungsdaten übertragen, oder Sie auf die entsprechenden Tabellen in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank anwenden.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationsfragebogen** ein, und wählen Sie dann den zugehörigen Link. Die Seite **Profilbefragung konfigurieren** wird geöffnet.  
2. Wählen Sie einen Konfigurationsfragebogen aus der Liste und wählen Sie **Liste bearbeiten** aus.  
3. Sie können Antworten auf eine von zwei Arten anwenden.  

- Um den gesamten Fragebogen anzuwenden, wählen Sie auf der Registerkarte Vorgang die Option **Antworten übernehmen** .  
- Um Antworten aus einem bestimmten **Fragenbereich** anzuwenden, aktivieren Sie **Fragebereiche** , wählen Sie einen **Fragenbereich** aus der Liste, und wählen Sie anschließend auf der Registerkarte Start die Option **Antworten anwenden** aus.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>So überprüfen Sie, ob Antworten erfolgreich angewendet wurden  
1. Prüfen Sie die Einrichtungsseiten für die verschiedenen Funktionsbereiche aus [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zum Lokalisieren der Seite wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie den Namen der Einrichtungsseite ein, und wählen Sie dann den zugehörigen Link.  
2. Vergewissern Sie sich, dass die Felder mit den richtigen Daten aus den verschiedenen Fragebereichen im Kofigurationsfragebogen gefüllt wurden.  

Sie haben nun die Einrichtung mit den Geschäftsinformationen und den Regeln des Debitors konfiguriert.

## <a name="see-also"></a>Siehe auch  
[Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
