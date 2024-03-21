---
title: Verspätete Zahlungen für Verkaufsbelege vorhersagen
description: 'In diesem Artikel wird erklärt, wie Sie mit unserem Vorhersagemodell vorhersagen können, ob eine Rechnung rechtzeitig bezahlt wird.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 12/06/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="the-late-payment-prediction-extension"></a>Die Erweiterung "Vorhersage verspäteter Zahlungen"

Die effektive Verwaltung von Forderungen ist für den Gesamtfinanzstatus eines Unternehmens wichtig. Um ausstehende Forderungen zu reduzieren und Ihnen bei der Abstimmung der Eintreibungsstrategie zu helfen, sagt die Erweiterung voraus, ob Sie mit verspäteten Zahlungen rechnen sollten. Wenn beispielsweise vorausgesagt wird, dass eine Zahlung zu spät erfolgen wird, können Sie sich entschieden, die Zahlungsfristen oder die Zahlungsform für den Debitor anzupassen.

## <a name="get-started"></a>Erste Schritte

Wenn Sie einen gebuchten Verkaufsbeleg öffnen, wird oben auf der Seite eine Meldung angezeigt. Um die Erweiterung „Vorhersage verspäteter Zahlungen“ zu verwenden, wählen Sie in der Meldung die Option **Aktivieren** aus. Sie können die Erweiterung auch manuell einrichten. Beispielsweise, wenn Sie die Benachrichtigung versehentlich verworfen haben.

Führen Sie folgende Schritte aus, um die Erweiterung manuell zu aktivieren:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einrichtung der Vorhersage verspäteter Zahlungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus.

> [!NOTE]
> Wenn Sie sich entscheiden, die Erweiterung manuell zu aktivieren, beachten Sie, dass [!INCLUDE[prod_short](includes/prod_short.md)] Ihnen dies nicht erlaubt, wenn die Qualität des Modells gering ist. Die Qualität des Modells zeigt an, wie genau die Vorhersagen des Modells wahrscheinlich sind. Einige Faktoren können sich auf die Qualität eines Modells auswirken. Es könnten z. B. nicht genügend Daten vorhanden gewesen sein oder es gab nicht genügend Variationen in den Daten. Sie können die Qualität des Modells, das Sie aktuell verwenden auf der Seite **Einrichtung der Vorhersage verspäteter Zahlungen** anzeigen. Sie können auch einen Mindestschwellenwert für die Modellqualität angeben.

## <a name="view-all-payment-predictions"></a>Alle Zahlungsvorhersagen anzeigen

Wenn Sie die Erweiterung aktivieren wird die Kachel **Voraussichtlich verspätete Zahlungen** im **Geschäftsführung**-Rollencenter verfügbar. Die Kachel zeigt die Anzahl der Zahlungen, die voraussichtlich verspätet sind und lässt Sie die Seite **Debitorenposten** öffnen, wo Sie die gebuchten Rechnungen genauer ansehen können. Sie sollten drei Spalten beachten:  

* **Zahlungsverzug** - Gibt an, ob die Zahlung für die Rechnung voraussichtlich verspätet sein wird.
* **Vorhersagegenauigkeit** - Zeigt an, wie zuverlässig die Vorhersage ist. **Hoch** bedeutet, dass die Vorhersage zu mindestens 90 % sicher ist. **Mittel** liegt zwischen 80 und 90 %, und **Niedrig** liegt unter 80 %.
* **Vorhersagegenauigkeit %** - Zeigt den tatsächlichen Prozentsatz auf dem die Genauigkeitsbewertung basiert. Standardmäßig ist die Spalte ausgeblendet. Sie kann jedoch auf Wunsch hinzugefügt werden. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

> [!TIP]
> Die Seite „Debitorenposten“ zeigt rechts eine Infobox. Die Information im Abschnitt **Debitorendetails** kann bei der Prüfung von Vorhersagen nützlich sein. Wenn Sie die Rechnung in der Liste auswählen, werden im Abschnitt Informationen zum Debitor angezeigt. Außerdem können Sie damit sofort Maßnahmen ergreifen. Wenn ein Debitor häufig die Geldbörse verlegt, können Sie die Debitorenkarte aus der Infobox heraus öffnen und den Debitor für künftige Verkäufe sperren.  

## <a name="design-details"></a>Designdetails

