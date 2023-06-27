---
title: Cashflow-Analyse einrichten (enthält Video)
description: 'Verwenden Sie die Diagramme des Buchhalter-Rollencenters, um den Flow des Geldes in Ihrem Unternehmen zu analysieren, einschließlich Ausgaben und Einnahmen, Liquidität und Bareinnahmen abzüglich Barzahlungen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 08/23/2022
ms.author: bholtorf
---
# <a name="setting-up-cash-flow-analysis"></a>Aufstellung Cashflow-Analyse

Wenn Sie etwas Unterstützung benötigen, was Sie mit Ihrem Barkonto zu tun sollen, schauen Sie sich das Diagramm im Buchhalter-Rollencenter an:

* **Bargeldumlauf**  
* **Einnahmen und Ausgaben**  
* **Cashflow**  
* **Cashflowplanungen**  

Dieser Artikel beschreibt, wo die Daten in den Diagrammen herkommen und was zu tun ist, um die Diagramme zu nutzen.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Diagramme Geldumlauf und Einnahmen und Ausgaben

Die Diagramme **Bargeldumlauf** und **Einnahmen und Ausgaben** stehen für die Nutzung bereit, basierend auf dem Kontenplan und den Finanzberichten. Die Konten sind dort, wo die Daten herkommen und die Finanzberichte berechnen die Beziehung zwischen Verkauf und Debitoren. Einige Konten und Finanzberichte werden bereitgestellt. Sie können sie verwenden, um sie zu ändern und neue hinzufügen. Wenn Sie z. B. Sachkonten Ihrem Kontenplan hinzufügen indem Sie sie aus QuickBooks importieren, müssen Sie die Konten auf der Seite **Finanzberichte** folgenden Berichten zuweisen:

| Finanzberichtsname | Wo sie verwendet werden |
| --- | --- |
| **I_CACYCLE** |Bargeldumlauf |
| **I_CASHFLOW** |Cashflow |
| **I_INCEXP** |Einnahmen und Ausgaben |
| **I_MINTRIAL** |Als GuV-Konten, wenn Sie nicht den Kontenplan verwenden |

> [!NOTE]
> Hinweis Es ist sinnvoll, die Berechnungen zu behalten, die für den Finanzbericht bereitgestellt werden.

Geben Sie im Feld **Zusammenzählung** das Feld **Umsätze, gesamt**, **Forderungen gesamt**, **Verbindlichkeiten gesamt** und **Lager gesamt** ein. Um eine Reihe von Konten zuzuordnen, geben Sie die Kontonummern getrennt durch ".." ein, Beispiel: **1111..4444**. Alternativ, um bestimmte zuzuordnen, geben Sie die Kontonummern getrennt durch "|" ein, Beispiel: **2222|3333|5555**.  

> [!TIP] 
> Überprüfen Sie die Zuordnung, indem Sie die Aktion **Übersicht** auswählen.  

## <a name="set-up-the-cash-flow-chart"></a>Richtet den Cashflow-Kontenplan ein.

Das Cashflow-Diagramm basiert auf Folgendem:  

* Einem Diagramm von Cashflow-Konten.
* Einem oder mehrerer Cashflow-Einstellungen. Diese Einrichtungen geben die Konten an, die für die Bereiche Finanzbuchhaltung, Einkauf, Verkauf, Services und Anlagen verwendet werden.  

Einige Konten und Cashfloweinrichtung sind bereits bereitgestellt. Sie können diese ändern, hinzufügen oder entfernen.  

Um die Konten einzurichten, suchen Sie nach **Cashflow-Kontenplan**, wählen Sie den Link aus, und füllen Sie die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Wiederholen Sie diese Schritte für **Cashfloweinrichtung**.

## <a name="set-up-cash-flow-forecasts"></a>Richtet Cashflowplanungen ein

