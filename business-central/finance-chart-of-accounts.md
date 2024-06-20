---
title: Den Kontenplan verstehen
description: 'Beschreibt den Kontenplan, wie man ihn einrichtet und verwendet.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/17/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="understanding-the-chart-of-accounts"></a>Den Kontenplan verstehen

Ein Kontenplan (COA) dient als umfassendes Verzeichnis der Finanzkonten und der entsprechenden Referenznummern. Ein COA verfügt normalerweise über zwei Hauptkategorien an Konten:

- Bilanzkonten: Diese Konten erfassen die Aktiva, Verbindlichkeiten und das Reinvermögen Ihres Unternehmens.
- GuV-Konten: Diese Konten erfassen Erträge aus verschiedenen Quellen und verfolgen darüber hinaus die Aufwendungen.

Bilanzkonten werden weiter in drei Gruppen unterteilt:

1. Aktivkonten: Diese Konten erfassen alle wertvollen Ressourcen Ihres Unternehmens.
1. Verbindlichkeitskonten: Sie erfassen die Verbindlichkeiten Ihres Unternehmens.
1. Eigenkapitalkonten: Stellen den Restwert des Unternehmens dar, nachdem die Verbindlichkeiten von den Aktiva abgezogen wurden.

GuV-Konten werden in zwei Gruppen unterteilt:

1. Ertragskonten: Diese Konten erfassen die Einnahmen Ihres Unternehmens aus verschiedenen Quellen.
1. Aufwandskonten: Auf diesen Konten werden sämtliche Ausgaben Ihres Unternehmens erfasst.

Verwenden Sie den COA, um Transaktionen in der Finanzbuchhaltung Ihres Unternehmens zu erfassen. Jedes Konto verfügt normalerweise über eine Kennung (Kontonummer) und eine beschreibende Überschrift oder Kopfzeile. Die Konten werden systematisch nach Kontotyp codiert.

[!INCLUDE[prod_short](includes/prod_short.md)] umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.

Die Zusammenstellung des Kontenplans Ihres Unternehmens ist eine strategische Entscheidung Ihrer Geschäftsleitung (oder unterliegt länderspezifischen Vorschriften). Er variiert je nach Branche, Geschäftsmodell und Finanzstruktur Ihres Unternehmens. Je nach Branche verfügen Sie beispielsweise möglicherweise über spezielle Aktivkonten, die auf die speziellen Abläufe und Bedürfnisse Ihres Unternehmens zugeschnitten sind:

* Ein Einzelhandelsunternehmen legt möglicherweise Wert auf Lagerbestände und Debitorenkonten.
* Ein Technologieunternehmen könnte sich auf immaterielle Vermögenswerte wie Patente und Software konzentrieren.
* Ein Produktionsbetrieb würde Anlagevermögen und Lieferungen nachverfolgen.

## <a name="the-chart-of-accounts-page"></a>Die Seite „Kontenplan“

Der Kontenplan zeigt alle Sachkonten an. Vom Kontenplan aus können Sie zum Beispiel Folgendes tun:  

* Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.  
* GuV-Kontennullstellung.  
* Die Karte „Sachkonto“ öffnen, um Einstellungen hinzuzufügen oder zu ändern.  
* Sie sehen eine Liste der Buchungsgruppen für dieses Konto.
* Zeigen Sie separate Soll- und Habensalden für ein einzelnes Konto an.

