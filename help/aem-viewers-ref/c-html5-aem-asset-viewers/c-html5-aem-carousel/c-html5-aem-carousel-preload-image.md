---
description: La imagen de precarga es una imagen de previsualización de recursos estática que se carga justo después de llamar al método init() y se muestra mientras se descarga la información de recursos y ajustes preestablecidos de las bibliotecas del SDK de visor. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visor y presentar contenido al usuario rápidamente.
seo-description: La imagen de precarga es una imagen de previsualización de recursos estática que se carga justo después de llamar al método init() y se muestra mientras se descarga la información de recursos y ajustes preestablecidos de las bibliotecas del SDK de visor. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visor y presentar contenido al usuario rápidamente.
seo-title: Precargar imagen
solution: Experience Manager
title: Precargar imagen
topic: Dynamic Media
uuid: bae99269-fd55-485e-b78e-873b77541d91
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Precargar imagen{#preload-image}

La imagen de precarga es una imagen de previsualización de recursos estática que se carga justo después de llamar al método init() y se muestra mientras se descarga la información de recursos y ajustes preestablecidos de las bibliotecas del SDK de visor. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visor y presentar contenido al usuario rápidamente.

La precarga de imágenes funciona bien para el método de incrustación del visor más común, que es una incrustación interactiva con altura ilimitada. Consulte el encabezado [Diseño interactivo incrustado con altura sin restricciones](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Sin embargo, la función tiene ciertas limitaciones cuando se utilizan otros métodos de incrustación o opciones de configuración específicas. Es posible que la imagen de precarga no se procese correctamente en los siguientes casos:

* Cuando el tamaño del visor es fijo y se define mediante el atributo de configuración `stagesize` dentro del registro de ajustes preestablecidos del visor o en el archivo CSS del visor externo para el elemento de contenedor del visor de nivel superior.
* Cuando se utiliza la incrustación de tamaño flexible con el método definido de anchura y altura de incrustación del visor. Consulte el encabezado [Integración de tamaño flexible con anchura y altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Es posible que deba desactivar la función de precarga de imagen mediante el atributo de configuración `preloadImage` si utiliza el visor en uno de los modos de operación enumerados anteriormente.

Además, la imagen de precarga no se utiliza, aunque esté habilitada en la configuración, si el visor está incrustado en el elemento DOM se oculta mediante `display:none` CSS o se desasocia del árbol DOM.
