---
title: Verwenden Sie Profile, um Kontakte zu klassifizieren
description: "Verwenden Sie Profilbefragungen, um Geschäftskontakten zu klassieren"
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 05/09/2018
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 00cfce8b467040a4de419c1b59a258c0eacf0b9a
ms.contentlocale: de-de
ms.lasthandoff: 05/15/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Verwenden Sie Profilbefragungen, um Geschäftskontakten zu klassieren
Sie können Profilbefragungen einrichten, die Sie beim Eingeben der Informationen über die Profile Ihrer Kontakte verwenden möchten. In jedem Fragebogen können Sie die unterschiedlichen Fragen einrichten, die Sie Ihren Kontakten stellen möchten.  

Sie können die Befragung auch dazu verwenden, um einige Fragen zum Kontakt, Debitor oder Kreditor automatisch zu beantworten.  

## <a name="to-add-a-profile-questionnaire"></a>So fügen Sie eine Profilbefragung hinzu
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurationsragebogen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Registerkarte **Start** in der Gruppe **Neu** die Option **Neu** aus.  
3.  Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>So fügen Sie einen Fragebogen einer Profilbefragung hinzu
1.  Wählen Sie die relevante Profilbefragung aus. Wählen Sie auf der Registerkarte **Start** in der Gruppe **Verarbeiten** die Option **Einrichtung Befragung bearbeiten** aus.  
2.  Wählen Sie in der ersten leeren Zeile im Feld **Art** die Option **Frage** aus, und geben Sie im Feld **Beschreibung** Ihre Frage ein. Füllen Sie die anderen Felder in dieser Zeile aus.  
3.  Wählen Sie in der nächsten leeren Zeile im Feld **Art** die Option **Antwort** aus, und geben Sie im Feld **Beschreibung** Ihre Antwort ein.  
4.  Wählen Sie im Feld **Priorität** die Priorität aus. Definieren Sie in den Feldern **Von Wert** und **Bis Wert** einen Punktbereich. Kontakte, die innerhalb des definierten Bereichs Punkte erhalten, erhalten die Antwort.  

Wiederholen Sie diese Schritte, um alle Fragen und Antworten für die Profilbefragung einzugeben.

Nachdem Sie eine Befragung erstellt haben, müssen Sie Kontaktbewertungen zu erstellen, um Ihre Kontakte zu klassifizieren. Sie können auch Fragen einrichten, die automatisch auf Grundlage der Informationen in der Kontaktkarte bewertet werden.  

> [!NOTE]
> Wenn Sie eine Frage eingeben, die automatisch beantwortet werden soll, wählen Sie die Optionen <STRONG>Zeile</STRONG> und dann <STRONG>Fragendetails</STRONG> aus, um die Kriterien einzugeben, die zur automatischen Beantwortung verwendet werden.

## <a name="the-automatic-classification-of-contacts"></a>Die automatische Klassifizierung von Kontakten
Sie können Ihre Kontakte nach Debitoren, Kreditoren und Kontaktinformationen klassifizieren, indem Sie in dem Fenster "Profilbefragung Einrichtung" automatisch beantwortete **Profilbefragungen** einrichten.  

> [!NOTE]
> Nur als Debitor gespeicherten Kontakten kann eine Klassifizierung auf Debitordatenbasis zugeordnet werden und nur als Kreditor gespeicherten Kontakten kann eine Klassifizierung auf Kreditordatenbasis zugeordnet werden. Die automatische Klassifizierung wird nicht automatisch aktualisiert. Deshalb können Sie die Profilbefragungen aktualisieren, nachdem Sie die Debitor-, Kreditor- oder Kontaktdaten aktualisiert haben, auf denen sie basieren.  

Nachdem Sie automatische beantwortete Profilbefragungen eingerichtet haben, werden dem Kontakt [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch die richtigen Antworten zugeordnet, wenn Sie die Profilbefragung mit diesen Fragen einem Kontakt zuordnen.  

## <a name="example"></a>Beispiel
Sie können Ihre Kontakte danach klassifizieren, wie viel sie bei Ihnen gekauft haben:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Antwort</strong></th>
<th><strong>Gilt für</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>Kontakte, die für 500.000 MW oder mehr gekauft haben</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>Kontakte, die von 100.000 bis 499.000 MW gekauft haben</p></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>Kontakte, die für 99.999 MW oder weniger gekauft haben</p></td>
</tr>
</tbody>
</table>

Füllen Sie hierzu das Fenster **Profilbefragung Einrichtung** folgendermaßen aus:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Art</strong></th>
<th><strong>Beschreibung</strong></th>
<th><strong>Automatische Klassifizierung</strong></th>
<th><strong>Von Wert</strong></th>
<th><strong>Bis Wert</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Frage</p></td>
<td><p>ABC Klassifizierung</p></td>
<td><p>Klicken Sie in das Feld, um ein Häkchen einzufügen.</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Antwort</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500.000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Antwort</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100.000</p></td>
<td><p>499.999</p></td>
</tr>
<tr class="even">
<td><p>Antwort</p></td>
<td><p>L</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99.999</p></td>
</tr>
</tbody>
</table>

Füllen Sie dann das Fenster **Profilbefragungsdetails** folgendermaßen aus:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Feld</strong></th>
<th><strong>Wert</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Debitorenklassifizierungsfeld</strong></td>
<td><emphasis>Verkauf (MW)</emphasis></td>
</tr>
<tr>
<td><strong>Klassifizierungsmethode</strong></td>
<td><emphasis>Definierter Wert</emphasis></td>
</tr>
</tbody>
</table>

Wenn Sie einem Kontakt die Profilbefragung mit dieser Frage zuordnen, wird in die Profilzeilen der Kontaktkarte automatisch die entsprechende Antwort für diesen Kontakt eingetragen.

## <a name="see-also"></a>Siehe auch
[Kontaktpersonen erstellen](marketing-create-contact-persons.md)  
[Anlegen von Kontaktpersonen](marketing-how-create-contact-persons.md)  
[Kontaktunternehmenerstellen](marketing-create-contact-companies.md)  

