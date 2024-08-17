---
title: Terminologie in der Kostenrechnung
description: 'In diesem Artikel werden die wichtigsten Begriffe der Kostenrechnung definiert, beispielsweise Zuordnungsschlüssel und Zuordnungsquelle.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 1123
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Terminologie in der Kostenrechnung

In diesem Artikel werden die wichtigsten Begriffe der Kostenrechnung definiert.  

## Schlüsselbegriffe

 In der folgenden Tabelle werden Definitionen der Schlüsselbegriffe in der Kostenrechnung gezeigt.  

|**Begriff**|**Definition**|  
|--------------|--------------------|  
|Verteilungsschlüssel|Der Verteilungsschlüssel ist die Basis, die verwendet wird, um Kosten zuzuordnen. Dabei handelt es sich in der Regel um eine Menge, beispielsweise belegte Quadratmeter, Mitarbeiterzahl oder geleistete Arbeitsstunden. Beispielsweise teilen sich zwei Abteilungen mit je 20 und 10 Mitarbeitern die Kantinenkosten. Die Kosten werden auf die Abteilungen verteilt, indem Sie einen Verteilungsschlüssel verwenden, der die Anzahl der Mitarbeiter darstellt. Zwei Drittel der Kosten werden der ersten Abteilungen zugeordnet, und ein Drittel der Kosten wird der zweiten Abteilung zugeordnet.|  
|Verteilungsquelle|Die Zuordnungsquelle definiert, welche Kosten zugeordnet werden. Zuordnungen werden in den Quell- und Zieltabellen der Verteilung definiert. Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Beispielsweise können alle Kosten für die Heizkostenart, die einer Verteilungsquelle entspricht, dem Workshop, der Produktion und den Verkaufskostenstellen, also den drei Zuordnungszielen, zugeordnet werden.|  
|Verteilungsziel|Die Zuordnungsziele bestimmen, wie die Kosten zugeordnet werden. Zuordnungen werden in den Quell- und Zieltabellen der Verteilung definiert. Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Beispielsweise können alle Kosten für die Heizkostenart, die einer Verteilungsquelle entspricht, dem Workshop, der Produktion und den Verkaufskostenstellen, also den drei Zuordnungszielen, zugeordnet werden.|  
|Kostenrechnung|In der Kostenrechnung werden Ist-Kosten für Arbeitsgänge, Prozesse, Abteilungen oder Produkte erfasst. Diese Kosten werden Kostenstellen und Kostenträgern zugeordnet, indem verschiedene Kostenzuteilungsmethoden verwendet werden. Manager verwenden Statistiken und Berichte, wie Kostenaufteilungsblätter sowie Gewinn- und Verlustanalysen, um Entscheidungen zu treffen und Kosten zu verringern. Die Kostenrechnung ruft Daten aus dem Sachkonto ab, funktioniert aber unabhängig. Deshalb haben in der Kostenrechnung gebuchte Transaktionen keinen Einfluss auf die Daten im Hauptbuch.|  
|Kostenart|Der Kostenartenplan hat dieselbe Funktion wie der Kontenplan im Sachkonto. Sie sind oft ähnlich aufgebaut. Hierzu ist es möglich, den Hauptbuchkontenplan in den Kostenartenplan zu übernehmen und diesen anschließend anzupassen. Der Kostenartenplan kann auch von Grund auf neu erstellt werden.|  
|Kostenstelle|Kostenstellen sind häufig Abteilungen und Profiteinheiten, die für die Kosten und die Einnahmen des Unternehmens in großem Maße zuständig sind. Kostenstellen können mit Dimensionen im Sachkonto synchronisiert werden. Zudem besteht die Möglichkeit, neue Kostenstellen hinzuzufügen und eine eigene Sortierung mit Zwischensummen festzulegen.|  
|Kostenträger|Kostenträger sind Produkte, Produktgruppen oder Dienstleistungen eines Unternehmens, also die fertigen Erzeugnisse eines Unternehmens, die letztlich die Kosten tragen. Kostenträger können mit Dimensionen im Sachkonto synchronisiert werden. Zudem besteht die Möglichkeit, neue Kostenträger hinzuzufügen und eine eigene Sortierung mit Zwischensummen festzulegen.|  
|Kostenzuordnung|Kostenzuteilung ist ein Prozess des Zuordnens von Kosten auf die Kostenstellen oder Kostenträger. Beispielsweise wird der Lohn des LKW-Fahrers der Verkaufsabteilung der Vertriebsabteilungskostenstelle zugeordnet. Eine Umlage der Lohnkosten auf andere Kostenstellen ist nicht erforderlich. Ein anderes Beispiel wäre, dass die Kosten eines teuren Computersystems den Produkten des Unternehmens zugeordnet werden, die das System verwenden.|  
|Dynamische Zuteilung|Dynamische Zuteilungen sind unabhängig von den veränderbaren Zuordnungsgrundlagen, zum Beispiel von der Anzahl der Abteilungsmitarbeiter oder dem Verkaufserlös des Projekts innerhalb eines bestimmten Zeitraums. Es gibt neun vordefinierte dynamische Zuteilungsbasen, die Benutzer festlegen können, indem Sie fünf Filter verwenden.|  
|Direkte Kosten|Direkte Kosten sind die Kosten, die einem Kostenträger direkt zugeordnet werden können, zum Beispiel der Materialeinkauf für ein bestimmtes Produkt.|  
|Fixkosten|Fixkosten sind Kosten, die nicht von der Menge der vom Unternehmen produzierten Waren oder Dienstleistungen abhängen. Sie sind meistens zeitbezogen, zum Beispiel Gehalt oder Miete, das bzw. die pro Monat bezahlt wird. Sie stehen im Gegensatz zu variablen Kosten, die mengenbezogen sind, und werden pro produzierte Menge bezahlt.|  
|Indirekte Kosten|Indirekte Kosten sind nicht direkt einem Kostenobjekt wie einer bestimmten Funktion oder einem Produkt zuzuordnen. Die indirekten Kosten können entweder fest oder variabel sein. Indirekte Kosten können Kosten für Steuern, Verwaltung, Mitarbeiter und Sicherheit sein und werden auch als Gemeinkosten bezeichnet.|  
|Ebene|Die Ebene wird verwendet, um die Zuteilungsreihenfolge zu definieren. Gibt eine Stufe als Nummer zwischen 1 und 99 an. Die Verteilungsbuchung richtet sich nach der Reihenfolge der Stufen. Die Ebene stellt beispielsweise sicher, dass die erste Verwaltung dem Workshop zugeordnet wird, bevor der Workshop Fahrzeug und Produktion zugeordnet wird.|  
|Statische Verteilung|Statische Verteilungen basieren auf einem festen Satz von Werten, zum Beispiel die verwendeten Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4.|  
|Betriebskosten|Betriebskosten sind wiederkehrende Ausgaben, die mit dem Betrieb eines Unternehmens, eines Geräts und einer Komponente verbunden sind.|  
|Gemeinkosten|Gemeinkosten beziehen sich auf laufende Ausgaben für den Betrieb eines Geschäfts. Mit Ausnahme der direkten Arbeitskosten, der direkten Materialkosten und der direkten Ausgaben handelt es sich dabei um sämtliche Kosten in der Gewinn- und Verlustrechnung. Gemeinkosten enthalten Kosten für Rechnungsgebühren, Werbung, Abschreibungen, Versicherung, Zinsen, Anwaltskosten, Miete, Reparaturen, Zubehör, Steuern, Telefonrechnungen, Reise und Hilfsmittel.|  
|Variable Sprungkosten|Schritt Variable Kosten sind Kosten, die sich zu bestimmten Zeitpunkten drastisch ändern, weil es sich um große Anschaffungen handelt, die nicht über einen längeren Zeitraum verteilt werden können. Beispielsweise kann ein Mitarbeiter 100 Tabellen in einem Monat produzieren. Das Gehalt des Mitarbeiters ist über einen Produktionsbereich von 1 bis 100 Tabellen konstant. Wenn das Unternehmen 110 Tabellen produziert möchte, benötigt das Unternehmen zwei Mitarbeiter. Daher verdoppeln sich die Kosten.|  
|Anteil|Der Teil, der auf Kostenstellen oder Kostenträger aufgeteilt wird.|  
|Statische Gewichtung|Kosten werden entsprechend Verteilungsschlüsseln zugewiesen, die durch einen Multiplikator geändert werden können. <br />Beispielsweise teilen sich zwei Abteilungen mit je 20 und 10 Mitarbeitern die Kantinenkosten. Die Kosten werden auf die Abteilungen verteilt, indem Sie einen Verteilungsschlüssel verwenden, der die Anzahl der Mitarbeiter darstellt, die in der Kantine essen. In der ersten Abteilung essen nur fünf Mitarbeiter in der Kantine, daher gilt für diese Abteilung ein Multiplikator von 0,25. Die Grundlage für die Zuordnung ist 20 x 0,25 = 5. Die Gesamtzahl der Mitarbeiter, die in der Kantine essen, ist 15. Zwei Drittel der Kosten werden der ersten Abteilungen zugeordnet, und ein Drittel der Kosten wird der zweiten Abteilung zugeordnet.|  
|Variable Kosten|Variable Kosten sind Ausgaben, die sich abhängig von der Aktivität eines Geschäftes ändern. Variable Kosten sind die Summe der Grenzkosten über alle erzeugten Einheiten hinweg. Fixkosten und variable Kosten ergeben die beiden Komponenten der Gesamtkosten.|  
|Variante|Eine Variante wird als optionale benutzerdefinierte Beschriftung für Zuordnungen verwendet. Der Zweck der Beschriftung ist es, Gruppen nach Zuordnung zu filtern.|  

## Siehe auch

 [Informationen zur Kostenrechnung](finance-about-cost-accounting.md)  
 [Kostenrechnung](finance-manage-cost-accounting.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
