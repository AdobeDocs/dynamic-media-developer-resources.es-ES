---
title: Requisitos del sistema para los visores Dynamic Media HTML5
description: Requisitos del sistema para los visores Dynamic Media HTML5.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 8e09f8168987788f7d55849b4a275c488cfcc0b9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 2%

---

# Requisitos del sistema para los visores HTML5 de Dynamic Media{#system-requirements}

Requisitos del sistema para los visores Dynamic Media HTML5.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Hardware y software del servidor {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1 o posterior.
* Los visores HTML5 requieren bibliotecas de SDK JavaScript del lado del servidor 3.11.5 o posterior.
* *Enviar un correo electrónico a un amigo* las funciones sociales requieren s7ondemand 5.0.9 o posterior.
* Visor de catálogos electrónicos - [Ventana emergente del panel Información](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) la compatibilidad con requiere el servidor de información 2.1.8 o posterior.
* Los componentes de las funciones de búsqueda requieren s7search 2.3.0 o posterior.

## Requisitos del sistema de visores {#section-cc72b1e209524d038b4d5b92b35e998e}

**Requisitos mínimos del navegador del cliente para los visores de componentes:**

* Compatible con las siguientes versiones del sistema operativo o posteriores:
   * Microsoft® Windows® 7
   * macOS X 10.12
* Compatible con las siguientes versiones de explorador/plataforma o posteriores:
   * Android™ OS 4.x
   * BlackBerry® 10 en navegadores nativos. Solo se admite la reproducción de vídeo.
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 (solo navegadores Safari y Chrome)
   * iPhone 3GS
   * Safari 11
* No se admite Internet Explorer en dispositivos móviles.
* *Visor panorámico* es compatible con las siguientes versiones de explorador/plataforma o versiones posteriores:
   * Android™ 4.4 (solo dispositivos móviles)
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Visor de vídeos360* y *Visor dimensional* es compatible con las siguientes versiones de explorador/plataforma o versiones posteriores:
   * Android™ 5 (solo dispositivos móviles)
   * Chrome 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* es compatible con las siguientes versiones de explorador/plataforma o versiones posteriores:
   * Android™ 4.x
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

**IMPORTANTE**
A partir del 30 de septiembre de 2022, los visores de Adobe de Dynamic Media dejarán de ser compatibles con lo siguiente:

* TLS (Transport Layer Security) 1.0 y 1.1
* Las siguientes cifras débiles en TLS 1.2:
   * `TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384`
   * `TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`
   * `TLS_RSA_WITH_AES_256_GCM_SHA384`
   * `TLS_RSA_WITH_AES_256_CBC_SHA256`
   * `TLS_RSA_WITH_AES_256_CBC_SHA`
   * `TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256`
   * `TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`
   * `TLS_RSA_WITH_AES_128_GCM_SHA256`
   * `TLS_RSA_WITH_AES_128_CBC_SHA256`
   * `TLS_RSA_WITH_AES_128_CBC_SHA`
   * `TLS_RSA_WITH_CAMELLIA_256_CBC_SHA`
   * `TLS_RSA_WITH_CAMELLIA_128_CBC_SHA`
   * `TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA`
   * `TLS_RSA_WITH_SDES_EDE_CBC_SHA`

<!-- Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android™ 2.3.7
* Android™ 4.0.4
* Android™ 4.1.1
* Android™ 4.2.2
* Android™ 4.3
* Internet Explorer 7 on Window Vista®
* Internet Explorer 8 on Windows® XP
* Internet Explorer 8-10 on Windows® 7
* Internet Explorer 10 on Windows® Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java™ 6u45
* Java™ 7u25
* OpenSSL 0.9.8y
* Baidu January 2015 -->

<!-- FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->
