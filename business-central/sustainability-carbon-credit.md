---
title: Arbeiten mit Emissionszertifikaten
description: 'Erfahren Sie, wie Sie Emissionszertifikate einrichten und erwerben.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, carbon, credit, CO2'
ms.search.form: null
ms.date: 08/20/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# <a name="work-with-carbon-credit"></a>Arbeiten mit Emissionszertifikaten

Wenn Unternehmen aus verschiedenen Gründen ihre Emissionen nicht reduzieren können, können sie zum Ausgleich ihrer Emissionen Emissionsrechte erwerben. Durch den Kauf von Emissionszertifikaten kann ein Unternehmen weiterhin die gleiche Menge an Gasen ausstoßen und gleichzeitig CO2-neutral bleiben. Diese Gutschriften werden von spezialisierten Anbietern erworben und bieten Anreize für die Reduzierung der Emissionen.  

Im Allgemeinen handelt es sich bei Emissionsgutschriften um Genehmigungen, die ihrem Eigentümer den Ausstoß einer bestimmten Menge Kohlendioxid (CO₂) oder anderer Treibhausgase (THG) gestatten. Ein Emissionszertifikat berechtigt in der Regel zum Ausstoß einer Tonne CO₂ oder der entsprechenden Menge eines anderen Treibhausgases. Daher ist es wichtig, einigen Organisationen diese Option zu ermöglichen.  

## <a name="set-up-the-carbon-credit"></a>Richten Sie den CO2-Kredit ein

CO2-Guthaben kann als  [!INCLUDE[prod_short](includes/prod_short.md)] Artikel festgelegt werden **.** Um den **Artikel** als CO2-Gutschrift einzurichten, folgen Sie die folgenden Schritte:
  
1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, Symbol, geben Sie **Artikel** ein, und wählen Sie dann den entsprechenden Link aus. 
2. [Erstellen Sie wie erläutert ein neues Element](inventory-how-register-new-items.md).   
3. Sobald das Element erstellt ist, Auswählen das Feld  **Treibhausgasgutschrift**  auf der Registerkarte  **Nachhaltigkeit**  und fügen Sie den Wert der CO2-Gutschrift mithilfe des Felds  **CO2-Gutschrift pro ME**  hinzu.

> [!NOTE]
> **„CO2-Gutschrift pro Maßeinheit“** stellt die CO2-Menge in der Maßeinheit dar, die im  **Code der Emissionsmaßeinheit** im  **Nachhaltigkeits-Setup** konfiguriert ist. Damit ist der Gesamtwert der CO2-Gutschrift als die Menge an gutgeschriebenem CO₂ pro  **Basismaßeinheit** gebrauchtem Gegenstand gemeint.  

> [!NOTE]
> Sie können für jeden Artikeltyp (Inventar, Dienstleistung oder Nicht-Inventar) eine CO2-Gutschrift einrichten.  

## <a name="to-purchase-carbon-credit"></a>Um Emissionsrechte zu erwerben

### <a name="purchase-documents"></a>Kauf Belege

Um mit kaufbezogenen Dokumenten zu arbeiten, folgen Sie die Schritte:

1. Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol und:  
   1. Geben Sie  **Einkaufsrechnungen**  ein, wenn Sie eine Rechnung als  **Dokumenttyp** wünschen, und Auswählen Sie dann die zugehörige verknüpfen.  
   2. Geben Sie  **Bestellungen**  ein, wenn Sie als  **Dokumententyp** bestellen möchten, und Auswählen Sie dann das zugehörige verknüpfen.   
2. Füllen Sie den Dokumentkopf anhand der folgenden Anleitung  [zum Arbeiten mit Einkaufsrechnungen und Bestellungen](purchasing-how-record-purchases.md) aus. 
3. Wählen Sie unter  **Nr. den als CO2-Gutschrift konfigurierten Artikel aus.** In den Einkaufsbelegzeilen und fügen Sie die entsprechende  **Menge** und  **Direkte Stückkosten** hinzu. 
4. Fügen Sie die  **Nachhaltigkeitskontonummer**  hinzu, die Sie zur Senkung Ihres Kohlendioxidwerts (CO₂) verwenden würden. Das System trägt den Wert im Feld  **CO2-Emission**  automatisch ein, basierend auf dem Wert, den Sie im Feld  **CO2-Gutschrift pro ME**  unter  **Artikel** Karte konfiguriert haben.
5. Buchen Sie den Beleg

> [!NOTE]
> Obwohl sich durch die Emissionsgutschrift der Wert der Einträge verringert, wird unter  **CO2-Emission** ein positiver Wert ausgewiesen. Wenn Sie das Dokument jedoch buchen, wird im  **Nachhaltigkeitshauptbucheintrag**  mit der  **Treibhausgasgutschrift**  als  **Dokumentart** ein Wert mit einem negativen Logarithmus angezeigt.  

### <a name="sustainability-journals"></a>Nachhaltigkeits-Buch.-Blätter

So arbeiten Sie mit dem **Sustainability Journal** folgen:  

1. Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Nachhaltigkeits-Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link. 
2. Geben Sie auf der Seite  **Sustainability Journal**  so viele Zeilen ein, wie Sie im selben Stapel veröffentlichen möchten.  
3. Wählen Sie im Feld  **Dokumenttyp**  die  **Treibhausgasgutschrift**  aus.    
4. Im Feld **Kontonr.** können Sie nur nicht gesperrte Nachhaltigkeitskonten auswählen, wenn das Feld **Direktbuchung** ausgewählt ist und das Feld **Buchungsart** auf **Buchung** festgelegt ist. Außerdem muss für die Konten eine Kategorie und eine Unterkategorie konfiguriert sein. Wählen Sie das entsprechende Konto zum Buchen von Emissionsgutschriften aus.
5. Auswählen **Manuelle Eingabe** und geben Sie den Wert, den Sie als CO2-Gutschrift buchen möchten, in das Feld **CO2-Emission**  ein.  
6. Buchen Sie die Buch.-Blattzeile.   

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)    
[Nachhaltigkeitsposten erfassen](finance-sustainability-journal.md)    
[Nachhaltigkeitsverwaltung – Übersicht](finance-manage-sustainability.md)    
[Nachhaltigkeitseinrichtung](finance-sustainability-setup.md)   
[Diagramm der Nachhaltigkeitskonten und -posten](finance-sustainability-accounts-ledger.md)  
[Ad-hoc-Analysen von Nachhaltigkeitsdaten](ad-hoc-analysis-sustainability.md)    
[Nachhaltigkeitsberichte und Analysen in [!INCLUDE[prod_short](includes/prod_short.md)]](sustainability-reports.md)   
[Nachhaltigkeits-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
