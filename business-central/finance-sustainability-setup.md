---
title: Nachhaltigkeitseinrichtung
description: 'Erfahren Sie, wie Sie Nachhaltigkeitsfeatures einrichten.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Nachhaltigkeitseinrichtung

Bevor das Nachhaltigkeitsmodul richtig funktioniert, müssen Sie einige grundlegende Steuerelemente und Anweisungen festlegen, die mit der gesamten Funktionalität zusammenhängen.

Um ein Nachhaltigkeitsmodul einzurichten, gehen Sie wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Nachhaltigkeitseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Konfigurieren Sie auf dem Inforegister **Allgemein** die erforderlichen Felder, die mit dem Nachhaltigkeitsmodul zusammenhängen.

    | Feld | Description |
    |-------|-------------|
    | **Code der Emissionsmaßeinheit** | Geben Sie den Einheitencode an, der zum Registrieren der Emissionen verwendet wird. |
    | **Emissionsdezimalzahl Places** | Geben Sie die Anzahl der Nachkommastellen an, die bei Emissionsmengen angezeigt werden. Die Standardeinstellung *2:5* bedeutet, dass für alle Mengen mindestens zwei und höchstens fünf Nachkommastellen angezeigt werden. Sie können auch manuell eine feste Nummer eingeben. Wenn Sie beispielsweise *2* eingeben, werden alle Beträge mit zwei Dezimalstellen angezeigt. |
    | **Land/Region erforderlich** | Geben Sie an, ob Land/Region obligatorisch ist. Benutzende können das Feld „Land/Region“ in Buch.-Blättern festlegen, auch wenn Sie dieses Feld nicht auswählen. Wenn Sie diese Option auswählen, müssen Benutzende jedoch vor dem Posten das Feld „Land/Region“ festlegen. |
    | **Zuständigkeitseinheit obligatorisch** | Geben Sie an, ob die Zuständigkeitseinheit obligatorisch ist. Die Zuständigkeitseinheit kann als Anlage genutzt werden, sodass Sie anlagenbezogene Emissionen messen können. Benutzende können das Feld „Zuständigkeitseinheit“ in Buch.-Blättern festlegen, auch wenn Sie dieses Feld nicht auswählen. Wenn Sie diese Option auswählen, müssen Benutzende jedoch vor dem Posten das Feld „Zuständigkeitseinheit“ festlegen. |
    | **Änderung der Blockberechnungsgrundlage, wenn Posten vorhanden sind** | Geben Sie an, ob an der Berechnungsgrundlage (Formel) auf Ebene der Kontokategorie vorgenommene Änderungen zum Zeitpunkt der Nachhaltigkeitserfassung gesperrt sind, wenn die Formel bereits angewendet wurde. |
    | **Fehlerüberprüfung im Hintergrund aktivieren** | Geben Sie an, ob die Hintergrundfehlerprüfung von Nachhaltigkeits-Buch.-Blattzeilen aktiviert ist. |

    > [!NOTE]
    > Nachdem Sie die Hintergrundfehlerprüfung in Buch.-Blättern aktiviert bzw. deaktiviert haben, müssen Sie sich erneut anmelden, bevor Sie mit der neuen Einrichtung beginnen können.

3. Konfigurieren Sie auf dem Inforegister **Berechnungen** die erforderlichen Felder, die mit den zur Berechnung von Emissionen verwendeten Formeln zusammenhängen.

    | Feld | Description |
    |-------|-------------|
    | **Dezimalstellen Kraftstoff/Strom** | Geben Sie die Anzahl der Nachkommastellen an, die bei Kraftstoff-/Strommengen angezeigt werden. Die Standardeinstellung *2:5* bedeutet, dass für alle Mengen mindestens zwei und höchstens fünf Nachkommastellen angezeigt werden. Sie können auch manuell eine feste Nummer eingeben. Wenn Sie beispielsweise *2* eingeben, werden alle Beträge mit zwei Dezimalstellen angezeigt. |
    | **Dezimalstellen Entfernung** | Gebe Sie die Anzahl der Nachkommastellen an, die bei Entfernungsmessungen angezeigt werden. Die Standardeinstellung *2:5* bedeutet, dass für alle Mengen mindestens zwei und höchstens fünf Nachkommastellen angezeigt werden. Sie können auch manuell eine feste Nummer eingeben. Wenn Sie beispielsweise *2* eingeben, werden alle Beträge mit zwei Dezimalstellen angezeigt. |
    | **Benutzerdefinierte Mengendezimalstellen** | Geben Sie die Anzahl der Nachkommastellen an, die bei benutzerdefinierten Mengen angezeigt werden. Die Standardeinstellung *2:5* bedeutet, dass für alle Mengen mindestens zwei und höchstens fünf Nachkommastellen angezeigt werden. Sie können auch manuell eine feste Nummer eingeben. Wenn Sie beispielsweise *2* eingeben, werden alle Beträge mit zwei Dezimalstellen angezeigt. |

4. Schließen Sie die Einrichtung auf dem Inforegister **Berichterstellung** ab, indem Sie die Felder konfigurieren, die sich auf die Meldung an Behörden beziehen.

    > [!NOTE]
    > In Version 24.0 unterstützt [!INCLUDE[prod_short](includes/prod_short.md)] keine Meldung an Behörden. Daher sind die Felder, die sich auf die Konfiguration dieser Funktionalität auf dem Inforegister **Berichterstellung** beziehen, für zukünftige Berichtsfunktionen vorgesehen. Partner können diese Felder jedoch auch in lokalisierten Versionen verwenden.

    | Feld | Description |
    |-------|-------------|
    | **Einheitencode für die Emissionsberichterstattung** | Geben Sie den Einheitencode an, der zur Emissionsmeldung verwendet wird, da Sie bei der Meldung an die Behörden eventuell unterschiedliche Einheiten verwenden. Dieses Feld ist auf die Standardberichte nicht anwendbar. |
    | **Mengenfaktor für Berichterstattung** | Geben Sie den Einheitenfaktor an, der zur Emissionserfassung verwendet wird, wenn Sie bei der Meldung an die Behörden unterschiedliche Einheiten verwenden. |
    | **Emissionsrundungsgenauigkeit** | Geben Sie die Intervallgröße an, die beim Runden von Emissionsmengen bei der Meldung an Behörden verwendet wird. |
    | **Emissionsrundungsart** | Geben Sie an, wie das Programm bei der Meldung an Behörden Emissionsmengen rundet. Folgende Optionen stehen zur Verfügung: **Kaufmännisch**, **Aufrunden** und **Abrunden**. |

## Siehe auch

[Finanzen](finance.md)  
[Nachhaltigkeitsmanagement – Überblick](finance-manage-sustainability.md)  
[Nachhaltigkeitskontenplan und Nachhaltigkeitssachkonto](finance-sustainability-accounts-ledger.md)  
[Nachhaltigkeitsposten erfassen](finance-sustainability-journal.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
