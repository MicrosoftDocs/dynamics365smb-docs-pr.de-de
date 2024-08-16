---
title: Verstehen Sie das Hauptbuch und den Kontenplan
description: 'Beschreibt das Hauptbuch, den Kontenplan und die Kontenkategorien. Verwenden Sie die Seite Finanzbuchhaltung Einrichtung, um die Handhabung der Buchhaltung in Ihrer Firma festzulegen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="understand-the-general-ledger-and-chart-of-accounts"></a>Verstehen Sie das Hauptbuch und den Kontenplan

Die Finanzbuchhaltung speichert Ihre Finanzdaten, und der Kontenplan (COA) zeigt die Konten, auf die alle Sachposten gebucht werden. [!INCLUDE[prod_short](includes/prod_short.md)] umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finanzbuchhaltungs-Einrichtung und Buchungsmatrix Einrichtung

Die Einrichtung der Finanzbuchhaltung ist das Kernstück der Finanzvorgängen, da sie definieren, wie Sie Daten buchen. Bei der Konfiguration Ihrer Finance-Prozesse spielen vor allem zwei Seiten eine wichtige Rolle:  

* **Finanzbuchhaltung Einrichtung**
* **Buchungsmatrix Einrichtung**

### <a name="the-general-ledger-setup-page"></a>Die Seite **Finanzbuchhaltung Einrichtung**

Geben Sie auf der Seite **Finanzbuchhaltung einrichten** an, wie bestimmte finanzbuchhalterische Sachverhalte in Ihrem Unternehmen gehandhabt werden sollen, wie beispielsweise:  

* Rechnungsrundungskontodetails  
* Adressformate  
* Finanzberichterstellung

