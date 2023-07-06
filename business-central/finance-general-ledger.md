---
title: Verstehen des Hauptbuchs und des COA
description: 'Beschreibt das Hauptbuch, den Kontenplan und die Kontenkategorien. Verwenden Sie die Seite Finanzbuchhaltung Einrichtung, um die Handhabung der Buchhaltung in Ihrer Firma festzulegen.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts"></a><a name="understanding-the-general-ledger-and-chart-of-accounts"></a><a name="understanding-the-general-ledger-and-chart-of-accounts"></a>Das Hauptbuch und den Kontenplan verstehen

Das Hauptbuch (G/L) speichert Ihre Finanzdaten, und der Kontenplan (COA) zeigt die Konten, auf die alle Hauptbucheinträge gebucht werden. [!INCLUDE[prod_short](includes/prod_short.md)] umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.

## <a name="general-ledger-setup-and-general-posting-setup"></a><a name="general-ledger-setup-and-general-posting-setup"></a><a name="general-ledger-setup-and-general-posting-setup"></a>Finanzbuchhaltungs-Einrichtung und Buchungsmatrix Einrichtung

Die Einrichtung der Finanzbuchhaltung ist das Kernstück der Finanzvorgängen, da sie definieren, wie Sie Daten buchen. Bei der Konfiguration Ihrer Finance-Prozesse spielen vor allem zwei Seiten eine wichtige Rolle:  

