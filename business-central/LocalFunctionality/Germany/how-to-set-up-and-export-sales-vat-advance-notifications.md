---
title: 'Gewusst wie: Einrichten und Exportieren von Umsatzsteuervoranmeldungen'
description: In Business Central können Sie die Umsatzsteuervoranmeldungsdatei-Benachrichtigung elektronisch an das Portal übermitteln.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: soalex
ms.openlocfilehash: 7af3ad9bd1684b069148b4e00d63037a1abb4ff3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920060"
---
# <a name="sales-vat-advance-notifications"></a>Umsatzsteuervoranmeldungen  
Eine Umsatzsteuervoranmeldung in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] ist eine XML-Datei, die Sie verwenden können, um MwSt die deutsche Steuerbehörden an dem das Elektronische Steuererklärungen (ELSTER) - Onlineportal zu melden. Die XML-Datei enthält Steuerbeträge und Bemessungsgrundlagen und Informationen über den Mandanten und wird im Format und im Layout erstellt, die deutsche Finanzämter benötigen.    

> [!NOTE]
 >  Der größte Teil der Funktionen ist in der Erweiterung **ELSTER VAT-Lokalisierung für Deutschland** enthalten. Stellen Sie sicher, dass dies in Ihrem [!INCLUDE[prodshort](../../includes/prodshort.md)] installiert ist.
 
 
## <a name="set-up-and-export-sales-vat-advance-notifications"></a>Einrichten und Exportieren von Umsatzsteuervoranmeldungen
Um gültige Umsatzsteuervoranmeldungen zu erstellen, müssen Sie Folgendes einrichten:  

- Die Firmendaten und die Steuerinformationen.  
- Grundlegende Umsatzsteuervoranmeldung auf der Seite **Elektronische Mehrwertsteuerdeklaration einrichten**.
- MwSt.-Abrechnung  

### <a name="to-set-up-company-information"></a>Um Unternehmensinformationen einzurichten:  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Unternehmensinformationen** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Firmendaten** im Inforegister Allgemein, im Feld **MwSt-Vertreter**, geben Sie die Kontaktperson für MwSt-bezogene Informationen ein.  
3. Wählen Sie die Schaltfläche **OK** aus.  

### <a name="to-set-up-the-electronic-vat-decl-setup"></a>Elektronische Mehrwertsteuerdeklaration einrichten
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Electronic VAT-Erkl.-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.

|Feld|Description|
|-----|-----|
|**USt.-Voranmeldungsnr.**|Wählen Sie den Nummernseriencode, der zum Zuweisen von Nummern zur Umsatzsteuervoranmeldung verwendet wird.|
|**USt.-Voranmeldungspfad**|Gibt den Pfad und den Namen des Ordners an, in dem Sie die XML-Dateien speichern möchten.|
|**Standardname der XML-Datei**|Geben Sie den Namen der Datei ein.|

### <a name="to-set-up-a-vat-statement-for-sales-vat-advance-notifications"></a>Um MwSt-Berichte für Umsatzsteuervoranmeldungs-Benachrichtigungen einzurichten  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") öffnet, geben Sie **MwSt.-Abrechnung** ein, und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie auf der Seite **MwSt-Bericht** im Feld **Name**, den Drop-Down-Pfeil.  
3.  Auf der Seite **MwSt.-Abrechnungsnamen** in der Zeile für den entsprechenden MwSt.-Abrechnungsnamen wählen Sie das Feld **Verkaufs MwSt-Benachrichtigung** aus.

> [!NOTE]  
 >  Die MwSt.-Abrechnung muss eine MwSt.-Abrechnungszeile für jede Kennzahl aufweisen, die vom Finanzamt, in der **Zeilennr.** gefordert wird Feld enthält die Kennzahl und das Feld **Betragsart** gibt an, ob es sich um eine Bemessungsgrundlage oder um einen Steuerbetrag handelt. Wenden Sie sich an Ihr Finanzamt, wenn Fragen zu den Schlüsselnummern und ihrer Definition bestehen.

4. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-create-an-xml-document-for-sales-vat-advance-notification"></a>So erstellen Sie ein XML-Dokument für Umsatzsteuervoranmeldung  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Umsatzsteuer-Vorankündigungsliste** ein, und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Umsatzsteuervoranmeldungsliste** auf der Registerkarte Aktionen, wählen Sie **Neu** aus.  
3. Füllen Sie auf der Seite **MehrwertsteuerLagerortkarte** die Felder nach Bedarf aus.
4. Wählen Sie **Verarbeiten** und wählen die **XML-Datei erstellen** Aktion aus.  
5. Wählen Sie auf Seite **XML - MwSt Kontennachweis erstellen** im Feld **XML-Datei**, wählen Sie entweder **Erstellen** oder die Option **Erstellen und exportieren** aus.  
6. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch
[MwSt.-Abrechnung](vat-reporting.md)  
[Lokale Funktion (Deutschland)](germany-local-functionality.md)  
[Anpassen von Business Central mithilfe der Erweiterungen](../../ui-extensions.md)  
