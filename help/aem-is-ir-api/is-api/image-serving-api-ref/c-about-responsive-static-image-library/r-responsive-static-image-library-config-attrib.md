---
description: Los atributos de configuración se definen como atributos directamente en un elemento IMG que administra la biblioteca de imágenes interactivas. Cada imagen puede tener su propio conjunto de atributos.
solution: Experience Manager
title: 'Referencia de comando: atributos de configuración'
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 1%

---

# Referencia de comando: atributos de configuración{#command-reference-configuration-attributes}

Los atributos de configuración se definen como atributos directamente en un elemento IMG que administra la biblioteca de imágenes interactivas. Cada imagen puede tener su propio conjunto de atributos.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Opcional.

URL de la imagen que sirve el servicio de imágenes. Si la dirección URL no está presente, la biblioteca utiliza el valor establecido en `src` como alternativa. Este atributo sirve para la imagen inicial y la imagen dinámica que la biblioteca de imágenes interactivas administra desde diferentes ubicaciones.

**Ejemplo**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

If `data-src` está configurado, `src` es opcional y puede contener cualquier dirección URL que desee agregar. Por ejemplo, puede contener una URL a la misma imagen basada en el servicio de imágenes que utiliza la biblioteca. O bien, puede contener un marcador de posición de GIF o incluso un URI de datos para evitar un viaje de ida y vuelta al servidor adicional durante el inicio.

If `data-src` no se ha establecido, `src` es obligatorio y debe contener una URL a la imagen que suministra el servicio de imágenes.

**Ejemplo**

Uso del URI de datos para `src` y URL del servicio de imágenes para `data-src` atributo:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Lista de puntos de interrupción separados por comas y, opcionalmente, seguidos de dos puntos ( `:`) y los comandos del servicio de imágenes o ajustes preestablecidos de imagen. Cada punto de interrupción es un valor de anchura de imagen definido en píxeles CSS lógicos. La biblioteca carga la imagen con el valor más grande más cercano de la lista y la reduce en el cliente para que coincida con el ancho de la imagen CSS en tiempo de ejecución. (Si trabaja en una pantalla de alta densidad, las representaciones de imágenes cargadas desde el servidor representan valores de punto de interrupción multiplicados por la proporción de píxeles del dispositivo).

Para cualquier punto de interrupción de la lista, es posible definir uno o más comandos del servicio de imágenes o nombres de ajustes preestablecidos de imagen. Estos parámetros adicionales solo se aplican a la imagen en caso de que este punto de interrupción en particular esté activo actualmente.

Puede utilizar cualquier comando del servicio de imágenes admitido, excepto los comandos de vista que afectan al tamaño de la imagen de respuesta, como `wid=`, `hei=`, o `scl=`. La misma restricción se aplica a los ajustes preestablecidos de imagen: un ajuste preestablecido de imagen utilizado con la biblioteca de imágenes adaptables no debe contener estos comandos.

Los comandos del servicio de imágenes múltiples o los nombres de ajustes preestablecidos de imagen se separan con &quot; `&`Carácter &quot;. Si un comando del servicio de imágenes tiene una coma en su valor, dicha coma se reemplaza por `%2C`. Los nombres de ajustes preestablecidos de imagen están envueltos en símbolos de dólar ( `$`).

**Ejemplos**

**Usar solo puntos de interrupción**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Uso de comandos del servicio de imágenes**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Uso de ajustes preestablecidos de imagen**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Uso de ajustes preestablecidos de imagen y comandos de servicio de imágenes**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM Los dos modos de recorte inteligente siguientes están disponibles en la versión 6.4 y posteriores de la y en los visores de Dynamic Media 5.9 y posteriores:

* **Manual** : los puntos de interrupción definidos por el usuario y los comandos del servicio de imágenes correspondientes se definen dentro de un atributo en el elemento de imagen.
* **Recorte inteligente** : las representaciones de recortes inteligentes calculadas se recuperan automáticamente del servidor de entrega. La mejor representación se selecciona utilizando el tamaño de tiempo de ejecución del elemento de imagen.

Para utilizar el modo de recorte inteligente, configure las `data-mode` atribuir a `smart crop`.

**Ejemplo**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

El elemento de imagen asociado distribuye un `s7responsiveViewer` durante el tiempo de ejecución cuando cambia el punto de interrupción.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