* Die Seite **Finanzbuchhaltung Einrichtung**

  Auf der Seite **Finanzbuchhaltung einrichten** geben Sie an, wie bestimmte finanzbuchhalterische Sachverhalte in Ihrem Unternehmen gehandhabt werden sollen, wie beispielsweise:  

  * Rechnungsrundungskontodetails  
  * Adressformate  
  * Finanzberichterstellung

  > [!TIP]
  > Die Seite **Finanzbuchhaltung Einrichtung** enthält allgemeine Felder sowie Felder, die für Ihr Land oder Ihre Region spezifisch sind. Wenn Sie sich über die Bedeutung eines Feldes nicht im Klaren sind, empfehlen wir Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um festzustellen, ob es für Ihr Unternehmen relevant ist. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

  Öffnen Sie die Seite [hier](https://businesscentral.dynamics.com/?page=118).
  
* Die Seite **Buchungsmatrix Einrichtung**

  Ebenso geben Sie auf der Seite **Buchungsmatrix Einrichtung** an, wie Sie Kombinationen aus Geschäftsbuchungsgruppen und Produktbuchungsgruppen einrichten wollen. Buchungsgruppen ordnen Entitäten wie Kunden, Lieferanten, Artikel, Ressourcen sowie Verkaufs- und Kaufbelege den Hauptbuch-Konten zu. Für jede Kombination aus Geschäftsbuchungsgruppe und Produktbuchungsgruppe geben Sie eine Zeile ein. Sie können jedoch auch jede Zeile in einer eigenen Buchungseinrichtungskarte öffnen. Erfahren Sie mehr unter [Buchungsgruppen Einrichtungen](finance-posting-groups.md).  

  > [!TIP]
  > Wenn Sie die Felder, die Sie suchen, auf der Seite **Allgemeine Buchungsmatrixeinrichtung** nicht sehen können, verwenden Sie die horizontale Bildlaufleiste am unteren Rand der Seite, um nach rechts zu blättern.  

  Öffnen Sie die Seite [hier](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a>Der Kontenplan

Der Kontenplan zeigt alle Sachkonten an. Vom Kontenplan aus können Sie Dinge tun wie:  

* Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.  
* GuV-Kontennullstellung.  
* Öffnen Sie die Karteikarte des Hauptbuchs (Sachkonto), um Einstellungen hinzuzufügen oder zu ändern.  
* Sie sehen eine Liste der Buchungsgruppen für dieses Konto.
* Zeigen Sie separate Soll- und Habensalden für ein einzelnes Konto an.

Sie können Sachkonten hinzufügen, ändern oder löschen. Um jedoch Differenzen zu verhindern, können Sie ein Sachkonto nicht löschen, wenn Daten im Kontenplan verwendet werden. Außerdem können Sie ab dem zweiten Veröffentlichungszyklus 2022 das versehentliche Löschen von Konten in sensiblen Zeiträumen blockieren. Erfahren Sie mehr im Abschnitt [Löschen von Konten](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories"></a><a name="account-categories"></a><a name="account-categories"></a>Kontokategorien

Sie können die Struktur der Finanzberichte personalisieren, indem Sie Sachkonten den Kontenkategorien hinzufügen.  

Die Seite **Sachkonto-Kategorien** zeigt Ihre Kategorien und Unterkategorien sowie die ihnen zugeordneten Sachkonten an. Sie können neue Unterkategorien erstellen und diese bestehenden Konten zuweisen.  

Sie können eine Kategoriegruppe erstellen, indem Sie andere Unterkategorien unter einer Zeile auf der Seite **Sachkonto Kategorien** einrücken. Kategoriegruppen erleichtern den Überblick, da jede Gruppierung einen Gesamtsaldo anzeigt. Sie können z.B. Unterkategorien für verschiedene Arten von Assets erstellen und dann Kategoriegruppen für Anlagen und Umlaufvermögen erstellen.  

Sie können festlegen, ob bestimmte Arten von Berichten die Konten in jeder Unterkategorie enthalten müssen. Die Kontengruppen helfen Ihnen dabei, das Layout Ihrer Finanzberichte zu definieren.  

### <a name="example"></a><a name="example"></a><a name="example"></a>Beispiel

Zum Beispiel hat der Standard-Bilanzauszug eine Unterkategorie für *Kasse* unter *Anlagevermögen*. Wenn Sie möchten, dass die Bilanzauszüge die Portokasse und die Girokonten berücksichtigen, müssen Sie die folgenden Schritte ausführen:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Sachkonto Kategorien** ein und wählen Sie dann den entsprechenden Link.
   1. Alternativ können Sie auch [die Seite hier öffnen](https://businesscentral.dynamics.com/?page=790).
2. Wählen Sie die Aktion **Liste bearbeiten** aus.
3. Fügen Sie zwei neue Unterkategorien hinzu: Eine für die Portokasse und eine für Ihr Girokonto:
   1. Wählen Sie die Kategorie **Anlagevermögen**.
   2. Wählen Sie die Aktion **Neu**.
   3. Geben Sie den Namen der Unterkategorie in das Feld **Beschreibung** ein.
   4. Wählen Sie im Feld **Sachkonten in Kategorie** das entsprechende Sachkonto aus.
   5. Wählen Sie im Feld **Zusätzliche Berichtsdefinition** die Option **Kassenkonten**.
4. Fassen Sie diese in der Unterkategorie **Bar** zusammen.
   1. Wählen Sie die Unterkategorie, die in Schritt 3 erstellt wurde.
   2. Wählen Sie die Aktion **Einrücken** aus.
   3. Wählen Sie die Aktion **Nach unten verschieben**.
   4. Wählen Sie die Aktion **Einrücken**, um unter der Unterkategorie **Kasse** einzurücken.

Wenn Sie die Aktion **Finanzberichte generieren** wählen - oder wenn der Bericht das nächste Mal generiert wird - wird Ihr Kontoauszug die folgenden Zeilen enthalten:

* Gesamtguthaben für Bargeld.
* Zeilen mit Guthaben für die Portokasse und das Girokonto.  

> [!NOTE]
> Wenn Sie ein Sachkonto anlegen, ohne einen Kontentyp zuzuordnen, wenn Sie das Konto einer Buchungsgruppe zuordnen, ordnet [!INCLUDE[prod_short](includes/prod_short.md)] automatisch die Kontenkategorie aus dem Sachkonto direkt über dem Konto in Ihrem Kontenplan zu. Um das neue Konto jedoch in Ihre Finanzberichte aufzunehmen, müssen Sie die Aktion **Finanzberichte generieren** auf der Seite **Sachkonto Kategorien** wählen. Alternativ können Sie die Seite Sachkonto-Karte öffnen, die Kontokategorie angeben und dann Ihren Finanzbericht neu generieren.

## <a name="get-a-quick-overview"></a><a name="get-a-quick-overview"></a><a name="get-a-quick-overview"></a>Einen schnellen Überblick erhalten

Auf der Seite **Kontenplan** werden die Konten in einer hierarchischen Liste angezeigt, die einen schnellen Zugriff auf die wichtigsten Informationen zu jedem Konto bietet. Allerdings ist die Liste statisch, und wenn Sie viele Konten haben, müssen Sie möglicherweise blättern, um die verschiedenen Konten anzuzeigen. Wenn Sie nur einen schnellen Überblick über die Grundlagen wie Nettoveränderungen und Salden haben möchten, ist die Seite **Kontenplan Übersicht** eine nützliche Alternative. Das Spaltenlayout auf der Seite ist jetzt dasselbe wie auf der Seite **Kontenplan** (allerdings mit weniger Spalten), so dass Sie sich nicht neu orientieren müssen. Sie können die hierarchischen Ebenen erweitern oder reduzieren, um die Ansicht zu verdichten. Um den Wechsel zwischen den Seiten zu erleichtern, ist die Seite **Kontenplan Übersicht** von der Seite **Kontenplan** aus zugänglich.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a><a name="access-to-create-and-edit-accounts-and-account-categories"></a><a name="access-to-create-and-edit-accounts-and-account-categories"></a>Zugriff auf das Erstellen und Bearbeiten von Konten und Kontokategorien

In einem kleinen Unternehmen, wie der CRONUS-Demofirma, können die meisten Benutzer den Kontenplan bearbeiten, mit Ausnahme der Benutzer mit einer TEAMMITGLIED-Lizenz. In größeren Organisationen ist der Zugriff auf die Bearbeitung des Kontenplans typischerweise durch Rollen und Berechtigungen eingeschränkt. Wenn Sie Administrator sind oder die Rolle *Business Manager* oder *Buchhalter* haben, können Sie die Berechtigungen der Benutzer steuern, um den richtigen Personen Zugriff auf die entsprechenden Tabellen zu geben. Mehr dazu erfahren Sie im Abschnitt [Sie erhalten einen Überblick über die Berechtigungen eines Benutzers](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
