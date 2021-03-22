---
description: Los atributos de configuración se definen como atributos directamente en un elemento IMG que administra la biblioteca de imágenes adaptables. Cada imagen puede tener su propio conjunto de atributos.
seo-description: Los atributos de configuración se definen como atributos directamente en un elemento IMG que administra la biblioteca de imágenes adaptables. Cada imagen puede tener su propio conjunto de atributos.
seo-title: 'Referencia de comandos: Atributos de configuración'
solution: Experience Manager
title: 'Referencia de comandos: Atributos de configuración'
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---


# Referencia de comandos: Atributos de configuración{#command-reference-configuration-attributes}

Los atributos de configuración se definen como atributos directamente en un elemento IMG que administra la biblioteca de imágenes adaptables. Cada imagen puede tener su propio conjunto de atributos.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Opcional.

Dirección URL de la imagen que sirve Image Serving. Si la dirección URL no está presente, la biblioteca utiliza el valor establecido en el atributo `src` como alternativa. Este atributo sirve para la imagen inicial y la imagen dinámica que administra la biblioteca de imágenes adaptables desde diferentes ubicaciones.

**Ejemplo**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Si `data-src` está establecido, `src` es opcional y puede contener cualquier dirección URL que desee agregar. Por ejemplo, puede contener una dirección URL a la misma imagen basada en el servicio de imágenes que utiliza la biblioteca. O bien, puede contener un marcador de posición GIF o incluso un URI de datos para evitar un viaje de ida y vuelta al servidor adicional al inicio.

Si `data-src` no está establecido, `src` es obligatorio y debe contener una dirección URL a la imagen que proporciona el servicio de imágenes.

**Ejemplo**

Uso del URI de datos para el atributo `src` y la URL del servicio de imágenes para el atributo `data-src`:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## puntos de interrupción de datos {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Lista de puntos de interrupción separados por coma y, opcionalmente, seguidos de dos puntos ( `:`) y comandos de servicio de imágenes o ajustes preestablecidos de imagen. Cada punto de interrupción es un valor de anchura de imagen definido en píxeles CSS lógicos. La biblioteca carga la imagen con el valor más grande de la lista y la escala en el cliente para que coincida con el ancho de la imagen CSS en tiempo de ejecución. (Si trabaja en una pantalla de alta densidad, las representaciones de imágenes cargadas desde el servidor representan valores de punto de interrupción multiplicados por la proporción de píxeles del dispositivo).

Para cualquier punto de interrupción de la lista, es posible definir uno o varios comandos de servicio de imágenes o nombres de ajustes preestablecidos de imagen. Estos parámetros adicionales solo se aplican a la imagen en caso de que este punto de interrupción en particular esté activo actualmente.

Puede utilizar cualquier comando de servicio de imágenes admitido, excepto los comandos de vista que afecten al tamaño de la imagen de respuesta, como `wid=`, `hei=` o `scl=`. La misma restricción se aplica a los ajustes preestablecidos de imagen: un ajuste preestablecido de imagen utilizado con la biblioteca de imágenes interactiva no debe contener estos comandos.

Los comandos de servicio de imágenes múltiple o los nombres de ajustes preestablecidos de imagen se separan con el carácter &quot; `&`&quot;. Si un comando de servicio de imágenes tiene una coma en su valor, dicha coma se sustituye por `%2C`. Los nombres de ajustes preestablecidos de imagen se envuelven en signos de dólar ( `$`).

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

* **Manual** : los puntos de interrupción definidos por el usuario y los comandos correspondientes del servicio de imágenes se definen dentro de un atributo en el elemento de imagen.
* **Recorte inteligente** : las representaciones de recorte inteligente calculadas se recuperan automáticamente del servidor de entrega. La mejor representación se selecciona utilizando el tamaño de tiempo de ejecución del elemento de imagen.

Para utilizar el modo de recorte inteligente, establezca el atributo `data-mode` en `smart crop`.

**Ejemplo**

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

El elemento de imagen asociado distribuye un evento `s7responsiveViewer` durante el tiempo de ejecución cuando cambia el punto de interrupción.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```