Microsoft bietet und betreibt prädiktive Webdienste in allen Regionen, in denen [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar ist. Der Zugang zu diesen Webdiensten ist in Ihrem [!INCLUDE[prod_short](includes/prod_short.md)]-Abonnement enthalten. Weitere Informationen finden Sie im Microsoft Dynamics 365 Business Central-Lizenzierungshandbuch. Der Leitfaden steht auf der Website [Business Central](https://dynamics.microsoft.com/business-central/overview/) zum Herunterladen zur Verfügung.

Die Webdienste arbeiten in drei Modi:

* Trainingsmodell. Der Webdienst trainiert das Modell auf der Grundlage des bereitgestellten Datensatzes.
* Modell evaluieren. Der Webdienst prüft, ob das Modell zuverlässige Daten für den bereitgestellten Datensatz liefert.
* Vorhersagen. Der Web-Service wendet das Modell auf den bereitgestellten Datensatz an, um eine Vorhersage zu treffen.

Diese Webdienste sind zustandslos, d.h. sie verwenden Daten nur zur Berechnung von Vorhersagen bei Bedarf. Sie speichern keine Daten.

> [!NOTE]  
> Sie können anstelle unseres eigenen Prognose-Webdienstes Ihren eigenen Prognose-Webdienst verwenden. Weitere Informationen finden Sie unter [Erstellen und verwenden Sie Ihren eigenen Prognose-Webservice für Zahlungsverzugsprognosen](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model"></a>Daten, die zum Trainieren und Auswerten des Modells erforderlich sind

Für jede **Debitorenposten**, zu der eine zugehörige **gebuchte Verkaufsrechnung** vorliegt:

* Betrag (LW) einschließlich Steuer
* Die Zahlungsfrist in Tagen wird berechnet als **Zahlungsdatum** minus **Buchungsdatum**
* Ob es eine beantragte Gutschrift gibt

Zusätzlich verfügt der Datensatz über aggregierte Daten aus anderen Rechnungen, die sich auf dieselbe Kundschaft beziehen.

- Gesamtzahl und Beträge der bezahlten Rechnungen
- Gesamtzahl und Beträge der Rechnungen, die verspätet bezahlt wurden
- Gesamtzahl und Beträge der ausstehenden Rechnungen
- Gesamtzahl und Beträge der ausstehenden Rechnungen, die bereits verspätet sind
- Durchschnittlich Tage Verspätung
- Verhältnis: Anzahl der verspätet bezahlten/bezahlten Rechnungen
- Verhältnis: Betrag verspätet bezahlter/bezahlter Rechnungen
- Verhältnis: Anzahl der ausstehenden verspäteten/ausstehende Rechnungen
- Verhältnis: Betrag der ausstehenden verspäteten/ausstehenden Rechnungen

> [!NOTE]
> Die Informationen über den Debitor sind nicht im Dataset enthalten.

### <a name="standard-model-and-my-model"></a>Standardmodell und Mein Modell

Das Vorhersagemodell der Erweiterung „Vorhersage verspäteter Zahlungen“ wird anhand von Daten trainiert, die eine Reihe von kleinen bis mittleren Unternehmen repräsentieren. Wenn Sie anfangen, Rechnungen zu buchen und Zahlungen zu erhalten, bewertet [!INCLUDE[prod_short](includes/prod_short.md)], ob das Standardmodell zu Ihrem Geschäftsablauf passt.

Wenn Ihre Prozesse nicht mit dem Standardmodell übereinstimmen, können Sie die Erweiterung verwenden, aber Sie brauchen mehr Daten. Verwenden Sie einfach weiterhin [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Wir verwenden jede Woche einen Teil Ihrer Rechenzeit, wenn wir das Modell bewerten und neu trainieren.

[!INCLUDE[prod_short](includes/prod_short.md)] führt Training und Bewertungen automatisch durch, wenn genügend bezahlte und verspätete Rechnungen verfügbar sind. Sie können es jedoch jederzeit manuell ausführen.

#### <a name="to-train-and-use-your-model"></a>So trainieren und verwenden Sie Ihr Modell

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einrichtung der Vorhersage verspäteter Zahlungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Geben Sie im Feld **Ausgewähltes Modell** die Option **Mein Modell** aus.
3. Wählen Sie die Aktion **Mein Modell erstellen**, um das Modell anhand Ihrer Daten zu trainieren.  

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Erstellen und verwenden Sie Ihren eigenen Prognose-Webdienst zur Vorhersage von Zahlungsverzug

Sie können auch Ihren eigenen Vorhersage-Webdienst auf der Grundlage eines öffentlichen Modells mit dem Namen **Vorhersage-Experiment für Dynamics 365 Business Central** erstellen. Dieses vorhersagende Modell ist online im Azure AI Katalog verfügbar. Um das Modell zu verwenden, gehen folgendermaßen vor:  

1. Öffnen Sie einem Browser und gehen Sie zum [Azure AI Katalog](https://go.microsoft.com/fwlink/?linkid=2086310)  
2. Suchen Sie nach **Vorhersage-Experiment für Dynamics 365 Business Central** und öffnen Sie dann das Modell im Azure Machine Learning Studio.  
3. Verwenden Sie das Microsoft-Konto, um sich für einen Arbeitsbereich anzumelden und kopieren Sie dann das Muster.  
4. Führen Sie die Vorlage aus und veröffentlichen Sie dieses als Webdienst.  
5. Notieren Sie den API URL und den API Schlüssel. Sie verwenden diese Anmeldeinformationen für die Cashfloweinrichtung.  
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einrichtung der Vorhersage verspäteter Zahlungen** ein, und wählen Sie dann den zugehörigen Link.  
7. Wählen Sie das Kontrollkästchen **Mein Azure-Abonnement verwenden**.
8. Im Inforegister **Anmeldeinformationen für mein Modell** geben Sie die API-URL und den API-Schlüssel für Ihr Modell ein.  

## <a name="see-also"></a>Siehe auch

[Azure Machine Learning Studio-Dokumentation](/azure/machine-learning/classic/)  
[Anpassen von Business Central über Erweiterungen](ui-extensions.md)  
[Willkommen bei [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)  
[Nutzen Sie künstliche Intelligenz in Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
