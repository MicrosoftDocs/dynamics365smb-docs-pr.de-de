---
title: 'Gewusst wie: Einrichten und Exportieren von Umsatzsteuervoranmeldungen'
description: In Business Central können Sie die Umsatzsteuervoranmeldungsdatei-Benachrichtigung elektronisch an das Portal übermitteln.
services: project-madeira
documentationcenter: ''
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/30/2018
ms.author: soalex
ms.openlocfilehash: abab79974e0cd60dd29941b44fe24b440c004f40
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "826711"
---
# <a name="sales-vat-advance-notifications"></a>Umsatzsteuervoranmeldungen  
Eine Umsatzsteuervoranmeldung in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] ist eine XML-Datei, die Sie verwenden können, um MwSt die deutsche Steuerbehörden an dem das Elektronische Steuererklärungen (ELSTER) - Onlineportal zu melden. Die XML-Datei enthält Steuerbeträge und Bemessungsgrundlagen und Informationen über den Mandanten und wird im Format und im Layout erstellt, die deutsche Finanzämter benötigen.    

## <a name="set-up-and-export-sales-vat-advance-notifications"></a>Einrichten und Exportieren von Umsatzsteuervoranmeldungen
Um gültige Umsatzsteuervoranmeldungen zu erstellen, müssen Sie Folgendes einrichten:  

- Die Firmendaten und die Steuerinformationen.  
- Grundlegende Umsatzsteuervoranmeldung auf der Seite **Elektronische Mehrwertsteuerdeklaration einrichten**. 
- MwSt.-Abrechnung  

### <a name="to-set-up-company-information"></a>Um Unternehmensinformationen einzurichten:  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol \"Nach Seite oder Bericht suchen\"") aus, geben Sie **Unternehmensdaten** ein, und wählen Sie dann den verknüpften Link aus.  
2. Auf der Seite **Firmendaten** im Inforegister Allgemein, im Feld **MwSt-Vertreter**, geben Sie die Kontaktperson für MwSt-bezogene Informationen ein.  
3. Wählen Sie die Schaltfläche **OK** aus.  

### <a name="to-set-up-the-electronic-vat-decl-setup"></a>Elektronische Mehrwertsteuerdeklaration einrichten
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Elektronische Mehrwertsteuerdeklaration einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.

|Feld|Description|
|-----|-----|
|**USt.-Voranmeldungsnr.**|Wählen Sie den Nummernseriencode, der zum Zuweisen von Nummern zur Umsatzsteuervoranmeldung verwendet wird.|
|**USt.-Voranmeldungspfad**|Gibt den Pfad und den Namen des Ordners an, in dem Sie die XML-Dateien speichern möchten.|
|**Standardname der XML-Datei**|Geben Sie den Namen der Datei ein.|

### <a name="to-set-up-a-vat-statement-for-sales-vat-advance-notifications"></a>Um MwSt-Berichte für Umsatzsteuervoranmeldungs-Benachrichtigungen einzurichten  
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **MwSt-Bericht** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Seite **MwSt-Bericht** im Feld **Name**, den Drop-Down-Pfeil.  
3.  Auf der Seite **MwSt.-Abrechnungsnamen** in der Zeile für den entsprechenden MwSt.-Abrechnungsnamen wählen Sie das Feld **Verkaufs MwSt-Benachrichtigung** aus. 

> [!NOTE]  
 >  Die MwSt.-Abrechnung muss eine MwSt.-Abrechnungszeile für jede Kennzahl aufweisen, die vom Finanzamt, in der **Zeilennr.** gefordert wird Feld enthält die Kennzahl und das Feld **Betragsart** gibt an, ob es sich um eine Bemessungsgrundlage oder um einen Steuerbetrag handelt. Wenden Sie sich an Ihr Finanzamt, wenn Fragen zu den Schlüsselnummern und ihrer Definition bestehen. 

4. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-create-an-xml-document-for-sales-vat-advance-notification"></a>So erstellen Sie ein XML-Dokument für Umsatzsteuervoranmeldung  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”") aus, und geben Sie **Umsatzsteuervoranmeldungsliste** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Auf der Seite **Umsatzsteuervoranmeldungsliste** auf der Registerkarte Aktionen, wählen Sie **Neu** aus.  
3. Füllen Sie auf der Seite **MehrwertsteuerLagerortkarte** die Felder nach Bedarf aus.
4. Wählen Sie **Verarbeiten** und wählen die **XML-Datei erstellen** Aktion aus.  
5. Wählen Sie auf Seite **Erstellen XML - MwSt Kontennachweis** im Feld **XML-Datei**, wählen Sie entweder **Erstellen** oder die Option **Erstellen und exportieren** aus.  
6. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch
[Lokale Funktion (Deutschland)](germany-local-functionality.md)