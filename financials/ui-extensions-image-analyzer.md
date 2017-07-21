---
title: Bild-Analyzer-Erweiterung verwenden | Microsoft Docs
description: "Mit dieser Erweiterung können Bilder von Kontaktpersonen und Artikel analysieren und Attribute finden, damit Sie diese in Financials rasch zuweisen können."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/19/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c981c5528c7a622f9d78ed6a77c27e2ceeba44e3
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---

# <a name="the-image-analyzer-extension-for-microsoft-dynamics-365-for-financials"></a>Die Bild-Analyzer-Eweiterung für Microsoft Dynamics 365 for Financials
Die Bild-Analyser-Erweiterung verwendet die leistungsstarke Bildanalytik, die von der Computer Vision API for Microsoft Cognitive Servcies bereitgestellt wird, um Attribute in Bildern zu ermitteln, die Sie für Artikel und Kontaktpersonen importieren, sodass Sie sie einfach überprüfen und zuordnen können. Für Artikel können Attribute sein, ob der Artikel eine Tabelle oder ein Auto ist und und ob er rot oder blau ist. Für Personen können Attribute Geschlecht oder Alter sein.

Bild-Analyser schlagen Attribute basierend auf Tags vor, die der Computer Vision API findet und einen Vertrauensbereich. Standardmäßig schlägt er Attribute vor, wenn mindestens zu 80% sichergestellt ist, dass das Attribut korrekt ist. Sie können einen anderen Vertrauensbereich festlegen, nach Bedarf. Um mehr darüber zu erfahren, wie die Kategorien und der Vertrauensbereich bestimmt wird, gehen Sie zu[Computer Vision API](https://go.microsoft.com/fwlink/?linkid=851476).  

Bild-Analyzer ist kostenlos in[!INCLUDE[d365fin](includes/d365fin_md.md)], aber es gibt einen Grenzwert der Anzahl von Artikeln, die Sie für einen bestimmten Zeitraum auswerten können. Standardmäßig können Sie 100 Bilder pro Monat analysieren.

Nachdem Sie die Erweiterung ausführten, wird der Bild-Analyzer ausgeführt, wenn Sie ein Bild einem Artikel oder einer Kontaktperson importieren. Sie finden die Attribute, den Vertrauensbereich und Details sofort und können sich entscheiden, was, jedes Attribut durchzuführen. Wenn Sie Bilder importierten, bevor Sie die Bild-Analyzer-Erweiterung aktiviert haben, müssen Sie zum Artikel oder zur Kontaktkarten wechseln und **Bild analysieren** auswählen.  

>   [!NOTE]  
>   Durch diese Erweiterung sind Sie damit einverstanden, dass Microsoft Ihre Daten speichern und verwenden kann, um Microsoft-Dienstleistungen wie Computer Vision API zu verbessern. Um zu helfen Ihren Daten zu schützen, unternehmen  wir Schritte, um die Daten anonym zu machen und sie sicher zu halten. Wir veröffentlichen nicht Ihren Daten oder lassen zu, dass sie andere verwenden. Sie können das Bild des Artikels entfernen in [!INCLUDE[d365fin](includes/d365fin_md.md)], jedoch hat die Computer Vision API das Bild noch in der de-identifizierten Formular. Weitere Informationen finden Sie unter [Microsoft-Sicherheitscenter](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Anforderungen
Es gibt mehrere Anforderungen für Bilder:

* Bildformate: JPEG, PNG, GIF, BMP  
* Maximale Dateigröße: Weniger als 4 MB  
* Bilddimensionen: Größer als 50 x 50 Pixel  

## <a name="blacklisting-suggested-attributes"></a>Für die schwarze Liste aktivieren aus vorgeschlagenen Attributen
Wenn die Analyseansicht ein Attribut vorschlägt, dass Sie nicht sehen möchten, können Sie das Umlagerungs- Attribut auf die schwarze Liste setzen. Vorsicht walten lassen. Für die schwarze Liste gesetzte Attribute werden nicht für andere Artikel oder Kontaktpersonen vorgeschlagen. Wenn Sie bedauern, ein Attribut auf die schwarze Liste gesetzt zu haben, wählen Sie **Für die schwarze Liste gesetzte Attribute** dann löschen Sie das Attribut in der Liste.

## <a name="to-enable-image-analyzer"></a>Bild-Analyzer aktiveren
Die Bild-Analyser-Erweiterugn ist in [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert. Sie müssen sie nur aktivieren.

> [!NOTE]  
> Um die Bild-Analyzer-Erweiterung zu aktivieren, müssen Sie ein Administrator sein. Überprüfen, ob Sie dem Benutzerberechtigungssatz **SUPER** zugeordnet werden.

1. Um die Bild-Analyser-Erweiterung auszuführen, führen Sie einen der folgenden Schritte aus:
  
* Öffnen Sie eine Kontaktkarte. In der Benachrichtigungsleiste wählen Sie **Bilder analysieren** und führen Sie dann die Schritte im unterstützen Einrichtungshandbuch durch.  
* Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "") Symbol **Service-Verbindungen** und dann **Bild-Analyse einrichten** ein. In der Benachrichtigungsleiste wählen Sie **Bilder analysieren aktivieren** und führen Sie dann die Schritte im unterstützen Einrichtungshandbuch durch.  

>   [!TIP]  
>   Auf der Seite **Bildanalyse-Einrichtung** können Sie auch den Grad des Vertrauens für Attributvorschläge ändern. Wenn Sie beispielsweise einen höheren Prozentsatz an Vertrauen möchten, können Sie einen höheren Prozentsatz eingeben. 

## <a name="to-analyze-an-image-of-an-item"></a>Um ein Bild eines Artikels zu analysieren
Die folgenden Schritte beschreiben, wie ein Bild analysiert wird, das importiert wurde, bevor Sie die Bild-Analyse-Erweiterung aktivierten.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Bild analysieren** aus.  
3. Die Seite **Bild-Analyse-Attribute** zeigt die erkannten Attribute, den Vertrauensbereich und andere Details zum Attribut an. Verwenden Sie die Optionen **Aktion auszuführen** um anzugeben, was mit dem Attribut gemacht wird.  

>   [!TIP]  
>   Sie können den Namen des Attributs der Artikelbeschreibung hinzufügen, indem Sie **Fügen Sie Artikelbeschreibung hinzu** auswählen. Beispielsweise kann dies nützlich sein, um schnell Details hinzufügen.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Um ein Bild einer Kontaktperson zu analysieren
Die folgenden Schritte beschreiben, wie ein Bild analysiert wird, das importiert wurde, bevor Sie die Bild-Analyse-Erweiterung aktivierten.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Kontakte** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Kontaktperson und wählen Sie dann die Aktion **Bild analysieren** aus.  
3. Wählen Sie im Feld Inforegister **Profilbefragung** überprüfen Sie die Vorschläge und machen Sie Korrekturen nach Bedarf.  

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Um Ihr eigenes Konto für die Computer Vision API zu verwenden
Sie können auch Ihr eigenes Konto für die Computer Vision API verwenden, beispielsweise wenn Sie mehr Bilder analysieren möchten als wir zulassen..  
  
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Bild-Analyse einrichten** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie die **API URI** und die **API Key** ein,  die Sie für die Computer Vision API erhalten.  
  
>   [!NOTE]  
>   Sie müssen am Ende **/analyze** API URIs hinzufügen hinzufügen, wenn nicht bereits vorhanden ist. Zum Beispiel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Um zu sehen, wie viele Analysen Sie in der laufenden Periode gelassen haben
Sie können die Anzahl Analysen anzeigen, die Sie durchgeführt haben, und wie viele Sie noch tun können, in der laufenden Periode.  
  
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Bild-Analyse einrichten** ein. Wählen Sie dann den zugehörigen Link aus.  
2. **Grenzentyp**, **Grenzwert** und **Analye ausgeführt** liefer die Verbrauchsdaten.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Bild-Analyzer-Erweiterung beenden
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "") Symbol **Service-Verbindungen** und dann **Bild-Analyse einrichten** ein.  
2. Deaktivieren Sie das Kontrollkästchen **Bild-Analyse aktivieren**.  

## <a name="see-also"></a>Siehe auch
[Gewusst wie: Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Willkommen bei [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  


