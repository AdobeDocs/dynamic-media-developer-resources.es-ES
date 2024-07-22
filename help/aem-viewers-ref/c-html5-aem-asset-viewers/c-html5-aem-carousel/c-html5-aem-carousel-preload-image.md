---
title: Precargar imagen
description: La imagen de precarga es una imagen de vista previa de recursos estáticos que se carga justo después de llamar al método init() y se muestra mientras se descargan las bibliotecas, los recursos y la información de ajustes preestablecidos del SDK del visualizador. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visualizador y presentar contenido al usuario rápidamente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Precargar imagen{#preload-image}

La imagen de precarga es una imagen de vista previa de recursos estáticos que se carga justo después de llamar al método init() y se muestra mientras se descargan las bibliotecas, los recursos y la información de ajustes preestablecidos del SDK del visualizador. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visualizador y presentar contenido al usuario rápidamente.

La imagen de precarga funciona bien para el método de incrustación de visor más común, que es la incrustación adaptable con altura sin restricciones. Ver el encabezado [Diseño interactivo incrustado con altura sin restricciones](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Sin embargo, la función tiene ciertas limitaciones cuando se utilizan otros métodos de incrustación u opciones de configuración específicas. La imagen de precarga puede no procesarse correctamente en los siguientes casos:

* Cuando el visor tiene un tamaño fijo y el tamaño se define mediante el atributo de configuración `stagesize` dentro del registro de ajustes preestablecidos del visor o en el archivo CSS del visor externo para el elemento contenedor del visor de nivel superior.
* Al utilizar la incrustación de tamaño flexible con el método definido de anchura y altura de incrustación del visualizador. Ver el encabezado [Tamaño flexible incrustado con la anchura y la altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Si usa el visor en uno de los modos de operación enumerados arriba, deshabilite la característica de imagen de precarga usando el atributo de configuración `preloadImage`.

Además, la imagen de precarga no se utiliza (aunque esté habilitada en la configuración) si el visor está incrustado en el elemento DOM, está oculto mediante la configuración CSS `display:none` o se ha separado del árbol DOM.
