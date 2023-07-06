---
title: Überblick über Druckereinrichtung und -verwaltung
description: 'Erfahren Sie, was die verschiedenen Druckermöglichkeiten in Business Central sind'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 02/10/2023
ms.custom: bap-template
---

# <a name="printer-setup-and-management-overview"></a><a name="printer-setup-and-management-overview"></a><a name="printer-setup-and-management-overview"></a>Überblick über Druckereinrichtung und -verwaltung

Das Drucken von Dokumenten und Berichten aus [!INCLUDE[prod_short](includes/prod_short.md)] ist eine wichtige Aufgabe für Geschäftsanwender. Sie möchten normalerweise Druckaufträge direkt an einen der Drucker Ihres Unternehmens senden,&mdash;egal welchen [!INCLUDE[prod_short](includes/prod_short.md)]-Client oder welche App Sie verwenden. Da [!INCLUDE[prod_short](includes/prod_short.md)] Online ein Cloud-Dienst ist, kann er lokale Drucker, die mit den Geräten der Benutzer verbunden sind, nicht direkt erreichen, aber eine Verbindung zu Cloud-fähigen Druckern herstellen.

## <a name="what-are-your-printer-possibilities-in-business-central"></a><a name="what-are-your-printer-possibilities-in-business-central"></a><a name="what-are-your-printer-possibilities-in-business-central"></a>Was sind Ihre Druckmöglichkeiten in Business Central?

Um Ihre Druckanforderungen zu erfüllen, bietet [!INCLUDE[prod_short](includes/prod_short.md)] folgende Funktionen:

|Funktion|Beschreibung|Webclient| Mobile App|App für Teams|
|-------|-----------|----------|-----------|--------------|
|Universal Print|Universal Print ist eine Druckerverwaltungslösung, die als Cloud-Service von Microsoft erhältlich ist. Mit dieser Funktion können Sie Ihre Drucker in Universal Print einrichten und dann für die Verwendung in [!INCLUDE[prod_short](includes/prod_short.md)] registrieren. Diese Funktion erfordert ein Universal Print-Abonnement und die Erweiterung **Universal Print-Integration**.|![Funktioniert online.](media/check.png)|![Funktioniert online.](media/check.png)|![Funktioniert online](media/check.png)|
|E-Mail-Druck|Mit dieser Funktion können Sie E-Mail-fähige Drucker einrichten. [!INCLUDE[prod_short](includes/prod_short.md)] sendet anschließend Druckaufträge unter Verwendung der E-Mail-Adresse des Druckers an einen Drucker. Für diese Funktion sind E-Mail-fähige Drucker und die Erweiterung **E-Mail an Drucker senden** erforderlich.|![Funktioniert online.](media/check.png)|![Funktioniert online](media/check.png)|![Funktioniert online](media/check.png)|
|Browserdruck|Druckaufträge werden von der Druckfunktion des Browsers des Benutzers verarbeitet. Wenn ein Cloud-Drucker nicht installiert und eingerichtet ist oder wenn ein installierter Drucker ausfällt, werden beim Drucken standardmäßig die Druckoptionen des Browsers verwendet. Das Feld **Drucker** auf der Berichtsanforderungsseite zeigt *(Vom Browser gehandhabt)* an.|![Funktioniert online](media/check.png)|||

Die meisten Arbeiten zum Einrichten von Druckern können auf der Seite **Druckerverwaltung** in [!INCLUDE[prod_short](includes/prod_short.md)] erledigt werden. Bei Universal Print-Druckern müssen Sie möglicherweise auch im Microsoft 365 Admin Center oder im Azure-Portal arbeiten.

> [!IMPORTANT]
> Für Business Central lokal erfordern Universal Print und Email Print, dass die Azure Active Directory (AD)- oder NavUserPassword-Authentifizierung verwendet wird.

## <a name="custom-printer-extensions"></a><a name="custom-printer-extensions"></a><a name="custom-printer-extensions"></a>Benutzerdefinierte Druckererweiterungen

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt andere benutzerdefinierte Druckererweiterungen, die noch mehr Druckfunktionen hinzufügen. Wenn Sie also benutzerdefinierte Druckererweiterungen installiert haben, enthält Ihre Anwendung möglicherweise Druckfunktionen, die in diesem Artikel nicht beschrieben werden.

Wenn Sie ein AL-Entwickler sind und erfahren möchten, wie Sie Druckererweiterungen erstellen, gehen Sie zu [Entwickeln von Druckererweiterungen in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## <a name="next-steps"></a><a name="next-steps"></a><a name="next-steps"></a>Nächste Schritte

- [Drucker für Universal Print einrichten](admin-printer-setup-universal-print.md)  
- [E-Mail-Drucker einrichten](admin-printer-setup-email.md)  
- [Standarddrucker einrichten](ui-specify-printer-selection-reports.md)
