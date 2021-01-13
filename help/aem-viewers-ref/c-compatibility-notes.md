---
description: Notas de compatibilidad para sistemas operativos, navegadores y dispositivos móviles.
seo-description: Notas de compatibilidad para sistemas operativos, navegadores y dispositivos móviles.
seo-title: Notas de compatibilidad
solution: Experience Manager
title: Notas de compatibilidad
topic: Dynamic media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: 07eb6cf84a46753b41307187d5c5b2a077fa9009
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 1%

---


# Notas de compatibilidad{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Notas de compatibilidad para sistemas operativos, navegadores y dispositivos móviles.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilidad con conjuntos de vídeos adaptables anteriores. Es posible que tenga que volver a cargar los conjuntos de vídeos adaptables para permitir la reproducción.

## General {#section-7b9a9fcba85148d1802b7b3016b48e02}

* La escala del lado del explorador puede hacer que la interfaz de usuario y las imágenes se desdibujen a medida que el usuario se acerque a la página. El formato de la interfaz de usuario también puede mostrarse incorrectamente en función del zoom. Esto pasará a la pantalla completa.
* Debido a la limitación de tamaño en dispositivos móviles, el visor de medios mixtos utiliza gestos de diapositiva para intercambiar fotogramas en conjuntos de imágenes incrustadas en lugar de tocar el componente de muestras incrustadas. El componente está allí como indicador visual.
* En los navegadores Internet Explorer y algunos dispositivos táctiles, el modo de pantalla completa no ocupa toda la pantalla del dispositivo. En su lugar, cambia el tamaño de la aplicación al tamaño de la ventana del explorador.
* El botón Cerrar no funciona en iOS 8.0 e iOS 8.1, pero funciona en iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Pérdida de memoria observada con los visores de catálogos electrónicos y zoom. La navegación repetida a través de marcos puede provocar que el navegador se bloquee.
* Al tocar el doble en un visor, es posible que se aplique zoom a toda la página en lugar de solo al visor con la escala del navegador activada.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Dispositivo detectado como tableta en modo vertical con pantalla completa marcada en la configuración del navegador.

## Nexo de galaxia {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Al tocar el doble en un visor, es posible que toda la página se acerque en lugar de solo al visor, con el ajuste de escala del navegador activado.

## Galaxy Nexus 10 y Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* El catálogo electrónico muestra una distribución incorrecta de la página con orientaciones vertical y horizontal.

## Dispositivos móviles HTC {#section-dc42c80414c842e488738fc157c55b01}

* La incapacidad de desactivar el zoom de pellizco nativo es una &quot;característica&quot; del envoltorio de la interfaz de usuario de HTC (HTC Sense). Esta función puede hacer que una página entera se acerque al usar el gesto de &quot;pellizcar para hacer zoom&quot; en el visor. En su lugar, utilice un gesto de toque de doble.
* Los iconos de mapas de imagen pueden superponerse si los mapas de imagen son pequeños y están próximos entre sí.

## Visor de vídeo HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` solo se admite con la reproducción de software HLS y flash HDS. No funciona cuando la reproducción utiliza el reproductor nativo.
* No se admite la reproducción progresiva de OGG y WebM.
* La escala del explorador puede hacer que el reproductor de vídeo se muestre con un tamaño incorrecto (incluye la configuración de visualización del panel de control del sistema operativo Windows).
* La búsqueda de vídeos mediante flujo HLS en Safari puede ser incoherente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* No se admite el modo Quirks.
* No se admite el modo de compatibilidad.
* No se admite Internet Explorer en dispositivos móviles.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Los catálogos electrónicos grandes pueden provocar que el explorador se bloquee en el iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 o posterior: La configuración del complemento Internet puede impedir la reproducción de vídeo Flash.
* La búsqueda de vídeos mediante flujo HLS en Safari puede ser incoherente.
* No se puede buscar el final del vídeo en Safari 6 mediante el flujo HLS.
