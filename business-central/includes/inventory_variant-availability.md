---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2022
ms.author: bholtorf
---
Wenn Sie die Seite **Artikelverfüg. nach Variante** aus einer Belegzeile öffnen, dann können Sie eine Variante in die Belegzeile einfügen, indem Sie die Zeile mit der hinzuzufügenden Variante auswählen und dann auf OK klicken. Wenn Sie die Seite nur verwendet haben, um die Verfügbarkeit anzuzeigen und keine Variante einfügen möchten, müssen Sie das Fenster schließen, ohne auf OK zu klicken.

Die Seite zeigt eine Zeile für jede Periode an. Jede Zeile zeigt die Verfügbarkeitszahlen des Artikels in den folgenden Schlüsselfeldern an:

| Feld | Description |
|--|--|
| **Bruttobedarf**| Gibt die Summe des gesamten Bedarfs an diesem Artikel an. Der Bruttobedarf ist der *abhängige Bedarf* plus *unabhängiger Bedarf*. Der *unabhängige Bedarf* resultiert aus Verkaufsaufträgen, Serviceaufträgen, Umlagerungsaufträgen und den Absatzplänen. Der *abhängige Bedarf* resultiert aus den FA-Komponenten der geplanten, fest geplanten und freigegebenen Fertigungsaufträge. Es enthält auch Anforderungs- und Planungsarbeitsblattzeilen.|
| **Geplanter Zugang** | Gibt die Summe aus Aufträgen an, mit denen das Lager aufgefüllt wird. Die Berechnung schließt fest geplante und freigegebene Fertigungsaufträge, Bestellungen und Umlagerungsaufträge ein. |
| **Voraussichtlicher Zugang** | Gibt die Summe der Artikel aus geplanten Fertigungsaufträgen an. |
| **Verfügbarkeitssaldo** | Gibt den berechneten verfügbaren Lagerbestand an. |
| **Voraussichtliche Freigabemenge** | Dies ist die Summe aus geplanten Lagerzugängen. Die Berechnung umfasst geplante Fertigungsaufträge. sie enthält auch PPlanungs‑ und Anforderungsarbeitsblätter, die auf der Basis des Startdatums (im Planungsarbeitsblatt und Fertigungsauftrag) oder des Bestelldatums (im Anforderungsarbeitsblatt) berechnet wurden. Diese Summe ist im Verfügbarkeitssaldo nicht enthalten. Sie zeigt jedoch, welche Mengen von voraussichtlichen in geplante Zugänge überführt werden sollten. |
