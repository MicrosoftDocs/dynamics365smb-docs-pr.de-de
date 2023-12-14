---
title: Design Details – Elementverfolgung und Reservierungen
description: Dieses Thema behandelt die Artikelverfolgung und Reservierungen und beschreibt die Konzepte hinter den beiden Optionen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
---
# Designdetails: Artikelverfolgung und Reservierungen

Die gleichzeitige Verwendung von Reservierung und spezifischer Artikelnachverfolgung ist selten, da beide eine Kopplung zwischen Vorrat und Bedarf erstellen. Mit Ausnahme von Situationen, in denen ein Kunde oder ein Produktionsplaner eine bestimmte Charge anfragt, ist es selten sinnvoll, Lagerartikel zu reservieren, die bereits Artikelverfolgungsnummern für bestimmte Anwendungen tragen. Obwohl es möglich ist, Artikel zu reservieren, die eine spezifische Artikelnachverfolgung erfordern, sind spezielle Funktionen erforderlich, um Verfügbarkeitskonflikte zwischen Auftragsbearbeitern zu vermeiden, die dieselben artikelnachverfolgten Artikel anfordern.  
  
Das Konzept der späten Bindung stellt sicher, dass eine nicht-spezifische Reservierung einer Seriennummer oder einer Chargennummer bis zur Buchung lose verbunden bleibt. Zum Zeitpunkt der Buchung kann das Reservierungssystem nicht-spezifische Reservierungen umändern, um sicherzustellen, dass ein fester Ausgleich anhand der Serien- oder Chargennummer möglich ist, die tatsächlich kommissioniert wurde. Unterdessen wird die Serien- oder Chargennummer für spezifische Reservierungen in anderen Belegen bereitgestellt, die bestimmte Serien- oder Chargennummern erfordern.  
  
Eine nicht-spezifische Reservierung ist eine Reservierung, bei der der Benutzer nicht interessiert ist, welcher bestimmte Artikel kommissioniert wird, und eine spezifische Reservierung ist eine, bei der der Benutzer daran interessiert ist.  
  
> [!NOTE]  
> Die Funktionalität der späten Bindung bezieht sich nur auf Artikel, die mit spezifischer Artikelverfolgung eingerichtet wurden, sowie nur auf Reservierungen gegen den Bestand, nicht gegen eingehende Beschaffungsaufträge.  
  
Die Reservierung von Artikelverfolgungsnummern zerfällt in zwei Kategorien, wie in der folgenden Tabelle dargestellt.  
  
|Reservierung|Description|  
|-----------------|---------------------------------------|  
|Ausgewählt|Sie wählen eine bestimmte Serien- oder Chargennummer aus, wenn Sie den Lagerartikel aus einem Bedarf reservieren, beispielsweise einem Verkaufsauftrag.<br /><br /> Dies stellt eine gewöhnliche Reservierung dar. Dies ist eine feste Verknüpfung zwischen Vorrat und Bedarf, die beide Serien- oder Chargennummern enthalten. **Hinweis**  Der Bedarf trägt Serien- oder Chargennummern. <br /><br /> Beispielsweise möchten Sie eine Dose blaue Farbe von Charge A reservieren, da der Kunde dies verlangt. Eine Dose blaue Farbe aus Charge A wird an den Kunden geliefert.|  
|Unspezifisch|Sie können keine bestimmte Serien- oder Chargennummer auswählen, wenn Sie den Lagerartikel aus einem Bedarf reservieren, beispielsweise einem Verkaufsauftrag.<br /><br /> Dies ist ein Status, der einem Reservierungsposten für Serien- oder Chargennummern, die nicht speziell ausgewählt werden, auferlegt wird. **Hinweis:**  Der Bedarf trägt keine Serien- oder Chargennummern. <br /><br /> Sie möchten beispielsweise eine Dose blaue Farbe von einer Charge für Ihren Verkaufsauftrag reservieren. Eine Dose blaue Farbe einer zufälligen Serien- oder Chargennummer wird an den Kunden geliefert.|  
  
Der hauptsächliche Unterschied zwischen spezifischer und unspezifischer Reservierung ist durch das Vorhandensein von Serien- oder Chargennummern auf in der Bedarfsseite definiert, wie in der folgenden Tabelle gezeigt.  

