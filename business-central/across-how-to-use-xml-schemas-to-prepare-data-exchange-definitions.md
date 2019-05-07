---
title: Erstellen Sie XMLports auf Grundlage von XML-Schemata | Microsoft Docs
description: Verwenden Sie XML-Schemata, um das Belegaustauschframework festzulegen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: bac8d19bd48d9b7ad981c75dc54b155c8fe765a5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935900"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinitionen
Um das Importieren/Exportieren von Daten in XML-Dateien durch das Datenaustauschframework in [!INCLUDE[d365fin](includes/d365fin_md.md)], können Sie das XML-Schema der Datei verwenden, um zu definieren, welche Datenelemente Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)] austauschen möchten. Sie führen diese Arbeit auf der Seite **XML-Schema-Ansicht** aus, indem Sie die XML-Schemadatei laden, die entsprechenden Datenelemente auswählen und dann entweder eine Datenaustauschdefinition oder einen XMLport initialisieren.  

 Wenn Sie festgelegt haben, welche Datenelemente Sie auf Grundlage des XML-Schemas einschließen möchten, können Sie die Aktion **XMLport generieren** verwenden, um das XMLport-Objekt zu erstellen.  

 Sie können auch die Aktion **Datenaustauschdefinition generieren** verwenden, um eine Datenaustauschdefinition basierend auf den ausgewählten Datenelementen zu initialisieren, die Sie dann im Datenaustauschframework abschließen. Dies erstellt einen Datensatz auf der Seite **Austauschdefinition buchen**. Darin legen Sie anschließend fest, welche Elemente in der Datei welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

 In diesem Thema werden die folgenden Prozeduren beschrieben:  

-   So laden Sie eine XML-Schemadatei  

-   So wählen oder löschen Sie Knoten in XML-Schema  

-   So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert  

-   So generieren Sie einen XMLport für die Datei, der auf einem XML-Schema basiert  

-   So importieren Sie einen XMLport in den Objekt-Designer  

### <a name="to-load-an-xml-schema-file"></a>So laden Sie eine XML-Schemadatei  

1.  Vergewissern Sie sich, dass die relevante XML-Schemadatei verfügbar ist. Die Dateierweiterung lautet „.xsd“.  

2.  Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.  

3.  Wählen Sie auf der Registerkarte **Start** in der Gruppe **Neu** die Option **Neu** aus.  

4.  Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Geben Sie einen Code an, um das XML-Schema zu identifizieren.|  
    |**Beschreibung**|Geben Sie eine Beschreibung des XML-Schemas an.|  

     Das Feld **Ziel-Namespace** gibt den Namespace in der XML-Schemadatei an, der für die Zeile geladen wurde.  

5.  Wählen Sie in der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Schema laden**, und wählen Sie dann die XML-Schemadatei.  

     Wenn die Datei geladen wird, werden die restlichen Felder auf der Zeile mit Informationen aus der Datei ausgefüllt, und das Kontrollkästchen **Schema ist geladen** ist aktiviert.  

    > [!NOTE]  
    >  Die Struktur des geladenen XML-Schemas wird standardmäßig reduziert angezeigt. Sie erweitern die einzelnen Knoten über die Schaltfläche **+** für den Knoten. Um alle Knoten zu erweitern, wählen Sie **Alle aufklappen** auf dem Menüband aus.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>So wählen oder löschen Sie Knoten in XML-Schema  

1.  Geben Sie im Feld **Suchen** **XML Schema Viewer** ein, und wählen Sie dann den zugehörigen Link aus.  

2.  Füllen Sie im Kopfbereich die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**XML-Schemacode**|Geben Sie die XML-Schemadatei an, die Sie in Schritt 5 im Abschnitt „Laden der XML-Schemadatei“ geladen haben.|  
    |**Neue XMLport-Nr.**|Geben Sie die Nummer des XMLport an, der von diesem XML-Schema erstellt wird, wenn Sie die Aktion **XMLport generieren** auswählen.|  

     Die Zeilen werden nun mit den Knoten ausgefüllt, die alle Elemente im XML-Schema darstellen. Knoten für Elemente, die entsprechend dem XML-Schema erforderlich sind, sind standardmäßig aktiviert.  