Sie können Sachkonten hinzufügen, ändern oder löschen. Um jedoch Differenzen zu verhindern, können Sie ein Sachkonto nicht löschen, wenn Daten im Kontenplan verwendet werden. Sie können auch das Löschen von Konten in sensiblen Zeiträumen sperren. Weitere Informationen zum Schutz von Konten vor dem Löschen finden Sie unter [Konten löschen](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="the-code-hierarchy-in-gl-accounts"></a>Die Codehierarchie bei Sachkonten

Unternehmen erstellen in der Regel eine hierarchische Struktur in den Sachkontencodes, die widerspiegelt, wohin sie im Kontenplan gehört. In einigen Implementierungen können Sachkontencodes, die mit **1** beginnen, Aktivkonten bezeichnen, während Sachkontencodes, die mit „3“ beginnen, Eigenkapitalkonten bezeichnen. In manchen Regionen gelten es lokale Vorschriften für die Verwendung eines Standardkontenplans. Damit Benutzende diese Hierarchie besser verstehen, ohne die interne Codestruktur kennen zu müssen, können Sie in Ihrem Kontenplan Überschriften und Zwischensummen festlegen, die diese internen Strukturen zusammenfassen.

## <a name="designing-your-chart-of-accounts"></a>Ihren Kontenplan entwerfen

Jede Zeile im Kontenplan entspricht einem Sachkonto der folgenden Typen:

* Buchung (Fibu-Buch.-Blätter können Zeilen auf diese Konten buchen)
* Überschrift (legt eine alle Überschrift im Kontenplan fest)
* Gesamtsumme (legt eine Formel für eine Zwischensumme im Kontenplan fest)
* Anfangssumme (legt eine Anfangsüberschrift für eine Zwischensumme im Kontenplan fest; alle nachfolgenden Zeilen bis zu einer Zeile „Endsumme“ werden eingerückt)
* Endsumme (legt eine Endüberschrift für eine Zwischensumme und die Formel dafür im Kontenplan fest; alle nachfolgenden Zeilen nach dieser Zeile „Endsumme“ werden ausgerückt)

Ein minimalistischer Kontenplan kann lediglich aus Zeilen von Buchungskonten bestehen. Mit den anderen vier Typen legen Sie fest, wie der Kontenplan zusätzlich eine Bilanz mit Überschriften und Zwischensummen darstellen soll. Summierungskonten werden häufig in der Finanzberichterstattung verwendet.

> [!TIP]
> Wenn Sie in Ihrem Kontenplan andere Kontoarten als **Buchungskonten** verwenden, können Sie verschiedene Ansichten festlegen, um die „rohen“ Buchungskonten ohne die Berichtskontoarten für Summierungen und Überschriften anzuzeigen. Zum Beispiel: „Nur Buchungskonten anzeigen“ und „Gesperrte Konten ausblenden“.

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Ihren Kontenplan mithilfe von Dimensionen vereinfachen

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie auf Dokumenten wie Verkaufsaufträgen verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt. Anstatt also für jede Abteilung und jedes Projekt separate Sachkonten einzurichten, können Sie Dimensionen als Grundlage für die Analyse verwenden und müssen keinen komplizierten Kontenplan erstellen.

Um mehr über Dimensionen zu erfahren, gehen Sie zu [Arbeiten mit Dimensionen](finance-dimensions.md).

## <a name="get-a-quick-overview-of-your-finances"></a>Verschaffen Sie sich einen schnellen Überblick über Ihre Finanzen

Auf der Seite **Kontenplan** werden die Konten in einer hierarchischen Liste angezeigt, die einen schnellen Zugriff auf die wichtigsten Informationen zu jedem Konto bietet. Allerdings ist die Liste statisch, und wenn Sie viele Konten haben, müssen Sie möglicherweise blättern, um die verschiedenen Konten anzuzeigen. Wenn Sie nur einen schnellen Überblick über die Grundlagen wie Nettoveränderungen und Salden haben möchten, ist die Seite **Kontenplan Übersicht** eine nützliche Alternative. Das Spaltenlayout auf der Seite ist dasselbe wie auf der Seite **Kontenplan** (allerdings mit weniger Spalten) und damit leicht verständlich. Sie können die hierarchischen Ebenen erweitern oder reduzieren. Um den Wechsel zwischen den Seiten zu erleichtern, ist die Seite **Kontenplan Übersicht** von der Seite **Kontenplan** aus zugänglich.

## <a name="access-to-create-and-edit-the-chart-of-accounts"></a>Zugriff auf das Erstellen und Bearbeiten des Kontenplans

In einem kleinen Unternehmen, wie der CRONUS-Demofirma, können die meisten Benutzer den Kontenplan bearbeiten, mit Ausnahme der Benutzer mit einer TEAMMITGLIED-Lizenz. In größeren Organisationen ist der Zugriff auf die Bearbeitung des Kontenplans typischerweise durch Rollen und Berechtigungen eingeschränkt. Wenn Sie Administrator sind oder die Rolle Business Manager oder Buchhalter haben, können Sie die Berechtigungen der Benutzer steuern, um den richtigen Personen Zugriff auf die entsprechenden Tabellen zu geben. Mehr dazu erfahren Sie unter [Eine Übersicht der Benutzerberechtigungen erhalten](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## <a name="chart-of-accounts-best-practices"></a>Bewährte Vorgehensweisen bei Kontenplänen

Hier sind einige bewährte Vorgehensweise, die Sie bei der Entwicklung und Pflege Ihrer Kontenpläne berücksichtigen sollten:

* Erstellen Sie den Kontenplan Ihres Unternehmens, um die Anforderungen der Geschäftsleitung an die Finanzberichterstattung zu unterstützen und strategische Entscheidungen zu treffen.
* Erwägen Sie, mit einem einfachen Aufbau mit weniger Sachkonten zu beginnen. Sie können bei Bedarf jederzeit detailliertere Konten hinzufügen.
* Legen Sie in Ihrem Kontenplan Überschriften und Zwischensummen fest, die die internen Strukturen in Sachkonten zusammenfassen.
* Verwenden Sie Dimensionen, um Ihren Kontenplan zu vereinfachen. Verwenden Sie nicht für jedes Konto oder jede Abteilung ein eigenes Sachkonto.
* Fügen Sie neue Sachkonten hinzu, sobald diese eingehen, entfernen Sie Konten jedoch erst am Ende Ihrer Finanzperiode aus Ihrem Kontenplan.

## <a name="see-also"></a>Siehe auch

[Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md)  
[Die Finanzbuchhaltung verstehen](finance-general-ledger.md)
[Finanzielle Analysen](bi.md)  
[Finanzen – Übersicht](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
