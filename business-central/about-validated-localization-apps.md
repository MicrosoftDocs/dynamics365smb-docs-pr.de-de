---
title: Entwicklung validierter Lokalisierungs-Apps
description: Erfüllen Sie die gesetzlichen Anforderungen in Dynamics 365 Business Central als validierte Lokalisierungs-App.
author: altotovi
ms.custom: na
ms.date: 04/10/2024
ms.reviewer: solsen
ms.topic: conceptual
ms.author: altotovi
---


# <a name="development-of-validated-localization-apps"></a>Entwicklung validierter Lokalisierungs-Apps

Dieser Artikel beschreibt die Anforderungen und Leitlinien für die Entwicklung einer validierten Lokalisierungs-App für [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-is-a-validated-localization-app"></a>Was ist eine validierte Lokalisierungs-App?

[!INCLUDE[prod_short](includes/prod_short.md)] ist [weltweit in über 170 Märkten](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) verfügbar. Microsoft arbeitet in einer Reihe von Märkten mit ISV-Partnern zusammen, um [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe von Lokalisierungs-Apps zu lokalisieren, die auf [Microsoft AppSource](https://go.microsoft.com/fwlink/?linkid=2081646) verfügbar sind. Für diese Regionen stehen eventuell Lokalisierungen über das bevorzugte Lokalisierungs-App-Programm zur Verfügung. Das bevorzugte Lokalisierungs-App-Programm erkennt jene Apps, die gemäß den spezifischen Qualitätsleitlinien von Microsoft erstellt wurden. ISV-Partner, die diese Programmvoraussetzungen und -leitlinien erfüllen, können im Wiederverkauf und für Kundschaft sowohl technisch als auch kommerziell Vorteile bieten.  

In den folgenden Abschnitten finden Sie die Anforderungen und Leitlinien. Sie können sich das Programmteam wenden, wenn Sie an dem Programm teilnehmen möchten und die untenstehenden Anforderungen erfüllen. Sie erreichen uns über das [Microsoft-Lokalisierungsteam](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> Die [!INCLUDE[prod_short](includes/prod_short.md)]-Initiative für validierte Lokalisierungs-Apps wird derzeit als Pilotprogramm eingeführt. Die folgenden Anforderungen und Vorteile können sich je nach Feedback von Partnern und Kunden ändern.  

Apps im validierten Lokalisierungspilotprogramm enthalten eine Reihe von Funktionen, die lokale behördliche Anforderungen erfüllen und in eine der Kategorien auf der folgenden Liste fallen.  

- **Gesetzliche Anforderungen**: lokale Funktionen, die Unternehmen dabei unterstützen, ihre gesetzlichen Anforderungen zu erfüllen, zum Beispiel im Hinblick auf Steuererklärungen, lokale E-Rechnungsformate, lokale GAAP-Vorgaben und andere gesetzliche Anforderungen.
- **Anforderung nationaler Standards**: lokale Funktionalität, die lokale Standards berücksichtigt, wie etwa Adressformate, nationale Bankformate oder lokale Auslegungen globaler Standards.
- **Lokale Sprache**: lokale Sprache in der Lokalisierungs-App, aber auch für eine Basis-App, wenn diese Sprache derzeit nicht auf der Liste der [unterstützten Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) steht.
- **Lokale Sprache**: lokale Sprache in einer Lokalisierungs-App, aber auch für eine Basis-App, wenn diese Sprache derzeit nicht auf der Liste der [unterstützten Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) steht.

> [!NOTE]
> Lokale Marktbedürfnisse oder Branchenanforderungen sollten nicht in die bevorzugten Lokalisierungs-Apps aufgenommen werden. Wenn Apps diese Funktionen enthalten, können sie nicht als validierte Lokalisierungs-Apps zugelassen werden.

> [!NOTE]
> Lokale Funktionen wirken sich positiv auf die Produktivität der Geschäftsprozesse in einem Land aus und bieten Unternehmen dadurch einen höheren Mehrwert, sind jedoch aus gesetzlicher Sicht nicht erforderlich. So sollten etwa bestimmte Bank- und Zahlungsformate, Spesenabrechnungen, HR-Funktionen, Gehaltsabrechnungen und ähnliche kleinere oder größere sowie praktische, aber nicht notwendige Funktionen in anderen Apps umgesetzt werden. Wenn Apps diese Funktionen enthalten, werden sie nicht als validierte Lokalisierungs-Apps zugelassen.   

## <a name="validated-localization-app-business-requirements"></a>Geschäftliche Anforderungen an validierte Lokalisierungs-Apps

- Der Anbieter der validierten Lokalisierungs-App erfüllt alle Anforderungen an einen indirekten CSP-Anbieter.  
- Der Anbieter der validierten Lokalisierungs-App bringt mindestens in fünf Ländern/Regionen Angebote auf den Markt, die Dynamics 365 Business Central mit einer validierten Lokalisierungs-App bündeln. 
- Der Anbieter der validierten Lokalisierungs-App verfügt über mindestens 10 [!INCLUDE[prod_short](includes/prod_short.md)]-Onlinekunden mit Produktionsumgebungen, welche die validierte Lokalisierungs-App aktiv nutzen. 
- Der Anbieter der validierten Lokalisierungs-App reicht jährlich einen Geschäftsplan beim V-Team des Programms ein. Hierzu gehören geplante Marketing- und Bereitschaftsaktivitäten zur Bewerbung des gebündelten Angebots gegenüber den indirekten CSP-Wiederverkäufern in den entsprechenden Ländern/Regionen. Der Plan kann zu Beginn jedes Quartals beim [Microsoft-Lokalisierungsteam](mailto:d365bcloc@microsoft.com) eingereicht werden.  
- Validierte Lokalisierungs-Apps werden allen Kunden und Partnern zur Verfügung gestellt, die ihre Vorteile nutzen möchten.  
- Der Anbieter der validierten Lokalisierungs-App bringt mindestens in fünf Ländern/Regionen Angebote auf den Markt, die Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)] mit einer validierten Lokalisierungs-App bündeln. 
- Der Anbieter der validierten Lokalisierungs-App verfügt über mindestens 10 [!INCLUDE[prod_short](includes/prod_short.md)]-Onlinekunden mit Produktionsumgebungen, welche die validierte Lokalisierungs-App aktiv nutzen. 
- Der Anbieter der validierten Lokalisierungs-App reicht jährlich einen Geschäftsplan beim V-Team des Programms ein. Hierzu gehören geplante Marketing- und Bereitschaftsaktivitäten zur Bewerbung des gebündelten Angebots gegenüber den indirekten CSP-Wiederverkäufern in den entsprechenden Ländern/Regionen. Der Plan kann immer zu Beginn eines Quartals beim [Microsoft-Lokalisierungsteam](mailto:d365bcloc@microsoft.com) eingereicht werden.  
- Validierte Lokalisierungs-Apps werden allen Kunden und Partnern zur Verfügung gestellt, die ihre Vorteile nutzen möchten.  
- Der Anbieter der validierten Lokalisierungs-App führt wiederkehrende Arbeitsstreams mit Microsoft durch.

## <a name="validated-localization-app-functional-and-technical-requirements"></a>Funktionale und technische Anforderungen an validierte Lokalisierungs-App

### <a name="functionality-requirements"></a>Anforderungen an die Funktionalität

Die validierte Lokalisierungs-App muss nicht nur die technischen Anforderungen erfüllen, sondern auch mindestens den folgenden Produktumfang bieten:  

- Regionale gesetzliche Features:   
  - Gesetzliche Anforderungen.   
  - Offiziell vorgeschriebene Features. 
  - Nur horizontale Features (nicht branchenspezifisch).  
  - In den meisten Unternehmen einsetzbar.  
  - Entspricht der folgenden Blaupause:   
    - Bereiche mit den häufigsten Gesetzesänderungen. 
    - Wird in Microsoft-Lokalisierungen bereits zur Lokalisierung nachverfolgt. 
    - Featurereferenzen: selten neu.  
    - Keine anbieter-/bankspezifischen Formate, Gehaltsabrechnungen oder Ähnliches. 
    - Keine globalen Features, die nicht von Microsoft erstellt wurden. 
- Übersetzungen: 
  - Übersetzung einer Lokalisierungs-App in lokale Sprachen. 
  - Übersetzung einer Basis-App in lokale Sprachen: Falls die Sprache noch nicht [unterstützt](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) wird.  
  - Übersetzung der Dokumentation der Lokalisierungs-App in lokale Sprachen. 
- Obwohl beide Teil der Lokalisierung sind, wird empfohlen, nationale Standardfeatures (lokaler Teil) als separate Apps erstellt und nicht in dieselbe App wie die lokalen gesetzlichen Features integriert werden. 
- Demodaten in der für den jeweiligen Markt geltenden Landessprache.   
- Alle Features müssen so gestaltet sein, dass die Benutzeroberfläche einfach zu handhaben bleibt. Beachten Sie, dass sie in erster Linie für den KMU-Markt bestimmt sind.  
- Entwickeln Sie keine neuen Features, wenn dieselben oder ähnliche Features bereits in der Basis-App vorliegen, z. B. elektronische Fakturierung, Prüfungsexporte, MwSt.-Features, Datenaustausch und andere, bei denen die meisten Funktionen in allen Ländern/Regionen gleich sind, es jedoch einige lokale Regeln oder Geschäftsformate gibt, bei denen es sich um Erweiterungen globaler Frameworks oder Formate handelt. Anstatt neue Features zu erstellen, erweitern Sie vorhandene.  
- Erstellen Sie Einrichtungsleitfäden (Assistenten) für Bereiche, deren Einrichtung komplex ist, um Benutzenden die Aktivierung und Entdeckung Ihrer Lokalisierungs-App zu erleichtern und ihnen zu helfen, eine angenehme Erfahrungen mit der ersten Verwendung dieser App zu machen.  
- Alle Features müssen so gestaltet sein, dass die Benutzeroberfläche einfach zu handhaben bleibt. Beachten Sie dabei, dass die Features in erster Linie für den KMU-Markt bestimmt sind.  
- Entwickeln Sie keine neuen Features, wenn dieselben oder ähnliche Features bereits in der Basis-App vorliegen, z. B. elektronische Fakturierung, Prüfungsexporte, MwSt.-Features, Datenaustausch und andere, bei denen die meisten Funktionen in allen Ländern/Regionen gleich sind, es jedoch einige lokale Regeln oder Geschäftsformate gibt, bei denen es sich um Erweiterungen globaler Frameworks oder Formate handelt. Anstatt neue Features zu erstellen, erweitern Sie vorhandene.    
- Erstellen Sie Einrichtungsleitfäden (Assistenten) für Bereiche, deren Einrichtung komplex ist, um Benutzenden die Aktivierung und Entdeckung Ihrer Lokalisierungs-App zu erleichtern und ihnen zu helfen, eine angenehme Erfahrungen mit der ersten Verwendung dieser App zu machen.  
- Partner müssen für alle Aspekte ihrer Lokalisierung eine Funktionsdokumentation bereitstellen.  

### <a name="technical-requirements"></a>Technische Anforderungen

Im Folgenden finden Sie eine Liste der Anforderungen, die Sie erfüllen müssen, bevor Sie die validierte Lokalisierungs-App als Erweiterung zur Validierung einreichen können. Diese Liste ändert die [technische Validierungsliste](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) nicht und erweitert die Anforderungen lediglich von diesem Ausgangspunkt aus.  

- Die Anbieter validierter Lokalisierungs-Apps müssen die validierte Lokalisierungs-App auf Grundlage der W1-Basis-App erstellen.  
- Die Anbieter validierter Lokalisierungs-Apps müssen die Lebenszyklus- und Supportrichtlinien von Microsoft einhalten.   
- Die obligatorische Testautomatisierung muss mindestens 80 % des Codes und alle Geschäftsprozesse abdecken, die sich durch die validierte Lokalisierungs-App ändern.  
- Die Anbieter validierter Lokalisierungs-Apps müssen ihre validierte Lokalisierungs-App vor der offiziellen Einführung einer neuen Version aktualisieren und/oder testen (mindestens mit dem RC vor der neuen Version), um sicherzustellen, dass keine Probleme vorliegen. 
- Alle Objekte im Code der validierten Lokalisierungs-App müssen auf Englisch sein.   
- Die Anbieter validierter Lokalisierungs-Apps müssen die Microsoft-Richtlinien für veraltete Objekte und wichtige Änderungen sowie bewährte Methoden für die Abschaffung des AL-Codes befolgen.  
- Die Anbieter validierter Lokalisierungs-Apps sollten neue Ereignisse hinzufügen, wenn der Markt (anderen Implementierungspartnern oder Kundschaft) dies verlangt und sofern dies unter Beachtung der Richtlinien und Vorgehensweisen von Microsoft geschäftlich sinnvoll ist. Andernfalls müssen die Anbieter validierter Lokalisierungs-Apps auf derartige Anfragen begründen, warum die Hinzufügung aus geschäftlicher Sicht keinen Sinn ergibt. 
- Die Anbieter validierter Lokalisierungs-Apps müssen schriftliche Testszenarien in englischer Sprache bereitstellen und Microsoft die Durchführung manueller Tests erlauben, falls dies von Microsoft verlangt wird.  
- Wenn eine validierte Lokalisierungs-App das [!INCLUDE[prod_short](includes/prod_short.md)]-Datenmodell um neue Tabellen und/oder Felder erweitert, muss der Anbieter der validierten Lokalisierungs-App die Eigenschaft **DataClassification** korrekt festlegen.
- Die Anbieter validierter Lokalisierungs-Apps müssen die validierte Lokalisierungs-App auf Grundlage der W1-Basis-App erstellen.  
- Die Anbieter validierter Lokalisierungs-Apps müssen die Lebenszyklus- und Supportrichtlinien von Microsoft einhalten.   

> [!NOTE]  
> Sie können auch eine Integration erstellen, wenn es Ihrer Meinung nach von Vorteile wäre, einige Funktionen außerhalb der [!INCLUDE[prod_short](includes/prod_short.md)]-Umgebung zu platzieren und stattdessen die Verbindung zu [!INCLUDE[prod_short](includes/prod_short.md)] beispielsweise über APIs oder Webdienste herzustellen.

## <a name="see-also"></a>Siehe auch

[Technische Validierung](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Entwicklung einer Standardlokalisierungslösung](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Verfügbarkeit nach Ländern/Regionen und unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Was ist lokale Funktion in Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]?](about-localization.md)  
[Internationale Verfügbarkeit von Microsoft Dynamics 365](/dynamics365/get-started/availability)  
[Compliance – Übersicht](compliance/compliance-overview.md)  
[Geografische Verfügbarkeit für Dynamics 365](https://dynamics.microsoft.com/en-us/availability-reports/georeport/)  