| Typ            | Vorrat                | Bedarf                   |
|-----------------|-----------------------|--------------------------|
| **Ausgewählt**    | Serien- oder Chargennummer | Serien- oder Chargennummer    |
| **Unspezifisch** | Serien- oder Chargennummer | Keine Serien- oder Chargennummer. |
  
Wenn Sie reservieren, werden Lagerbestandsmengen aus einem ausgehenden Beleg für einen Artikel, der die zugeordneten Artikelverfolgungsnummern hat und für bestimmte Artikelverfolgung eingerichtet ist, führt Sie die Seite **Reservierung** durch verschiedene Workflows entsprechend Ihres Bedarfs für eine Serien- oder Chargennummer.  
  
## Spezifische Reservierung  
Wenn Sie **Reservieren** aus der Zeile Ausgehender Beleg aktivieren, erscheint ein Dialogfeld, in dem Sie gefragt werden, ob Sie bestimmte Serien- oder Chargennummern reservieren möchten. Wenn Sie **Ja** auswählen, wird eine Liste mit allen Serien- oder Chargennummern angezeigt, die der Belegzeile zugeordnet sind. Die Seite **Reservierung** wird geöffnet, nachdem Sie eine der Serien- oder Chargennummern auswählen, und Sie können dann unter den ausgewählten Serien- oder Chargennummern in typischer Weise eine Reservierung vornehmen.  
  
Wenn einige der speziellen Artikelverfolgungsnummern, die Sie zu reservieren versuchen, in den unspezifischen Reservierungen geführt werden, informiert Sie eine Meldung unten auf der **Reservierungs**-Seite darüber, wie viel der reservierten Gesamtmenge in nichtspezifischen Reservierungen geführt wird, und ob diese Mengen noch verfügbar sind.  
  
## Unspezifische Reservierungen  
Wenn Sie **Nein** im Dialogfeld auswählen, wird die Seite **Reservierung** geöffnet und ermöglicht Ihnen, unter allen Serien- oder Chargennummern im Bestand zu reservieren.  
  
Aufgrund der Struktur des Reservierungssystems gilt: Wenn Sie eine nicht-spezifische Reservierung für einen Artikel mit Artikelverfolgung setzen, muss das System bestimmte Artikelposten auswählen, gegen die reserviert werden kann. Da die Artikelposten die Artikelverfolgungsnummern enthalten, reserviert die Reservierung indirekt bestimmte Serien- oder Chargennummern, obwohl dies nicht gewünscht ist. Um diese Situation zu behandeln, versucht das Reservierungssystem, nicht-spezifische Reservierungsposten vor der Buchung umzugruppieren.  
  
Die Anwendung reserviert tatsächlich weiterhin für bestimmte Posten, aber dann verwendet es einen Umgruppierungsmechanismus, sobald es speziellen Bedarf für die Chargen- oder Seriennummer in der unspezifischen Reservierung gibt. Dies kann der Fall sein, wenn Sie eine Bedarfstransaktion, beispielsweise einen Verkaufsauftrag, ein FA-Verbrauchs Buch.-Blatt oder einen Umlagerungsauftrag für eine Serien- oder Chargennummer buchen, oder wenn Sie versuchen, die Serien- oder Chargennummer speziell zu reservieren. Die Anwendung gruppiert die Reservierungen um, um die Chargen- oder Seriennummer für den Bedarf oder die spezifische Reservierung zugänglich zu machen, und platziert dadurch eine andere Chargen- oder Seriennummer in die unspezifische Reservierung. Wenn die Menge im Bestand nicht ausreicht, nimmt das System so weit wie möglich Umgruppierungen vor, und Sie erhalten einen Verfügbarkeitsfehler, wenn der Vorrat zum Zeitpunkt der Buchung immer noch nicht ausreicht.  
  
> [!NOTE]  
>  In einer unspezifischen Reservierung ist das Chargennummeren- oder Seriennummernfeld im Reservierungsposten, der wie der Verkauf auf den Bedarf verweist, leer.  
  
