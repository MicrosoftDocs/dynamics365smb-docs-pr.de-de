---
title: Nachhaltigkeitseinrichtung
description: 'Erfahren Sie, wie Sie Nachhaltigkeitsfeatures einrichten.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/24/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="sustainability-setup"></a>Nachhaltigkeitseinrichtung

Damit das Nachhaltigkeitsmodul ordnungsgemäß funktioniert, müssen Sie zunächst einige grundlegende Steuerelemente und Anweisungen für die gesamte Funktionalität einrichten.  

Um ein Nachhaltigkeitsmodul einzurichten, gehen Sie wie folgt vor:  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Nachhaltigkeitseinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Konfigurieren Sie auf dem Inforegister **Allgemein** die erforderlichen Felder für dieses Modul:   

|  Feld  |  Beschreibung  |  
|--------|--------------| 
| **Code der Emissionsmaßeinheit** | Gibt den Maßeinheitencode an, der zum Registrieren der Emissionen verwendet wird. |
| **Emissionsdezimalzahl Places** | Gibt die Anzahl der Nachkommastellen an, die bei Emissionsmengen angezeigt werden. Die Standardeinstellung 2:5 bewirkt, dass alle Mengen mit mindestens 2 und höchstens 5 Nachkommastellen angezeigt werden. Sie können auch eine feste Zahl eingeben, beispielsweise 2, was gleichzeitig zur Folge hat, dass Mengen mit zwei Nachkommastellen angezeigt werden. |
| **Land/Region erforderlich** | Gibt an, ob Land/Region obligatorisch ist. Sie können dieses Feld in Buch.-Blättern verwenden, ohne es zu konfigurieren. Sie können es jedoch auswählen, wenn Sie Benutzende dazu zwingen möchten, das Feld vor dem Buchen auszufüllen. |
| **Zuständigkeitseinheit obligatorisch** | Gibt an, ob die Angabe der Zuständigkeitseinheit obligatorisch ist, da es als Einrichtung zur Messung anlagenbezogener Emissionen verwendet werden kann. Sie können dieses Feld in Buch.-Blättern verwenden, ohne es zu konfigurieren. Sie können es jedoch auswählen, wenn Sie Benutzende dazu zwingen möchten, das Feld vor dem Buchen auszufüllen. |
| **Änderung der Blockberechnungsgrundlage, wenn Posten vorhanden sind** | Gibt an, ob zum Zeitpunkt der Nachhaltigkeitserfassung die Änderung der Berechnungsgrundlage in der Kontokategorie gesperrt ist, d. h., ob diese Formel bereits angewendet wurde. |
| **Fehlerüberprüfung im Hintergrund aktivieren** | Gibt an, ob die Hintergrundfehlerprüfung von Nachhaltigkeits-Buch.-Blattzeilen aktiviert ist. |

> [!NOTE]
> Nachdem Sie die **Hintergrundfehlerprüfung** in Buch.-Blättern aktiviert oder deaktiviert haben, müssen Sie sich erneut anmelden, bevor Sie mit der neuen Einrichtung beginnen.
 

3.  Konfigurieren Sie auf dem Inforegister **Berechnungen** die erforderlichen Felder im Zusammenhang mit den Formeln zur Berechnung der Emissionen:  

|  Feld  |  Beschreibung  |  
|--------|--------------| 
| **Dezimalstellen Kraftstoff/Strom** | Gibt die Anzahl der Nachkommastellen an, die bei Kraftstoff-/Strommengen angezeigt werden. Die Standardeinstellung 2:5 bewirkt, dass alle Mengen mit mindestens 2 und höchstens 5 Nachkommastellen angezeigt werden. Sie können auch eine feste Zahl eingeben, beispielsweise 2, was gleichzeitig zur Folge hat, dass Mengen mit zwei Nachkommastellen angezeigt werden. |
| **Dezimalstellen Entfernung** | Gibt die Anzahl der Nachkommastellen an, die bei Entfernungsmessungen angezeigt werden. Die Standardeinstellung 2:5 bewirkt, dass alle Mengen mit mindestens 2 und höchstens 5 Nachkommastellen angezeigt werden. Sie können auch eine feste Zahl eingeben, beispielsweise 2, was gleichzeitig zur Folge hat, dass Mengen mit zwei Nachkommastellen angezeigt werden. |
| **Benutzerdefinierte Mengendezimalstellen** | Gibt die Anzahl der Nachkommastellen an, die bei benutzerdefinierten Mengen angezeigt werden. Die Standardeinstellung 2:5 bewirkt, dass alle Mengen mit mindestens 2 und höchstens 5 Nachkommastellen angezeigt werden. Sie können auch eine feste Zahl eingeben, beispielsweise 2, was gleichzeitig zur Folge hat, dass Mengen mit zwei Nachkommastellen angezeigt werden. |

4.  Beenden Sie die Einrichtung auf dem Inforegister **Berichterstellung** im Zusammenhang mit der Meldung an Behörden:   

|  Feld  |  Beschreibung  |  
|--------|--------------| 
| **Einheitencode für die Emissionsberichterstattung** | Gibt den Einheitencode an, der zur Emissionsmeldung verwendet wird, da Sie bei der Meldung an die Behörden eventuell unterschiedliche Einheiten verwenden. Dieses Feld ist auf die Standardberichte nicht anwendbar. |
| **Mengenfaktor für Berichterstattung** | Gibt den Einheitenfaktor an, der zur Emissionserfassung verwendet wird, wenn Sie bei der Meldung an die Behörden unterschiedliche Einheiten verwenden. |
| **Emissionsrundungsgenauigkeit** | Gibt die Intervallgröße beim Runden von Emissionsmengen bei der Meldung an Behörden an. |
| **Emissionsrundungsart** | Gibt an, wie das Programm eine Emissionsmenge bei der Meldung an die Behörden mit den Optionen „Kaufmännisch“, „Aufrunden“ oder „Abrunden“ rundet. |

>[!NOTE]
> In Version 24.0 unterstützt [!INCLUDE[prod_short](includes/prod_short.md)] keine Meldung an eine Behörde. Das Feld für die Konfiguration auf dem Inforegister **Berichterstellung** wird für zukünftige Berichtsfunktionen verwendet, kann aber auch von Partnern in lokalisierten Versionen verwendet werden.

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Nachhaltigkeitsverwaltung – Übersicht](finance-manage-sustainability.md)    
[Diagramm der Nachhaltigkeitskonten und -posten](finance-sustainability-accounts-ledger.md)    
[Vorgehensweise: Erfassen von Emissionen](finance-sustainability-journal.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