Das Diagramm **Cashflowplanung** verwendet Cashflowkonten, Cashfloweinrichtung und Cashflowplanungen. Einige werden bereitgestellt, aber Sie können eigene einrichten, indem Sie die unterstützte Einrichtung verwenden. Die unterstützte Einrichtung definiert u.a., wie oft die Planung aktualisiert werden soll, die Konten, die darauf basieren sollen, Informationen darüber, wann Sie Steuern bezahlen und ob [Azure AI](https://azure.microsoft.com/overview/ai-platform/) verwendet werden soll.  

Cashflow-Prognosen können Azure AI verwenden, um eine umfassendere Prognose zu erstellen. Die Verknüpfung zu Azure AI ist bereits eingerichtet. Sie müssen sie nur aktivieren. Wenn Sie sich bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden, wird eine Benachrichtigung in einer blauen Leiste angezeigt mit einem Link zur Standardcashfloweinrichtung. Die Mitteilung wird jeweils nur einmal angezeigt. Wenn Sie sie schließen, sich aber dazu entscheiden, Azure AI zu aktivieren, können Sie die unterstützte Einrichtung oder den manuellen Vorgang nutzen.  

> [!NOTE]
>
> Alternativ können Sie Ihren eigenen vorbestimmten Webdienst verwenden. Weitere Informationen finden Sie unter [Erstellen und verwenden von eigenen vorbestimmten Webdiensten für Cashflowplanungen](#AnchorText).  

Um die unterstützte Einrichtung zu verwenden:  

1. Im Buchhalterrollencenter unter **Cashflow-Planung** wählen Sie die Aktion **Unterstütze Einrichtung** aus.
2. Füllen Sie die Felder soweit erforderlich für jeden Schritt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Zurück im Buchhalterrollencenter unter **Cashflow-Planung** wählen Sie die Aktion **Planung neu berechnen** aus.

Um einen manuellen Vorgang zu verwenden:  

1. Wählen Sie im Buchhalter-Rollencenter die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Cashflow-Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Erweitern Sie das Inforegister **Azure AI** und aktivieren Sie das Feld **Azure AI aktiviert**.
3. Zurück im Buchhalterrollencenter unter **Cashflow-Planung** wählen Sie die Aktion **Planung neu berechnen** aus.

> [!TIP]  
> Beachten Sie die Länge der Perioden, die der Service in den Berechnungen verwendet. Je mehr Daten Sie liefern, umso genauer wird die Vorhersage sein. Halten Sie auch nach umfangreichen Abweichungen in Perioden Ausschau. Sie werden ebenfalls Auswirkungen auf die Vorhersagen haben. Wenn Azure AI nicht genügend Daten findet oder die Daten stark abweichen, wird der Service keine Vorhersage machen.  

## <a name="design-details"></a>Einzelheiten zum Entwurf

Abonnements für [!INCLUDE[prod_short](includes/prod_short.md)] beinhalten den Zugang zu mehreren prädiktiven Webdiensten in allen Regionen, in denen [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar ist. Erfahren Sie mehr im Microsoft Dynamics 365 Business Central-Lizenzierungsleitfaden. Der Leitfaden steht auf der Website [Business Central](https://dynamics.microsoft.com/business-central/overview/) zum Herunterladen zur Verfügung.

Diese Webdienste sind zustandslos, d.h. sie verwenden Daten nur zur Berechnung von Vorhersagen bei Bedarf. Sie speichern keine Daten.

> [!NOTE]
>
> Sie können anstelle unseres eigenen Prognose-Webdienstes Ihren eigenen Prognose-Webdienst verwenden. Weitere Informationen finden Sie unter [Erstellen und verwenden von eigenen vorbestimmten Webdiensten für Cashflowplanungen](#AnchorText).

### <a name="data-required-for-forecast"></a>Für die Prognose erforderliche Daten

Um Vorhersagen über zukünftige Einnahmen und Ausgaben treffen zu können, benötigen Webdienste historische Daten über Forderungen, Verbindlichkeiten und Steuern.

#### <a name="receivables"></a>Forderungen

**Fälligkeitsdatum**, **Betrag (MW)** Felder auf der Seite **Debitorenposten**, wobei:

* Die Belegart ist *Rechnung* oder *Gutschrift*.
* Das Fälligkeitsdatum liegt zwischen dem Datum, das auf der Grundlage der Werte in den Feldern **Historische Perioden** und **Periodenart** auf der Seite **Cashflow-Einrichtung** berechnet wird, und dem Arbeitsdatum.

Vor der Verwendung des Prognose-Webdienstes komprimiert [!INCLUDE[prod_short](includes/prod_short.md)] Transaktionen um **Fälligkeitsdatum** basierend auf dem Wert im Feld **Periodentyp** auf der Seite **Cash-Flow-Einrichtung**.

#### <a name="payables"></a>Verbindlichkeiten

**Fälligkeitsdatum**, **Betrag (MW)** Felder der Seite **Kreditorenbuchungen**, wobei:

* Die Belegart ist *Rechnung* oder *Gutschrift*.
* Das Fälligkeitsdatum liegt zwischen dem Datum, das auf der Grundlage der Werte in den Feldern **Historische Perioden** und **Periodentyp** auf der Seite **Cashfloweinrichtung** berechnet wird, und dem Arbeitsdatum.

Vor der Verwendung des Prognose-Webdienstes komprimiert [!INCLUDE[prod_short](includes/prod_short.md)] Transaktionen um **Fälligkeitsdatum** basierend auf dem Wert im Feld **Periodentyp** auf der Seite **Cash-Flow-Einrichtung**.

#### <a name="tax"></a>Steuer

**Dokumentdatum**, **Betrag** Felder auf der Seite **MwSt. (Steuer) Posten**, wobei:

* Die Belegart ist *Verkauf*.
* Das Belegdatum liegt zwischen dem Datum, das auf der Grundlage von Werten in den Feldern **Historische Perioden** und **Periodentyp** auf der Seite **Cashfloweinrichtung** berechnet wird, und dem Arbeitsdatum.

Vor der Verwendung des prädiktiven Webdienstes komprimiert [!INCLUDE[prod_short](includes/prod_short.md)] Transaktionen nach **Dokumentdatum** basierend auf dem Wert im Feld **Periodentyp** auf der Seite **Cash Flow Einrichtung**.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"></a> Erstellen und verwenden Sie Ihren eigenen vorhersagenden Webdienst für Cashflowplanungen.

Sie können Ihren eigenen vorhersagenden Webdienst auf einem öffentliches Modell erzeugen, dem **Prognosemodell für Microsoft Business Central**. Dieses vorhersagende Modell ist online im Azure AI Katalog verfügbar. Um das Modell zu verwenden, gehen folgendermaßen vor:  

1. Öffnen Sie einem Browser und gehen Sie zum [Azure AI Katalog](https://go.microsoft.com/fwlink/?linkid=828352)  
2. Suchen Sie nach dem **Vorhersagemodell für Microsoft Business Central** und öffnen Sie dann das Modell im Microsoft Azure Machine Learning Studio.  
3. Verwenden Sie das Microsoft-Konto, um sich für einen Arbeitsbereich anzumelden und kopieren Sie dann das Muster.  
4. Führen Sie die Vorlage aus und veröffentlichen Sie dieses als Webdienst.  
5. Notieren Sie den API URL und den API Schlüssel. Sie verwenden diese Anmeldeinformationen für die Cashfloweinrichtung.  
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Cashflow-Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
7. Erweitern Sie das Inforegister **Azure AI**, und füllen Sie dann die Felder aus, einschließlich der API-URL und des API-Schlüssels, die von Azure Machine Learning Studio bereitgestellt werden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. Im Buchhalterrollencenter unter **Cashflow-Planung** wählen Sie die Aktion **Planung neu berechnen** aus.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/forecast-cash-flow-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