## Umgruppierung  
Wenn ein Benutzer einen ausgehenden Beleg bucht, nachdem er die falsche Serien- oder Chargennummer kommissioniert hat, werden andere nicht-spezifische Reservierungen umgruppiert, um die aktuelle Serien- oder Chargennummer wiederzugeben, die kommissioniert wurde. Dadurch wird das Buchungsmodul mit einem festen Ausgleich zwischen Angebot und Nachfrage zufriedengestellt.  
  
Für alle unterstützten Geschäftsszenarien ist die Umgruppierung nur mit positiven Artikelposten möglich, die Reservierungs- und Serien- oder Chargennummern enthalten, aber ohne festgelegte Serien- oder Chargennummern auf der Bedarfsseite.  
  
## Unterstützte Geschäftsszenarien  
Die Funktionalität der späten Bindung unterstützt die folgenden Geschäftsszenarien:  
  
* Eingabe einer bestimmten Serien- oder Chargennummern auf einem ausgehenden Beleg mit unspezifischer Reservierung einer falschen Serien- oder Chargennummer.  
* So reservieren Sie eine bestimmte Serien- oder Chargennummer.  
* Buchen eines ausgehenden Belegs mit unspezifischer Reservierung einer Serien- oder Chargennummer.  
  
### Eingabe von Serien- oder Chargennummern auf einem ausgehenden Beleg mit fehlerhafter unspezifischer Reservierung  
Dies ist das häufigste der drei unterstützten Szenarien. In diesem Fall stellt die Late Binding-Funktion sicher, dass ein Benutzer eine Serien- oder Chargennummer eingeben kann, die tatsächlich kommissioniert wurde, auf einem ausgehenden Beleg, der bereits eine nicht-spezifische Reservierung einer anderen Serien- oder Chargennummer hat.  
  
Beispielsweise entsteht die Notwendigkeit, wenn ein Auftragsverarbeiter zuerst eine nicht-spezifische Reservierung von einer Serien- oder Chargennummer vorgenommen hat. Nachdem der Artikel tatsächlich aus dem Lager entnommen wurde, muss die kommissionierte Serien- oder Chargennummer auf dem Auftrag vor seiner Buchung eingegeben werden. Die nicht-spezifische Reservierung wird zur Buchungszeit umgruppiert, um sicherzustellen, dass die kommissionierte Serien- oder Chargennummer eingegeben werden kann, ohne die Reservierung zu verlieren, sowie um sicherzustellen, dass die kommissionierte Serien- oder Chargennummer vollständig ausgeglichen und gebucht werden kann.  
  
### So reservieren Sie eine bestimmte Serien- oder Chargennummer  
In diesem Szenario stellt die Late Binding-Funktion sicher, dass ein Benutzer, der versucht, eine bestimmte Serien- oder Chargennummer zu reservieren, die derzeit unspezifisch reserviert ist, dies tun kann. Eine nicht-spezifische Reservierung wird zum Zeitpunkt der Reservierung umgruppiert, um die Serien- oder Chargennummer für die spezifische Anfrage freizugeben.  
  
Die Umgruppierung erfolgt automatisch, aber die eingebettete Hilfe wird unten auf der Seite **Reservierung** angezeigt und zeigt den folgenden Text an:  
  
**XX der Gesamten Reservierten Menge sind unspezifisch und möglicherweise verfügbar.**  
  
Darüber hinaus zeigt das Feld **Unspezifische reservierte Menge** an, wie viele Reservierungsposten unspezifisch sind. Standardmäßig ist dieses Feld für Anwender nicht sichtbar.  
  
### Buchen eines ausgehenden Belegs mit unspezifischer Reservierung einer Serien- oder Chargennummer.  
Dieses Geschäftsszenario wird durch die Late Binding-Funktionalität unterstützt, die festen Ausgleich und ausgehende Buchung dessen aktiviert, was tatsächlich kommissioniert wird, indem eine andere nicht-spezifische Reservierung einer Serien- oder Chargennummer umgruppiert wird. Wenn die Umgruppierung nicht möglich ist, dann wird folgende Standardfehlermeldung angezeigt, wenn der Benutzer versucht, die Lieferung zu buchen:  
  
**Artikel XX kann nicht vollständig ausgeglichen werden.**  
  
## Siehe auch  
[Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]