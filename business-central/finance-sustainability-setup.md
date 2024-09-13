---
title: Nachhaltigkeitseinrichtung
description: 'Erfahren Sie, wie Sie Nachhaltigkeitsfeatures einrichten.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, equivalent, CO2e, CO2, carbon, role center, fees'
ms.search.form: '6221, 6235, 6245'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-module-setup"></a>Aufbau des Nachhaltigkeitsmoduls

Bevor das Nachhaltigkeitsmodul richtig funktioniert, müssen Sie einige grundlegende Steuerelemente und Anweisungen festlegen, die mit der gesamten Funktionalität zusammenhängen.

Um ein Nachhaltigkeitsmodul einzurichten, gehen Sie wie folgt vor:

## <a name="role-center"></a>Rollencenter

Für Personen, deren Hauptverantwortung Nachhaltigkeitsprozesse umfasst, wird empfohlen, das Rollencenter  *Sustainability Manager*  zu nutzen. Um dieses Rollencenter zu konfigurieren, folgen die Schritte:  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, Symbol, geben Sie  **Meine Einstellungen** ein und Auswählen dann das zugehörige verknüpfen.
2. Auswählen im Feld  **Rolle**  die Seite  **Verfügbare Rollen** .
3. Wählen Sie die Zeile  **Sustainability Manager** .
4. Wählen Sie **OK** aus.

Das Rollencenter  *Sustainability Manager*  ermöglicht die effiziente Verwaltung aller wichtigen Bereiche im Zusammenhang mit Nachhaltigkeit. Es umfasst zentrale Nachhaltigkeitsmerkmale sowie Finanz- und Beschaffungsprozesse. Darüber hinaus bietet es Einblick in die wichtigsten KPIs im Zusammenhang mit Nachhaltigkeit.

## <a name="sustainability-setup"></a>Nachhaltigkeitseinrichtung

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

3. Konfigurieren Sie auf der Registerkarte  **Beschaffung**  die erforderlichen Felder, die sich auf die Verwendung von Nachhaltigkeitsfunktionen im Einkaufsprozess beziehen.  

    | Feld | Description |
    |-------|-------------|
    | **Emissionen in Einkaufsdokumenten verwenden** | Wenn Sie dieses Feld aktivieren, werden in den Einkaufsdokumenten nachhaltigkeitsrelevante Felder und Merkmale angezeigt, wie beispielsweise ein  **Nachhaltigkeitskonto**  oder unterschiedliche Emissionen. |

4. Konfigurieren Sie auf dem Inforegister **Berechnungen** die erforderlichen Felder, die mit den zur Berechnung von Emissionen verwendeten Formeln zusammenhängen.

    | Feld | Description |
    |-------|-------------|
    | **Dezimalstellen Kraftstoff/Strom** | Geben Sie die Anzahl der Nachkommastellen an, die bei Kraftstoff-/Strommengen angezeigt werden. Die Standardeinstellung *2:5* bedeutet, dass für alle Mengen mindestens zwei und höchstens fünf Nachkommastellen angezeigt werden. Sie können auch manuell eine feste Nummer eingeben. Wenn Sie beispielsweise *2* eingeben, werden alle Beträge mit zwei Dezimalstellen angezeigt. |
    | **Dezimalstellen Entfernung** | Gebe Sie die Anzahl der Nachkommastellen an, die bei Entfernungsmessungen angezeigt werden. Die Standardeinstellung *2:5* bedeutet, dass für alle Mengen mindestens zwei und höchstens fünf Nachkommastellen angezeigt werden. Sie können auch manuell eine feste Nummer eingeben. Wenn Sie beispielsweise *2* eingeben, werden alle Beträge mit zwei Dezimalstellen angezeigt. |
    | **Benutzerdefinierte Mengendezimalstellen** | Geben Sie die Anzahl der Nachkommastellen an, die bei benutzerdefinierten Mengen angezeigt werden. Die Standardeinstellung *2:5* bedeutet, dass für alle Mengen mindestens zwei und höchstens fünf Nachkommastellen angezeigt werden. Sie können auch manuell eine feste Nummer eingeben. Wenn Sie beispielsweise *2* eingeben, werden alle Beträge mit zwei Dezimalstellen angezeigt. |

5. Schließen Sie die Einrichtung auf dem Inforegister **Berichterstellung** ab, indem Sie die Felder konfigurieren, die sich auf die Meldung an Behörden beziehen.

    > [!NOTE]
    > In Version 24.0 unterstützt [!INCLUDE[prod_short](includes/prod_short.md)] keine Meldung an Behörden. Daher sind die Felder, die sich auf die Konfiguration dieser Funktionalität auf dem Inforegister **Berichterstellung** beziehen, für zukünftige Berichtsfunktionen vorgesehen. Partner können diese Felder jedoch auch in lokalisierten Versionen verwenden.

    | Feld | Description |
    |-------|-------------|
    | **Einheitencode für die Emissionsberichterstattung** | Geben Sie den Einheitencode an, der zur Emissionsmeldung verwendet wird, da Sie bei der Meldung an die Behörden eventuell unterschiedliche Einheiten verwenden. Dieses Feld ist auf die Standardberichte nicht anwendbar. |
    | **Mengenfaktor für Berichterstattung** | Geben Sie den Einheitenfaktor an, der zur Emissionserfassung verwendet wird, wenn Sie bei der Meldung an die Behörden unterschiedliche Einheiten verwenden. |
    | **Emissionsrundungsgenauigkeit** | Geben Sie die Intervallgröße an, die beim Runden von Emissionsmengen bei der Meldung an Behörden verwendet wird. |
    | **Emissionsrundungsart** | Geben Sie an, wie das Programm bei der Meldung an Behörden Emissionsmengen rundet. Folgende Optionen stehen zur Verfügung: **Kaufmännisch**, **Aufrunden** und **Abrunden**. |

