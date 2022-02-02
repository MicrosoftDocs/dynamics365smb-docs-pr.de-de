---
title: Einrichten und Exportieren von Umsatzsteuervoranmeldungen
description: Um in Business Central gültige Umsatzsteuervoranmeldungen zu erstellen, müssen Sie die Erklärung und andere Einrichtungsseiten einrichten.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/21/2022
ms.author: soalex
ms.openlocfilehash: 9d218c2e8b69fc4a284ed0f2196acc2d649db78a
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2022
ms.locfileid: "8028948"
---
# <a name="set-up-and-export-sales-vat-advance-notifications"></a>Einrichten und Exportieren von Umsatzsteuervoranmeldungen

Eine Umsatzsteuervoranmeldung ist eine XML-Datei, die Sie verwenden können, um MwSt die deutsche Steuerbehörden an dem das Elektronische Steuererklärungen (ELSTER) - Onlineportal zu melden. [!INCLUDE [prod_short](../../includes/prod_short.md)] generiert eine XML-Datei mit Steuerbeträgen und Bemessungsgrundlagen sowie Informationen zu Ihrem Unternehmen im Format und im Layout, die deutsche Finanzämter benötigen.

> [!NOTE]
> Der größte Teil der Funktionen ist in der Erweiterung **ELSTER VAT-Lokalisierung für Deutschland** enthalten. Stellen Sie sicher, dass dies in Ihrem [!INCLUDE[prod_short](../../includes/prod_short.md)] installiert ist. Weitere Informationen finden Sie unter [Anpassen von Business Central Online mithilfe der Erweiterungen](../../ui-extensions.md).

## <a name="set-up-and-export-sales-vat-advance-notifications"></a>Umsatzsteuervoranmeldungen einrichten und exportieren

Sie müssen die folgenden Informationen einrichten, um gültige Umsatzsteuervoranmeldungen zu erstellen:  

- Die Firmendaten und die Steuerinformationen.  
- Grundlegende Umsatzsteuervoranmeldung auf der Seite **Elektronische Mehrwertsteuerdeklaration einrichten**.
- MwSt.-Abrechnung  

### <a name="to-set-up-company-information"></a>Um Unternehmensinformationen einzurichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **Unternehmensdaten** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder auf der Seite **Firmeninformationen** aus. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    Geben Sie speziell für Umsatzsteuervoranmeldungen im Feld **Steuerbevollmächtigter** die Kontaktperson für MwSt.-bezogene Informationen ein.  
3. Wählen Sie die Schaltfläche **OK**.  

### <a name="to-set-up-the-electronic-vat-declaration"></a>So richten Sie die elektronischen MwSt.-Anmeldung ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **Elektronische Umsatzsteuererklärung Einr.** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.

|Feld|Description|
|-----|-----|
|**USt.-Voranmeldungsnr.**|Wählen Sie den Nummernseriencode, der zum Zuweisen von Nummern zur Umsatzsteuervoranmeldung verwendet wird.|
|**USt.-Voranmeldungspfad**|Gibt den Pfad und den Namen des Ordners an, in dem Sie die XML-Dateien speichern möchten.|
|**Standardname der XML-Datei**|Geben Sie den Namen der Datei ein.|

### <a name="to-set-up-a-vat-statement-for-sales-vat-advance-notifications"></a>Um MwSt-Berichte für Umsatzsteuervoranmeldungs-Benachrichtigungen einzurichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **MwSt.-Abrechnung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **MwSt-Bericht** im Feld **Name**, den Drop-Down-Pfeil.  
3. Auf der Seite **MwSt.-Abrechnungsnamen** in der Zeile für den entsprechenden MwSt.-Abrechnungsnamen wählen Sie das Feld **Verkaufs MwSt-Benachrichtigung** aus.

    > [!NOTE]
    > Die MwSt.-Abrechnung muss eine MwSt.-Abrechnungszeile für jede Kennzahl aufweisen, die vom Finanzamt, in der **Zeilennr.** gefordert wird Feld enthält die Kennzahl und das Feld **Betragsart** gibt an, ob es sich um eine Bemessungsgrundlage oder um einen Steuerbetrag handelt. Wenden Sie sich an Ihr Finanzamt, wenn Fragen zu den Schlüsselnummern und ihrer Definition bestehen.

4. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-create-an-xml-document-for-sales-vat-advance-notification"></a>So erstellen Sie ein XML-Dokument für Umsatzsteuervoranmeldung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Umsatzsteuervoranmeldung** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Umsatzsteuervoranmeldungsliste** auf der Registerkarte Aktionen, wählen Sie **Neu** aus.  
3. Füllen Sie auf der Seite **MehrwertsteuerLagerortkarte** die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    > [!CAUTION]
    > Wenn Sie eine Umsatzsteuervoranmeldung durch Auswahl des Felds **Testversion** als Testmeldung eingereicht haben, können Sie sie später nicht in eine echte Meldung umwandeln. Die Steuerbehörde akzeptiert dieselbe XML-Datei nicht, wenn das Feld **Testversion** deaktiviert ist.

    Wählen Sie optional die Aktion **Vorschauversion der Erklärung anzeigen**, um eine MwSt.-Abrechnung mit den in der XML-Datei enthaltenen Daten anzuzeigen, die Sie an das ELSTER-Portal übermitteln. Diese Ansicht zeigt einen Betrag für jedes Element in der XML-Datei in einem visuell lesbaren Format.  

    > [!NOTE]
    > In Versionen älter als Version 19.3 und anderen Updates, die im Januar und Februar 2022 zur Verfügung gestellt werden, zeigt die Seite **USt.-Voranmeldungskarte** Felder und Aktionen basierend auf veralteten Funktionen des ELSTER-Portals und auf [!INCLUDE [prod_short](../../includes/prod_short.md)]. Insbesondere Felder, die an Stylesheets gebunden sind, werden nicht mehr verwendet, da das ELSTER-Portal solche Stylesheets nicht mehr bereitstellt.
4. Wählen Sie die Aktion **XML-Datei erstellen** aus.

5. Wählen Sie auf Seite **XML - MwSt Kontennachweis erstellen** im Feld **XML-Datei**, wählen Sie entweder **Erstellen** oder die Option **Erstellen und exportieren** aus.  

    Wenn Sie die Option **Erstellen und exportieren** auswählen, wird die XML-Datei generiert und auf Ihrem Gerät gespeichert. Wenn Sie die Option **Erstellen** auswählen, werden Daten in [!INCLUDE [prod_short](../../includes/prod_short.md)] generiert, die bei Auswahl der Aktion **Exportieren** auf der Seite **USt.-Voranmeldungskarte** als XML-Datei generiert werden.  
6. Wählen Sie die Schaltfläche **OK**.  

Nachdem das Dokument für die Umsatzsteuervoranmeldung erstellt wurde, können, mit Ausnahme des Felds **Beschreibung**, die Felder auf der Seite **USt.-Voranmeldungskarte** nicht mehr geändert werden, da sie den Inhalt des XML-Dokuments definieren. Wenn Sie ein XML-Dokument erstellt haben und für denselben Zeitraum ein neues XML-Dokument erstellen möchten, ohne das vorhandene Dokument an das Finanzamt zu übermitteln, müssen Sie die vorhandene XML-Datei löschen und anschließend das neue Dokument erstellen.

## <a name="see-also"></a>Weitere Informationen

[MwSt.-Abrechnung](vat-reporting.md)  
[Lokale Funktion (Deutschland)](germany-local-functionality.md)  
[Anpassen von Business Central mithilfe der Erweiterungen](../../ui-extensions.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]