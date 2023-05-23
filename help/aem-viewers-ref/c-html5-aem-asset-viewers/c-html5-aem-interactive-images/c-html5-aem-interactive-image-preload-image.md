---
title: Precargar imagen
description: La imagen de precarga es una imagen de vista previa de recursos estáticos que se carga justo después de llamar al método init() y se muestra mientras se descargan las bibliotecas, los recursos y la información de ajustes preestablecidos del SDK del visualizador. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visualizador y presentar contenido al usuario rápidamente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Precargar imagen{#preload-image}

La imagen de precarga es una imagen de vista previa de recursos estáticos que se carga justo después de llamar al método init() y se muestra mientras se descargan las bibliotecas, los recursos y la información de ajustes preestablecidos del SDK del visualizador. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visualizador y presentar contenido al usuario rápidamente.

La imagen de precarga funciona bien para el método de incrustación de visor más común, que es la incrustación adaptable con altura sin restricciones. Consulte el encabezado [Inserción de diseño interactivo con altura sin restricciones](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Sin embargo, la función tiene ciertas limitaciones cuando se utilizan otros métodos de incrustación u opciones de configuración específicas. La imagen de precarga puede no procesarse correctamente en los siguientes casos:

* Cuando el tamaño del visor es fijo y el tamaño se define mediante `stagesize` atributo de configuración dentro del registro de ajustes preestablecidos de visor. O bien, utilizando el archivo CSS del visor externo para el elemento contenedor del visor de nivel superior.
* Al utilizar la incrustación de tamaño flexible con el método definido de anchura y altura de incrustación del visualizador. Consulte el encabezado [Incrustación de tamaño flexible con anchura y altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Deshabilite la función de imagen de precarga con `preloadImage` atributo de configuración si utiliza el visor en uno de los modos de operación enumerados anteriormente.

Además, la imagen de precarga no se utiliza (incluso si está activada en la configuración) si el visor está incrustado en el elemento DOM y está oculto mediante `display:none` Configuración de CSS o independiente del árbol DOM.
