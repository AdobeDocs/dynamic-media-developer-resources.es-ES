---
description: Notas de compatibilidad para sistemas operativos, navegadores y dispositivos móviles.
seo-description: Notas de compatibilidad para sistemas operativos, navegadores y dispositivos móviles.
seo-title: Notas de compatibilidad
solution: Experience Manager
title: Notas de compatibilidad
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 1%

---


# Notas de compatibilidad{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Notas de compatibilidad para sistemas operativos, navegadores y dispositivos móviles.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilidad con conjuntos de vídeos adaptables más antiguos. Es posible que deba volver a cargar conjuntos de vídeos adaptables para permitir la reproducción.

## General {#section-7b9a9fcba85148d1802b7b3016b48e02}

* El escalado del lado del explorador puede hacer que la interfaz de usuario y las imágenes se vuelvan borrosas a medida que el usuario amplía la página. El formato de la interfaz de usuario también puede mostrarse incorrectamente según el zoom. Esto pasará a pantalla completa.
* Debido a la limitación del tamaño de los dispositivos móviles, el visualizador de medios mixtos utiliza un gesto de diapositivas para intercambiar fotogramas en conjuntos de imágenes incrustados en lugar de pulsar el componente de muestras incrustadas. El componente está ahí como indicador visual.
* En los navegadores Internet Explorer y en algunos dispositivos táctiles, el modo de pantalla completa no ocupa toda la pantalla del dispositivo. En su lugar, cambia el tamaño de la aplicación al tamaño de la ventana del explorador.
* El botón Cerrar no funciona en iOS 8.0 e iOS 8.1 pero funciona en iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Fuga de memoria vista con los visores Zoom y eCatalog. La navegación repetida a través de marcos puede causar que el navegador se bloquee.
* Al tocar dos veces un visor, es posible que toda la página se zoom en lugar de solo el visualizador con el escalado del lado del navegador activado.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Dispositivo detectado como tableta en modo vertical con pantalla completa marcada en la configuración del navegador.

## Nexo de galaxia {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Al tocar dos veces un visor, es posible que toda la página se zoom en lugar de solo el visor, con el escalado del lado del explorador habilitado.

## Galaxy Nexus 10 y Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* El catálogo electrónico muestra una página incorrecta con orientaciones verticales y horizontales.

## Dispositivos móviles HTC {#section-dc42c80414c842e488738fc157c55b01}

* La incapacidad de desactivar el zoom de pellizcar nativo es una &quot;función&quot; del envoltorio de la interfaz de usuario de HTC (HTC Sense). Esta función puede hacer que una página entera se zoom al usar el gesto de &quot;pellizcar para hacer zoom&quot; en el visor. En su lugar, utilice un gesto de doble toque.
* Los iconos del mapa de imágenes pueden superponerse si los mapas de imágenes son pequeños y están próximos entre sí.

## Visor de vídeo HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` sólo se admite con el software HLS y la reproducción flash HDS. No funciona cuando la reproducción utiliza el reproductor nativo.
* No se admite la reproducción progresiva de OGG y WebM.
* El escalado del explorador puede hacer que el reproductor de vídeo se muestre con un tamaño incorrecto (incluye la configuración de visualización del panel de control del sistema operativo Windows).
* La búsqueda de vídeo mediante el flujo HLS en Safari puede ser incoherente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* No se admite el modo Quirks.
* No se admite el modo de compatibilidad.
* Internet Explorer en dispositivos móviles no es compatible.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Los catálogos electrónicos grandes pueden provocar que el navegador se bloquee en el iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 o posterior: La configuración del complemento de Internet puede impedir la reproducción de vídeo de Flash.
* La búsqueda de vídeo mediante el flujo HLS en Safari puede ser incoherente.
* No se puede intentar finalizar el vídeo en Safari 6 mediante el flujo HLS.
