---
description: La imagen de precarga es una imagen de vista previa de recursos estática que se carga justo después de llamar al método init() y se muestra mientras se descarga la información de bibliotecas, recursos y ajustes preestablecidos del SDK de visor. El propósito de la imagen de carga previa es mejorar visualmente el tiempo de carga del visor y presentar el contenido al usuario rápidamente.
solution: Experience Manager
title: Precargar imagen
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Developer,Business Practitioner
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Precargar imagen{#preload-image}

La imagen de precarga es una imagen de vista previa de recursos estática que se carga justo después de llamar al método init() y se muestra mientras se descarga la información de bibliotecas, recursos y ajustes preestablecidos del SDK de visor. El propósito de la imagen de carga previa es mejorar visualmente el tiempo de carga del visor y presentar el contenido al usuario rápidamente.

La precarga de imagen funciona bien para el método de incrustación del visor más común, que es una incrustación interactiva con altura ilimitada. Consulte el encabezado [Diseño interactivo incrustado con altura ](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e) no restringida.

Sin embargo, la función tiene ciertas limitaciones cuando se utilizan otros métodos de incrustación o opciones de configuración específicas. Es posible que la imagen de precarga no se represente correctamente en los siguientes casos:

* Cuando el visor tiene un tamaño fijo y el tamaño se define mediante el atributo de configuración `stagesize` dentro del registro preestablecido del visor o en el archivo CSS del visor externo para el elemento contenedor del visor de nivel superior.
* Cuando se utiliza el método de incrustación del visor definido de anchura y altura, de tamaño flexible. Consulte el encabezado [Tamaño flexible incrustado con anchura y altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Es posible que tenga que desactivar la función de imagen de precarga mediante el atributo de configuración `preloadImage` si utiliza el visor en uno de los modos de operación enumerados anteriormente.

Además, la imagen de precarga no se utiliza (aunque esté habilitada en la configuración) si el visor está incrustado en el elemento DOM está oculto al utilizar la configuración `display:none` CSS o desasociado del árbol DOM.
