---
title: Digitale Belege einrichten
description: 'In diesem Artikel wird erläutert, wie Sie erzwungene digitale Belege in Microsoft Dynamics 365 Business Central einrichten und verwenden.'
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
---

# Digitale Belege einrichten

Administratoren können mithilfe der Funktion für digitale Belege verlangen, dass Dokumente bei der Buchung bestimmten Transaktionen beigefügt werden. Daher ermöglicht diese Funktionalität einen quellengesteuerten Ansatz und bietet einen besseren Prüfpfad. Abhängig von den Dokumenten bzw. Journaltypen können hierfür unterschiedliche Durchsetzungsarten konfiguriert werden.

Der Begriff *digitaler Beleg* bezieht sich auf eine digitale oder elektronische Form eines traditionellen Belegs in der Buchhaltung. Ein Beleg ist ein Dokument, das zur Unterstützung und Autorisierung von Finanztransaktionen verwendet wird. In der Buchhaltung dient ein Beleg typischerweise als Nachweis einer Ausgabe oder eines Geldeingangs. Der Beleg kann Details wie das Datum der Transaktion, eine Beschreibung, den Betrag und etwaige Autorisierungsunterschriften enthalten.

> [!IMPORTANT]
> In einigen Ländern und Regionen ist die Konfiguration einiger Optionen möglicherweise eingeschränkt, da bestimmte Einrichtungen möglicherweise gesetzlich vorgeschrieben sind. Wenn Sie auf diese Einschränkungen stoßen, suchen Sie auf der Dokumentationsseite für Ihr Land oder Ihre Region nach einer detaillierten Erklärung.

## Digitale Belege aktivieren

Befolgen Sie diese Schritte, um die digitale Belegfunktion zu aktivieren.

1. Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Einrichtung für digitalen Beleg** ein, und wählen Sie den entsprechenden Link aus.
2. Aktivieren Sie das Kontrollkästchen **Aktiviert**.

## Digitale Belege einrichten

Für die folgenden Dokumente und Buchungsblätter können Sie unterschiedliche Einrichtungen verwenden.

| Postenart | Beschreibung |
|------------|-------------|
| Verkaufsbeleg | Gibt Buchungen an, die aus Verkaufsbelegen abgeschlossen werden. |
| Einkaufsbeleg | Gibt Buchungen an, die aus Einkaufsbelegen abgeschlossen werden. |
| Fibu Buch.-Blatt | Gibt Buchungen an, die aus dem Fibu-Buchungsblatt für alle Kontoarten abgeschlossen werden, mit Ausnahme derjenigen, die sich auf den Debitor und den Kreditor beziehen. Wenn Sie einen dieser Kontotypen auswählen, ändern Sie die Kontrolle über den Buchungsprozess. Wenn Sie **Debitor** als Kontotyp auswählen, prüft das System Ihre Einrichtung, die sich auf das Verkaufsbuchungsblatt bezieht. Wenn Sie **Kreditor** als Kontotyp auswählen, prüft das System Ihre Einrichtung, die sich auf das Einkaufsbuchungsblatt bezieht. |
| Verkauf Buch.-Blatt | Gibt die Buchungen an, die aus dem Verkaufsbuchungsblatt und dem Hauptbuch abgeschlossen werden, wo **Debitor** als Kontotyp ausgewählt ist. |
| Einkauf Buch.-Blatt | Gibt die Buchungen an, die aus dem Einkaufsbuchungsblatt und dem Hauptbuch abgeschlossen werden, wo **Kreditor** als Kontotyp ausgewählt ist. |

Befolgen Sie diese Schritte, um zu definieren, wie Ihre Organisation erzwungene digitale Belege verwendet.

