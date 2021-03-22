---
description: La imagen de precarga es una imagen de vista previa de recursos estática que se carga justo después de llamar al método init() y se muestra mientras se descarga la información de bibliotecas, recursos y ajustes preestablecidos del SDK de visor. El propósito de la imagen de carga previa es mejorar visualmente el tiempo de carga del visor y presentar el contenido al usuario rápidamente.
seo-description: La imagen de precarga es una imagen de vista previa de recursos estática que se carga justo después de llamar al método init() y se muestra mientras se descarga la información de bibliotecas, recursos y ajustes preestablecidos del SDK de visor. El propósito de la imagen de carga previa es mejorar visualmente el tiempo de carga del visor y presentar el contenido al usuario rápidamente.
seo-title: Precargar imagen
solution: Experience Manager
title: Precargar imagen
uuid: cb5db16d-b496-40e4-b8ef-5573c42d2850
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Precargar imagen{#preload-image}

La imagen de precarga es una imagen de vista previa de recursos estática que se carga justo después de llamar al método init() y se muestra mientras se descarga la información de bibliotecas, recursos y ajustes preestablecidos del SDK de visor. El propósito de la imagen de carga previa es mejorar visualmente el tiempo de carga del visor y presentar el contenido al usuario rápidamente.

La precarga de imagen funciona bien para el método de incrustación del visor más común, que es una incrustación interactiva con altura ilimitada. Consulte el encabezado [Diseño interactivo incrustado con altura ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435) no restringida.

Sin embargo, la función tiene ciertas limitaciones cuando se utilizan otros métodos de incrustación o opciones de configuración específicas. Es posible que la imagen de precarga no se represente correctamente en los siguientes casos:

* Cuando el visor tiene un tamaño fijo y el tamaño se define mediante el atributo de configuración `stagesize` dentro del registro preestablecido del visor o en el archivo CSS del visor externo para el elemento contenedor del visor de nivel superior.
* Cuando se utiliza el método de incrustación del visor definido de anchura y altura, de tamaño flexible. Consulte el encabezado [Tamaño flexible incrustado con anchura y altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Es posible que tenga que desactivar la función de imagen de precarga mediante el atributo de configuración `preloadImage` si utiliza el visor en uno de los modos de operación enumerados anteriormente.

Además, la imagen de precarga no se utiliza (aunque esté habilitada en la configuración) si el visor está incrustado en el elemento DOM está oculto al utilizar la configuración `display:none` CSS o desasociado del árbol DOM.