## <a name="emission-fees"></a>Emissionsgebühren

Um interne CO2-Gebühren zu verfolgen oder Ihre Emissionen anhand von Kohlendioxid-Äquivalenten (CO2) zu berechnen, müssen Sie die Seite  **Emissionsgebühren**  konfigurieren. Um diese Informationen einzurichten, folgen diese Schritte:  

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie  **Emissionsgebühren** ein und Auswählen dann das zugehörige verknüpfen. 
2. Wählen Sie im Feld  **Emissionstyp**  die Treibhausgasemission aus, die Sie konfigurieren möchten:  **CO2**,  **CH4** oder  **N2O**. Diese Option ist obligatorisch.   
3. Sie können den  **Bereichstyp** weiter spezifizieren. Wenn Sie dieses Feld leer lassen, gilt es für alle Bereiche, Sie können es aber für jeden Bereich konfigurieren.  
4. Sie können das  **Startdatum** und das  **Enddatum** konfigurieren. Das bedeutet insbesondere, dass Sie für unterschiedliche Zeiträume unterschiedliche Konfigurationen verwenden können. 
5. Der  **Länder-/Regionscode** und der  **Verantwortungscode** sind optionale Felder und Sie können auswählen, ob Sie sie verwenden möchten. Diese Felder können nützlich sein, da es möglich ist, je nach Land unterschiedliche CO2-Abgaben zu erheben oder unterschiedliche Umrechnungen in CO2e je nach Land oder Einrichtung (Verantwortungszentrum) zu verwenden.  
6. Das Feld  **CO₂-Gebühr**  stellt die interne Gebühr CO₂-Gebühr dar, die sich ein Unternehmen für jede Einheit CO2-Äquivalent in Rechnung stellt, die es ausstößt. Es kann auf der Grundlage bestimmter lokaler oder regionaler Vorschriften, aber auch für interne Berechnungen verwendet werden. **CO₂-Gebühr** wird jedes Mal berechnet, wenn Sie Emissionen buchen, und diese Information wird in den  **Nachhaltigkeitshauptbucheinträgen** angezeigt, ohne dass eine zusätzliche Buchung im  **Hauptbuch** erforderlich ist. Sie können  **CO₂-Gebühr** pro Maßeinheit einrichten, die Sie im  **Nachhaltigkeits-Setup**  haben, und es kann nur für die Zeile ausgefüllt werden, in der der  **Emissionstyp**  **CO2** ist. 
7. Der  **Kohlenstoffäquivalentfaktor** gibt den Koeffizienten an, der die Auswirkungen verschiedener Treibhausgase auf der Grundlage ihres Treibhauspotenzials in die Äquivalentmenge an Kohlendioxid umrechnet. Wenn der  **Emissionstyp** CO2 ist, beträgt der  **Kohlenstoffäquivalentfaktor** immer  *1*  und Sie können diesen Wert nicht ändern, da CO2 das Referenzgas ist, das zur Berechnung des Treibhauseffektpotenzials (GWP) anderer Treibhausgase verwendet wird. Da CO2 die Basis darstellt, wird sein GWP auf  *1* gesetzt. Für andere Treibhausgase müssen Benutzer die Werte manuell konfigurieren. Zur korrekten Berechnung können Sie das folgende Beispiel verwenden: Wenn wir davon ausgehen, dass 1 Kilogramm N2O 298 Kilogramm CO2 entspricht, müssen Sie 1/298 berechnen und das einzutragende Ergebnis lautet 0.00336.  

> [!NOTE]
> **Das Feld** CO₂-Gebühr im Feld  **Nachhaltigkeitshauptbucheinträge** wird nicht auf Grundlage der  **CO2-Emissionswerte** berechnet. Stattdessen wird als Grundlage für diese Formel das Feld  [!INCLUDE[prod_short](includes/prod_short.md)] CO2e-Emissionen **verwendet.**  **Das Feld „CO2e-Emissionen“**  wird auf Grundlage aller im Eintrag angegebenen Emissionen und des für jedes Gas auf der Seite  **Emissionsgebühren**  konfigurierten  **Kohlenstoffäquivalentfaktors**  berechnet.  

Wenn Sie die  **Emissionsgebühren**  vor der Buchung Ihrer Nachhaltigkeitseinträge nicht konfiguriert haben und Ihre CO2-Gebühren und CO2e nachträglich berechnen möchten, müssen Sie die Aktion  **Emissionsgebühren berechnen**  ausführen, um die Werte in den  **Nachhaltigkeitshauptbucheinträgen** zu aktualisieren.  

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)    
[Nachhaltigkeitsverwaltung – Übersicht](finance-manage-sustainability.md)    
[Diagramm der Nachhaltigkeitskonten und des Sachkontos](finance-sustainability-accounts-ledger.md)    
[Nachhaltigkeitsposten erfassen](finance-sustainability-journal.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