1. Wählen Sie das ![Glühbirne, öffnet die „Wie möchten Sie weiter verfahren“-Funktion 3.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol, geben Sie **Einrichtung für digitalen Belegposten** ein, und wählen Sie den entsprechenden Link aus. Alternativ wählen Sie **Posteneinrichtung** auf der Seite **Einrichtung für digitalen Beleg** aus.
2. Wählen Sie in der Spalte **Postenart** eine Option aus.
3. Wählen Sie in der Spalte **Scheckart** eine Durchsetzungsoption aus. Wenn Sie **Keine** auswählen, können Sie den gewählten Postentyp ohne digitalen Beleg buchen. Wenn Sie **Anhang** auswählen, muss der Posten einen Anhang enthalten. Wenn Sie **Anhang oder Notiz** auswählen, können Sie dem Posten einen Anhang oder eine Notiz beifügen. 
4. Aktivieren Sie das Kontrollkästchen **Automatisch generieren**, um den digitalen Beleg automatisch zu generieren. Wenn Sie Ihrer Transaktion beispielsweise keine Verkaufsrechnung manuell hinzufügen möchten, aktivieren Sie dieses Kontrollkästchen. Dann müssen Sie nur noch das Dokument buchen. Das System erstellt das Dokument automatisch basierend auf Ihrem Berichtslayout und hängt es an die Transaktion an.
5. Aktivieren Sie das Kontrollkästchen **Überspringen, wenn manuell hinzugefügt**, wenn Sie keinen automatisch generierten digitalen Beleg hinzufügen möchten, wenn der Benutzer bereits einen manuellen Anhang hinzugefügt hat.

### Verwenden Sie Quellcodes für die Einrichtung

Um die Erzwingung für Buchungsblätter, aber nicht für alle Transaktionstypen, zu verwenden, verbinden Sie den spezifischen Quellcode, um den Postentyp im Fibu-Buchungsblatt, Verkaufsbuchungsblatt oder Einkaufsbuchungsblatt zu identifizieren.

Gehen Sie folgendermaßen vor, um spezifische Quellcodes für digitale Belege einzurichten:

1. Wählen Sie **Quellcodes** auf der Seite **Einrichtung für digitalen Belegposten** aus.
2. Wählen Sie auf der Seite **Quellcodes für Belegposten** die Quellcodes aus, die Sie konfigurieren möchten.
3. Schließen Sie die Seite.

## Funktionen verwenden

Öffnen Sie einen Einkaufs- oder Verkaufsbeleg und geben Sie Informationen in die erforderlichen Felder ein. Bevor Sie den Beleg buchen, müssen Sie die folgenden Schritte ausführen, um einen digitalen Beleg anzuhängen.

1. Wählen Sie in der **Eingehende Belegdateien**-Infobox **Datei anhängen** aus.
2. Ziehen Sie eine Datei direkt auf die Seite **Datei einfügen** oder navigieren Sie von dieser Seite aus zur Datei.

Der Beleg wird der Infobox **Eingehende Belegdateien** angehängt. Für jede Zeile finden Sie den Belegnamen und -typ.

Wenn Sie versehentlich den falschen Beleg anhängen, befolgen Sie diese Schritte, um ihn zu löschen, bevor Sie den Beleg buchen.

1. Wählen Sie in der Infobox **Eingehende Belegdateien** aus der Belegzeile **Eingehender Beleg** aus.
2. Auf der Seite **Eingehender Beleg** wählen Sie **Löschen** aus.

> [!NOTE]
> Wenn das Anhängen eines digitalen Belegs als obligatorisch konfiguriert ist und Sie versuchen, Belege oder Buchungsblätter zu buchen, ohne einen Beleg anzuhängen, verhindert das System das Buchen. Sie erhalten die folgende Fehlermeldung: „Buchen ohne Anhängen des digitalen Belegs nicht möglich.“

### Angehängte Belege in Transaktionen finden

Sie finden den beigefügten Beleg aus dem gebuchten Beleg oder der Seite **Sachposten** in der Infobox **Eingehende Belegdateien**.

Sie können einen angehängten Beleg nicht löschen, nachdem die Buchung abgeschlossen ist. Sie können jedoch nach Abschluss der Buchung weitere Anhänge hinzufügen.

## Siehe auch

[Finanzmanagement](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
