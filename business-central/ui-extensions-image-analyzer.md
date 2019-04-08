---
title: Bild-Analyzer-Erweiterung verwenden | Microsoft Docs
description: Mit dieser Erweiterung können Bilder von Kontaktpersonen und Artikel analysieren und Attribute finden, damit Sie diese in Business Central rasch zuweisen können.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 803d755a7caa470b97bf606f0f8916d0135d047e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799061"
---
# <a name="the-image-analyzer-extension"></a>Die Bildanalyse-Erweiterung
Die Bild-Analyser-Erweiterung verwendet die leistungsstarke Bildanalytik, die von der Computer Vision API for Microsoft Cognitive Servcies bereitgestellt wird, um Attribute in Bildern zu ermitteln, die Sie für Artikel und Kontaktpersonen importieren, sodass Sie sie einfach überprüfen und zuordnen können. Für Artikel können Attribute sein, ob der Artikel eine Tabelle oder ein Auto ist und und ob er rot oder blau ist. Für Personen können Attribute Geschlecht oder Alter sein.

Bild-Analyser schlagen Attribute basierend auf Tags vor, die der Computer Vision API findet und einen Vertrauensbereich. Standardmäßig schlägt er Attribute vor, wenn mindestens zu 80% sichergestellt ist, dass das Attribut korrekt ist. Sie können einen anderen Vertrauensbereich festlegen, nach Bedarf. Um mehr darüber zu erfahren, wie die Kategorien und der Vertrauensbereich bestimmt wird, gehen Sie zu [Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).  

Bild-Analyzer ist kostenlos in [!INCLUDE[d365fin](includes/d365fin_md.md)], aber es gibt einen Grenzwert der Anzahl von Artikeln, die Sie für einen bestimmten Zeitraum auswerten können. Standardmäßig können Sie 100 Bilder pro Monat analysieren.

Nachdem Sie die Erweiterung ausführten, wird der Bild-Analyzer ausgeführt, wenn Sie ein Bild einem Artikel oder einer Kontaktperson importieren. Sie finden die Attribute, den Vertrauensbereich und Details sofort und können sich entscheiden, was, jedes Attribut durchzuführen. Wenn Sie Bilder importierten, bevor Sie die Bild-Analyzer-Erweiterung aktiviert haben, müssen Sie zum Artikel oder zur Kontaktkarten wechseln und **Bild analysieren** auswählen.  

