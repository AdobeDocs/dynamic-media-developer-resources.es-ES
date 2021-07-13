---
description: El visor de zoom en línea es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra sobre esa imagen estática cuando un usuario pasa por encima o toca la vista principal. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.
keywords: adaptable
solution: Experience Manager
title: Zoom en línea
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom en línea
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2404'
ht-degree: 0%

---

# Zoom en línea{#inline-zoom}

El visor de zoom en línea es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra sobre esa imagen estática cuando un usuario pasa por encima o toca la vista principal. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

El tipo de visor es 504.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Dirección URL de la demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## Uso del visor de zoom en línea {#section-f21ac23d3f6449ad9765588d69584772}

El visor de zoom en línea representa un archivo JavaScript principal y un conjunto de archivos de ayuda (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visor en particular, recursos y CSS) descargados por el visor durante la ejecución.

El visor de zoom en línea se puede utilizar tanto en el modo emergente mediante la página HTML lista para la producción proporcionada con los visualizadores de servicio de imágenes como en el modo incrustado, en el que se integra en una página web de destino mediante API documentada.

La configuración y el desollado son similares a los de los demás visores. Puede utilizar CSS personalizada para aplicar la aplicación de aspectos.

Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visualizadores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de zoom en línea {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visor de zoom en línea es compatible con gestos de un solo toque y de varios toque comunes en otras aplicaciones móviles.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Un solo toque </p> </td> 
   <td colname="col2"> <p> Activa la vista flotante o cambia entre el nivel de zoom primario y el secundario en muestras, selecciona nueva miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido horizontal o deslizamiento </p> </td> 
   <td colname="col2"> <p> Se desplaza por la lista de muestras de la barra de muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical </p> </td> 
   <td colname="col2"> <p>Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor también admite entrada táctil y entrada de ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad está limitada únicamente a los navegadores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante teclado.

Consulte [Accesibilidad del teclado y navegación](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor de zoom en línea {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo en el que se puede hacer clic que abre el visor en una ventana independiente del explorador. En otros casos, puede ser necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en distintos dispositivos o en diferentes tamaños de ventana del navegador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: elemento emergente, incrustación de tamaño fijo e incrustación interactiva.

**Ventana emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Toma todo el área de la ventana del explorador y se ajusta cuando se cambia el tamaño de la ventana del explorador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante `window.open()` llamada de JavaScript, un elemento HTML `A` configurado correctamente o de cualquier otra forma adecuada.

Se recomienda utilizar la página HTML predeterminada para el modo emergente denominado `FlyoutViewer.html`. Se encuentra en la subcarpeta [!DNL html5/] de la implementación estándar de Image Serving-Viewers:

`<s7viewers_root>/html5/FlyoutViewer.html`

También es necesario tener configurado el componente FlyoutZoomView para que funcione en el modo de zoom en línea. Se recomienda utilizar el ajuste preestablecido `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` predeterminado para el visor de zoom en línea o un ajuste preestablecido personalizado derivado de él. La personalización visual se puede lograr aplicando CSS personalizada.

El siguiente es un ejemplo de código HTML que abre el visor en una nueva ventana:

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Incrustación de tamaño fijo e Incrustación interactiva**

En el modo integrado, el visor se añade a la página web existente, que puede tener ya algún contenido de cliente no relacionado con el visor. Normalmente, el visor solo ocupa una parte del espacio de la página web.

El caso de uso principal son páginas web orientadas a equipos de escritorio o tabletas, así como páginas web adaptables que ajustan el diseño automáticamente en función del tipo de dispositivo.

Se utiliza el modo de incrustación de tamaño fijo cuando el visor no cambia su tamaño después de su carga inicial. Esta opción es mejor para las páginas web que tienen un diseño de página estático.

El modo de incrustación de diseño interactivo supone que el visor puede tener que cambiar el tamaño durante el tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

Cuando utilice el modo de incrustación de diseño interactivo con el visor de zoom en línea, asegúrese de especificar puntos de interrupción explícitos para la imagen de vista principal mediante el parámetro `imagereload`. Lo ideal es que sus puntos de interrupción coincidan con los puntos de interrupción de anchura del visor tal y como dicta el CSS de la página web.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño que tenga una página web en su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, sin restringir su altura, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utiliza. Esto significa que el recurso encaja perfectamente en la vista sin ningún relleno en los lados. Este caso de uso en particular es el más común para las páginas web que usan marcos de diseño interactivos como Bootstrap, Foundation, etc.

De lo contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellenará solo esa área y seguirá el tamaño proporcionado por el diseño de la página web. Un buen ejemplo de uso es integrar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Integración de tamaño fijo**

Para añadir el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   Para crear un visor es necesario agregar una etiqueta de script en el encabezado HTML. Antes de utilizar la API del visor, asegúrese de incluir `FlyoutViewer.js`. `FlyoutViewer.js` se encuentra en la siguiente  [!DNL html5/js/] subcarpeta de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores Dynamic Media de Adobe y se suministra desde el mismo dominio. De lo contrario, se especifica una ruta completa a uno de los servidores Dynamic Media de Adobe que tienen instalados los visores IS.

Una ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Solo debe hacer referencia al archivo JavaScript `include` del visor principal de la página. No debe hacer referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargar la lógica del visor durante la ejecución. En concreto, no haga referencia directamente a la biblioteca `Utils.js` del SDK de HTML5 cargada por el visor desde la ruta de contexto `/s7viewers` (denominada SDK consolidado `include`). El motivo es que la ubicación de las `Utils.js` o bibliotecas de visores de tiempo de ejecución similares se administra completamente mediante la lógica del visor y la ubicación cambia entre las versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, poner una referencia directa a cualquier JavaScript `include` secundario que utilice el visor en la página rompe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del contenedor DIV.

   Agregue un elemento DIV vacío a la página donde desee que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa más adelante a la API del visor.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la propiedad `position` CSS está establecida en `relative` o `absolute`.

   Es responsabilidad de la página web especificar el `z-index` apropiado para el elemento DIV del marcador de posición. De este modo, se garantiza que la parte flotante del visualizador aparezca encima de los demás elementos de la página web.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Configuración del tamaño del visor.

   Este visor muestra miniaturas al trabajar con conjuntos de varios elementos. En los sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal durante el tiempo de ejecución mediante la API `setAsset()`. Como desarrollador, tiene control sobre cómo administra el visor el área de miniaturas del área inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener estático el tamaño de la vista principal y contraer el área del visor exterior, lo que permite que el contenido de la página web se mueva hacia arriba y, a continuación, utilizar el espacio inmobiliario de la página libre que queda en las miniaturas.

   Para mantener intactos los límites exteriores del visor, defina el tamaño de la clase CSS de nivel superior `.s7flyoutviewer` en unidades absolutas. El tamaño en CSS se puede colocar directamente en la página HTML o en un archivo CSS de visor personalizado, que más tarde se asigna a un registro preestablecido de visor en Dynamic Media Classic, o se pasa explícitamente mediante el comando Estilo.

   Consulte [Personalización del visor de zoom en línea](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) para obtener más información sobre cómo diseñar el visor con CSS.

   A continuación se muestra un ejemplo de definición del tamaño estático del visor exterior en una página HTML:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un área fija del visor exterior en la siguiente página de muestra. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   Para que las dimensiones de vista principales sean estáticas, defina el tamaño del visor en unidades absolutas para el componente `Container` SDK interno mediante el selector de CSS `.s7flyoutviewer .s7container`. Además, debe anular el tamaño fijo definido para la clase CSS de nivel superior `.s7flyoutviewer` en el CSS del visor predeterminado, configurándolo en `auto`.

   A continuación se muestra un ejemplo de definición del tamaño del visor para el componente SDK `Container` interno, de modo que el área de vista principal no cambie su tamaño al cambiar el recurso:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La siguiente página de muestra muestra el comportamiento del visor con un tamaño fijo de vista principal. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   Además, tenga en cuenta que el visor CSS predeterminado proporciona un tamaño fijo para su área exterior predeterminada.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.FlyoutViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el campo `containerId` que contiene el nombre del ID de contenedor de visor y el objeto `params` JSON anidado con parámetros de configuración compatibles con el visor. En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl`, el recurso inicial como parámetro `asset`, la ruta base para cargar CSS como parámetro `contentUrl` y el nombre del ajuste preestablecido como parámetro `config`. La API de inicialización basada en JSON le permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor de visor agregado al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación del DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta `BODY` de cierre o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de página web todavía. Por ejemplo, puede ocultarse utilizando el estilo `display:none` asignado. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web vuelve a poner el elemento contenedor en el diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   El siguiente es un ejemplo de creación de una instancia de visor, pasando las opciones de configuración mínimas necesarias al constructor y llamando al método `init()`. El ejemplo supone que `inlineZoomViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; `http://s7d1.scene7.com/is/image/` es la URL del servicio de imágenes; y `Scene7SharedAssets/ImageSet-Views-Sample` es el recurso:

   ```
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incorpora el visor de zoom en línea con un tamaño fijo:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Diseño interactivo con altura ilimitada {#section-056cb574713c4d07be6d07cf3c598839}

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible en su lugar que dicta el tamaño de tiempo de ejecución del contenedor del visor `DIV`. En el siguiente ejemplo, supongamos que la página web permite que el contenedor `DIV` del visor tome el 40 % del tamaño de la ventana del explorador web, sin restringir su altura. El código HTML de la página web tendría el siguiente aspecto:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Añadir el visor a una página de este tipo es similar a los pasos para la incrustación de tamaño fijo. La única diferencia es que necesita anular el tamaño fijo del CSS del visor predeterminado con el tamaño establecido en unidades relativas.

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con el tamaño fijo que se integra con las tres excepciones siguientes:

* añada el contenedor `DIV` al &quot;titular&quot; `DIV` existente;
* se ha agregado el parámetro `imagereload` con puntos de interrupción explícitos;
* en lugar de establecer un tamaño de visor fijo mediante unidades absolutas, utilice CSS que establezca el visor `width` y `height` en 100% como se muestra a continuación:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo la proporción de aspecto del visor coincide con el recurso.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La página de ejemplos siguientes ilustra más usos reales de la incrustación de diseño interactivo con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/vlist/vlist.html)

## Integración de tamaño flexible con anchura y altura definidas {#section-0a329016f9414d199039776645c693de}

En caso de incrustación de tamaño flexible con anchura y altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños al DIV `"holder"` y lo centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en 100 por ciento.

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

El resto de los pasos de incrustación son idénticos a los pasos utilizados para el diseño interactivo incrustado con altura ilimitada. El ejemplo resultante es el siguiente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incrustación mediante API basada en Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor no-args. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican utilizando métodos de API `setContainerId()`, `setParam()` y `setAsset()`, con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de incrustación de tamaño fijo con API basada en establecedor:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```
