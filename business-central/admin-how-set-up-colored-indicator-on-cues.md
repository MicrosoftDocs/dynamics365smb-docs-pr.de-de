---
title: Richten Sie Ihre benutzerdefinierten Farbindikatoren für die Aktivität eines Cues ein
description: 'Als Administrator können Sie Stapel einrichten, die in den Rollencentern des Benutzers mit einem Indikator angezeigt werden, dessen Farbe sich basierend auf den Datenwerten in den Stapeln ändert.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: '9701, 9702'
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Einrichten eines farbigen Indikators auf Stapeln für das ganze Unternehmen oder einzelne Benutzer

Als Administrator können Sie Stapel einrichten, die in den Rollencentern des Benutzers mit einem Indikator angezeigt werden, dessen Farbe sich basierend auf den Datenwerten in den Stapeln ändert.  

Der Indikator erscheint als farbige Leiste an der oberen Kante der Stapelfläche. Es wird ein optisches Signal zu dem Status der Aktivität des Stapels angezeigt, dss Bedingungen (vorteilhaft oder ungünstig) angeben kann, und den Benutzer auffordern kann, Maßnahmen zu ergreifen. Wenn beispielsweise ein Stapel laufende Verkaufsrechnungen angezeigt, können Sie die Markierung so einrichten, dass sie grün (vorteilhaft) angezeigt wird, wenn die Gesamtanzahl laufender Verkaufsrechnungen unter 10 ist, und in Rot (ungünstig), wenn die Anzahl größer als 20 ist.  

Auf der Seite **Stapel einrichten** können Sie Indikatoren für alle Stapel einrichten, die in der Unternehmensdatenbank verfügbar sind. Sie können die Indikatoren so einrichten wollen, dass für alle Benutzer im Unternehmen oder nur für einen einzigen Benutzer gelten. Die Indikatoreinstellungen auf der Seite **Stapeleinrichtung** werden als Standard-Indikatoreinstellungen verwendet. Wenn die **Stapeleinrichtung Endnutzer**-Seite den Benutzern zugänglich gemacht wird, können sie die Indikatoreinstellungen personalisieren, die Sie im **Stapeleinrichtung**-Fenster festlegen.  

Um den Indikator einzurichten, geben Sie bis zu zwei Schwellenwerte an, die drei Bereiche von Datenwerten definieren (niedrig, mittel und hoch), die Sie jeweils mit einer anderen Farbe (oder einem anderen Format) anzeigen können.  

### So richten Sie farbige Indikatoren auf Stapeln ein.  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Stapeleinrichtung** ein und wählen Sie dann den zugehörigen Link.  

     Die Seite **Stapel einrichten** wird angezeigt. Auf der Seite sind die Indikatoren aufgelistet, die derzeit in Stapeln eingerichtet sind. Indikatoren, die für alle Benutzer im Unternehmen gelten, haben ein leeres **Benutzername**-Feld. Indikatoren, die für einen bestimmten Benutzer gelten, enthalten den **Benutzernamen** im -Feld.  

    > [!NOTE]  
    >  Wenn Sie einen Mandant-weiten Indikator einrichten und ein Benutzer diesen dann später ändert, dann erscheint ein separater Eintrag für den Indikator in der Liste für diesen Benutzer.  

2. Wählen Sie die Aktion **Liste bearbeiten** aus.  
3. Um einen Indikator für einen Stapel einzurichten, der nicht auf der Seite aufgeführt ist, wählen Sie **Neu** und füllen Sie dann die Felder aus, wie in der folgenden Tabelle beschrieben. Wenn Sie einen bestehenden Indikator ändern möchten, gehen Sie zum nächsten Schritt.  

    |  Feld  |  Description  |    
    |---------|---------------|  
    |**Benutzername**|Wenn Sie den Indikator für alle Benutzer einrichten möchten, lassen Sie das Feld leer.<br /><br /> Wenn Sie den Indikator für einen bestimmten Benutzer einrichten möchten, dann legen Sie als Wert für dieses Feld den Benutzernamen fest.|  
    |**Tabellennr.**|Gibt die Kennung der Objekt-Tabelle mit dem Stapel an. Verwenden Sie die Dropdownliste, um die Tabelle zu finden. Die Dropdownliste umfasst alle Stapeltabellen in der Datenbank.<br /><br /> Das **Tabellennamen**-Feld wird automatisch auf der Grundlage Ihrer Auswahl ausgefüllt.|  
    |**Feldnr.**|Gibt die ID ddes Stapels an, für den Sie einen Indikator einrichten möchten. Verwenden Sie die Dropdownliste, um den Stapel zu finden, den Sie anzeigen möchten. **Hinweis**: Die Stapel-ID entspricht der Feldnummer, die dem Stapel in der Tabelle zugewiesen wird. <br /><br /> Das **Feldname**-Feld wird automatisch auf der Grundlage Ihrer Auswahl ausgefüllt.|  

4. Um den Indikator für einen Stapel einzurichten, legen Sie die Felder fest, wie in der folgenden Tabelle beschrieben.  

    |  Feld  |  Description  |    
    |---------|---------------|  
    |**LowStyle**|Gibt die Farbe des Indikators an, wenn der Wert des Stapels unter dem Wert des **Schwellenwert 1**-Feldes ist.|  
    |**LowThreshold**|Gibt den Wert an, ab dem sich die Farbe des Indikators in die im Feld **Stil für mittleren Bereich** angegebene Farbe ändert.|  
    |**MiddleStyle**|Gibt die Farbe des Indikators an, wenn der Wert des Stapels größer oder gleich dem Wert im Feld **Schwellenwert 1**, jedoch kleiner oder gleich dem Wert im Feld **Schwellenwert 2** ist.|  
    |**HighThreshold**|Gibt den Wert an, ab dem sich die Farbe des Indikators in die im Feld **Stil für oberen Bereich** angegebene Farbe ändert.|  
    |**HighStyle**|Gibt die Farbe des Indikators an, wenn der Wert des Stapels über dem Wert des **Schwellenwert 2**-Feldes ist.|  

     Die folgende Tabelle enthält die Farben, die den Optionen der Felder **LowStyle**, **MiddleStyle** und **HighStyle** entsprechen.  

    |  Option  |  Farbe  |  
    |----------|---------|  
    |**"Keine"**|Keine Farbe (dieselbe Farbe wie die Stapelfläche)|  
    |**Vorteilhaft**|Grün|  
    |**Ungünstig**|Rot|  
    |**Mehrdeutig**|Gelb|  
    |**Untergeordnet**|Grau|  

## Siehe auch


[!INCLUDE[footer-include](includes/footer-banner.md)]