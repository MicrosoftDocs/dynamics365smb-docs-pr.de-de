---
title: 'Problembehebung: Auf Kamera und Standort zugreifen'
description: In diesem Artikel wird beschrieben, wie Fehler beim Zugriff auf Kamera- und Standortinformationen in Business Central behoben werden.
author: blrobl
ms.author: t-blrobl
ms.date: 04/22/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics365-business-central
ms.openlocfilehash: befb7af01ba26512a4b62005e81b5a3ff351b02f
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324468"
---
# <a name="troubleshooting-accessing-camera-and-location"></a>Problembehebung: Auf Kamera und Standort zugreifen

Wenn Sie versuchen, die Kamera- und Standortinformationen eines Geräts über [!INCLUDE[prodshort](includes/prodshort.md)] aufzurufen, können Probleme auftreten. Nachfolgend sind die möglichen Ursachen für diese Probleme und deren Umgehung aufgeführt.

## <a name="device-must-have-camera-and-location-capabilities"></a>Das Gerät muss über Kamera- und Standortfunktionen verfügen

Das Gerät muss über eine physische Kamera bzw. die Fähigkeit verfügen, Standortinformationen abzurufen, um von einem Gerät aus auf die Kamera oder den Standort eines Benutzers zugreifen zu können.

Wenn Ihr Gerät über Kamera- und Standortfunktionen verfügt, jedoch weiterhin Probleme auftreten, müssen möglicherweise einige Treiber aktualisiert oder neu installiert werden. Auch wenn Sie nicht sicher sind, empfehlen wir immer, das Betriebssystem, die Treiber und den Browser Ihres Geräts auf die neueste Version zu aktualisieren, um eine optimale Nutzung zu erzielen.

## <a name="access-permissions-not-enabled"></a>Zugriffsberechtigungen sind nicht aktiviert

Sie müssen den allgemeinen Zugriff auf die Kamera und den Standort über die Datenschutzeinstellungen Ihres Geräts aktivieren und [!INCLUDE[prodshort](includes/prodshort.md)] ausdrücklich die Erlaubnis erteilen, darauf zuzugreifen. Wechseln Sie zu **Einstellungen**, und wählen Sie **Datenschutz** und dann **App-Berechtigungen** aus, wenn Sie beispielsweise die Berechtigungen für ein unter Windows ausgeführtes Gerät anzeigen oder ändern möchten. 

Bei mobilen Geräten müssen Sie der mobilen [!INCLUDE[prodshort](includes/prodshort.md)]-App Zugriffsberechtigungen für die Kamera und den Standort gewähren. Wechseln Sie dazu bei einem iOS-Gerät zu **Einstellungen**, und wählen Sie **Datenschutz** und dann **Kamera** oder **Standort** aus. Gehen Sie bei Android-Geräten zu **Einstellungen**, und wählen Sie **Apps & Benachrichtigungen**, **Erweitert**, **Berechtigungsmanager** und dann **Kamera** oder **Standort** aus.

Wenn Sie [!INCLUDE[prodshort](includes/prodshort.md)] in einem Browser verwenden, müssen Sie [!INCLUDE[prodshort](includes/prodshort.md)] außerdem die Websiteberechtigung zum Zugriff auf die Kamera oder Standortinformationen gewähren. Zum Anzeigen oder Ändern der Berechtigungen einer Website im Microsoft Edge-Browser wechseln Sie zu **Einstellungen**, wählen Sie **Websiteberechtigungen** und dann **Kamera** oder **Standort** aus. Beachten Sie, dass dies bei anderen Browsern möglicherweise anders ist.

Das Gerät oder der Browser zeigt standardmäßig eine Anforderung für den Zugriff auf diese Funktionen an, wenn der Benutzer sie zum ersten Mal aktiviert.

> [!NOTE]  
> Einige alte Browser gewähren keinen Zugriff auf die Kamera und den Standort. In Internet Explorer oder in der Vorversion des Edge-Browsers ist beispielsweise keine Kamerafunktion verfügbar.

## <a name="web-client-connection-not-secure"></a>Webclient-Verbindung ist nicht sicher

Die Kamera- und Standortfunktionen sind nur verfügbar, wenn der Zugriff auf den Webclient über SSL-gesicherte HTTP-Verbindungen unter Verwendung des `https://` URI-Schemas erfolgt. 

Die einzige Ausnahme ist die Verbindung zu `http://localhost`, die für Entwicklungs- und Testzwecke verwendet wird.


## <a name="working-with-virtualization-technologies"></a>Mit Virtualisierungstechnologien arbeiten

Wenn eine Verbindung mit [!INCLUDE[prodshort](includes/prodshort.md)] über Remotedesktop oder eine andere Virtualisierung hergestellt wird, ist der Zugriff auf die Kamera oder den Standort möglicherweise nicht verfügbar. Verwenden Sie in diesem Fall stattdessen das physische System.

## <a name="antivirus-software"></a>Antivirensoftware
Es gibt Antivirensoftware, die den Zugriff auf die Kamera und den Standort standardmäßig blockiert. Denken Sie daran, die Einstellungen Ihrer Antivirensoftware zu überprüfen.

## <a name="see-also"></a>Siehe auch
[Kamera in AL implementieren](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Standort in AL implementieren](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
