---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Lagermitarbeiter können im Rahmen von Verkaufs- und Bestellungen Nicht-Lagerartikel zusammen mit physischen Gütern versenden und empfangen. Nicht zum Lagerbestand gehörende Gegenstände sind immaterielle Werte, wie z. B. Versicherungen oder zusätzliche Kosten.

Bei Verkaufs- und Einkaufsaufträgen stehen oft verschiedene Dinge auf dem Programm. Beispielsweise können Aufträge Hauptbuchposten, Konten und Anlagevermögen umfassen. Wenn Sie Lagerbelege zur Abwicklung physischer Artikel verwenden, können Sie auch einige Arten von Nicht-Lagerartikeln buchen. Es folgen Beispiele für ausgehende Lagerbelege:

* Lagereinlagerungen
* Wareneingänge
* Lagerkommissionierungen
* Warenausgänge

Damit Lagerarbeiter Artikel versenden und empfangen können, die nicht zum Lagerbestand gehören, füllen Sie das Feld **Lag-unab. aut. über Lager buchen** Feld auf den Seiten **Debitoren & Verkauf Einr.** und **Kreditoren & Einkauf Einr.** Das Feld bietet die folgenden Optionen:

|Option  |Description  |
|---------|---------|
|Keine     |Versenden oder empfangen Sie keine Artikel, die nicht zum Lagerbestand gehören.         |
|Angehängt/zugewiesen     | Buchen Sie Artikelgebühren und andere Nicht-Lagerartikelzeilen, die physischen Artikeln zugewiesen oder diesen zugeordnet sind. Um Nicht-Lagerpositionen an physische Artikel anzuhängen, verwenden Sie die Aktion **Zu Lagerartikelzeile hinzufügen**.        |
|Alle     | Buchen Sie alle Nicht-Bestandszeilen im Quellbeleg, sobald mindestens ein Artikel vom Lagerbeleg gebucht wird.        |

> [!NOTE]
> Die Option **Vollständig** im Feld **Versandhinweis** des Kundenauftrags hat Vorrang vor der Auswahl im **Lag-unab. aut. über Lager buchen** -Feld auf der Seite **Debitoren & Verkauf Einr.**.