> [!TIP]
> Die Seite **Finanzbuchhaltung Einrichtung** enthält allgemeine sowie für Ihr Land oder Ihre Region spezifische Felder. Wenn Sie sich über die Bedeutung eines Feldes nicht im Klaren sind, empfehlen wir Ihnen, mit Ihrer Buchhaltung zu sprechen, um festzustellen, ob es für Ihr Unternehmen relevant ist. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Um die Seite jetzt zu öffnen, verwenden Sie den folgenden Link [Finanzbuchhaltung Einrichtung](https://businesscentral.dynamics.com/?page=118).

### <a name="the-general-posting-setup-page"></a>Die Seite **Buchungsmatrix Einrichtung**

Verwenden Sie die Seite **Buchungsmatrix** um Kombinationen aus Geschäfts- und Produktbuchungsgruppen einzugeben. Buchungsgruppen ordnen Entitäten wie Kunden, Lieferanten, Artikel, Ressourcen sowie Verkaufs- und Kaufbelege den Hauptbuch-Konten zu. Für jede Kombination aus Geschäftsbuchungsgruppe und Produktbuchungsgruppe geben Sie eine Zeile ein. Sie können jedoch auch jede Zeile in einer eigenen Buchungseinrichtungskarte öffnen. Erfahren Sie mehr unter [Buchungsgruppen Einrichtungen](finance-posting-groups.md).  

> [!TIP]
> Wenn Sie die Felder, die Sie suchen, auf der Seite **Allgemeine Buchungsmatrixeinrichtung** nicht sehen können, verwenden Sie die horizontale Bildlaufleiste am unteren Rand der Seite, um nach rechts zu blättern.  

Um die Seite jetzt zu öffnen, verwenden Sie den folgenden Link [Buchungsmatrix](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Der Kontenplan

Die Seite **Kontenplan** zeigt alle Sachkonten an. Vom Kontenplan aus können Sie Dinge tun wie:  

* Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.  
* GuV-Kontennullstellung.  
* Öffnen Sie die Karteikarte des Hauptbuchs (Sachkonto), um Einstellungen hinzuzufügen oder zu ändern.  
* Sie sehen eine Liste der Buchungsgruppen für dieses Konto.
* Zeigen Sie separate Soll- und Habensalden für ein einzelnes Konto an.

Weitere Informationen finden Sie unter [Den Kontenplan verstehen](finance-chart-of-accounts.md).

## <a name="account-categories"></a>Kontokategorien

Sie können die Struktur der Finanzberichte personalisieren, indem Sie Sachkonten den Kontenkategorien hinzufügen.  

Die Seite **Sachkonto-Kategorien** zeigt Ihre Kategorien und Unterkategorien sowie die ihnen zugeordneten Sachkonten an. Sie können neue Unterkategorien erstellen und diese bestehenden Konten zuweisen.  

Sie können eine Kategoriegruppe erstellen, indem Sie andere Unterkategorien unter einer Zeile auf der Seite **Sachkonto Kategorien** einrücken. Kategoriegruppen erleichtern den Überblick, da jede Gruppierung einen Gesamtsaldo anzeigt. Sie können z.B. Unterkategorien für verschiedene Arten von Assets erstellen und dann Kategoriegruppen für Anlagen und Umlaufvermögen erstellen.  

Sie können festlegen, ob bestimmte Arten von Berichten die Konten in jeder Unterkategorie enthalten müssen. Die Kontengruppen helfen Ihnen dabei, das Layout Ihrer Finanzberichte zu definieren.  

### <a name="example"></a>Beispiel

Zum Beispiel hat der Standard-Bilanzauszug eine Unterkategorie für *Kasse* unter *Anlagevermögen*. Wenn Sie möchten, dass der Kontoauszug Portokasse und Scheck berücksichtigt, gehen Sie wie folgt vor:

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Sachkonto Kategorien** ein und wählen Sie dann den entsprechenden Link.
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

Wenn Sie die Aktion **Finanzberichte generieren** wählen oder wenn der Bericht das nächste Mal generiert wird, enthält Ihre Saldenaufstellung die folgenden Zeilen:

* Gesamtguthaben für Bargeld.
* Zeilen mit Guthaben für die Portokasse und das Girokonto.  

> [!NOTE]
> Wenn Sie ein Sachkonto anlegen, ohne einen Kontentyp zuzuordnen, wenn Sie das Konto einer Buchungsgruppe zuordnen, ordnet [!INCLUDE[prod_short](includes/prod_short.md)] automatisch die Kontenkategorie aus dem Sachkonto direkt über dem Konto in Ihrem Kontenplan zu. Um das neue Konto jedoch in Ihre Finanzberichte aufzunehmen, müssen Sie die Aktion **Finanzberichte generieren** auf der Seite **Sachkonto Kategorien** wählen. Alternativ können Sie die Seite „Sachkontokarte“ öffnen, die Kontokategorie angeben und dann Ihren Finanzbericht neu generieren.

## <a name="access-to-create-and-edit-gl-accounts-and-account-categories"></a>Zugriff auf das Erstellen und Bearbeiten von Sachkonten und Kontokategorien

In einem kleinen Unternehmen, wie dem CRONUS-Demounternehmen, können die meisten Benutzenden Finanzentitäten wie Sachkonten, Kontokategorien und den Kontenplan bearbeiten, mit Ausnahme der Benutzenden mit einer TEAMMITGLIED-Lizenz. In größeren Organisationen ist der Zugriff auf die Bearbeitung dieser Entitäten typischerweise durch Rollen und Berechtigungen eingeschränkt. Wenn Sie Administrator sind oder die Rolle *Business Manager* oder *Buchhalter* haben, können Sie die Berechtigungen der Benutzer steuern, um den richtigen Personen Zugriff auf die entsprechenden Tabellen zu geben. Mehr dazu erfahren Sie unter [Eine Übersicht der Benutzerberechtigungen erhalten](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Ihren Kontenplan mithilfe von Dimensionen vereinfachen

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie auf Dokumenten wie Verkaufsaufträgen verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt. Anstatt also für jede Abteilung und jedes Projekt separate Sachkonten einzurichten, können Sie Dimensionen als Grundlage für die Analyse verwenden und müssen keinen komplizierten Kontenplan erstellen.

Mehr über Dimensionen erfahren Sie unter [Standarddimensionen für Debitoren, Kreditoren und andere Konten einrichten](finance-dimensions.md#to-set-up-default-dimensions-for-customers-vendors-and-other-accounts).

## <a name="see-also"></a>Siehe auch

[Den Kontenplan verstehen](finance-chart-of-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Benutzer*innen und Gruppen Berechtigungen zuweisen](ui-define-granular-permissions.md)  
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
