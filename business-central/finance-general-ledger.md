---
title: Verstehen des Hauptbuchs und des COA
description: Beschreibt die Finanzbuchhaltung, den Kontenplan und die Kontenkategorien. Verwenden Sie die Seite Finanzbuchhaltung Einrichtung, um die Handhabung der Buchhaltung in Ihrer Firma festzulegen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 08/23/2022
ms.author: edupont
ms.openlocfilehash: 29f66fae0413bb0f8a757cfceedce8e0504e8686
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9362275"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Grundlegendes zur Finanzbuchhaltung und zum Kontenplan

Die Finanzbuchhaltung speichert Ihre Finanzdaten. Der Kontenplan zeigt die Konten, in die Sachkontoposten gebucht werden. [!INCLUDE[prod_short](includes/prod_short.md)] umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finanzbuchhaltungs-Einrichtung und Buchungsmatrix Einrichtung

Die Einrichtung der Finanzbuchhaltung ist das Kernstück der Finanzvorgängen, da sie definieren, wie Sie Daten buchen. Zwei Seiten spielen eine wichtige Rolle bei der Konfiguration Ihrer Finanzprozesse:  

* Die Seite **Finanzbuchhaltung Einrichtung**

  Auf der Seite **Finanzbuchhaltung einrichten** geben Sie an, wie bestimmte finanzbuchhalterische Sachverhalte in Ihrem Unternehmen gehandhabt werden sollen, wie beispielsweise:  

  * Rechnungsrundungskontodetails  
  * Adressformate  
  * Finanzberichterstellung  

  > [!TIP]
  > Die Seite **Finanzbuchhaltung Einrichtung** enthält allgemeine Felder sowie Felder, die für Ihr Land oder Ihre Region spezifisch sind. Wenn Sie nicht sicher sind, welche Bedeutung ein Feld hat, empfehlen wir Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um zu ermitteln, ob es für Ihre Organisation relevant ist. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    Öffnen Sie die Seite [hier](https://businesscentral.dynamics.com/?page=118)
* Die Seite **Buchungsmatrix Einrichtung**

    Ebenso geben Sie auf der Seite **Buchungsmatrix Einrichtung** an, wie Sie Kombinationen aus Geschäftsbuchungsgruppen und Produktbuchungsgruppen einrichten wollen. Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Sachkonten. Für jede Kombination aus Geschäftsbuchungsgruppe und Produktbuchungsgruppe geben Sie eine Zeile ein. Sie können jedoch auch jede Zeile in einer eigenen Buchungseinrichtungskarte öffnen. Weitere Informationen finden Sie unter [Gruppenbuchungen einrichten](finance-posting-groups.md).  

    > [!TIP]
    > Wenn Sie die gesuchten Felder auf der Seite **Buchungsmatrix einrichten** nicht sehen können, verwenden Sie die horizontale Bildlaufleiste am unteren Rand der Seite, um nach rechts zu scrollen.  

    Öffnen Sie die Seite [hier](https://businesscentral.dynamics.com/?page=314)

## <a name="the-chart-of-accounts"></a>Der Kontenplan

Der Kontenplan zeigt alle Sachkonten an. Vom Kontenplan aus können Sie Dinge tun wie:  

* Berichte ansehen, die die Sachkonteneinträge und -Salden zeigen.  
* GuV-Kontennullstellung.  
* Öffnen Sie die Karteikarte des Hauptbuchs (Sachkonto), um Einstellungen hinzuzufügen oder zu ändern.  
* Sie können außerdem eine Liste von Buchungsgruppen anzeigen, die auf dieses Konto buchen.
* Ansicht der Soll- und Habensalden von einzelnen Sachkonten  

Sie können Sachkonten hinzufügen, ändern oder löschen. Um jedoch Differenzen zu verhindern, können Sie ein Sachkonto nicht löschen, wenn Daten im Kontenplan verwendet werden. Um Fehler in sensiblen Zeiträumen zu vermeiden, können Sie auch das Löschen von Konten sperren. Weitere Informationen finden Sie unter [Löschen von Konten](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories"></a>Kontokategorien

Sie können die Struktur der Finanzberichte personalisieren, indem Sie Sachkonten den Kontenkategorien hinzufügen.  

Die Seite **Sachkontokategorien** zeigt Ihre Kategorien und Unterkategorien sowie die ihnen zugeordneten Sachkonten. Sie können neue Unterkategorien erstellen und diese bestehenden Konten zuweisen.  

Sie erstellen eine Kategoriengruppe, indem Sie weitere Unterkategorien unter einer Zeile auf der Seite **Sachkontokategorien** einrücken. Kategoriegruppen erleichtern Ihnen den Überblick, da jede Gruppierung einen Gesamtsaldo anzeigt. Beispielsweise können Sie Unterkategorien für unterschiedliche Arten von Anlagen erstellen und dann Kategoriengruppen für Anlagen gegenüber Umlaufvermögen erstellen.  

Für jede Unterkategorie können Sie festlegen, ob Konten dieser Kategorie in bestimmte Arten von Finanzberichten enthalten sein müssen. Die Kontengruppen helfen Ihnen dabei, das Layout Ihrer Finanzberichte zu definieren.  

### <a name="example"></a>Beispiel

Zum Beispiel hat der Standard-Bilanzauszug eine Unterkategorie für *Kasse* unter *Anlagevermögen*. Sie möchten, dass der Kontoauszug Portokasse und Scheck berücksichtigt, also gehen Sie wie folgt vor:  

1. Fügen Sie zwei neue Unterkategorien hinzu:

    * Eine für die Portokasse  
    * Eine für Ihr Girokonto  
2. Geben Sie die weitere Berichtsdefinition **Bargeldkonten** für diese Unterkategorien an.  
3. Fassen Sie diese in der Unterkategorie **Bar** zusammen.  

Wenn Sie das nächste Mal Kontoschemata erstellen, zeigt Ihr Kontoauszug die folgenden Zeilen:

* Gesamtguthaben für Bargeld.
* Zeilen mit Guthaben für die Portokasse und das Girokonto.  

> [!NOTE]
> Wenn Sie ein Sachkonto anlegen, ohne einen Kontentyp zuzuordnen, wenn Sie das Konto einer Buchungsgruppe zuordnen, ordnet [!INCLUDE[prod_short](includes/prod_short.md)] automatisch die Kontenkategorie aus dem Sachkonto direkt über dem Konto in Ihrem Kontenplan zu. Um das neue Konto jedoch in Ihre Finanzberichte aufzunehmen, müssen Sie die Aktion **Erstellen Sie Finanzberichte** auf der Seite **Allgemeine Sachkontokategorien**. Alternativ können Sie die Seite Sachkontokarte öffnen, die Kontokategorie angeben und dann Ihren Finanzbericht neu generieren.

## <a name="get-a-quick-overview"></a>Einen schnellen Überblick erhalten

Auf der Seite **Kontenplan** werden die Konten in einer hierarchischen Liste angezeigt, die einen schnellen Zugriff auf die wichtigsten Informationen zu jedem Konto bietet. Die Liste ist jedoch statisch. Wenn Sie viele Konten haben, müssen Sie möglicherweise scrollen, um verschiedene Konten anzuzeigen. Wenn Sie nur einen schnellen Überblick über die Grundlagen wie Nettoveränderungen und Salden haben möchten, ist die Seite **Kontenplan Übersicht** eine nützliche Alternative. Das Spaltenlayout auf der Seite ist jetzt dasselbe wie auf der Seite **Kontenplan** (allerdings mit weniger Spalten), sodass Sie sich nicht neu orientieren müssen. Sie können die hierarchischen Ebenen erweitern oder reduzieren, um die Ansicht zu verdichten. Um den Wechsel zwischen den Seiten zu erleichtern, ist die Seite **Kontenplan Übersicht** von der Seite **Kontenplan** aus zugänglich.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Zugriff auf das Erstellen und Bearbeiten von Konten und Kontokategorien

In einer kleinen Organisation, wie der CRONUS-Demo-Firma, können die meisten Benutzer den Kontenplan bearbeiten. Ausgenommen Benutzer mit einer TEAM MEMBER-Lizenz. In größeren Organisationen ist der Zugriff auf die Bearbeitung des Kontenplans typischerweise durch Rollen und Berechtigungen eingeschränkt. Wenn Sie ein Administrator sind oder die Rolle **Geschäftsführer** oder **Buchhalter** haben, können Sie die Berechtigungen für alle Benutzer kontrollieren, um richtigen Personen Zugriff auf die relevanten Tabellen zu erteilen. Weitere Informationen finden Sie unter [So erhalten Sie eine Übersicht der Benutzerberechtigungen](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
