---
title: Behandlung fehlender Optionswerte
description: 'Erfahren Sie, wie Sie verhindern können, dass die vollständige Synchronisierung fehlschlägt, weil sich die Optionen in den zugeordneten Feldern unterscheiden. Dieser Prozess erfordert die Hilfe eines Entwicklers.'
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.date: 12/12/2023
ms.service: dynamics-365-business-central
---

# Behandlung fehlender Optionswerte
> [!NOTE]
> Im 1. Veröffentlichungszyklus 2022 können Sie Ihre eigenen Optionszuordnungen erstellen. Weitere Informationen finden Sie unter [Anpassen von Optionszuordnungen mit Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-option-mapping). Für die neuen Funktionen muss Ihr Administrator die Option **Funktionsupdate: Zuordnung zu Optionssätzen in Dataverse ohne Code** auf der Seite **Funktionsverwaltung** aktivieren. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Dieser Artikel richtet sich an ein technisches Publikum. Die darin beschriebenen Prozesse erfordern die Hilfe eines Entwicklers.

[!INCLUDE[prod_short](includes/cds_long_md.md)] enthält drei Optionssatzfelder, die Werte enthalten, die Sie [!INCLUDE[prod_short](includes/prod_short.md)] Feldern vom Typ „Option“ zur automatischen Synchronisation zuordnen können. Während der Synchronisation werden nicht abgebildete Optionen ignoriert und die fehlenden Optionen werden an die zugehörige [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle angehängt und der **Dataverse-Optionszuordnung**-Systemtabelle hinzugefügt, um später manuell behandelt zu werden. Zum Beispiel, indem er die fehlenden Optionen in einem der beiden Produkte hinzufügt und dann die Zuordnung aktualisiert.

Die Seite **Integration Tabellenzuordnung** enthält drei Felder, die einen oder mehrere zugeordnete Optionswerte enthalten. Nach einer vollständigen Synchronisierung enthält die Seite **Dataverse-Optionszuordnung** jeweils die nicht zugeordneten Optionen in den drei Feldern.

|         Datensatz             | Optionswert | Optionswert Beschriftung |
|----------------------------|--------------|----------------------|
| Zahlungsbedingungen: NET30       | 1            | Netto 30               |
| Zahlungsbedingungen: 2%10NET30   | 2            | 2% 10; Netto 30        |
| Zahlungsbedingungen: NET45       | 3            | Netto 45               |
| Zahlungsbedingungen: NET60       | 4            | Netto 60               |
| Lieferbedingung: FOB       | 1            | FOB                  |
| Lieferbedingung: NOCHARGE  | 2            | Keine Gebühr            |
| Spediteur: AIRBORNE   | 1            | Airborne             |
| Spediteur: DHL        | 2            | DHL                  |
| Spediteur: FEDEX      | 3            | FedEx                |
| Spediteur: UPS        | 4            | UPS                  |
| Spediteur: POSTMAIL | 5            | Postversand          |
| Spediteur: FULLLOAD   | 6            | Volle Belastung            |
| Spediteur: WILLCALL   | 7            | Will Call            |

Der Inhalt der Seite **Dataverse-Optionszuordnung** basiert auf Aufzählungswerten in der Tabelle **CRM -Konto**. In [!INCLUDE[prod_short](includes/cds_long_md.md)] werden die folgenden Felder auf der Kontotabelle den Feldern der Debitoren- und Kreditorendatensätze zugeordnet:

- **Adresse 1: Frachtbedingungen** vom Datentyp Enumeration, wobei die Werte wie folgt definiert sind:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Adresse 1: Lieferbedingung** vom Datentyp Enum, wobei die Werte wie folgt definiert sind:

```
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Zahlungsbedingungen** vom Datentyp Enum, wobei die Werte wie folgt definiert sind:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Alle obigen [!INCLUDE[prod_short](includes/prod_short.md)] Enums werden den Optionssätzen in [!INCLUDE[prod_short](includes/cds_long_md.md)] zugeordnet.

## Optionssätze in [!INCLUDE[prod_short](includes/prod_short.md)] erweitern
1. Erstellen Sie eine neue AL-Erweiterung.

2. Fügen Sie eine Enum-Erweiterung für die Optionen hinzu, die Sie erweitern möchten. Achten Sie darauf, dass Sie den gleichen Wert verwenden. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Sie müssen die gleichen Options-ID-Werte von [!INCLUDE[prod_short](includes/cds_long_md.md)] verwenden, wenn Sie die Aufzählung [!INCLUDE[prod_short](includes/prod_short.md)] erweitern. Andernfalls wird die Synchronisation fehlschlagen.

> [!IMPORTANT]  
> Verwenden Sie in Aufzählungswerten und Beschriftungen nicht das Zeichen „,“. Dieses Zeichen wird von der [!INCLUDE[prod_short](includes/prod_short.md)]-Laufzeit noch nicht unterstützt.

> [!NOTE]
> Die ersten zehn Zeichen der neuen Optionswertnamen und Beschriftungen müssen eindeutig sein. Beispielsweise führen zwei Optionen mit den Namen „Übertragung 20 Arbeitstage“ und „Übertragung 20 Kalendertage“ zu einem Fehler, da beide die gleichen ersten 10 Zeichen, „Übertragung 2“, haben. Nennen Sie sie z.B. „TRF20 WD“ und „TRF20 CD“.

## Die [!INCLUDE[prod_short](includes/cds_long_md.md)]-Optionszuordnung aktualisieren
Jetzt können Sie die Zuordnung zwischen [!INCLUDE[prod_short](includes/cds_long_md.md)]-Optionen und [!INCLUDE[prod_short](includes/prod_short.md)]-Einträgen neu erstellen.

Wählen Sie auf der Seite **Integration Tabellenzuordnung** die Zeile für die Karte **Zahlungsbedingungen** und wählen Sie dann die Aktion **Modifizierte Datensätze synchronisieren**. Die Seite **Dataverse Optionszuordnung** wird mit den zusätzlichen Datensätzen unten aktualisiert.

|         Datensatz                 | Optionswert   | Optionswert Beschriftung |
|--------------------------------|----------------|----------------------|
| Zahlungsbedingungen: NET30           | 1              | Netto 30               |
| Zahlungsbedingungen: 2%10NET30       | 2              | 2% 10; Netto 30        |
| Zahlungsbedingungen: NET45           | 3              | Netto 45               |
| Zahlungsbedingungen: NET60           | 4              | Netto 60               | 
| **Zahlungsbedingungen: BARZAHLUNG**  | **779800001**  | **Barzahlung**     |
| **Zahlungsbedingungen: ÜBERWEISUNG**    | **779800002**  | **Umlagerung**         |

Die Tabelle **Zahlungsbedingungen** in [!INCLUDE[prod_short](includes/prod_short.md)] enthält dann neue Datensätze für die Optionen [!INCLUDE[prod_short](includes/cds_long_md.md)]. In der folgenden Tabelle sind neue Optionen fettgedruckt. Kursiv gedruckte Zeilen stellen alle Optionen dar, die jetzt synchronisiert werden können. Die verbleibenden Zeilen stellen Optionen dar, die nicht verwendet und während der Synchronisierung ignoriert werden. Sie können sie entfernen oder Dataverse-Optionen mit den gleichen Namen erweitern).

| Code       | Berechnung Fälligkeitsdatum | Berechnung des Diskontierungsdatums | Ermäßigung in % | Rechnungsrab. Zahl. Verk. im Zinsrechnung | Beschreibung       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 TAGE    | 10T                  |                           | 0.         | FALSCH                         | Netto 10 Tage       |
| 14 TAGE    | 14T                  |                           | 0.         | FALSCH                         | Netto 14 Tage       |
| 15 TAGE    | 15T                  |                           | 0.         | FALSCH                         | Netto 15 Tage       |
| 1M(8T)     | 1M                   | 8T                        | 2.         | FALSCH                         | 1 Monat/2% 8 Tage |
| 2 TAGE     | 2D                   |                           | 0.         | FALSCH                         | Netto 2 Tage        |
| *2%10NET30* |                      |                           | 0.         | FALSCH                         |                   |
| 21 TAGE    | 21T                  |                           | 0.         | FALSCH                         | Netto 21 Tage       |
| 30 TAGE    | 30T                  |                           | 0.         | FALSCH                         | Netto 30 Tage       |
| 60 TAGE    | 60T                  |                           | 0.         | FALSCH                         | Netto 60 Tage       |
| 7 TAGE     | 7T                   |                           | 0.         | FALSCH                         | Netto 7 Tage        |
| ***BARZAHLUNG*** |                      |                           | 0.         | FALSCH                         |                   |
| LM         | LM                   |                           | 0.         | FALSCH                         | Aktueller Monat     |
| COD        | 0T                   |                           | 0.         | FALSCH                         | Nachnahme  |
| *NET30*      |                      |                           | 0.         | FALSCH                         |                   |
| *NET45*      |                      |                           | 0.         | FALSCH                         |                   |
| *NET60*      |                      |                           | 0.         | FALSCH                         |                   |
| ***UMLAG*** |                      |                           | 0.         | FALSCH                         |                   |

## Siehe auch
[Zu synchronisierende Tabellen und Felder zuordnen](admin-how-to-modify-table-mappings-for-synchronization.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]