---
description: El visor de carrusel es un visor que muestra un carrusel de imágenes de letreros no ampliables con zonas interactivas o regiones en las que se puede hacer clic. El objetivo de este visor es implementar una experiencia de "carrusel de ventas" en la que los usuarios pueden seleccionar un punto interactivo o una región sobre la imagen del letrero y ser redirigidos a una vista rápida o a una página de detalles del producto en el sitio web del cliente. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
seo-description: El visor de carrusel es un visor que muestra un carrusel de imágenes de letreros no ampliables con zonas interactivas o regiones en las que se puede hacer clic. El objetivo de este visor es implementar una experiencia de "carrusel de ventas" en la que los usuarios pueden seleccionar un punto interactivo o una región sobre la imagen del letrero y ser redirigidos a una vista rápida o a una página de detalles del producto en el sitio web del cliente. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
seo-title: Carrusel
solution: Experience Manager
title: Carrusel
topic: Dynamic media
uuid: 0ba4f40b-8dde-4479-b906-3115f09ab249
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1978'
ht-degree: 0%

---


# Carrusel{#carousel}

El visor de carrusel es un visor que muestra un carrusel de imágenes de letreros no ampliables con zonas interactivas o regiones en las que se puede hacer clic. El objetivo de este visor es implementar una experiencia de &quot;carrusel de ventas&quot; en la que los usuarios pueden seleccionar un punto interactivo o una región sobre la imagen del letrero y ser redirigidos a una vista rápida o a una página de detalles del producto en el sitio web del cliente. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan Representación de imágenes o Contenido generado por el usuario (UGC).

El tipo de visor es 511.

## Dirección URL de demostración {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html)

## Requisitos del sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso del visor de carrusel {#section-e6c68406ecdc4de781df182bbd8088b4}

El visor de carrusel representa un archivo JavaScript principal y un conjunto de archivos auxiliares (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visor, recursos y CSS concretos) descargados por el visor en tiempo de ejecución.

El visor de carrusel se puede utilizar tanto en el modo emergente mediante una página HTML preparada para la producción proporcionada con los visores IS como en el modo incrustado, donde se integra en la página web de destinatario mediante API documentada.

La configuración y la aplicación de aspectos son similares a las de los demás visores descritos en esta Ayuda. Todos los aspectos se logran mediante CSS personalizada.

