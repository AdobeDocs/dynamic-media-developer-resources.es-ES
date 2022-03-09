---
title: Uso de la biblioteca de imágenes adaptables
description: Para agregar una biblioteca de imágenes adaptables a una página web y administrar las imágenes existentes con la biblioteca, complete los siguientes pasos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Uso de la biblioteca de imágenes adaptables{#using-responsive-image-library}

Para agregar una biblioteca de imágenes adaptables a una página web y administrar las imágenes existentes con la biblioteca, complete los siguientes pasos.

**Para usar la biblioteca de imágenes adaptables**

1. En Dynamic Media Classic, [crear un ajuste preestablecido de imagen](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) en caso de que planee utilizar la biblioteca de imágenes adaptables con ajustes preestablecidos.

   Cuando defina los ajustes preestablecidos de imagen que se utilizan con la biblioteca de imágenes interactiva, no utilice ninguna configuración que afecte al tamaño de la imagen, como `wid=`, `hei=`o `scl=`. No especifique ningún campo de tamaño en el ajuste preestablecido de imagen. En su lugar, déjelos como valores en blanco.
1. Agregue el archivo JavaScript de la biblioteca a la página web.

   Antes de usar la API de biblioteca, asegúrese de incluir `responsive_image.js`. Este archivo JavaScript se encuentra en la sección `libs/` subcarpeta de la implementación estándar de IS-Viewers:

   `<s7viewers_root>/libs/responsive_image.js`
1. Configure las imágenes existentes.

   La biblioteca lee ciertos atributos de configuración de una instancia de imagen con la que está trabajando. Defina los atributos antes de la variable `s7responsiveImage` La función API se llama para esta imagen.

   También se sugiere que coloque la URL de imagen existente en la variable `data-src` atributo. A continuación, configure el `src` para tener una imagen de GIF 1x1 codificada como URI de datos. De este modo, se reduce el número de solicitudes HTTP que envía la página web en el momento de la carga. Sin embargo, tenga en cuenta que si se necesita SEO (optimización de los motores de búsqueda), es mejor configurar un `title` en la instancia de imagen.

   A continuación se muestra un ejemplo de definición de `data-breakpoints` para la imagen y con un GIF de 1x1 codificado como URI de datos:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Llame a la función `s7responsiveImage` función API para cada instancia de imagen que administra la biblioteca.

   Llame a la función `s7responsiveImage` función API para cada instancia de imagen que administra la biblioteca. Después de una llamada de este tipo, la biblioteca sustituye la imagen original por la imagen descargada de Image Serving según el tamaño de tiempo de ejecución del `IMG` en el diseño de página web y la densidad de la pantalla del dispositivo.

   El siguiente código es un ejemplo de llamada a `s7responsiveImage` función de API en una imagen, suponiendo que `responsiveImage` es un ID de esa imagen:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Ejemplo {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La biblioteca admite el trabajo simultáneo con muchas instancias de imagen en la página web. Por lo tanto, repita los pasos 1 y 2 anteriores para cada imagen que desee que administre la biblioteca.

Es responsabilidad de la página web aplicar estilo al elemento de imagen para que sea flexible en tamaño. La propia biblioteca de imágenes interactivas no diferencia entre imágenes de tamaño fijo y &quot;fluidas&quot;. Si se aplica a una imagen de tamaño fijo, carga la nueva imagen solo una vez.

El siguiente código es un ejemplo completo de una página web trivial que tiene una sola imagen fluida administrada por la biblioteca de imágenes interactivas. El ejemplo contiene estilo CSS adicional para que la imagen &quot;responda&quot; al tamaño de la ventana del explorador web:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**Uso del recorte inteligente**

Hay dos modos de recorte inteligente disponibles en AEM 6.4 y en visores Dynamic Media 5.9:

* **Manual** - los puntos de interrupción definidos por el usuario y los comandos correspondientes del servicio de imágenes se definen dentro de un atributo en el elemento de imagen.
* **Recorte inteligente** - las representaciones de recorte inteligente calculadas se recuperan automáticamente del servidor de entrega. La mejor representación se selecciona utilizando el tamaño de tiempo de ejecución del elemento de imagen.

Para utilizar el modo de recorte inteligente, se establece la variable `data-mode` atributo a `smart crop`. Por ejemplo:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

El elemento de imagen asociado distribuye un `s7responsiveViewer` durante el tiempo de ejecución cuando cambie el punto de interrupción.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
