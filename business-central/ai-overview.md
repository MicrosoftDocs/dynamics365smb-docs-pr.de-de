---
title: "Vorschläge für Marketingtexte mit Copilot\_– Übersicht"
description: Verschaffen Sie sich einen Überblick über die Funktionen zur Generierung von KI-Inhalten in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 10/29/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---
# Vorschläge für Marketingtexte mit Copilot – Übersicht

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

Dieser Artikel gibt Ihnen einen Überblick über die von Copilot in Business Central bereitgestellten KI-gestützten Funktionen.

## Was ist KI-gestützter Marketingtext für Artikel mit Copilot

Copilot bietet KI-gestützte Schreibunterstützung für Business Central-Benutzende, die dafür zuständig sind, Marketingtexte (Produktbeschreibungen) für Artikel zu verfassen, die in Onlineshops wie Shopify verkauft werden. Mit einem Klick auf eine Schaltfläche generiert Copilot Text, der ansprechend und kreativ ist und die wichtigsten Attribute des jeweiligen Artikels hervorhebt. Mit ein wenig Überprüfung und Bearbeitung ist er für die Veröffentlichung bereit.

Copilot verwendet den [Microsoft Azure OpenAI-Dienst](/azure/cognitive-services/openai/overview), um auf Sprachmodelle zuzugreifen, die auf trainierten Datasets basierenden Text erkennen, vorhersagen und generieren.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Das Video gibt nicht genau wieder, wie das Feature derzeit funktioniert oder im Produkt aussieht. Das Feature hat sich seit der Produktion des Videos geändert. Aber es gibt Ihnen eine allgemeine Vorstellung von dem Feature und wofür Sie es verwenden können.*
  
## Wo sie verwendet werden

Copilot steht auf Artikelkarten in Business Central zur Verfügung. Artikel sind in Business Central wie Produkte in anderen Anwendungen und Geschäften. Jeder Artikel kann über eine Karte verwaltet werden, auf der Sie Details zum Artikel eingeben, z. B. Abmessungen, Kosten oder Bild. Diese Karte enthält auch ein Feld zur Eingabe von Marketingtext. Dieser Marketingtext kann in Ihrem Onlineshop veröffentlicht werden, um den Artikel zu bewerben. Hier kommt Copilot ins Spiel. Indem Sie auf der Artikelkarte einfach die Aktion **Entwurf mit Copilot** auswählen, generiert Copilot einen verständlichen Textentwurf für Sie. Sobald Sie den ersten Entwurf erhalten, können Sie Copilot immer wieder laufen lassen, bis Sie einen Entwurf erhalten, der Ihnen gefällt. Wenn Sie einen Vorschlag haben, der Ihnen gefällt, überprüfen Sie ihn auf Genauigkeit und bearbeiten und speichern ihn dann.

Wenn Business Central so eingerichtet ist, dass es sich mit Ihrem Onlineshop auf Shopify verbindet, können Sie den Text sogar mit einem Artikel direkt in Ihrem Shop veröffentlichen, indem Sie **Zu Shopify hinzufügen** auswählen.

## Warum sollte ich es verwenden und wie geht es

KI-generierter Text kann den Zeitaufwand für das Verfassen von Texten begrenzen und Ihnen somit helfen, die Markteinführungszeit von Produkten in Onlineshops zu verkürzen. Einige der wichtigsten Vorteile sind:

- Hilft Benutzern, Schreibblockaden zu überwinden, indem ihnen als Einstieg ein verständlicher Entwurf vorgeschlagen wird.
- Setzt Kreativität frei, sodass ansprechendere Produktbeschreibungen bereitgestellt werden können.
- Stärkt die Einheitlichkeit von Marketinginhalten für Produktlinien.

Sie sollten den von der KI generierten Text *nur als Vorschlag* betrachten. Vorschläge können in manchen Fällen Fehler und sogar unangemessenen Text enthalten, sodass sie von einem Menschen überwacht und überprüft werden müssen. Bevor Sie den Text öffentlich zugänglich machen, müssen Sie ihn auf Richtigkeit prüfen und entsprechende Änderungen vornehmen.

## Aktuelle Einschränkungen

In diesem Abschnitt werden die aktuellen Einschränkungen der von Copilot bereitgestellten KI-generierten Textfunktionen erläutert.

- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]
- Wenn vage oder allgemeine Produktnamen verwendet werden und Einzelheiten zu einem Artikel fehlen (zum Beispiel wichtige Attribute oder eien Kategorie) werden eventuell schlechte Vorschläge ausgegeben.
- Copilot wird nur in Business Central Online unterstützt, nicht aber in privaten Cloud-Umgebungen oder lokalen Business Central-Umgebungen.
- Copilot wird nicht über Verbindungen zu Ihrer eigenen Azure OpenAI-Dienstressource in Ihrem Azure-Abonnement unterstützt.

<!-- Partner extensibility of the AI capability by using AL code isn't supported.-->

## Nächste Schritte

Um loszulegen, benötigen Sie eine Business Central-Umgebung (Version 23.1 oder höher), die für Copilot aktiviert ist.

- Wenn Sie bereits Business Central haben, muss Ihr Business Central-Administrierender eine Umgebung einrichten, in der Marketingtextvorschläge aktiviert sind. Weitere Informationen finden Sie unter [Copilot- und KI-Funktionen konfigurieren](enable-ai.md).

- Wenn Sie Business Central noch nicht verwenden, es aber ausprobieren möchten, können Sie sich für eine kostenlose Testversion anmelden. Weitere Informationen finden Sie unter [Für eine kostenlose Dynamics 365 Business Central-Testversion registrieren](trial-signup.md).

Sobald Sie eine Umgebung oder eine entsprechende Testversion eingerichtet haben, gehen Sie zu [Marketingtext zu Artikeln mit Copilot hinzufügen](item-marketing-text.md).  

## Siehe auch

[Copilot- und KI-Funktionen konfigurieren](enable-ai.md)  
[Marketingtext für Artikel mit Copilot hinzufügen](item-marketing-text.md)  
[Häufig gestellte Fragen zu Vorschlägen für Marketingtexte](faqs-marketing-text.md)  
[Erste Schritte mit dem Shopify-Konnektor](shopify/get-started.md)  