Consulte [Referencia de comandos común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comandos común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de carrusel {#section-642e66ca38cd4032992840ec6c0b0cd2}

La navegación por el conjunto de carrusel se realiza con un barrido horizontal sobre la vista principal o con dos botones de flecha disponibles en el dispositivo de escritorio. Los puntos del indicador de conjunto muestran la posición actual dentro del conjunto.

El visor puede representar zonas interactivas o regiones en la parte superior de la imagen del letrero para indicar el área interactiva del producto.

Al tocar o hacer clic en una zona interactiva o una región, se activa una acción asociada a ella durante el tiempo de creación. La acción puede redirigirse a otra página del sitio web o puede devolver la información del producto a la lógica de la página web, lo que a su vez puede activar una vista rápida con el contenido del producto relacionado.

El visor es totalmente accesible mediante el teclado.

Consulte [Navegación y accesibilidad del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor de carrusel {#section-6bb5d3c502544ad18a58eafe12a13435}

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o ficha separada del explorador Web. Toma todo el área de la ventana del navegador y se ajusta en caso de que se cambie el tamaño del navegador o la orientación del dispositivo móvil.

El modo emergente es el más común para dispositivos móviles. La página web carga el visor mediante `window.open()` llamada de JavaScript, elemento HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página HTML lista para usar en el modo de operación emergente. En este caso, se denomina `CarouselViewer.html` y se encuentra dentro de la subcarpeta `html5/` de la implementación estándar de los visores de IS:

`<s7viewers_root>/html5/CarouselViewer.html`

Puede lograr la personalización visual mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código HTML que abre el visor en una ventana nueva:

```
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo incrustado, el visor se agrega a la página web existente. Es posible que esta página web ya tenga contenido para clientes no relacionado con el visor. Normalmente, el visor ocupa solo una parte del espacio de una página web.

Los casos de uso principales son las páginas web orientadas a equipos de escritorio o tabletas, y las páginas diseñadas con capacidad de respuesta que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta es la mejor opción para las páginas web con un diseño estático.

La incrustación de diseño adaptable supone que el visor puede necesitar cambiar el tamaño en tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, dejando su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso utilizado. Esta funcionalidad garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para las páginas Web que utilizan marcos de diseño de Web interactivos como Bootstrap, Foundation, etc.

De lo contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellenará solo esa área. También sigue el tamaño que proporciona el diseño de la página web. Un buen ejemplo es la incrustación del visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del navegador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor en la página web.

   La creación de un visor requiere que agregue una etiqueta de script en el encabezado HTML. Antes de usar la API de visor, asegúrese de incluir [!DNL CarouselViewer.js]. El archivo [!DNL CarouselViewer.js] se encuentra en la subcarpeta [!DNL html5/js/] de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se suministra desde el mismo dominio. En caso contrario, especifique una ruta completa a uno de los servidores Adobe Dynamic Media Classic que tenga instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>Solo debe hacer referencia al archivo JavaScript `include` del visor principal de la página. No debe hacer referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargarse mediante la lógica del visor en tiempo de ejecución. En particular, no haga referencia directa a la biblioteca `Utils.js` del SDK de HTML5 cargada por el visor desde la ruta de contexto `/s7viewers` (denominada SDK consolidado `include`). El motivo es que la ubicación de `Utils.js` o bibliotecas de visores de tiempo de ejecución similares se administra completamente mediante la lógica del visor y la ubicación cambia entre las versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, la colocación de una referencia directa a cualquier JavaScript `include` secundario utilizado por el visor en la página interrumpe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del contenedor `DIV`.

   Añada un elemento vacío `DIV` en la página donde desee que aparezca el visor. El elemento `DIV` debe tener su ID definido porque este ID se pasa más tarde a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El marcador de posición `DIV` es un elemento posicionado, lo que significa que la propiedad CSS `position` se establece en `relative` o `absolute`.

   A continuación se muestra un ejemplo de un elemento de marcador de posición definido `DIV`:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para la clase CSS de nivel superior `.s7carouselviewer` en unidades absolutas o utilizando el modificador `stagesize`.

   Puede colocar el tamaño en CSS directamente en la página HTML o en un archivo CSS de visor personalizado, que posteriormente se asignará a un registro de ajuste preestablecido de visor en AEM Assets (On-demand) o se pasará explícitamente mediante el comando `style`.

   Consulte [Personalización del visor de carrusel](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en la página HTML:

   ```
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Puede pasar explícitamente el modificador `stagesize` con el código de inicialización del visor con la colección `params` o como una llamada de API como se describe en la sección Referencia de comandos, de este modo:

   ```
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   En este ejemplo se recomienda un enfoque basado en CSS.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.CarouselViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener un campo `containerId` que contenga el nombre del ID de contenedor del visor y un objeto `params` JSON anidado con parámetros de configuración admitidos por el visor. En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON permite crear y inicio del visor con una sola línea de código.

   Es importante que el contenedor del visor se añada al DOM para que el código del visor pueda encontrar el elemento de contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta `BODY` de cierre o en el evento body `onload()`.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web. Por ejemplo, puede ocultarse con el estilo `display:none` asignado. En este caso, el visor retrasa el proceso de inicialización hasta el momento en que la página web devuelve el elemento de contenedor a la presentación. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de creación de una instancia de visor, pasando al constructor las opciones de configuración mínimas necesarias y llamando al método `init()`. El ejemplo asume que `carouselViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; `https://adobedemo62-h.assetsadobe.com/is/image` es la dirección URL del servicio de imágenes y `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` es el recurso:

   ```
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incorpora el visor de carrusel con un tamaño fijo:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incrustación de diseño adaptable con altura ilimitada**

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que determina el tamaño de tiempo de ejecución del contenedor `DIV` del visor. En el siguiente ejemplo, supongamos que la página web permite que el contenedor del visor `DIV` ocupe el 40 % del tamaño de la ventana del explorador web. Y su altura no está restringida. El código HTML de la página web tendría el siguiente aspecto:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Añadir el visor a una página de este tipo es similar a los pasos para la incrustación de tamaño fijo. La única diferencia es que no es necesario definir explícitamente el tamaño del visor.

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición del contenedor `DIV`.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Añada el contenedor `DIV` al `"holder"` `DIV` existente. El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del navegador y cómo coincide la proporción de aspecto del visor con el recurso.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La siguiente página de ejemplos ilustra los usos más reales del diseño interactivo que se incrusta con altura ilimitada:

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html)

**Incrustación de tamaño flexible con anchura y altura definidas**

En caso de incrustación de tamaño flexible con anchura y altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños a la DIV `"holder"` y la centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en 100 por ciento.

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

El resto de los pasos de incrustación son idénticos a los pasos utilizados para la incrustación interactiva con altura no restringida. El ejemplo resultante es el siguiente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incrustación mediante API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en setter y el constructor no-args. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante métodos de API `setContainerId()`, `setParam()` y `setAsset()` con llamadas JavaScript independientes.

El siguiente ejemplo ilustra el uso de la incrustación de tamaño fijo con la API basada en establecedor:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```