3.  Erweitern Sie in der ersten Zeile in der Spalte **Knotenname**, das Dokument **Knoten**, und erweitern Sie schrittweise die zugrundeliegenden Knoten, die Sie einsehen möchten.  

     Oder klicken Sie mit der rechten Maustaste auf einen Knoten, und wählen Sie dann **Alle aufklappen** aus.  

4.  Auf der Registerkarte **Start** in der Gruppe **Ansicht** wählen Sie eine der folgenden Aktionen, um die anzuzeigenden Knoten zu ändern.  

    |**Aktion**|Beschreibung|  
    |----------------|---------------------------------------|  
    |**Alle anzeigen**|Alle Knoten werden angezeigt.|  
    |**Nicht notwendige ausblenden**|Nur Knoten, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind, werden angezeigt. Diese Knoten werden in der Regel durch eine **1** im -Feld **MinOccurs** angegeben.<br /><br /> Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.|  
    |**Nicht ausgewählte ausblenden**|Nur Knoten, in denen das Kontrollkästchen **Ausgewählt** aktiviert ist, werden angezeigt.<br /><br /> Wählen Sie **Alle anzeigen**, um die Ansicht umzukehren.|  

5.  Wählen Sie auf der Registerkarte **Start** in der Gruppe **Verwalten** die Option **Bearbeiten** aus.  

6.  Geben Sie mit dem **Ausgewählt**-Kontrollkästchen für jeden Knoten an, ob das Element im Datenaustauschdefinition für die entsprechende SEPA-Bankdatei unterstützt werden soll.  

    > [!NOTE]  
    >  Wenn Sie den erforderlichen untergeordneten Knoten auswählen, werden alle übergeordneten Knoten dafür aktiviert.  

7.  Wählen Sie die Aktion **Alle erforderlichen Elemente auswählen** aus, um alle Knoten erneut auszuwählen, die Elemente darstellen, die entsprechend dem XML-Schema erforderlich sind.  

8.  Wählen Sie die Aktion **Auswahl aufheben** aus, um alle Auswahlen zu löschen.  

     Das Feld **Wahl** gibt an, dass der Knoten zwei oder mehr gleichgeordnete Knoten hat, die als Optionen fungieren.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>So generieren Sie eine Datenaustauschdefinition, die auf einem XML-Schema basiert  

1.  Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.  

2.  Wählen Sie das relevante XML-Schema aus und dann auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **XML-Schema-Viewer öffnen**.  

3.  Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden. Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.  

4.  Wählen Sie auf der Seite **XML Schema Viewer** auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **Datenaustauschdefinition generieren** aus.  

 Eine Datenaustauschdefinition wird auf der Seite **Austauschdefinition buchen** erstellt, die Sie vervollständigen können, indem Sie festlegen, welche Elemente in der Datei welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden sollen. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  Sie können auch die Funktion **Dateistruktur abrufen** im Fenster **Austauschdefinition buchen** verwenden. Hier wird die Funktion auf der Seite **SML Schema Viewer** eingesetzt, um das Inforegister **Spaltendefinitionen** vorab auszufüllen.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>So generieren Sie einen XMLport, der auf einem XML-Schema basiert  

1.  Geben Sie im Feld **Suchen** **XML Schemas** ein, und wählen Sie dann den zugehörigen Link aus.  

2.  Wählen Sie das relevante XML-Schema aus und dann auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **XML-Schema-Viewer öffnen**.  

3.  Im **Neue XMLport-Nr.** -Feld geben Sie die Nummer an, die das neue XMLport-Objekt erhalten wird, wenn es erzeugt wird.  

4.  Stellen Sie sicher, dass die entsprechenden Knoten ausgewählt werden. Weitere Informationen finden Sie im Abschnitt „Auswahl oder Löschen von Knoten in einem XML-Schema“.  

5.  Auf der Registerkarte **Start** in der Gruppe **Verarbeiten** wählen Sie **XMLport generieren** aus, und speichern Sie dann das Objekt als .txt- Datei an einem entsprechenden Speicherort.  

6. Importieren Sie den neuen XMLport in die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Entwicklungsumgebung und kompilieren Sie ihn.

## <a name="see-also"></a>Siehe auch  
[Richten Sie Datenaustauschdefinitionen ein.](across-how-to-set-up-data-exchange-definitions.md)   
[Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md)   
[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
[Über das Datenaustauschframework](across-about-the-data-exchange-framework.md)
