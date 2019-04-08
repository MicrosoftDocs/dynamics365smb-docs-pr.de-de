---
title: Verspätete Zahlung für Verkaufsbelege vorhersagen | Microsoft Docs
description: Verwenden Sie unser Vorhersagemodell, um vorauszusagen, ob eine Rechnung rechtzeitig bezahlt wird.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 4e47858bf1f7253f8fb8951fe8ea3cb611138852
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799066"
---
# <a name="the-late-payment-prediction-extension"></a>Die Erweiterung "Vorhersage verspäteter Zahlungen"  
Die effektive Verwaltung von Forderungen ist für den Gesamtfinanzstatus eines Unternehmens wichtig. Die Erweiterung "Vorhersage verspäteter Zahlungen" kann nützlich sein, um ausstehende Forderungen zu reduzieren und die Sammlungsstrategie abzustimmen, die voraussagt, ob Verkaufsrechnungen pünktlich bezahlt werden. Wenn beispielsweise vorausgesagt wird, dass eine Zahlung zu spät erfolgen wird, können Sie sich entschieden, die Zahlungsfristen oder die Zahlungsform für den Debitor anzupassen.

## <a name="what-are-predictions-based-on"></a>Auf welcher Grundlage erfolgen die Vorhersagen?  
Die Erweiterung "Vorhersage verspäteter Zahlungen" verwendet ein Vorhersagemodell, das wir in Azure Machine Learning Studio entwickelt und mit repräsentativer Daten aus kleinen und mittelgroßen Unternehmen geschult haben. Obwohl wir es bereits geschult und ausgewertet haben, lernt unser Vorhersagemodell von Ihren Daten weiter. Je mehr Sie das Modell verwenden und je mehr Daten Sie eingeben, umso genauer werden die Vorhersagen. Standardmäßig prüft die Erweiterung das Modell und aktualisiert die Vorhersagen wöchentlich. Sie können die Vorhersagen jedoch aktualisieren, wann Sie wünschen, indem Sie die Aktion **Vorhersage aktualisieren** auf der Seite **Debitorenposten** auswählen.  

> [!Note]
> Wir verwenden jede Woche einen kleinen Teil Ihrer Rechnerzeit, um unser Modell auswerten und Ihre Vorhersagen zu aktualisieren. Zusätzlich zur manuellen Aktualisierung Ihrer Vorhersagen sind für die Schulung des Modells (was nötig sein kann, wenn Sie vor Kurzem Daten hinzugefügt haben) und für die Auswertung des Modells (die Qualität des Modells betrachten) Rechnerzeit erforderlich.

## <a name="getting-started"></a>Erste Schritte
Die Erweiterung in [!INCLUDE[d365fin](includes/d365fin_md.md)] kostenlos, und wir stellen ein Abonnement für Azure Machine Learning bereit. Das Abonnement bietet 30 Minuten Rechnerzeit pro Monat. Wenn Sie mehr benötigen, können Sie Ihr eigenes Vorhersagemodell erstellen und stattdessen dieses verwenden. Weitere Informationen finden Sie im Abschnitt _Erstellen Ihres eigenen Vorhersagemodells_ weiter unten in diesem Thema.  

Wenn Sie einen gebuchten Verkaufsbeleg öffnen, wird oben auf der Seite eine Meldung angezeigt. Um die Erweiterung "Vorhersage verspäteter Zahlungen" zu verwenden, wählen Sie in der Meldung die Option **Aktivieren** aus. Sie können die Erweiterung auch manuell einrichten. Beispielsweise, wenn Sie die Benachrichtigung versehentlich verworfen haben.  

Führen Sie folgende Schritte aus, um die Erweiterung manuell zu aktivieren:

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Dienstverbindungen** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Option **Einrichtung der Vorhersage verspäteter Zahlungen**, und füllen Sie dann je nach Bedarf die Felder aus.

## <a name="viewing-all-payment-predictions"></a>Anzeigen aller Zahlungsvorhersagen
Wenn Sie die Erweiterung aktivieren wird die Kachel **Voraussichtlich verspätete Zahlungen** im **Geschäftsführer**-Rollencenter verfügbar. Die Kachel zeigt die Anzahl der Zahlungen, die voraussichtlich verspätet sind und lässt Sie die Seite **Debitorenposten** öffnen, in dem Sie die gebuchten Rechnungen genauer ansehen können. Sie sollten drei Spalten beachten:  

