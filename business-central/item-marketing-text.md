---
title: Marketingtext zu Artikeln hinzufügen
description: Marketingtext für Artikel in Business Central schreiben
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Marketingtext zu Artikeln hinzufügen

Sie können für jeden in Business Central registrierten Artikel *Marketingtext* über den Artikel schreiben. Obwohl Marketingtext eine Art Beschreibung ist, unterscheidet er sich vom Feld **Beschreibung** des Artikels. Das Feld **Beschreibung** wird normalerweise als prägnanter Anzeigename verwendet, um das Produkt schnell identifizieren zu können. Der Marketingtext hingegen ist ein umfassenderer und detailreicherer Schritt. Durch ihn sollen Marketing- und Werbeinhalten, sogenanntes *Textmaterial*, hinzugefügt werden. Dieser Text kann dann mit dem Artikel veröffentlicht werden, wenn er in einem Webshop wie Shopify veröffentlicht wird.

Es gibt zwei Möglichkeiten, Marketingtext zu erstellen. Am einfachsten gelingt der Einstieg mit Copilot, das Ihnen KI-generierten Text vorschlägt. Die andere Möglichkeit ist, den Text von Grund auf selbst zu verfassen. 

## <a name=copilot></a>KI-generierte Marketingtexte (Vorschauversion) mit Copilot erstellen

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Copilot bietet Ihnen schnell einen Textvorschlag an, der automatisch für Sie generiert wird. Der KI-generierte Text ist auf den Artikel zugeschnitten und bietet einen guten Ausgangspunkt. Der Text basiert zum Teil auf den folgenden Informationen:

- Für den Artikel festgelegte Attribute, z. B. Beschreibung, Farbe, Dimensionen, Material usw.
- Auswählbare Einstellungen zum Stil wie Tonfall, Format und Länge.

Copilot soll Ihnen Zeit sparen und Ihnen dabei helfen, kreative und ansprechende Texte zu schreiben, die Ihre Marke widerspiegeln und über Ihre gesamte Produktlinie hinweg konsistent sind. Erstellen Sie zunächst einen Vorschlag und ändern Sie ihn dann nach Bedarf.

> [!NOTE]
> In der Vorschauversion von Business Central ist KI-generierter Text nur auf Englisch.

### Voraussetzungen

- Sie verwenden eine [Vorschauversion](ai-preview-getstarted.md) von Business Central, die für Copilot aktiviert ist. Die Aktivierung von Copilot erfolgt durch einen Administrator. Weitere Informationen finden Sie unter [KI-gestützten Marketingtext für Artikel mit Copilot konfigurieren](enable-ai.md).
- Die Sprache, die Sie in Business Central verwenden, muss Englisch sein. Alle verfügbaren englischen Gebietsschemas funktionieren, wie z. B. Englisch (Vereinigte Staaten), Englisch (Vereinigtes Königreich) oder Englisch (Südafrika).

   Um die Sprache zu ändern, wählen Sie in der oberen rechten Ecke das **Einstellungen**-Symbol ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") > **Meine Einstellungen** > **Sprache** aus. Weitere Informationen finden Sie unter [Grundeinstellungen ändern](ui-change-basic-settings.md#language).
- In den [FAQ zu Copilot](ai-faq.md) erfahren Sie mehr über KI-generierte Textvorschläge von Copilot und deren Verwendung.

### Einen ersten Entwurf mit Copilot erstellen

