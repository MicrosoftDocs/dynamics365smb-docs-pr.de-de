---
title: "Schließen der Bücher| Microsoft Docs"
description: "Erklärt die Vorgänge beim Abschließen der Bücher für ein Geschäftsjahr oder eine Periode."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a8d379c971d9b21b0eac552f8c7f68926090f037
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="closing-books"></a>Schließen der Bücher
Nachdem sichergestellt wurde, dass sich alle Konten auf dem neuesten Stand befinden und Kosten und Umsatz verteilt wurden, können die Bücher für ein Geschäftsjahr oder für eine Periode abgeschlossen werden.

Ein Jahresabschluss muss nicht zwingend durchgeführt werden, erleichtert Ihnen aber die Arbeit im System, da Sie auf diese Weise die Vorteile der benutzerfreundlichen Filteroptionen nutzen können. Es besteht auch kein Anlass zur Sorge, dass beim Jahresabschluss Details der Transaktionen verloren gehen, da alle Details auch nach Abschluss eines Jahrs beibehalten werden.

## <a name="closing-book-process"></a>Prozess zum Abschließen der Bücher
Der Prozess für den Abschluss der Bücher umfasst diese Hauptaufgaben:

1. Abschließen der Buchhaltungsperiode.

    Ein Geschäftsjahr ist definiert als mindestens eine offene Periode im Fenster **Buchhaltungsperioden**. Üblicherweise umfasst ein Geschäftsjahr 12 Perioden von jeweils einem Monat, das Jahr kann jedoch auch auf andere Weise definiert werden.

    Weitere Informationen finden Sie unter [Vorgehensweise: Abschließen von Buchhaltungsperioden](year-close-account-periods.md).
2. Erfassen der Vorjahresposten.

    Beim Abschließen eines Geschäftsjahrs müssen eine Reihe verwaltungsbezogener Transaktionen (wie Artikel mit Vorauszahlung oder abgegrenzte Artikel) eingegeben werden. Diese Transaktionen werden als Regulierungsposten bezeichnet. Für die Buchung dieser Posten gelten keine besonderen Regeln, und auch bei diesen Posten ist das Kontrollkästchen **Nachbuchung** aktiviert, wenn sie für ein Datum gebucht werden, das innerhalb eines abgeschlossenen Geschäftsjahrs liegt. Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden.
3. Übertragen der Salden aus der GuV in die Bilanz.

    Nachdem ein Geschäftsjahr abgeschlossen wurde und alle Nachbuchungen gebucht wurden, müssen die GuV-Konten abgeschlossen werden, und der Nettoertrag des Jahres muss auf ein Konto übertragen werden, das in der Bilanz unter dem Eigenkapital aufgeführt ist. Verwenden Sie zu diesem Zweck die Stapelverarbeitung GuV-Konten Nullstellung. Mithilfe dieser Stapelverarbeitung werden alle Sachkonten vom Typ GuV verarbeitet und Posten erstellt, mit denen die Salden storniert werden. Diese Posten werden in ein Buch.-Blatt eingefügt, von wo aus sie gebucht werden können. Durch die Stapelverarbeitung erfolgt keine automatische Buchung, es sei denn, es wird eine Berichtswährung verwendet. Bei Verwendung einer Berichtswährung erfolgt eine direkte Buchung in die Finanzbuchhaltung.

    Weitere Informationen finden Sie unter [GuV-Konten Nullstellung](year-close-income-statement.md).
4. Buchen des Ultimopostens für den Jahresabschluss sowie Gegenbuchen von Eigenkapitalkontoposten.

    Wenn die Stapelverarbeitung "GuV-Konten Nullstellung" generiert wurde, buchen Sie die erstellten Einträge. Wurde in der Stapelverarbeitung kein GuV-Abschlusskonto angegeben, geben Sie eine Zeile mit einem Saldoposten ein, durch den der Nettoertrag auf das korrekte Konto (in der Bilanz unter "Eigenkapital") gebucht wird. Anschließend kann das Buch.-Blatt gebucht werden.

    Weitere Informationen finden Sie unter [Vorgehensweise: Buchen von Jahresabschlussposten](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close"></a>Was erfolgt, wenn Sie abschließen
Wenn Sie am Ende des Jahres den Jahresabschluss durchführen, werden Ihre Erträge aus den berechneten Erträgen auf das Konto "Abschlusskonto GuV" verschoben. Das Geschäftsjahr wird als "Geschlossen" gekennzeichnet, und alle nachfolgenden Posten für das geschlossene Jahr werden als "Nachbuchungen" gekennzeichnet.

Anschließend wird ein Ultimoposten generiert, der jedoch nicht automatisch gebucht wird. Sie erhalten die Möglichkeit, die Gegenbuchung der Posten des Eigenkapitalkontos durchzuführen, sodass Sie entscheiden können, wie der Ultimoposten zugeordnet wird. Wenn Ihr Unternehmen über mehrere Geschäftsbereiche verfügt, können Sie vom System einen einzigen Ultimoposten für alle Geschäftsbereiche generieren lassen und dann für das Eigenkapitalkonto jedes Geschäftsbereichs eine Gegenbuchung erstellen.

Sie können Buchungen in einem früheren Geschäftsjahr auch durchführen, nachdem die GuV-Konten geschlossen wurden, wenn Sie danach die Stapelverarbeitung GuV-Konten Nullstellung erneut ausführen.

## <a name="see-also"></a>Siehe auch
[So geht's: Ein neues Geschäftsjahr eröffnen](finance-how-open-new-fiscal-year.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

