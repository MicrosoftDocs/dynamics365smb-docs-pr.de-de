---
title: Verwenden Sie Profile, um Kontakte zu klassifizieren
description: Rot darüber, wie Sie Profilfragebögen festlegen können, um die Profile Ihrer Geschäftskontakte zu klassifizieren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 06/22/2021
ms.openlocfilehash: 6ce13672651a5b6b65712928b764ad11b3db514d
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588526"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Verwenden Sie Profilbefragungen, um Geschäftskontakten zu klassieren
Sie können Profilbefragungen einrichten, die Sie beim Eingeben der Informationen über die Profile Ihrer Kontakte verwenden möchten. In jedem Fragebogen können Sie die unterschiedlichen Fragen einrichten, die Sie Ihren Kontakten stellen möchten.  

Sie können die Befragung auch dazu verwenden, um einige Fragen zum Kontakt, Debitor oder Kreditor automatisch zu beantworten.  

## <a name="to-add-a-profile-questionnaire"></a>So fügen Sie eine Profilbefragung hinzu
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Fragebogen Einrichtung** ein und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Neu**.  
3.  Füllen Sie die Felder bei Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>So fügen Sie einen Fragebogen einer Profilbefragung hinzu
1.  Wählen Sie den entsprechenden Profilfragebogen aus und wählen Sie dann die Aktion **Einstellung Fragebogen bearbeiten**.  
2.  Wählen Sie in der ersten leeren Zeile im Feld **Art** die Option **Frage** aus, und geben Sie im Feld **Beschreibung** Ihre Frage ein. Füllen Sie die anderen Felder in dieser Zeile aus.  
3.  Wählen Sie in der nächsten leeren Zeile im Feld **Art** die Option **Antwort** aus, und geben Sie im Feld **Beschreibung** Ihre Antwort ein.  
4.  Wählen Sie im Feld **Priorität** die Priorität aus. Definieren Sie in den Feldern **Von Wert** und **Bis Wert** einen Punktbereich. Kontakte, die innerhalb des definierten Bereichs Punkte erhalten, erhalten die Antwort.  

Wiederholen Sie diese Schritte, um alle Fragen und Antworten für die Profilbefragung einzugeben.

Nachdem Sie eine Befragung erstellt haben, müssen Sie Kontaktbewertungen zu erstellen, um Ihre Kontakte zu klassifizieren. Sie können auch Fragen einrichten, die automatisch auf Grundlage der Informationen in der Kontaktkarte bewertet werden.  

> [!NOTE]
> Wenn Sie eine Frage eingeben, die automatisch beantwortet werden soll, wählen Sie die Optionen <STRONG>Zeile</STRONG> und dann <STRONG>Fragendetails</STRONG> aus, um die Kriterien einzugeben, die zur automatischen Beantwortung verwendet werden.

## <a name="the-automatic-classification-of-contacts"></a>Die automatische Klassifizierung von Kontakten
Sie können Ihre Kontakte nach Debitoren, Kreditoren und Kontaktinformationen klassifizieren, indem Sie auf der Seite Profilbefragung einrichten automatisch beantwortete **Profilbefragungen** einrichten.  

> [!NOTE]
> Nur als Debitor gespeicherten Kontakten kann eine Klassifizierung auf Debitordatenbasis zugeordnet werden und nur als Kreditor gespeicherten Kontakten kann eine Klassifizierung auf Kreditordatenbasis zugeordnet werden. Die automatische Klassifizierung wird nicht automatisch aktualisiert. Deshalb können Sie die Profilbefragungen aktualisieren, nachdem Sie die Debitor-, Kreditor- oder Kontaktdaten aktualisiert haben, auf denen sie basieren.  

Nachdem Sie automatische beantwortete Profilbefragungen eingerichtet haben, werden dem Kontakt [!INCLUDE[prod_short](includes/prod_short.md)] automatisch die richtigen Antworten zugeordnet, wenn Sie die Profilbefragung mit diesen Fragen einem Kontakt zuordnen.  

## <a name="example"></a>Beispiel

Sie können Ihre Kontakte danach klassifizieren, wie viel sie bei Ihnen gekauft haben:

|Antwort|Gilt für|
|--- |--- |
|A|Kontakte, die für 500.000 MW oder mehr gekauft haben|
|B|Kontakte, die von 100.000 bis 499.999 MW gekauft haben|
|U|Kontakte, die für 99.999 MW oder weniger gekauft haben|

Füllen Sie hierzu die Seite **Profilbefragung einrichten** folgendermaßen aus:

| Typ     | Beschreibung        | Automatische Klassifizierung     | Von Wert | Nach Wert |
|----------|--------------------|------------------------------|------------|----------|
| Frage | ABC Klassifizierung | Klicken Sie in das Feld, um ein Häkchen einzufügen. |            |          |
| Antwort   | A                  |                              | 500.000    |          |
| Antwort   | F                  |                              | 100,000    | 499,999  |
| Antwort   | U                  |                              |            | 99,999   |

Füllen Sie dann das Fenster **Profilfragendetails** folgendermaßen aus:

| Feld                         | Wert         |
|-------------------------------|---------------|
| Feld für die Klassifizierung des Debitors | Umsatz (LCY)   |
| Klassifizierungsmethode         | Definierter Wert |

Wenn Sie einem Kontakt die Profilbefragung mit dieser Frage zuordnen, wird die Anwendung in die Profilzeilen der Kontaktkarte automatisch die entsprechende Antwort für diesen Kontakt eingetragen.

## <a name="see-also"></a>Siehe auch

[Kontakte erstellen](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]