---
title: Notas de compatibilidad
description: Notas de compatibilidad para sistemas operativos, exploradores y dispositivos móviles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 1%

---

# Notas de compatibilidad{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Notas de compatibilidad para sistemas operativos, exploradores y dispositivos móviles.

## Blackberry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilidad con conjuntos de vídeos adaptables anteriores. Vuelva a cargar los conjuntos de vídeos adaptables para permitir la reproducción.

## General {#section-7b9a9fcba85148d1802b7b3016b48e02}

* La escala del lado del explorador hace que la interfaz de usuario y las imágenes se vuelvan borrosas a medida que el usuario amplía la página. El formato de la interfaz de usuario también se muestra incorrectamente en función del zoom y se transfiere a pantalla completa.
* Debido a la limitación de tamaño en dispositivos móviles, el visualizador de medios mixtos utiliza el gesto de diapositiva para intercambiar fotogramas en conjuntos de imágenes incrustados en lugar de pulsar el componente de muestras incrustado. El componente está presente como indicador visual.
* En los exploradores de Internet Explorer y en algunos dispositivos táctiles, el modo de pantalla completa no ocupa toda la pantalla del dispositivo. En su lugar, cambia el tamaño de la aplicación según el tamaño de la ventana del explorador.
* El botón Cerrar no funciona en iOS 8.0 y iOS 8.1, pero sí en iOS 8.2.

## Galaxia SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Pérdida de memoria con visores de zoom y catálogo electrónico. La navegación repetida a través de fotogramas hace que el explorador se bloquee.
* Al tocar dos veces en un visor, se hace que toda la página se haga zoom en lugar de hacerlo solo en el visor con la escala del lado del explorador habilitada.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* El dispositivo se ha detectado como tablet en modo vertical con la opción Pantalla completa activada en la configuración del navegador.

## Nexo galáctico {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Al tocar dos veces en un visor, toda la página se amplía, en lugar de hacerlo únicamente el visor, con la escala en el explorador habilitada.

## Galaxy Nexus 10 y Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* El catálogo electrónico muestra un pliego de páginas incorrecto con orientaciones verticales y horizontales.

## Dispositivos móviles HTC {#section-dc42c80414c842e488738fc157c55b01}

* La incapacidad para deshabilitar el zoom de pellizco nativo es una &quot;función&quot; del envoltorio de la interfaz de usuario de HTC (HTC Sense). Esta función puede hacer que toda una página se haga zoom al utilizar el gesto de &quot;pellizco para zoom&quot; en el visor. En su lugar, pulse dos veces.
* Los iconos de mapa de imagen se superponen si los mapas de imagen son pequeños y están muy juntos.

## Visor de vídeo de HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` El modificador solo es compatible con el software de reproducción HLS y Flash HDS. No funciona cuando la reproducción utiliza el reproductor nativo.
* No se admite la reproducción progresiva OGG y WebM.
* La escala del explorador hace que el reproductor de vídeo se muestre en un tamaño incorrecto (incluye la configuración de visualización del Panel de control de Campaign de Windows®).
* Las búsquedas de vídeo mediante el streaming HLS en Safari son incoherentes.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* El modo Quirks no es compatible.
* No se admite el modo de compatibilidad.
* No se admite Internet Explorer en dispositivos móviles.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Los catálogos electrónicos grandes hacen que el explorador se bloquee en iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 o posterior: la configuración del complemento de Internet impide la reproducción de vídeo en Flash.
* Las búsquedas de vídeo mediante el streaming HLS en Safari son incoherentes.
* No se puede buscar el final del vídeo en Safari 6 mediante flujo HLS.
