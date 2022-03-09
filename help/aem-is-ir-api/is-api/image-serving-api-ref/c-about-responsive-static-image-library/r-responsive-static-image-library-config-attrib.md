---
description: Los atributos de configuración se definen como atributos directamente en un elemento IMG que administra la biblioteca de imágenes adaptables. Cada imagen puede tener su propio conjunto de atributos.
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 1%

---

# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Los atributos de configuración se definen como atributos directamente en un elemento IMG que administra la biblioteca de imágenes adaptables. Cada imagen puede tener su propio conjunto de atributos.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Opcional.

Dirección URL de la imagen que sirve Image Serving. Si la dirección URL no está presente, la biblioteca utiliza el valor establecido en `src` como visita en el orden previsto. Este atributo sirve para la imagen inicial y la imagen dinámica que administra la biblioteca de imágenes adaptables desde diferentes ubicaciones.

**Ejemplo**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

If `data-src` está configurado, `src` es opcional y puede contener cualquier dirección URL que desee añadir. Por ejemplo, puede contener una dirección URL a la misma imagen basada en el servicio de imágenes que utiliza la biblioteca. O bien, puede contener un marcador de posición de GIF o incluso un URI de datos para evitar un viaje de ida y vuelta al servidor adicional al inicio.

If `data-src` no está configurado, `src` es obligatorio y debe contener una dirección URL a la imagen que sirve Image Serving.

**Ejemplo**

Uso del URI de datos para la variable `src` y URL del servicio de imágenes para la variable `data-src` atributo:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## puntos de interrupción de datos {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Una lista de puntos de interrupción separados por coma y, opcionalmente, seguidos de dos puntos ( `:`) y comandos de servicio de imágenes o ajustes preestablecidos de imagen. Cada punto de interrupción es un valor de anchura de imagen definido en píxeles CSS lógicos. La biblioteca carga la imagen con el valor más grande de la lista y la escala en el cliente para que coincida con el ancho de la imagen CSS en tiempo de ejecución. (Si trabaja en una pantalla de alta densidad, las representaciones de imágenes cargadas desde el servidor representan valores de punto de interrupción multiplicados por la proporción de píxeles del dispositivo).

Para cualquier punto de interrupción de la lista, es posible definir uno o varios comandos de servicio de imágenes o nombres de ajustes preestablecidos de imagen. Estos parámetros adicionales solo se aplican a la imagen en caso de que este punto de interrupción en particular esté activo actualmente.

Puede utilizar cualquier comando admitido de Image Serving, excepto aquellos comandos de vista que afecten al tamaño de la imagen de respuesta, como `wid=`, `hei=`o `scl=`. La misma restricción se aplica a los ajustes preestablecidos de imagen: un ajuste preestablecido de imagen utilizado con la biblioteca de imágenes interactiva no debe contener estos comandos.

Los comandos de servicio de imágenes múltiple o los nombres de ajustes preestablecidos de imagen se separan con &quot; `&`&quot;. Si un comando de servicio de imágenes tiene una coma en su valor, dicha coma se sustituye por `%2C`. Los nombres de los ajustes preestablecidos de imagen se envuelven en signos de dólar ( `$`).

**Ejemplos**

**Usar solo puntos de interrupción**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Uso de comandos de Image Serving**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Uso de ajustes preestablecidos de imagen**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Uso de ajustes preestablecidos de imagen y comandos de servicio de imágenes**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Los dos modos de recorte inteligente siguientes están disponibles en AEM 6.4 y superiores y en los visores de Dynamic Media 5.9 y superiores:

* **Manual** - los puntos de interrupción definidos por el usuario y los comandos correspondientes del servicio de imágenes se definen dentro de un atributo en el elemento de imagen.
* **Recorte inteligente** - las representaciones de recorte inteligente calculadas se recuperan automáticamente del servidor de entrega. La mejor representación se selecciona utilizando el tamaño de tiempo de ejecución del elemento de imagen.

Para utilizar el modo de recorte inteligente, se establece la variable `data-mode` atributo a `smart crop`.

**Ejemplo**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

El elemento de imagen asociado distribuye un `s7responsiveViewer` durante el tiempo de ejecución cuando cambie el punto de interrupción.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
