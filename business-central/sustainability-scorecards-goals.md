---
title: Leitfäden und Ziele zur Nachhaltigkeit
description: 'Erfahren Sie, wie Sie Scorecards und Ziele zur Nachhaltigkeit einrichten und verwenden.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, scorecard, goal, forecast, budget'
ms.search.form: null
ms.date: 08/19/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# <a name="sustainability-scorecards-and-goals-overview"></a>Übersicht über Nachhaltigkeits-Scorecards und -Ziele

Dieser Artikel bietet Anleitungen zum Erstellen von Scorecards und Zielen sowie zum Aktualisieren des Zielstatus. Scorecards und Ziele ermöglichen es Unternehmen, Nachhaltigkeitskennzahlen zu erfassen und sie anhand wichtiger Geschäftsziele zu verfolgen. Ziele können auf Basis aktueller Werte und Zielwerte erstellt werden, sodass Benutzer die Entwicklung der aktuellen Emissionen im Vergleich zu früheren Zeiträumen verfolgen können.  

## <a name="create-a-scorecard"></a>Erstellen einer Scorecard

So erstellen Sie eine neue  *Nachhaltigkeits-Scorecard*: folgen Sie die folgenden Schritte:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, Symbol, geben Sie  **Sustainability Scorecards** und dann Auswählen das zugehörige verknüpfen ein. 
2. Klicken Sie auf der Seite  **Nachhaltigkeits-Scorecards**  auf Auswählen **Neu**, um eine neue Scorecard zu erstellen.  
3. Geben Sie die  **Nr. an.** Und die Felder  **Name**  auf der Registerkarte  **Allgemein**, und fügen Sie dann den  **Eigentümer** hinzu. 

> [HINWEIS!] Im Feld  **Eigentümer**  können Sie nur Benutzer auswählen, die in der Tabelle  **Benutzereinrichtung**  das Feld  **Sustainability Manager**  ausgewählt haben. 

## <a name="create-goals"></a>Ziele erstellen

Um ein neues  *Nachhaltigkeitsziel* zu erstellen, führen Sie die folgenden Schritte aus:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie  **Sustainability Scorecards** und dann Auswählen das zugehörige verknüpfen ein.
2. Wählen Sie die Aktion  **Ziele**  aus, um ein neues  **Nachhaltigkeitsziel**  für die ausgewählte Scorecard zu erstellen.  
3. Auswählen **Neu**, um mit der Erstellung eines neuen Ziels zu beginnen.
4. Die **Scorecard-Nr.** Wird automatisch basierend auf dem Wert der verbundenen  **Sustainability Scorecard** hinzugefügt und der Benutzer kann dieses Feld nicht bearbeiten. Das System richtet außerdem das Feld  **Maßeinheit**  basierend auf dem  **Emissionsmaßeinheitscode**  auf der Seite  **Nachhaltigkeitseinrichtung**  ein.  
5. Sie müssen die  **Nr. ausfüllen.** Und  **Name** des neuen  **Nachhaltigkeitsziels**. Das Feld  **Eigentümer**  wird automatisch anhand des Werts aus der verbundenen  **Sustainability Scorecard** ausgefüllt.   
6. Benutzer können beschließen, *Nachhaltigkeitsziele* für das gesamte Unternehmen, ein bestimmtes Land/eine bestimmte Region oder eine Einrichtung zu erstellen. Wenn Benutzer ein bestimmtes Ziel erstellen möchten, müssen sie im Feld  **Länder-/Regionscode**  das Land oder die Region oder im Feld  **Verantwortungszentrum**  die Einrichtung auswählen.  
7. Auswählen die Felder  **Startdatum** und  **Enddatum**, um einen dedizierten Zeitraum für die Verfolgung aktueller Werte einzurichten. Diese Konfiguration bestimmt die Werte in den folgenden Feldern:  **aktueller Wert für CO2**,  **aktueller Wert für CH4** und  **aktueller Wert für N2O**. 
8. Auswählen die Felder  **Basisstartdatum** und  **Basisenddatum**, um einen dedizierten Basiszeitraum für den Vergleich aktueller Werte einzurichten. Diese Konfiguration bestimmt die Werte in den folgenden Feldern:  **Basislinie für CO2**,  **Basislinie für CH4** und  **Basislinie für N2O**.
9. Darüber hinaus können Benutzer mithilfe der folgenden Felder Zielwerte im ausgewählten Feld  **Maßeinheit**  für den aktuellen Zeitraum hinzufügen:  **Zielwert für CO2**,  **Zielwert für CH4** und  **Zielwert für N2O**.   
10. Eines dieser Ziele kann als  **Hauptziel** ausgewählt werden. Werte aus dem Hauptziel werden im Rollencenter  **Sustainability Manager**  verwendet.  

Wenn Sie viele Ziele auf der Seite haben, können Sie die Aktion  **Meine Ziele anzeigen**  verwenden, um nur Ihre Ziele anzuzeigen. Wenn Sie alle anzeigen möchten, müssen Sie die Aktion  **Alle Ziele anzeigen**  ausführen.  

> [!NOTE]
> *Nachhaltigkeitsziele* können nur für eine bestimmte *Nachhaltigkeits-Scorecard* erstellt werden, und Sie können keine Ziele erstellen, die nicht mit der Scorecard in Zusammenhang stehen. Sie können jedoch mehrere Ziele für eine Scorecard erstellen. Sie können nur ein  **Nachhaltigkeitsziel**  als  **Hauptziel** kennzeichnen.

> [!NOTE]
> Benutzer können verschiedene Zielkombinationen für das gesamte Unternehmen, bestimmte Länder oder Regionen und ein Verantwortungszentrum für eine Nachhaltigkeits-Scorecard einrichten *.* Benutzer können für dasselbe Tracking-Modell auch unterschiedliche Zeiträume verwenden. 

## <a name="see-also"></a>Siehe auch

[Nachhaltigkeitseinrichtung](finance-sustainability-setup.md)    
[Diagramm der Nachhaltigkeitskonten und des Sachkontos](finance-sustainability-accounts-ledger.md)    
[So erfassen Sie Nachhaltigkeitseinträge](finance-sustainability-journal.md)    
[Ad-hoc-Analysen von Nachhaltigkeitsdaten](ad-hoc-analysis-sustainability.md)    
[Nachhaltigkeitsberichte und -analysen in Business Central](sustainability-reports.md)   
[Nachhaltigkeits-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Finanzen](finance.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
