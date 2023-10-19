---
title: Einrichten von eingehenden Belegen
description: 'Richten Sie die Funktion Eingehende Belege ein, um elektronische Belege zu erstellen, OCR-Aufgaben zu verwalten, Rechnungen zu importieren und Bilddateien zu konvertieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
---
# Einrichten von eingehenden Belegen

Wenn Sie Fibu Buch.-Blattzeilen für eingehende Belege erstellen, müssen Sie auf der Seite **Einrichtung für eingehende Belege** angeben, welche Buch.-Blattvorlage und welches Buch.-Blatt verwendet werden sollen.

Wenn die Funktion **Eingehende Belege** festgelegt ist, können Sie verschiedene Funktionen verwenden, um Spesenbelege zu prüfen, OCR-Aufgaben zu verwalten und eingehende Dokumentdateien manuell oder automatisch in die entsprechenden Dokumente oder Buchungsblattzeilen umzuwandeln. Die externen Dateien können in jeder Prozessphase angehängt werden, auch an gebuchte Belege und an die daraus resultierenden Kreditoren-, Kunden- und Hauptbuchhaltungsposten. Weitere Informationen finden Sie unter [Erstellen von Datensätzen für eingehende Belege](across-how-create-income-document-records.md).

## So richten Sie die Funktion für eingehende Belege ein

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Einrichtung für eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Im Rahmen der Einrichtung müssen Sie entscheiden, ob Sie die Genehmigung eingehender Belege benötigen. Um eine Genehmigung zu verlangen, müssen Sie [Genehmiger und Genehmigungs-Workflows festlegen](#to-set-up-approvers-of-incoming-document-records). Wenn Ihr Unternehmen nicht beabsichtigt, eine Genehmigung zu verlangen, können Sie den nächsten Abschnitt überspringen.

Wenn Sie schließlich einen OCR-Dienst zur Konvertierung von PDF- oder Bilddateien verwenden, die eingehende Dokumente darstellen, [müssen Sie ihn festlegen](#to-set-up-an-ocr-service). Andernfalls können Sie diesen Abschnitt auch überspringen.

## So richten Sie Genehmiger für eingehende Belege ein

Wenn Sie nicht möchten, dass Benutzer Rechnungen oder Allgemeine Buchungsblattzeilen aus eingehenden Datensätzen erstellen, ohne dass die Dokumente zuvor genehmigt wurden, legen Sie einen Genehmigungsprozess für die eingehenden Dokumente fest. Genehmiger von eingehenden Belegen müssen als Genehmigungsworkflow-Benutzer eingerichtet werden.

Bevor Sie Workflows erstellen können, die Genehmigungsschritte betreffen, müssen Sie die Workflowbenutzer einrichten, die von den Genehmigungsprozessen betroffen sind. Auf der Seite **Genehmigungsbenutzereinrichtung** müssen Sie zusätzlich Grenzbeträge für bestimmte Arten von Anforderungen festlegen und Ersatzgenehmiger definieren, an die Genehmigungsanforderungen delegiert werden, wenn der ursprüngliche Genehmiger abwesend ist. Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md).

## So richten Sie einen OCR-Service ein

Um PDF- und Bilddateien in elektronische Belege zu verwandeln, die Sie in Rechnungen, Gutschriften oder Buchungsblattzeilen umwandeln können, legen Sie die OCR-Funktion fest. Alternativ können Sie Einträge manuell erstellen, um die externen Dokumente darzustellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **OCR-Dienst Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Sie informieren Daten werden verschlüsselt automatisch an.

Weitere Informationen finden Sie unter [Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md).  

## Siehe auch

[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
