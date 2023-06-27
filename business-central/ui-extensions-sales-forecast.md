---
title: 'Verkaufsaufträge und Lagerplanungserweiterung verwenden, um das Lager zu verwalten | Microsoft Docs'
description: 'Diese Erweiterung hilft Ihnen, Verkäufe zu planen und eine klare Übersicht über erwartete fehlende Lagerbestände zu erhalten und hilft Ihnen sogar dabei, Lagerauffüllungsanfragen an Verkäufer zu stellen.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 12/20/2021
ms.author: edupont
---

# <a name="the-sales-and-inventory-forecast-extension" />Die Verkaufs- und Bestandprognosen-Erweiterung

Lagerverwaltung ist ein Austausch zwischen Serviceabteilung und Verwaltung der Kosten. Auf der einen Seite benötigt ein niedriger Bestand weniger Betriebskapital, andererseits führen fehlende Lagerbestände evtl. zu entgangenen Verkäufen. Die Erweiterung "Geplanter voraussichtlicher Verkauf und Lagerbestand" sagt potenzielle Verkäufe anhand der historischen Daten voraus und gibt eine klare Übersicht über erwartete fehlende Lagerbestände. Auf Grundlage der Planung helfen die Erweiterungen dabei, Beschaffungsanfragen an Ihre Kreditoren zu stellen und Zeit zu spraren.  

## <a name="setting-up-forecasting" />Einrichten der Planung

In [!INCLUDE[prod_short](includes/prod_short.md)] ist die Verknüpfung zu [Azure AI](https://azure.microsoft.com/overview/ai-platform/) bereits eingerichtet. Sie können jedoch die Planung konfigurieren, um eine andere Art von Periode zu erfassen, zum Beispiel von der Planung nach Monaten auf die Planung nach Quartal. Sie können außerdem die Anzahl von Perioden zur Berechnung der Planung festlegen, abhängig davon, wie differenziert die Planung sein soll. Wir empfehlen, dass Sie die Planung nach Monaten und über einen Zeitraum von 12 Monaten prognostizieren.

> [!TIP]  
> Beachten Sie die Länge der Perioden, die der Service in den Berechnungen verwendet. Je mehr Daten Sie liefern, umso genauer wird die Vorhersage sein. Halten Sie auch nach umfangreichen Abweichungen in Perioden Ausschau. Sie werden ebenfalls Auswirkungen auf die Vorhersagen haben. Wenn Azure AI nicht genügend Daten findet oder die Daten stark variieren, wird der Dienst keine Vorhersage treffen.

## <a name="use-the-forecasts" />Planungen verwenden

Die Erweiterung verwendet Azure AI, um künftige Verkäufe basierend auf dem Verkaufsverlauf vorauszusagen und so fehlenden Lagerbestand zu vermeiden. Wenn Sie beispielsweise einen Artikel auf der Seite **Artikel** auswählen, zeigt das Diagramm im Bereich **Artikelplanung** die geschätzten Verkäufe dieses Artikels in der kommenden Periode an. Auf diese Weise können Sie sehen, ob der Artikel evtl. in Kürze nicht mehr am Lager sein wird.  

Sie können auch die Erweiterung verwenden, um vorzuschlagen, wann der Lagerbestand aufgefüllt werden soll. Wenn Sie beispielsweise eine Bestellung für Fabrikam erstellen, weil Sie den neuen Schreibtischstuhl von Fabrikam kaufen möchten, schlägt die Erweiterung „Verkaufs- und Bestandsprognose“ vor, dass Sie auch den LONDON-Drehstuhl, den Sie normalerweise bei diesem Anbieter kaufen, auffüllen. Der Grund dafür ist, dass die Erweiterung vorausplant, dass der LONDON-Schreibtischstuhl in den kommenden zwei Monaten nicht mehr am Lager verfügbar sein wird und Sie bereits jetzt mehr Stühle bestellen sollten.  

## <a name="design-details" />Einzelheiten zum Entwurf

Abonnements für [!INCLUDE[prod_short](includes/prod_short.md)] beinhalten den Zugang zu mehreren prädiktiven Webdiensten in allen Regionen, in denen [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar ist. Weitere Informationen finden Sie im Microsoft Dynamics 365 Business Central-Lizenzierungshandbuch. Der Leitfaden steht auf der Website [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/) zum Herunterladen zur Verfügung. 

Diese Webdienste sind zustandslos, d.h. sie verwenden Daten nur zur Berechnung von Vorhersagen bei Bedarf. Sie speichern keine Daten.

> [!NOTE]  
>   Sie können auch Ihren eigenen Vorhersage-Webdienst anstelle von unserem verwenden. Weitere Informationen finden Sie unter [Erstellen und verwenden Sie Ihren eigenen Prognose-Webservice für Verkaufs- und Bestandsprognosen](#AnchorText). 

### <a name="data-required-for-forecast" />Für die Prognose erforderliche Daten

Um Vorhersagen über zukünftige Verkäufe machen zu können, benötigt der Webservice quantitative Daten über vergangene Verkäufe. Diese Daten stammen aus den Feldern **Buchungsdatum**, **Positionsnummer** und **Menge** auf der Seite **Positionsledger-Einträge**, wobei folgendes gilt:

- Die Eintragsart ist „Verkauf“.
- Das Buchungsdatum liegt zwischen dem Datum, das auf der Grundlage der Werte in den Feldern **Historische Perioden** und **Periodentyp** auf der Seite **Verkaufs- und Bestandsprognoseeinrichtung** berechnet wird, und dem Arbeitsdatum.

Vor der Verwendung des Webdienstes komprimiert [!INCLUDE[prod_short](includes/prod_short.md)] Transaktionen um **Positionsnummer** und **Buchungsdatum** basierend auf dem Wert im Feld **Periodentyp** auf der Seite **Verkaufs- und Bestandsprognoseeinrichtung**.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts" /><a name="AnchorText"> </a>Erstellen und verwenden Sie Ihren eigenen Prognose-Webdienst für Verkaufs- und Bestandsprognosen

Sie können Ihren eigenen vorhersagenden Webdienst auf einem öffentliches Modell erzeugen, dem **Prognosemodell für Microsoft Business Central**. Dieses vorhersagende Modell ist online im Azure AI Katalog verfügbar. Um das Modell zu verwenden, gehen folgendermaßen vor:  

1. Öffnen Sie einem Browser und gehen Sie zum [Azure AI Katalog](https://go.microsoft.com/fwlink/?linkid=828352)  
2. Suchen Sie nach dem **Vorhersagemodell für Microsoft Business Central** und öffnen Sie dann das Modell im Azure Machine Learning Studio.  
3. Verwenden Sie das Microsoft-Konto, um sich für einen Arbeitsbereich anzumelden und kopieren Sie dann das Muster.  
4. Führen Sie die Vorlage aus und veröffentlichen Sie dieses als Webdienst.  
5. Notieren Sie den API URL und den API Schlüssel. Sie verwenden diese Anmeldeinformationen für die Cashfloweinrichtung.  
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einrichtung von Umsatz- und Lagerbestandsplanung** ein, und wählen Sie dann den entsprechenden Link.  
7. Erweitern Sie die Registerkarte **Allgemein** und füllen Sie dann die Felder API-URL und API-Schlüssel aus.  

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/use-sales-inventory-forecast-extension/)

## <a name="see-also" />Siehe auch

[Verkauf](sales-manage-sales.md)  
[Bestand](inventory-manage-inventory.md)  
[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe von Erweiterungen](ui-extensions.md)  
[Nutzen Sie künstliche Intelligenz in Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
