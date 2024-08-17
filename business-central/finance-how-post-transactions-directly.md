---
title: Datensätze für Ausgaben oder Einnahmen direkt im Hauptbuch erfassen
description: 'Sie können auf der Seite „Hauptbuch“ Transaktionen für Geschäftsaktivitäten erstellen, die kein Dokument beinhalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 08/06/2024
ms.service: dynamics-365-business-central
---

# Transaktionen direkt in der Finanzbuchhaltung buchen

Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Debitoren- oder Mitarbeiterkonten.  

Eine typische Verwendung des Fibu Buch.-Blatt gehört die Buchung der Ausgaben der Mitarbeiter während Geschäftsaktivitäten zur späteren Rückvergütung. Weitere Informationen finden Sie unter [Ausgaben der Mitarbeiter erfassen und zurückerstatten](finance-how-record-reimburse-employee-expenses.md).

Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Mitarbeiterkonten. Bei der Buchung mit einem Fibu Buch.-Blatt werden Posten für Sachkonten erstellt. Posten werden auch dann erstellt, wenn beispielsweise eine Buch.-Blattzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird. Sie können Ihre Version eines Fibu Buch.-Blattes anpassen, indem Sie einen Buch.-Blattnamen oder eine Vorlage einrichten. Weitere Informationen finden Sie unter [Arbeiten mit Allgemeinen Buch.-Blättern](ui-work-general-journals.md).

Posten, die Sie mit Belegen buchen, erfordern einen Gutschriftsprozess. Sie können jedoch Posten stornieren, die Sie mit dem Hauptbuch buchen. Weitere Informationen finden Sie unter [Erfassungsbuchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md).

## Transaktionen direkt in die Finanzbuchhaltung buchen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Allgemeine Erfassungen** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnet Sie das Fibu Buch.-Blatt. Weitere Informationen finden Sie unter [Arbeiten mit Allgemeinen Buch.-Blättern](ui-work-general-journals.md).
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Wiederholen Sie Schritt 3 für alle Transaktionen, die Sie buchen möchten.

    > [!TIP]  
    > Wenn Sie Zeilen mit mehreren Transaktionszeilen vor einer Gegenkontozeile, beispielsweise für ein Bankkonto, eingeben möchten, aktivieren Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel auf der Seite **Fibu Buch.-Blatt-Stapelverarbeitungen**. Das Feld **Betrag** auf der Gegenkontozeile wird automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.
5. Wählen Sie die **Buchen** Aktion aus, um die Transaktionen in den angegebenen Sachkonten zu erfassen.

## Siehe auch

[Arbeiten mit Fibu-Buch.-Blättern](ui-work-general-journals.md)    
[Spesen der Mitarbeiter erfassen und erstatten](finance-how-record-reimburse-employee-expenses.md)    
[Journalbuchungen stornieren und Wareneingänge/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md)    
[Finanzen](finance.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]