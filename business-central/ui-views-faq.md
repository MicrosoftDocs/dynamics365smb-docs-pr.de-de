---
title: Häufig gestellte Fragen zu Listenansichten
description: Detaillierte Informationen zum Speichern von Filtern als Listenansichten.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 04/01/2021
ms.author: mikebc
ms.openlocfilehash: c47f7a6ad3f60cf7f2b0cab31e4abc995fdbae12
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783011"
---
# <a name="list-views-faq"></a>FAQ zu Listenansichten
In diesem Artikel werden Fragen beantwortet, die unsere erfahrenen Benutzer häufig zum Arbeiten mit Listenansichten und zum Speichern von Filtern stellen.  

### <a name="how-do-views-handle-expressions"></a>Wie behandeln Ansichten Ausdrücke?

Beim Speichern einer Ansicht, die Filter mit Ausdrücken wie Datumsbereichen, Operatoren, Schlüsselwörtern oder Filtertoken enthält, wird der Ausdruck und nicht die resultierenden Werte gespeichert&mdash;. Speichern Sie beispielsweise eine Ansicht, die nach dem Filter **Erstellungsdatum** Feld mit dem Ausdruck `-1W..today` filtert, werden immer Datensätze zum aktuellen Datum gefunden, auch wenn im nächsten Monat auf die Ansicht zugegriffen wird.

### <a name="where-are-list-views-saved"></a>Wo werden Listenansichten gespeichert?

