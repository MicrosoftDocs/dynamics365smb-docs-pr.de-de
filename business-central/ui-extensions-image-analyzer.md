---
title: Die Bildanalyse-Erweiterung
description: Mit dieser Erweiterung können Bilder von Kontaktpersonen und Artikel analysieren und Attribute finden, damit Sie diese in Business Central rasch zuweisen können.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: bbeffd4175751e08043d79f596027a79c88503bc
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074612"
---
# <a name="the-image-analyzer-extension"></a>Die Bildanalyse-Erweiterung

Die Bild-Analyser-Erweiterung verwendet die leistungsstarke Bildanalytik, die von der Computer Vision API für Azure Cognitive Services bereitgestellt wird, um Attribute in Bildern zu ermitteln, die Sie für Artikel und Kontaktpersonen importieren, sodass Sie sie einfach überprüfen und zuordnen können. Für Artikel können Attribute sein, ob der Artikel eine Tabelle oder ein Auto ist und und ob er rot oder blau ist. Für Personen können Attribute Geschlecht oder Alter sein.

Bild-Analyser schlagen Attribute basierend auf Tags vor, die der Computer Vision API findet und einen Vertrauensbereich. Standardmäßig schlägt er Attribute vor, wenn mindestens zu 80% sichergestellt ist, dass das Attribut korrekt ist. Sie können einen anderen Vertrauensbereich festlegen, nach Bedarf. Um mehr darüber zu erfahren, wie die Kategorien und der Vertrauensbereich bestimmt wird, gehen Sie zu [Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).  

Bild-Analyzer ist kostenlos in [!INCLUDE[prod_short](includes/prod_short.md)], aber es gibt einen Grenzwert der Anzahl von Artikeln, die Sie für einen bestimmten Zeitraum auswerten können. Standardmäßig können Sie 100 Bilder pro Monat analysieren.

Nachdem Sie die Erweiterung ausführten, wird der Bild-Analyzer ausgeführt, wenn Sie ein Bild einem Artikel oder einer Kontaktperson importieren. Sie finden die Attribute, den Vertrauensbereich und Details sofort und können sich entscheiden, was, jedes Attribut durchzuführen. Wenn Sie Bilder importierten, bevor Sie die Bild-Analyzer-Erweiterung aktiviert haben, müssen Sie zum Artikel oder zur Kontaktkarten wechseln und **Bild analysieren** auswählen.  

## <a name="privacy-notice"></a>Datenschutzhinweis

