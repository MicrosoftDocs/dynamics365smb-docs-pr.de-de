---
title: 'Verkaufs- und Lagerbestandsplanungserweiterung verwenden, um den Lagerbestand zu verwalten'
description: 'Diese Erweiterung hilft Ihnen, Verkäufe zu planen und eine klare Übersicht über erwartete fehlende Lagerbestände zu erhalten und hilft Ihnen sogar dabei, Lagerauffüllungsanfragen an Verkäufer zu stellen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 07/01/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-sales-and-inventory-forecast-extension"></a>Die Verkaufs- und Lagebestandsplanungserweiterung

Lagerverwaltung ist ein Austausch zwischen Serviceabteilung und Verwaltung der Kosten. Auf der einen Seite benötigt ein niedriger Bestand weniger Betriebskapital, andererseits führen fehlende Lagerbestände evtl. zu entgangenen Verkäufen. Die Erweiterung "Geplanter voraussichtlicher Verkauf und Lagerbestand" sagt potenzielle Verkäufe anhand der historischen Daten voraus und gibt eine klare Übersicht über erwartete fehlende Lagerbestände. Auf Grundlage der Planung helfen die Erweiterungen dabei, Beschaffungsanfragen an Ihre Kreditoren zu stellen und Zeit zu spraren.  

## <a name="setting-up-forecasting"></a>Einrichten der Planung

In [!INCLUDE[prod_short](includes/prod_short.md)] ist die Verknüpfung zu [Azure AI](https://azure.microsoft.com/overview/ai-platform/) bereits eingerichtet. Sie können jedoch die Planung konfigurieren, um eine andere Art von Periode zu erfassen, zum Beispiel von der Planung nach Monaten auf die Planung nach Quartal. Sie können außerdem die Anzahl von Perioden zur Berechnung der Planung festlegen, abhängig davon, wie differenziert die Planung sein soll. Wir empfehlen, dass Sie die Planung nach Monaten und über einen Zeitraum von 12 Monaten prognostizieren.

> [!TIP]  
> Beachten Sie die Länge der Perioden, die der Service in den Berechnungen verwendet. Je mehr Daten Sie liefern, umso genauer wird die Vorhersage sein. Halten Sie auch nach umfangreichen Abweichungen in Perioden Ausschau. Sie werden ebenfalls Auswirkungen auf die Vorhersagen haben. Wenn Azure AI nicht genügend Daten findet oder die Daten stark variieren, wird der Dienst keine Vorhersage treffen.

## <a name="use-the-forecasts"></a>Planungen verwenden

Die Erweiterung verwendet Azure AI, um künftige Verkäufe basierend auf dem Verkaufsverlauf vorauszusagen und so fehlenden Lagerbestand zu vermeiden. Wenn Sie beispielsweise einen Artikel auf der Seite **Artikel** auswählen, zeigt das Diagramm im Bereich **Artikelplanung** die geschätzten Verkäufe dieses Artikels in der kommenden Periode an. Auf diese Weise können Sie sehen, ob der Artikel evtl. in Kürze nicht mehr auf Lager sein wird.  

Sie können auch die Erweiterung verwenden, um vorzuschlagen, wann der Lagerbestand aufgefüllt werden soll. Angenommen, Sie erstellen eine Bestellung für Fabrikam zum Kauf eines neuen Schreibtischstuhls. Die Verkaufs- und Lagerbestandsplanungserweiterung schlägt Ihnen möglicherweise vor, auch den Lagerbestand des Drehstuhls LONDON aufzufüllen, den Sie normalerweise von diesem Anbieter kaufen. Die Erweiterung kann prognostizieren, dass der LONDON-Schreibtischstuhl bald nicht mehr auf Lager sein wird, also ist es vielleicht eine gute Idee, schon jetzt mehr Stühle zu bestellen.  

## <a name="design-details"></a>Designdetails

Abonnements für [!INCLUDE[prod_short](includes/prod_short.md)] beinhalten den Zugang zu mehreren prädiktiven Webdiensten in allen Regionen, in denen [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar ist. Weitere Informationen finden Sie im Microsoft Dynamics 365 Business Central-Lizenzierungshandbuch. Der Leitfaden steht auf der Website [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/) zum Herunterladen zur Verfügung. 

Diese Webdienste sind zustandslos, d.h. sie verwenden Daten nur zur Berechnung von Vorhersagen bei Bedarf. Sie speichern keine Daten.

> [!NOTE]  
>   Sie können auch Ihren eigenen Vorhersage-Webdienst anstelle von unserem verwenden. Weitere Informationen finden Sie unter [Erstellen und verwenden Sie Ihren eigenen Prognose-Webservice für Verkaufs- und Bestandsprognosen](#AnchorText). 

### <a name="data-required-for-forecast"></a>Für die Prognose erforderliche Daten

Um Vorhersagen über zukünftige Verkäufe machen zu können, benötigt der Webservice quantitative Daten über vergangene Verkäufe. Diese Daten stammen aus den Feldern **Buchungsdatum**, **Positionsnummer** und **Menge** auf der Seite **Positionsledger-Einträge**, wobei folgendes gilt:

- Die Eintragsart ist „Verkauf“.
- Das Buchungsdatum liegt zwischen dem Datum, das auf der Grundlage der Werte in den Feldern **Historische Perioden** und **Periodentyp** auf der Seite **Verkaufs- und Bestandsprognoseeinrichtung** berechnet wird, und dem Arbeitsdatum.

Vor der Verwendung des Webdienstes komprimiert [!INCLUDE[prod_short](includes/prod_short.md)] Transaktionen nach **Positionsnummer** und **Buchungsdatum** basierend auf dem Wert im Feld **Periodentyp** auf der Seite **Verkaufs- und Lagerbestandsplanungseinrichtung**.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Erstellen und verwenden Sie Ihren eigenen Prognose-Webdienst für Verkaufs- und Bestandsprognosen

Für [!INCLUDE[prod_short](includes/prod_short.md)] online wird das Modell von Microsoft veröffentlicht und mit dem Microsoft-Abonnement verknüpft. Für andere Bereitstellungsoptionen müssen Sie in Ihrem eigenen Azure-Abonnement Machine-Learning-Ressourcen erstellen. Beispielschritte finden Sie im [Beispiel-Repository](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Diese Aufgabe ist dazu da, die API-URI und den API-Schlüssel abzurufen.

1. Wählen Sie das ![Glühbirne, die das „Sie wünschen ...“-Feature öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Einrichtung von Umsatz- und Lagerbestandsplanung** ein, und wählen Sie dann den entsprechenden Link.  
2. Erweitern Sie die Registerkarte **Allgemein** und füllen Sie dann die Felder API-URL und API-Schlüssel aus.  

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Bestand](inventory-manage-inventory.md)  
[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe von Erweiterungen](ui-extensions.md)  
[Nutzen Sie künstliche Intelligenz in Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  
[Überblick über die Planungs-API](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
