---
title: Verstehen des Hauptbuchs und des COA
description: Beschreibt das Hauptbuch, den Kontenplan und die Kontenkategorien. Verwenden Sie die Seite Finanzbuchhaltung Einrichtung, um die Handhabung der Buchhaltung in Ihrer Firma festzulegen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: bb94f725c57f538f9d8704ba66e3d66e120d41d2
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079142"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Grundlegendes zum Sachkonto und zum Kontenplan

Die Finanzbuchhaltung speichert Finanzdaten, und der Kontenplan zeigt die Konten, auf die alle Sachposten gebucht werden, an. [!INCLUDE[prod_short](includes/prod_short.md)] umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.

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

Sie können Sachkonten hinzufügen, ändern oder löschen. Um jedoch Differenzen zu verhindern, können Sie ein Sachkonto nicht löschen, wenn Daten im Kontenplan verwendet werden. Außerdem können Sie ab dem zweiten Veröffentlichungszyklus 2022 das versehentliche Löschen von Konten in sensiblen Zeiträumen blockieren. Weitere Informationen finden Sie unter [Löschen von Konten](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories"></a>Kontokategorien

Sie können die Struktur der Finanzberichte personalisieren, indem Sie Sachkonten den Kontenkategorien hinzufügen.  

Die Seite **Sachkontokategorien** zeigt Ihre Kategorien und Unterkategorien sowie die ihnen zugeordneten Sachkonten. Sie können neue Unterkategorien erstellen und diese bestehenden Konten zuweisen.  

Sie erstellen eine Kategoriengruppe, indem Sie weitere Unterkategorien unter einer Zeile auf der Seite **Sachkontokategorien** einrücken. Dieses erleichtert Ihnen den Überblick, da jede Gruppierung einen Gesamtsaldo anzeigt. Beispielsweise können Sie Unterkategorien für unterschiedliche Arten von Anlagen erstellen und dann Kategoriengruppen für Anlagen gegenüber Umlaufvermögen erstellen.  

Für jede Unterkategorie können Sie festlegen, ob Konten dieser Kategorie in bestimmte Arten von Finanzberichten enthalten sein müssen. Die Kontengruppen helfen Ihnen dabei, das Layout Ihrer Finanzberichte zu definieren.  

### <a name="example"></a>Beispiel

Zum Beispiel hat der Standard-Bilanzauszug eine Unterkategorie für *Kasse* unter *Anlagevermögen*. Sie möchten, dass der Kontoauszug Portokasse und Scheck berücksichtigt, also gehen Sie wie folgt vor:  

1. Fügen Sie zwei neue Unterkategorien hinzu:

    * Eine für die Portokasse  
    * Eine für Ihr Girokonto  
2. Geben Sie die weitere Berichtsdefinition **Bargeldkonten** für diese Unterkategorien an.  
3. Fassen Sie diese in der Unterkategorie **Bar** zusammen.  

Wenn Sie das nächste Mal Kontenschemata erstellen, zeigt Ihr Kontoauszug einen Gesamtsaldo für Bargeld und zwei Zeilen mit Salden für die Portokasse und das Girokonto.  

## <a name="get-a-quick-overview"></a>Einen schnellen Überblick erhalten

Auf der Seite **Kontenplan** werden die Konten in einer hierarchischen Liste angezeigt, die einen schnellen Zugriff auf die wichtigsten Informationen zu jedem Konto bietet. Allerdings ist die Liste statisch, und wenn Sie viele Konten haben, müssen Sie möglicherweise ein wenig blättern, um die Informationen zu den einzelnen Konten anzuzeigen. Wenn Sie nur einen schnellen Überblick über die Grundlagen wie Nettoveränderungen und Salden haben möchten, ist die Seite **Kontenplan Übersicht** eine nützliche Alternative. Das Spaltenlayout auf der Seite ist jetzt dasselbe wie auf der Seite **Kontenplan** (es gibt nur weniger davon), sodass Sie sich nicht neu orientieren müssen, und Sie können die Hierarchieebenen erweitern oder reduzieren, um die Ansicht zu verdichten. Um den Wechsel zwischen den Seiten zu erleichtern, ist die Seite **Kontenplan Übersicht** von der Seite **Kontenplan** aus zugänglich.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Zugriff auf das Erstellen und Bearbeiten von Konten und Kontokategorien

In einer kleinen Organisation, wie der CRONUS-Demo-Firma, können die meisten Benutzer den Kontenplan bearbeiten, mit Ausnahme von Benutzern mit einer TEAM MEMBER-Lizenz. In größeren Organisationen ist der Zugriff auf die Bearbeitung des Kontenplans jedoch durch Rollen und Berechtigungen eingeschränkt. Wenn Sie ein Administrator sind oder die Rolle *Geschäftsführer* oder *Buchhalter* haben, können Sie die Berechtigungen für alle Benutzer überprüfen, um sicherzustellen, dass die richtigen Personen Zugriff auf die relevanten Tabellen haben. Weitere Informationen finden Sie unter [So erhalten Sie eine Übersicht der Benutzerberechtigungen](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