Diese Erweiterung verwendet die API des maschinellen Sehens von Azure Cognitive Services, die unterschiedliche Niveaus von Kompatibilitätsverpflichtungen als [!INCLUDE[prod_short](includes/prod_short.md)] haben können. Wenn Sie die Bildanalysatorerweiterung aktivieren, werden zum Beispiel Debitorendaten als ein Kontaktbild oder ein Artikelbild die an API des maschinellen Sehens gesendet. Durch die Installation dieser Erweiterung stimmen Sie zu, dass diese begrenzte Reihe von Daten zur maschinellen API des Sehens gebucht werden kann. Beachten Sie, dass Sie die Bildanalysatorerweiterung deaktivieren oder deinstallieren können, um die Verwendung dieser Funktionalität anzupassen. Weitere Informationen finden Sie unter [Microsoft-Sicherheitscenter](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Anforderungen

Es gibt mehrere Anforderungen für Bilder:

* Bildformate: JPEG, PNG, GIF, BMP  
* Maximale Dateigröße: Weniger als 4 MB  
* Bilddimensionen: Größer als 50 x 50 Pixel  

## <a name="to-enable-image-analyzer"></a>Bild-Analyzer aktiveren

Die Bild-Analyser-Erweiterugn ist in [!INCLUDE[prod_short](includes/prod_short.md)] integriert. Sie müssen sie nur aktivieren.

> [!NOTE]  
> Um die Bild-Analyzer-Erweiterung zu aktivieren, müssen Sie ein Administrator sein. Überprüfen, ob Sie dem Benutzerberechtigungssatz **SUPER** zugeordnet werden. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

Führen Sie einen der folgenden Schritte aus, um die Bild-Analyser-Erweiterung auszuführen:

* Öffnen Sie eine Kontaktkarte. In der Benachrichtigungsleiste wählen Sie **Bilder analysieren** und führen Sie dann die Schritte im unterstützen Einrichtungshandbuch durch.  
* Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Serviceverbindungen** ein, und wählen Sie dann **Bildanalyseeinrichtung**. In der Benachrichtigungsleiste wählen Sie **Bilder analysieren aktivieren** und führen Sie dann die Schritte im unterstützen Einrichtungshandbuch durch.  

    > [!TIP]  
    > Auf der Seite **Bildanalyse-Einrichtung** können Sie auch den Grad des Vertrauens für Attributvorschläge ändern. Wenn Sie beispielsweise einen höheren Prozentsatz an Vertrauen möchten, können Sie einen höheren Prozentsatz eingeben.

## <a name="to-analyze-an-image-of-an-item"></a>Um ein Bild eines Artikels zu analysieren

Die folgenden Schritte beschreiben, wie ein Bild analysiert wird, das importiert wurde, bevor Sie die Bild-Analyse-Erweiterung aktivierten.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Bild analysieren** aus.  
3. Die Seite **Bild-Analyse-Attribute** zeigt die erkannten Attribute, den Vertrauensbereich und andere Details zum Attribut an. Verwenden Sie die Option **Auszuführende Aktion** aus, um die für das Attribut auszuführenden Aktionen festzulegen, oder wählen Sie **Zur Artikelbeschreibung hinzufügen** aus, um der Artikelbeschreibung den Namen des Attributs hinzuzufügen. Beispielsweise kann dies nützlich sein, um schnell Details hinzufügen. 

Die Aktion **Auszuführende Aktion** stellt die folgende Optionen zur Verfügung:

  * *Ignorieren*

    Es werden keine Aktionen ausgeführt
  * *Als Attribut verwenden*

    Der Wert wird den Artikelattributen hinzugefügt. Weitere Informationen finden Sie unter [Mit Artikelattributen arbeiten](inventory-how-work-item-attributes.md).
  * *Als Kategorie verwenden*

    Der ausgewählte Wert wird als Kategorie hinzugefügt. Weitere Informationen finden Sie unter [Artikel kategorisieren](inventory-how-categorize-items.md).
  * *Zur Ausschlussliste hinzufügen*

    Wenn die Analyse ein Attribut vorschlägt, das Sie nicht sehen möchten, können Sie das Attribut blockieren. Vorsicht walten lassen. Blockierte Attribute werden auch nicht für andere Artikel vorgeschlagen. Wenn Sie ein Attribut versehentlich blockiert haben, wählen Sie **Attribute auf der Ausschlussliste anzeigen** aus, und löschen dann das Attribut aus der Liste.
  
    > [!NOTE]  
    > **Artikelattribute** zeigen standardmäßig Attribute an, deren **Genauigkeitsbewertung** über dem **Schwellenwert Genauigkeitsbewertung in %** liegt, der im **Bildanalysator-Setup** definiert ist. Um alle erkannten Attribute anzuzeigen, wählen Sie die Aktion **Alle Attribute anzeigen** aus.

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Um ein Bild einer Kontaktperson zu analysieren

Die folgenden Schritte beschreiben, wie ein Bild analysiert wird, das importiert wurde, bevor Sie die Bildanalyse-Erweiterung aktiviert haben.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Kontakte** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie die entsprechende Kontaktperson und wählen Sie dann die Aktion **Bild analysieren** aus.  
3. Wählen Sie im Feld Inforegister **Profilbefragung** überprüfen Sie die Vorschläge und machen Sie Korrekturen nach Bedarf. Weitere Informationen finden Sie unter [Geschäftskontakte mit Profilfragebögen klassifizieren](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    > 
    > Die Computer Vision API gibt folgende Attribute zurück:
    > * *Alter*
    >
    >     Ein geschätztes „visuelles Alter“ in Jahren. Es geht darum, wie alt eine Person aussieht, im Gegensatz zum tatsächlichen biologischen Alter.
    > * *Geschlecht*
    >
    >    Weiblich oder männlich
    > 
    > Die Computer Vision API gibt kein Konfidenzniveau für Alters- und Geschlechtsattribute zurück.
  
## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Um Ihr eigenes Konto für die Computer Vision API zu verwenden

Sie können auch Ihr eigenes Konto für die Computer Vision API verwenden, beispielsweise wenn Sie mehr Bilder analysieren möchten als wir zulassen..  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Bildanalysator-Setup** ein, und wählen Sie dann den entsprechenden Link aus.  
2. Geben Sie die **API URI** und die **API Key** ein, die Sie für die Computer Vision API erhalten.  

    > [!NOTE]  
    > Sie müssen am Ende **/analyze** API URIs hinzufügen hinzufügen, wenn nicht bereits vorhanden ist. Zum Beispiel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Um zu sehen, wie viele Analysen Sie in der laufenden Periode gelassen haben

Sie können die Anzahl Analysen anzeigen, die Sie durchgeführt haben, und wie viele Sie noch tun können, in der laufenden Periode.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Bildanalysator-Setup** ein, und wählen Sie dann den entsprechenden Link aus.  
2. **Grenzentyp**, **Grenzwert** und **Analye ausgeführt** liefer die Verbrauchsdaten.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Bild-Analyzer-Erweiterung beenden

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Service-Verbindungen** ein und wählen Sie dann **Bildanalysator-Setup**.  
2. Deaktivieren Sie das Kontrollkästchen **Bild-Analyse aktivieren**.  

Sie können die Erweiterung auch vollständig deinstallieren. Sie können es jederzeit wieder von AppSource abrufen. Weitere Informationen finden Sie unter [Installieren und Deinstallieren von Erweiterungen in Business Central](ui-extensions-install-uninstall.md#uninstalling-an-extension).  

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)  
[Artikel kategorisieren](inventory-how-categorize-items.md)  
[Verwenden Sie Profilbefragungen, um Geschäftskontakten zu klassieren](marketing-create-contact-profile-questionnaire.md)  
[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] über Erweiterungen](ui-extensions.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
