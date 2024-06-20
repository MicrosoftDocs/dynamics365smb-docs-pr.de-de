---
title: XML-Schemata zum Vorbereiten von Data Exchange-Definitionen
description: 'Verwenden Sie XML-Schemata, um das Framework für den Datenaustausch festzulegen, um zu definieren, mit welchen Datenelementen Sie austauschen wollen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen

Um das Importieren/Exportieren von Daten in XML-Dateien durch das Datenaustauschframework in [!INCLUDE[prod_short](includes/prod_short.md)], können Sie das XML-Schema der Datei verwenden, um zu definieren, welche Datenelemente Sie mit [!INCLUDE[prod_short](includes/prod_short.md)] austauschen möchten. Sie führen diese Arbeit auf der Seite **XML-Schema-Ansicht** aus, indem Sie die XML-Schemadatei laden, die entsprechenden Datenelemente auswählen und dann eine Datenaustauschdefinition initialisieren.  

 Wenn Sie festgelegt haben, welche Datenelemente Sie auf Grundlage des XML-Schemas einschließen möchten, können Sie die Aktion **Datenaustauschdefinition generieren** verwenden, um eine Datenaustauschdefinition basierend auf den ausgewählten Datenelementen zu initialisieren, die Sie dann im Datenaustauschframework abschließen. Dies erstellt einen Datensatz auf der Seite **Austauschdefinition buchen**. Darin legen Sie anschließend fest, welche Elemente in der Datei welchen Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

 In diesem Thema werden die folgenden Prozeduren beschrieben:  

- So laden Sie eine XML-Schemadatei  

- So wählen oder löschen Sie Knoten in XML-Schema  

- So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert  

## So laden Sie eine XML-Schemadatei

1. Vergewissern Sie sich, dass die relevante XML-Schemadatei verfügbar ist. Die Dateierweiterung lautet „.xsd“.  

2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **XML-Schemata** ein und wählen Sie dann den entsprechenden Link.  

3. Wählen Sie die Aktion **Neu**.  

4. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Geben Sie einen Code an, um das XML-Schema zu identifizieren.|  
    |**Beschreibung**|Geben Sie eine Beschreibung des XML-Schemas an.|  

     Das Feld **Ziel-Namespace** gibt den Namespace in der XML-Schemadatei an, der für die Zeile geladen wurde.  

5. Wählen Sie die Aktion **Schema laden** und dann die XML-Schemadatei aus.  

     Wenn die Datei geladen wird, werden die restlichen Felder auf der Zeile mit Informationen aus der Datei ausgefüllt, und das Kontrollkästchen **Schema ist geladen** ist aktiviert.  

    > [!NOTE]  
    >  Die Struktur des geladenen XML-Schemas wird standardmäßig reduziert angezeigt. Sie erweitern die einzelnen Knoten über die Schaltfläche **+** für den Knoten. Um alle Knoten zu erweitern, wählen Sie **Alle aufklappen** auf dem Menüband aus.  

### So wählen oder löschen Sie Knoten in XML-Schema  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **XML-Schema-Viewer** ein und wählen Sie dann den zugehörigen Link.  

2. Füllen Sie im Kopfbereich die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**XML-Schemacode**|Geben Sie die XML-Schemadatei an, die Sie in Schritt 5 im Abschnitt „Laden der XML-Schemadatei“ geladen haben.|  
    |**Neue XMLport-Nr.**|Geben Sie die Nummer des XMLport an, der von diesem XML-Schema erstellt wird, wenn Sie die Aktion **XMLport generieren** auswählen.|  

     Die Zeilen werden nun mit den Knoten ausgefüllt, die alle Elemente im XML-Schema darstellen. Knoten für Elemente, die entsprechend dem XML-Schema erforderlich sind, sind standardmäßig aktiviert.  

3. Erweitern Sie in der ersten Zeile in der Spalte **Knotenname**, das Dokument **Knoten**, und erweitern Sie schrittweise die zugrundeliegenden Knoten, die Sie einsehen möchten.  

     Oder klicken Sie mit der rechten Maustaste auf einen Knoten, und wählen Sie dann **Alle aufklappen** aus.  

4. Wählen Sie eine der folgenden Aktionen, um zu ändern, welche Knoten angezeigt werden.  

    |**Aktion**|Beschreibung|  
    |----------------|---------------------------------------|  
    |**Alle anzeigen**|Alle Knoten werden angezeigt.|  
    |**Nicht notwendige ausblenden**|Nur Knoten, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind, werden angezeigt. Diese Knoten werden in der Regel durch eine **1** im -Feld **MinOccurs** angegeben.<br /><br /> Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.|  
    |**Nicht ausgewählte ausblenden**|Nur Knoten, in denen das Kontrollkästchen **Ausgewählt** aktiviert ist, werden angezeigt.<br /><br /> Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.|  

5. Wählen Sie die Aktion **Bearbeiten** aus.  

6. Geben Sie mit dem **Ausgewählt**-Kontrollkästchen für jeden Knoten an, ob das Element im Datenaustauschdefinition für die entsprechende SEPA-Bankdatei unterstützt werden soll.  

    > [!NOTE]  
    >  Wenn Sie den erforderlichen untergeordneten Knoten auswählen, werden alle übergeordneten Knoten dafür aktiviert.  

7. Wählen Sie die Aktion **Alle erforderlichen Elemente auswählen** aus, um alle Knoten erneut auszuwählen, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind.  

8. Wählen Sie die Aktion **Auswahl aufheben** aus, um alle Auswahlen zu löschen.  

     Das Feld **Wahl** gibt an, dass der Knoten zwei oder mehr gleichgeordnete Knoten hat, die als Optionen fungieren.  

### So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **XML-Schemata** ein und wählen Sie dann den zugehörigen Link.  

2. Wählen Sie das entsprechende XML-Schema und dann die Aktion **XML-Schema-Viewer öffnen** aus.  

3. Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden. Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.  

4. Wählen Sie auf der Seite **XML Schema Viewer** die Aktion **Datenaustauschdefinition generieren**.  

 Eine Datenaustauschdefinition wird auf der Seite **Austauschdefinition buchen** erstellt, die Sie vervollständigen können, indem Sie festlegen, welche Elemente in der Datei welchen Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden sollen. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
> Sie können auch die Funktion **Dateistruktur abrufen** im Fenster **Austauschdefinition buchen** verwenden. Hier wird die Funktion auf der Seite **SML Schema Viewer** eingesetzt, um das Inforegister **Spaltendefinitionen** vorab auszufüllen.  

> [!NOTE]
> In der Veröffentlichungswelle 1 von 2019 und früheren Versionen konnten Sie einen auf dem Schema basierenden XMLport generieren und diesen anschließend in Ihre Lösung importieren. Dies wird nicht mehr unterstützt.

## Siehe auch

[Richten Sie Datenaustauschdefinitionen ein](across-how-to-set-up-data-exchange-definitions.md)  
[Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Über das Datenaustauschframework](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]