Ähnlich wie das Ausblenden eines Felds oder das Umordnen Ihres Navigationsmenüs sind Listenansichten Teil der Benutzerpersonalisierung und werden in der Datenbank gespeichert. Wenn Sie alle Personalisierungen in einer Liste löschen, werden auch Ihre persönlichen Ansichten dauerhaft entfernt und zusätzliche Personalisierungen, z. B. das Neuordnen von Ansichten, werden ebenfalls deaktiviert. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsplatz](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a><a name="save"></a>Warum habe ich kein Speichern-Symbol?

Es gibt einige Gründe, warum das Symbol und das Optionsmenü Speichern neben den Ansichten im Filterbereich möglicherweise nicht angezeigt werden.

Ein Grund könnte sein, dass die Personalisierung für Ihre Benutzerrolle nicht aktiviert ist. In diesem Fall haben Sie weiterhin Zugriff auf Systemansichten, die ein Standardbestandteil der Seiten sind. Sie können diese Ansichten ändern, z. B. Filter ändern oder hinzufügen. Sie können die Änderungen einfach nicht speichern. Ein weiterer Grund könnte sein, dass die Seite, die Sie betrachten, eine *Arbeitsblatt* Typ Seite&mdash;ist und keine Liste.

### <a name="on-which-page-types-can-i-use-list-views"></a>Auf welchen Seitentypen kann ich Listenansichten verwenden?

Ansichten sind nur auf Listen- und Arbeitsblattseiten verfügbar.

### <a name="how-do-i-know-whether-im-on-list-type-page"></a>Woher weiß ich, ob ich auf der Seite mit dem Listentyp bin

Seitenüberprüfung verwenden. Drücken Sie zum Öffnen der Seitenprüfung Strg + ALT+F1. Dann im Feld **Seite** suchen Sie nach dem Wort **Liste** in der Klammer am Ende.

### <a name="are-views-also-available-on-other-form-factors"></a>Sind Ansichten auch für andere Formfaktoren verfügbar?

Ja. Alle Ansichten, die Sie in Ihrem Desktop-Browser oder Ihrer Desktop-App speichern, sind auch auf Ihrem Tablet oder Smartphone verfügbar. Sie können Ansichten auf Mobilgeräten nicht ändern oder personalisieren.

### <a name="are-my-personal-views-always-accessible"></a>Sind meine persönlichen Ansichten immer zugänglich?

Ihre Ansichten sind auf einer Listenseite verfügbar, wenn Sie über das Navigationsmenü über das Fenster **Sag mir** oder über einen URL-Link zur Listenseite darauf zugreifen. Ansichten sind in Listenteilen, Suchen oder immer dann nicht verfügbar, wenn eine Listenseite als Dialogfeld angezeigt wird.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Wie kann ich eine Ansicht nach dem Ändern auf die ursprünglichen Filter zurücksetzen?

Wählen Sie unten im Filterbereich die Option **Filter zurücksetzen** Aktion zum Löschen von Filteränderungen, die Sie an der Ansicht vorgenommen haben, und kehren Sie zu den ursprünglich gefilterten Feldern und Filterkriterien zurück.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Was ist der Unterschied zwischen dem Ausblenden und Entfernen von Ansichten?

Durch das Entfernen einer Ansicht wird diese Ansicht dauerhaft gelöscht. Wenn Sie eine Ansicht ausblenden, können Sie sie vorübergehend im Filterbereich ausblenden. Sie können sie jedoch später wieder einblenden, indem Sie auf die Schaltfläche klicken **Anzeigen** Aktion.

### <a name="how-can-i-share-my-views-with-others"></a>Wie kann ich meine Ansichten mit anderen teilen?

[!INCLUDE[prod_short](includes/prod_short.md)] bietet keine Möglichkeit, die genaue Listenansicht freizugeben. Sie können jedoch Ihre aktuellen Filter freigeben, damit andere Benutzer eine ähnliche Liste von Datensätzen sehen können. Kopieren Sie in Ihrem Desktop-Browser einfach die URL und geben Sie sie dann an Ihre Kollegen weiter. Bei der Freigabe von Filtern kann nicht garantiert werden, dass der Empfänger die gleichen Filter erhält, die auch in Ihrem Browser angezeigt werden.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Kann ich im Tell Me-Fenster nach Ansichten suchen?

Nr. Das **Sag mir** Fenster zeigt nur Suchergebnisse für die Seite an, aber Sie sind nur einen Schritt davon entfernt, zu Ihrer Lieblingsansicht zu gelangen, sobald Sie zur Seite navigieren.

### <a name="what-is-shared-layout"></a>Was ist ein geteiltes Layout?

Alle Ansichten auf einer Listenseite haben ein gemeinsames Spaltenlayout. Das Layout enthält die angezeigten Spalten, deren Reihenfolge, Breite, Einfrierbereich und Einstellungen für die Schnelleingabe. Das Personalisieren eines beliebigen Spaltenlayouts wirkt sich auch auf andere Ansichten aus, die das gleiche Layout auf der Listenseite haben.

Einige Systemansichten können eindeutige Layouts der Spalten in der Liste haben. Beispielsweise könnten sie die Spalten neu anordnen, um nur die Spalten anzuzeigen, die für diese Ansicht am relevantesten sind. Sie können feststellen, welche Ansichten eindeutige Layouts haben, indem Sie das Symbol ![Weitere Optionen anzeigen](media/show-more-options-icon.png "Weitere Optionen anzeigen") auswählen und beobachten, dass das Kontrollkästchen **Gemeinsames Layout** nicht aktiviert ist. Als Benutzer können Sie das Spaltenlayout für eine Ansicht mit einem eindeutigen Layout personalisieren, ohne dass die anderen Ansichten auf der Listenseite davon betroffen sind. Nur Entwickler können ein eindeutiges Spaltenlayout für eine Ansicht definieren, die ursprünglich ein gemeinsames Layout hat.

### <a name="what-does-the-show-system-filters-link-do"></a>Was bewirkt der Link Systemfilter anzeigen?

Auf einigen Listenseiten wird der Filterbereich **Systemfilter anzeigen** am unteren Rand des Filterbereichs angezeigt, wenn die Seite vom System festgelegte Filter enthält. Diese speziellen Filter werden normalerweise verwendet, um Datensätze basierend auf dem aktuellen Kontext anzuzeigen. Ein Beispiel wäre, wenn eine Auftragsliste für einen bestimmten Kunden gefiltert werden muss.

Systemfilter werden von Anwendungsentwicklern mithilfe der Filtergruppe 0 festgelegt. Weitere Informationen zu Systemfiltern finden Sie unter [Filtergruppenmethode](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method).

### <a name="i-see-multiple-views-on-my-page-but-i-didnt-create-them-where-did-they-come-from"></a>Auf meiner Seite werden mehrere Ansichten angezeigt, die ich aber nicht erstellt habe. Wo kamen Sie her?

Die in einer Liste angezeigten Ansichten sind eine Kombination aus Ihren persönlichen Ansichten und Systemansichten. Systemansichten können von der Geschäftsanwendung oder von Erweiterungen stammen oder rollenabhängig sein, wenn die Liste für Ihre Rolle angepasst wurde.

### <a name="why-do-some-views-provide-fewer-options"></a>Warum bieten einige Ansichten weniger Optionen?

Einige Ansichten bieten nur die Möglichkeit, eine Kopie der Ansicht zu speichern, während andere das Speichern von Änderungen an der Ansicht hingegen nicht zulassen. Wie die Ansicht erstellt wurde, bestimmt die verfügbaren Optionen für diese Ansicht. Ansichten können auf verschiedene Arten erstellt werden:

- Persönliche Ansichten, die Sie gespeichert haben
- Systemansichten, die ein Standardbestandteil der Geschäftsanwendung sind oder durch Erweiterungen oder rollenspezifische Ansichten hinzugefügt werden. Im Gegensatz zu persönlichen Ansichten können Sie Änderungen an Filtern nicht in dieser Systemansicht speichern.
- Ältere Systemansichten, die ein Standardbestandteil der Geschäftsanwendung sind, jedoch mit älteren Versionen von [!INCLUDE[prod_short](includes/prod_short.md)] erstellt wurden. Diese Ansichten bieten Ihnen deutlich weniger Optionen. Sie können sie nur als neue Ansicht speichern aber nicht ausblenden oder neu anordnen. Beachten Sie, dass ältere Systemansichten in einem zukünftigen Update von [!INCLUDE[prod_short](includes/prod_short.md)] nicht weiter unterstützt werden.

### <a name="how-do-i-convert-legacy-system-views"></a>Wie konvertiere ich ältere Systemansichten?

Ältere Systemansichten sind Listenansichten, die von Entwicklern in älteren Versionen von [!INCLUDE[prod_short](includes/prod_short.md)] erstellt wurden, indem Sie sie auf der Seite Rollencenter platzieren. Diese Ansichten werden jetzt direkt auf der Listenseite angezeigt, bieten jedoch eine beeinträchtigte Erfahrung und deutlich weniger Optionen. Sie können eine alte Systemansicht in eine vollständig anpassbare persönliche Ansicht umwandeln, indem Sie diese alte Ansicht einfach als neue Ansicht speichern. Ebenso können Administratoren die rollenabhängigen älteren Systemansichten konvertieren, indem sie die Benutzerrolle anpassen und die ältere Ansicht als neue rollenabhängige Ansicht speichern.

Beachten Sie, dass ältere Systemansichten in einem zukünftigen Update von [!INCLUDE[prod_short](includes/prod_short.md)] nicht weiter unterstützt werden.

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Andere in meiner Organisation benötigen standardmäßig ähnliche Listenansichten. Was kann ich tun?

Das Arbeiten mit persönlichen Ansichten ist jedoch schnell und effektiv aber [!INCLUDE[prod_short](includes/prod_short.md)] bietet weitere Tools zum Definieren von Listenansichten, die von bestimmten Benutzerrollen oder allen Benutzern in der Organisation benötigt werden.
 - Entwickler können die Umgebung anpassen und Listenansichten in Erweiterungen für alle Benutzer in der Organisation erstellen.
 - Nicht-Programmierer wie Administratoren oder Abteilungsleiter können rollenbezogene Listenansichten erstellen, wenn Sie eine Rolle auf der Seite **Profile (Rollen)** anpassen.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Ich arbeite mit mehreren Sprachen: Wie übersetze ich den Namen der Ansicht?

Wenn Sie eine neue Ansicht speichern oder eine vorhandene Ansicht umbenennen, müssen Sie einen erkennbaren und aussagekräftigen Namen für diese Ansicht eingeben. Der Name wird für Ihre aktuelle Sprache gespeichert und auch angezeigt, wenn Sie oder andere Benutzer damit in [!INCLUDE[prod_short](includes/prod_short.md)] in verschiedenen Sprachen arbeiten. Um übersetzte Ansichtsnamen bereitzustellen, wechseln Sie die Sprache mithilfe der Seite **Meine Einstellungen**. Benennen Sie dann die Ansicht um, in der der übersetzte Name in der neuen Sprache gespeichert wird.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Arbeiten Ansichten mit Ausdrücken in allen Sprachen?

Ausdrücke, die nur Symbole verwenden, z. B. `|` oder `..` gelten als sicher für Benutzer, auf die in jeder Sprache zugegriffen werden kann. Alle Ansichten mit Ausdrücken, die Buchstaben, Schlüsselwörter oder Filtertoken enthalten, funktionieren nur für die Sprache, in der sie auch verfasst wurden.

### <a name="see-also"></a>Siehe auch

[Speichern und personalisieren Sie Listenansichten](ui-views.md)  
[Suchen von Funktionen und Informationen](ui-search.md)  
[Sortieren, Suchen und Filtern](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]