## <a name="privacy-notice"></a>Datenschutzhinweis
Diese Erweiterung verwendet die API des maschinellen Sehens vom Microsoft kognitiven Services, die sich unterschiedliche Niveaus von Kompatibilitätsverpflichtungen als [!INCLUDE[d365fin](includes/d365fin_md.md)] haben können. Wenn Sie die Bildanalysatorerweiterung aktivieren, werden zum Beispiel Debitorendaten als ein Kontaktbild oder ein Artikelbild die an API des maschinellen Sehens gesendet. Durch die Installation dieser Erweiterung stimmen Sie zu, dass diese begrenzte Reihe von Daten zur maschinellen API des Sehens gebucht werden kann. Beachten Sie, dass Sie die Bildanalysatorerweiterung deaktivieren oder deinstallieren können, um die Verwendung dieser Funktionalität anzupassen. Weitere Informationen finden Sie unter [Microsoft-Sicherheitscenter](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Anforderungen
Es gibt mehrere Anforderungen für Bilder:

* Bildformate: JPEG, PNG, GIF, BMP  
* Maximale Dateigröße: Weniger als 4 MB  
* Bilddimensionen: Größer als 50 x 50 Pixel  

## <a name="to-enable-image-analyzer"></a>Bild-Analyzer aktiveren
Die Bild-Analyser-Erweiterugn ist in [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert. Sie müssen sie nur aktivieren.

> [!NOTE]  
> Um die Bild-Analyzer-Erweiterung zu aktivieren, müssen Sie ein Administrator sein. Überprüfen, ob Sie dem Benutzerberechtigungssatz **SUPER** zugeordnet werden.

1. Um die Bild-Analyser-Erweiterung auszuführen, führen Sie einen der folgenden Schritte aus:

* Öffnen Sie eine Kontaktkarte. In der Benachrichtigungsleiste wählen Sie **Bilder analysieren** und führen Sie dann die Schritte im unterstützen Einrichtungshandbuch durch.  
* Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Dienstverbindungen** ein, und wählen dann **Bildanalyse-Einrichtung** aus. In der Benachrichtigungsleiste wählen Sie **Bilder analysieren aktivieren** und führen Sie dann die Schritte im unterstützen Einrichtungshandbuch durch.  

    > [!TIP]  
    > Auf der Seite **Bildanalyse-Einrichtung** können Sie auch den Grad des Vertrauens für Attributvorschläge ändern. Wenn Sie beispielsweise einen höheren Prozentsatz an Vertrauen möchten, können Sie einen höheren Prozentsatz eingeben.

## <a name="to-analyze-an-image-of-an-item"></a>Um ein Bild eines Artikels zu analysieren
Die folgenden Schritte beschreiben, wie ein Bild analysiert wird, das importiert wurde, bevor Sie die Bild-Analyse-Erweiterung aktivierten.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Bild analysieren** aus.  
3. Die Seite **Bild-Analyse-Attribute** zeigt die erkannten Attribute, den Vertrauensbereich und andere Details zum Attribut an. Verwenden Sie die Optionen **Aktion auszuführen** um anzugeben, was mit dem Attribut gemacht wird.  

    > [!TIP]  
    > Sie können den Namen des Attributs der Artikelbeschreibung hinzufügen, indem Sie **Fügen Sie Artikelbeschreibung hinzu** auswählen. Beispielsweise kann dies nützlich sein, um schnell Details hinzufügen.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Um ein Bild einer Kontaktperson zu analysieren
Die folgenden Schritte beschreiben, wie ein Bild analysiert wird, das importiert wurde, bevor Sie die Bild-Analyse-Erweiterung aktivierten.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontakte** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Kontaktperson und wählen Sie dann die Aktion **Bild analysieren** aus.  
3. Wählen Sie im Feld Inforegister **Profilbefragung** überprüfen Sie die Vorschläge und machen Sie Korrekturen nach Bedarf.  

## <a name="blacklisting-suggested-attributes"></a>Für die schwarze Liste aktivieren aus vorgeschlagenen Attributen
Wenn die Analyseansicht ein Attribut vorschlägt, dass Sie nicht sehen möchten, können Sie das Umlagerungs- Attribut auf die schwarze Liste setzen. Vorsicht walten lassen. Für die schwarze Liste gesetzte Attribute werden nicht für andere Artikel oder Kontaktpersonen vorgeschlagen. Wenn Sie bedauern, ein Attribut auf die schwarze Liste gesetzt zu haben, wählen Sie **Für die schwarze Liste gesetzte Attribute** dann löschen Sie das Attribut in der Liste.

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Um Ihr eigenes Konto für die Computer Vision API zu verwenden
Sie können auch Ihr eigenes Konto für die Computer Vision API verwenden, beispielsweise wenn Sie mehr Bilder analysieren möchten als wir zulassen..  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bildanalyse-Einrichtung** ein, und wählen dann den zugehörigen Link aus.  
2. Geben Sie die **API URI** und die **API Key** ein, die Sie für die Computer Vision API erhalten.  

    > [!NOTE]  
    > Sie müssen am Ende **/analyze** API URIs hinzufügen hinzufügen, wenn nicht bereits vorhanden ist. Zum Beispiel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Um zu sehen, wie viele Analysen Sie in der laufenden Periode gelassen haben
Sie können die Anzahl Analysen anzeigen, die Sie durchgeführt haben, und wie viele Sie noch tun können, in der laufenden Periode.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bildanalyse-Einrichtung** ein, und wählen dann den zugehörigen Link aus.  
2. **Grenzentyp**, **Grenzwert** und **Analye ausgeführt** liefer die Verbrauchsdaten.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Bild-Analyzer-Erweiterung beenden
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Dienstverbindungen** ein, und wählen dann **Bildanalyse-Einrichtung** aus.  
2. Deaktivieren Sie das Kontrollkästchen **Bild-Analyse aktivieren**.  

## <a name="see-also"></a>Siehe auch
[Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Erste Schritte](product-get-started.md)  
