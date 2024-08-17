---
title: Abschluss der Bücher
description: 'Erhalten von Informationen über das Schließens der Bücher für ein Geschäftsjahr oder für eine Periode, und was passiert, nachdem Sie das Jahr abgeschloßen haben.'
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 08/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Abschluss der Bücher
Nachdem sichergestellt wurde, dass sich alle Konten auf dem neuesten Stand befinden und Kosten und Umsatz verteilt wurden, können die Bücher für ein Geschäftsjahr oder für eine Periode abgeschlossen werden.

Der Abschluss eines Jahres ist für Sie keine Pflicht, erleichtert Ihnen aber die Arbeit im System, da Sie so komfortable Filtermöglichkeiten nutzen können. Es besteht auch kein Anlass zur Sorge, dass beim Jahresabschluss Details der Transaktionen verloren gehen, da alle Details auch nach Abschluss eines Jahrs beibehalten werden.

## Abschlussbuchprozess
Der Prozess für den Abschluss der Bücher umfasst diese Hauptaufgaben:

1. Abschließen der Buchhaltungsperiode.

    Ein Geschäftsjahr ist definiert als mindestens eine offene Periode entsprechend der Definition auf der Seite **Buchhaltungsperioden**. Üblicherweise umfasst ein Geschäftsjahr 12 Perioden von jeweils einem Monat, das Jahr kann jedoch auch auf andere Weise definiert werden.

    Weitere Informationen finden Sie unter [Abschließen von Buchhaltungsperioden](year-close-account-periods.md).
2. Erfassen der Vorjahresposten.

    Beim Abschließen eines Geschäftsjahrs müssen eine Reihe verwaltungsbezogener Transaktionen (wie Artikel mit Vorauszahlung oder abgegrenzte Artikel) eingegeben werden. Diese Transaktionen werden als Regulierungsposten bezeichnet. Für das Buchen dieser Einträge gelten keine besonderen Regeln. Wenn sie (wie andere Einträge auch) an einem Datum in einem abgeschlossenen Geschäftsjahr gebucht werden, ist im Feld  **Eintrag des Vorjahres**  ein Häkchen markiert. Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden.
3. Übertragen der Salden aus der GuV in die Bilanz.

    Nachdem ein Geschäftsjahr abgeschlossen wurde und alle Nachbuchungen gebucht wurden, müssen die GuV-Konten abgeschlossen werden, und der Nettoertrag des Jahres muss auf ein Konto übertragen werden, das in der Bilanz unter dem Eigenkapital aufgeführt ist. Verwenden Sie zu diesem Zweck die Stapelverarbeitung GuV-Konten Nullstellung. Mithilfe dieser Stapelverarbeitung werden alle Sachkonten vom Typ GuV verarbeitet und Posten erstellt, mit denen die Salden storniert werden. Diese Posten werden in ein Buch.-Blatt eingefügt, von wo aus sie gebucht werden können. Die Stapelverarbeitung bucht sie nicht automatisch, außer wenn eine zusätzliche Berichtswährung verwendet wird. Bei Verwendung einer Berichtswährung erfolgt eine direkte Buchung in die Finanzbuchhaltung.

    Weitere Informationen finden Sie unter [GuV-Konten Nullstellung](year-close-income-statement.md).
4. Buchen des Ultimopostens für den Jahresabschluss sowie Gegenbuchen von Eigenkapitalkontoposten.

    Wenn die Stapelverarbeitung "GuV-Konten Nullstellung" generiert wurde, buchen Sie die erstellten Einträge. Wenn Sie in der Stapelverarbeitung kein Bilanzgewinnkonto angegeben haben, geben Sie eine Zeile mit einem Ausgleichseintrag ein, der den Nettoertrag in der Bilanz unter dem Eigenkapital auf das richtige Hauptkonto Sachkonto verbucht. Anschließend kann das Buch.-Blatt gebucht werden.

    Weitere Informationen finden Sie unter [Buchen von Jahresabschlussposten](year-how-post-year-end-close-entry.md).

## Was geschieht beim Abschluss?

Wenn Sie am Ende des Jahres den Jahresabschluss durchführen, werden Ihre Erträge aus den berechneten Erträgen auf das Konto "Abschlusskonto GuV" verschoben. Das Geschäftsjahr wird als "Geschlossen" gekennzeichnet, und alle nachfolgenden Posten für das geschlossene Jahr werden als "Nachbuchungen" gekennzeichnet.

Anschließend wird vom System ein Abschlussposten erstellt, der Posten wird jedoch nicht automatisch gebucht. Sie haben die Möglichkeit, die Gegenbuchung(en) auf dem Eigenkapitalkonto vorzunehmen und so über die Zuordnung Ihrer Abschlussbuchung zu entscheiden. Wenn Ihr Unternehmen über mehrere Geschäftsbereiche verfügt, können Sie vom System einen einzigen Ultimoposten für alle Geschäftsbereiche generieren lassen und dann für das Eigenkapitalkonto jedes Geschäftsbereichs eine Gegenbuchung erstellen.

Sie können Buchungen in einem früheren Geschäftsjahr auch durchführen, nachdem die GuV-Konten geschlossen wurden, wenn Sie danach die Stapelverarbeitung GuV-Konten Nullstellung erneut ausführen.

## Siehe auch

[Arbeiten mit Abrechnungszeiträumen und Geschäftsjahren](finance-accounting-periods-and-fiscal-years.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]