1. Öffnen Sie in Business Central den Artikel, den Sie ändern möchten. Öffnen Sie einen Artikel und gehen Sie wie folgt vor:

   1. Wählen Sie in der oberen rechten Ecke die ![Glühbirne aus, die die „Sie wünschen ...“-Funktion 22 öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Artikel** ein und wählen Sie dann den dazugehörigen Link aus, um eine Liste der verfügbaren Artikel aufzurufen.
   2. Um den Artikel zu öffnen, machen Sie einen Doppelklick darauf oder wählen Sie in der Spalte **Nr.** seinen Wert aus.

   Weitere Informationen zum Erstellen eines Artikels finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

   [![Zeigt eine Artikelkarte mit Bereich „Marketingtext“](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. Von der Artikelkarte aus gibt es zwei Möglichkeiten, mit Copilot mit dem Schreiben von Marketingtexten zu beginnen:

   - Verwenden Sie den Bereich **Marketingtext** in der Infobox rechts auf der Seite. Führen Sie die folgenden Schritte aus:

     1. Wählen Sie im Bereich **Marketingtext** **Mit Copilot erstellen** aus.

        Der vorgeschlagene Text wird im Bereich angezeigt.
     2. Wenn Sie einen weiteren Vorschlag erhalten möchten, wählen Sie erneut **Mit Copilot erstellen** aus. Wenn Ihnen ein Vorschlag nicht gefällt, wählen Sie **Verwerfen**, um den Bereich zu leeren.

        Sie können diesen Schritt so lange wiederholen, bis Sie einen Vorschlag erhalten, der ein guter Ausgangspunkt ist. Beachten Sie jedoch, dass der aktuelle Vorschlag überschrieben wird und Sie ihn nicht wiederherstellen können. Wenn Ihnen der aktuelle Vorschlag also gefällt, gehen Sie zum nächsten Schritt. Sie können zu einem späteren Zeitpunkt immer noch weitere Vorschläge abrufen und die Vorschläge später sogar verbessern, wenn Sie möchten.
      3. Wählen Sie **Diesen Vorschlag überprüfen und speichern** oder **Bearbeiten** aus, um den Text zu überprüfen, zu bearbeiten und zu speichern.

         Mit diesem Schritt gelangen Sie zur Seite **Mit Copilot erstellen**. Gehen Sie zum nächsten Abschnitt.

         > [!NOTE]
         > Der Text wird erst gespeichert, wenn Sie diesen Schritt ausführen.

   - Wählen Sie die Aktion **Marketingtext** oben auf der Seite „Artikelkarte“ aus und gehen Sie direkt zur Seite **Mit Copilot erstellen**.

     Wählen Sie auf der Seite **Mit Copilot erstellen** die Option **Mit Copilot erstellen** aus, um den ersten Vorschlag zu erhalten. Sie können dann weitere Vorschläge erhalten, die erhaltenen Vorschläge verbessern, Text bearbeiten und vieles mehr. Weitere Informationen finden Sie unter [Überprüfen, bearbeiten und speichern](#review-edit-and-save-text).

   > [!TIP]
   > [Woher stammt der Vorschlag?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### Text überprüfen, bearbeiten und speichern

Sobald Sie den ersten Entwurf haben, müssen Sie ihn überprüfen und ändern, um ihn für die Veröffentlichung vorzubereiten. Das geschieht auf der Seite **Mit Copilot erstellen**. Der aktuelle Text wird im Feld **Marketingtext** angezeigt. Auf der Seite können Sie weitere Vorschläge abrufen, Einstellungen ändern, um die Vorschläge zu beeinflussen, und den Text manuell ändern und formatieren.

[![Zeigt das „Mit Copilot erstellen“-Fenster](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> Der KI-generierte Text von Copilot ist nur ein Vorschlag und kann Fehler enthalten. Er muss von einem Menschen überwacht und überprüft werden, um sicherzustellen, dass er richtig und angemessen ist. Überprüfen Sie jeden vorgeschlagenen Text und bearbeiten Sie ihn nach Bedarf, bevor Sie ihn speichern und veröffentlichen.

Verwenden Sie die folgenden Richtlinien, um den Marketingtext fertigzustellen und zu speichern.

1. Nehmen Sie Änderungen am Text direkt im Feld **Marketingtext** vor. Verwenden Sie die Symbolleiste am unteren Rand des Felds, um Text zu formatieren und zu gestalten, Links hinzuzufügen und mehr.
2. Um einen neuen Vorschlag zu erhalten, wählen Sie **Entwurf erstellen** aus.
3. Wenn Sie mit den Vorschlägen nicht zufrieden sind, verbessern Sie sie ganz nach Belieben.

   Wählen Sie **Weitere Einstellungen**, ändern Sie die Optionen unter **Auswählen, wie Copilot Vorschläge erstellt** und wählen Sie dann **Entwurf erstellen**, um einen neuen Vorschlag zu erhalten.

   Richtlinien zur Verbesserung von Vorschlägen finden Sie unter [Textvorschläge verbessern und anpassen](#improve-and-tailor-text-suggestions).

4. Wenn Sie zum vorherigen Vorschlag zurückkehren möchten, wählen Sie **Rückgängig**.
5. Überprüfen Sie den Text sorgfältig auf Genauigkeit und Angemessenheit und wählen Sie dann **OK**, um ihn zu speichern.

### Textvorschläge verbessern und anpassen

Sie können einige Schritte unternehmen, um Textvorschläge zu verbessern und sie an Ihre persönlichen oder die Präferenzen Ihres Unternehmens anzupassen.

1. Verwenden Sie die Optionen oben auf der Seite **Mit Copilot erstellen**, um zu beeinflussen, wie der ausgegebene KI-generierte Text aussieht. 

   |Option|Beschreibung|
   |-|-|
   |Einzuschließende Attribute|Verwenden Sie diese Option, wenn die Vorschläge teilweise auf den dem Artikel zugewiesenen Attribute basieren sollen. Wählen Sie die Attribute aus, die am besten zu den Eigenschaften passen, die Sie hervorheben möchten. Je mehr relevante Attribute Sie einbeziehen, desto aussagekräftiger wird das Ergebnis. Wenn Sie das Gefühl haben, dass Ihnen einige entscheidende Attribute fehlen, fügen Sie weitere hinzu. Weitere Informationen über Attribute finden Sie unter [Mit Artikelattributen arbeiten](inventory-how-work-item-attributes.md) |
   |Qualität betonen|Verwenden Sie diese Option, um aus einer Liste vordefinierter Eigenschaften auszuwählen, die Sie im Text hervorheben möchten. Wählen Sie eine Qualität, die am besten zu der Art des Artikels passt, über den Sie schreiben. Die Eigenschaften entsprechen nicht direkt den Attributen, der Beschreibung oder der Kategorie des Artikels. Zum Beispiel könnte **Qualität** sowohl für ein Fahrrad als auch für einen Schreibtisch eine gute Wahl sein, während **Geschwindigkeit** für ein Fahrrad geeignet wäre, aber nicht für einen Schreibtisch.|
   |Ton der Stimme|Verwenden Sie diese Option, um zu beeinflussen, welche Art von Wörtern, Phrasen und Satzzeichen verwendet werden, um die Zielgruppe anzusprechen. Sie haben die Wahl aus mehreren vordefinierten Tonfällen von **Formell** (dabei handelt es sich um einen geschäftlich klingenden Tonfall) bis zu **Kreativ** (der zu einem lässigen Text führt). |
   |Format und Länge|Verwenden Sie diese Option, um die allgemeine Struktur des Textes zu steuern, die aus drei Teilen besteht, die von vier verschiedenen Optionen abgedeckt werden: <ul><li>**Slogan**: Eine einprägsamer Formulierung oder ein kurzer Satz, der den Artikel oder die Marke identifiziert.</li><li>**Absatz**: Ein einzelner Absatz mit fließendem und ausführlichem Text, der aus mehreren vollständigen Sätzen besteht.</li><li>**Slogan + Absatz**: Ein Slogan gefolgt von einem Absatz</li><li>**Kurzfassung**: Ein einleitender Satz, ähnlich einem Slogan, gefolgt von einer Aufzählung der wichtigsten interessanten Punkte.</li></ul> |

2. Verbessern Sie das Feld **Beschreibung** auf der Artikelkarte.

   Der Text im Feld **Beschreibung** wird an vielen Stellen im vorgeschlagenen Text unverändert verwendet. Daher ist es wichtig, dass die Beschreibung am besten wiedergibt, wie der Artikel im Marketingtext dargestellt werden soll. 

3. Stellen Sie sicher, dass das Feld **Artikelkategoriencode** auf der Artikelkarte auf eine geeignete Kategorie eingestellt ist.

   Copilot findet Wörter und Sätze, die sich auf die Kategorie beziehen, und arbeitet sie in den vorgeschlagenen Text ein.

## Marketingtexte von Grund auf neu erstellen

1. Öffnen Sie in Business Central den Artikel, den Sie ändern möchten, wie folgt:

    1. Wählen Sie in der oberen rechten Ecke die ![Glühbirne aus, die die „Sie wünschen ...“-Funktion 22 öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Artikel** ein und wählen Sie dann den dazugehörigen Link aus, um eine Liste der verfügbaren Artikel aufzurufen.
    2. Um den Artikel zu öffnen, machen Sie einen Doppelklick darauf oder wählen Sie im Feld **Nr.** Feld

2. Führen Sie einen der folgenden Schritte aus:

   - Wählen Sie im Bereich **Marketingtext** in der Infobox rechts auf der Seite **Bearbeiten** aus.
   - Wählen Sie die Aktion **Marketingtext** aus.
3. Nehmen Sie Änderungen am Text direkt im Feld **Marketingtext** vor. Verwenden Sie die Symbolleiste am unteren Rand des Felds, um Text zu formatieren und zu gestalten, Links hinzuzufügen und mehr.
4. Wählen Sie **OK** aus, wenn Sie soweit sind, den Text zu speichern.

## Siehe auch

[Überblick über KI-gestützte Marketingtexte für Artikel mit Copilot](ai-overview.md)  
[KI-gestützten Marketingtext für Artikel mit Copilot konfigurieren](enable-ai.md)  
[FAQ zu KI-gestützten Marketingtext für Artikel mit Copilot](ai-faq.md)  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
