---
description: Para agregar una biblioteca de imágenes interactivas a una página web y administrar las imágenes existentes con la biblioteca, complete los siguientes pasos.
solution: Experience Manager
title: Uso de la biblioteca de imágenes interactivas
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 0%

---


# Uso de la biblioteca de imágenes interactivas{#using-responsive-image-library}

Para agregar una biblioteca de imágenes interactivas a una página web y administrar las imágenes existentes con la biblioteca, complete los siguientes pasos.

**Para utilizar la biblioteca de imágenes interactivas**

1. En SPS, [cree un ajuste preestablecido de imagen](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) en caso de que desee utilizar la biblioteca de imágenes interactivas con ajustes preestablecidos.

   Al definir los ajustes preestablecidos de imagen que se utilizan con la biblioteca de imágenes interactivas, no utilice ninguna configuración que afecte al tamaño de la imagen, como `wid=`, `hei=` o `scl=`. No especifique ningún campo de tamaño en el ajuste preestablecido de imagen. En su lugar, déjelos como valores en blanco.
1. Añada el archivo JavaScript de la biblioteca en la página web.

   Antes de usar la API de biblioteca, asegúrese de incluir `responsive_image.js`. Este archivo JavaScript se encuentra en la subcarpeta `libs/` de la implementación estándar de los visores de IS:

   `<s7viewers_root>/libs/responsive_image.js`
1. Configure las imágenes existentes.

   La biblioteca lee determinados atributos de configuración de una instancia de imagen con la que está trabajando. Defina los atributos antes de que se llame a la función de API `s7responsiveImage` para dicha imagen.

   También se recomienda colocar la dirección URL de imagen existente en el atributo `data-src`. A continuación, configure el atributo `src` existente para que tenga una imagen GIF de 1x1 codificada como URI de datos. Al hacerlo, se reduce el número de solicitudes HTTP que envía la página web en el momento de la carga. Sin embargo, tenga en cuenta que si se necesita SEO (optimización del motor de búsqueda), es mejor configurar un atributo `title` en la instancia de imagen.

   A continuación se muestra un ejemplo de definición del atributo `data-breakpoints` para la imagen y uso de un GIF de 1x1 codificado como URI de datos:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Llame a la función de API `s7responsiveImage` para cada instancia de imagen que administra la biblioteca.

   Llame a la función de API `s7responsiveImage` para cada instancia de imagen que administra la biblioteca. Después de esta llamada, la biblioteca reemplaza la imagen original por la imagen que se descarga del servicio de imágenes según el tamaño de tiempo de ejecución del elemento `IMG` en el diseño de la página web y la densidad de la pantalla del dispositivo.

   El siguiente código es un ejemplo de llamada a la función de API `s7responsiveImage` en una imagen, suponiendo que `responsiveImage` es un ID de esa imagen:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Ejemplo {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La biblioteca admite el trabajo simultáneo con muchas instancias de imagen en la página web. Por lo tanto, repita los pasos 1 y 2 anteriores para cada imagen que desee que administre la biblioteca.

Es responsabilidad de la página web aplicar estilo al elemento de imagen para que sea flexible en tamaño. La propia biblioteca de imágenes interactivas no diferencia entre imágenes de tamaño fijo y imágenes &quot;fluidas&quot;. Si se aplica a una imagen de tamaño fijo, carga la nueva imagen solo una vez.

El siguiente código es un ejemplo completo de una página web trivial que tiene una sola imagen fluida administrada por la biblioteca de imágenes interactivas. El ejemplo contiene estilos CSS adicionales para que la imagen sea &quot;adaptable&quot; al tamaño de la ventana del navegador web:

```
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

**Uso de recorte inteligente**

Hay dos modos de recorte inteligente disponibles en AEM 6.4 y Dynamic Media Viewer 5.9:

* **Los puntos de interrupción manuales**  definidos por el usuario y los comandos correspondientes del servicio de imágenes se definen dentro de un atributo del elemento de imagen.
* **Recorte**  inteligente: las representaciones de recorte inteligente calculadas se recuperan automáticamente desde el servidor de envío. La mejor representación se selecciona con el tamaño de tiempo de ejecución del elemento de imagen.

Para utilizar el modo de recorte inteligente, establezca el atributo `data-mode` en `smart crop`. Por ejemplo:

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
