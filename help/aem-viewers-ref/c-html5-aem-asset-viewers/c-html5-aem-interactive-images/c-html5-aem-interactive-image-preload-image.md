---
title: Precargar imagen
description: La imagen de precarga es una imagen de previsualización de recurso estático que se carga justo después de llamar al método init() y se muestra mientras se descargan las bibliotecas, los recursos y la información de ajustes preestablecidos de Viewer SDK. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visualizador y presentar contenido al usuario rápidamente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
TQID: 'https://experienceleague.adobe.com/GlTbkyDeUNGf4gjmEEGbh1NaQ-nOgPZLtrz9kH4eK7o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 0%

---

# Precargar imagen{#preload-image}

La imagen de precarga es una imagen de previsualización de recurso estático que se carga justo después de llamar al método init() y se muestra mientras se descargan las bibliotecas, los recursos y la información de ajustes preestablecidos de Viewer SDK. El propósito de la imagen de precarga es mejorar visualmente el tiempo de carga del visualizador y presentar contenido al usuario rápidamente.

La imagen de precarga funciona bien para el método de incrustación de visor más común, que es la incrustación adaptable con altura sin restricciones. Ver el encabezado [Diseño interactivo incrustado con altura sin restricciones](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Sin embargo, la función tiene ciertas limitaciones cuando se utilizan otros métodos de incrustación u opciones de configuración específicas. La imagen de precarga puede no procesarse correctamente en los siguientes casos:

* Cuando el visor tiene un tamaño fijo y el tamaño se define mediante el atributo de configuración `stagesize` dentro del registro de ajustes preestablecidos del visor. O bien, utilizando el archivo CSS del visor externo para el elemento contenedor del visor de nivel superior.
* Al utilizar la incrustación de tamaño flexible con el método definido de anchura y altura de incrustación del visualizador. Ver el encabezado [Tamaño flexible incrustado con la anchura y la altura definidas](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Deshabilite la característica de imagen de precarga con el atributo de configuración `preloadImage` si utiliza el visor en uno de los modos de operación enumerados arriba.

Además, la imagen de precarga no se utiliza (aunque esté habilitada en la configuración) si el visor está incrustado en el elemento DOM, está oculto mediante la configuración CSS `display:none` o se ha separado del árbol DOM.