* **Zahlungsverzug** - Gibt an, ob die Zahlung für die Rechnung voraussichtlich verspätet sein wird.
* **Vorhersagegenauigkeit** - Zeigt an, wie zuverlässig die Vorhersage ist. **Hoch** bedeutet, dass die Vorhersage zu mindestens 90 % sicher ist. **Mittel** liegt zwischen 80 und 90 %, und **Niedrig** liegt unter 80 %.
* **Vorhersagegenauigkeit %** - Zeigt den tatsächlichen Prozentsatz auf dem die Genauigkeitsbewertung basiert. Standardmäßig wird die Spalte nicht angezeigt. Sie kann jedoch auf Wunsch hinzugefügt werden. Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).

> [!Tip]
> Die Seite "Debitorenposten" zeigt zudem rechts eine Infobox. Die Information im Abschnitt **Debitorendetails** kann bei der Prüfung von Vorhersagen nützlich sein. Wenn Sie die Rechnung in der Liste auswählen, werden im Abschnitt Informationen zum Debitor angezeigt. Sie können auch sofort Maßnahmen ergreifen. Wenn ein Debitor häufig die Geldbörse verlegt, können Sie die Debitorenkarte aus der Infobox heraus öffnen und den Debitor für künftige Verkäufe sperren.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Anzeigen einer Zahlungsvorhersage für einen bestimmten Verkaufsbeleg
Sie können auch verspätete Zahlungen vorhersagen. Auf den Seiten **Verkaufsangebote**, **Verkaufsaufträge** und **Verkaufsrechnungen** können Sie die Aktion **Zahlung vorhersagen** verwenden, um eine Vorhersage für einen Verkaufsbeleg zu erstellen, den Sie anzeigen.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Erstellen Ihres eigenen Vorhersagemodells
Möchten Sie Ihr eigenes Vorhersagemodell erstellen? Sie können Azure Machine Learning Studio verwenden, um Ihr eigenes Vorhersagemodell zu erstellen und es in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden. Um Ihr eigenes Modell zu verwenden, müssen Sie Azure Machine Learning abonnieren. Weitere Informationen finden Sie in der [Azure Machine Learning Studio-Dokumentation](https://go.microsoft.com/fwlink/?linkid=861765).  

Wir bieten jedoch eine einfachere Methode zur Erstellung und Verwendung Ihres eigenen Vorhersagemodells an. Sie können die Daten Ihrer Rechnungen für unser Vorhersageexperiment in Azure Machine Learning freigeben und von unserem Experiment ein Vorhersagemodell basierend auf Ihren Daten erstellen und schulen lassen. Um Ihre Daten auf der Seite **Einrichtung der Vorhersage verspäteter Zahlungen** freizugeben, wählen Sie die Aktion **Mein Modell erstellen** aus. Danach basieren Vorhersagen auf Ihrem Modell und Ihren Daten, nicht unseren.  

> [!Note]
>   Die Qualität des Modells ist wichtig. Wenn unser Vorhersageexperiment Ihre Daten verwendet, um ein Modell zu schulen, wird ein Qualitätswert für das Modell als Prozentzahl bestimmt. Die Modellqualität gibt an, wie genau die Vorhersagen des Modells wahrscheinlich sind. Einige Faktoren können sich auf die Qualität eines Modells auswirken. Beispielsweise lagen nicht genug Daten vor oder die Daten boten nicht genug Varianz. Sie können die Qualität des Modells, das Sie aktuell verwenden auf der Seite **Einrichtung der Vorhersage verspäteter Zahlungen** anzeigen. Sie können auch einen Mindestschwellenwert für die Modellqualität angeben. Modelle mit einem Qualitätswert unter dem Schwellenwerts erzeugen keine Vorhersagen.  

### <a name="to-use-your-model-instead-of-ours"></a>So verwenden Sie Ihr Modell anstelle von unserem  
Wenn Sie Ihr eigenes Modell in Azure Machine Learning Studio erstellen, ohne die Tools in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu verwenden, müssen Sie Ihre Anmeldeinformationen angeben, sodass [!INCLUDE[d365fin](includes/d365fin_md.md)] auf das Modell zugreifen kann. Dafür sind einige Schritte erforderlich:

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Einrichtung der Vorhersage verspäteter Zahlungen** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie das Kontrollkästchen **Mein Azure-Abonnement verwenden**.  
3. Geben Sie im Feld **Ausgewähltes Modell** die Option **Mein Modell** aus.  
4. Im Inforegister **Anmeldeinformationen für mein Modell** geben Sie die API-URL und den API-Schlüssel für Ihr Modell ein.  

## <a name="see-also"></a>Siehe auch  
[Azure Machine Learning Studio-Dokumentation](https://go.microsoft.com/fwlink/?linkid=861765)  
[Anpassen von Business Central mithilfe der Erweiterungen](ui-extensions.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
