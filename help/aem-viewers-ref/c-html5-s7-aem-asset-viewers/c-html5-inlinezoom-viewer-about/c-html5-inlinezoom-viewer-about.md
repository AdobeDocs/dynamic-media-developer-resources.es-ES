---
description: El visor de zoom en línea es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra sobre esa imagen estática cuando un usuario pasa el cursor sobre la vista principal o la toca. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
keywords: responsive
seo-description: El visor de zoom en línea es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra sobre esa imagen estática cuando un usuario pasa el cursor sobre la vista principal o la toca. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
seo-title: Zoom en línea
solution: Experience Manager
title: Zoom en línea
topic: Dynamic media
uuid: 2287aef0-79ba-4d63-911a-969fa1c63385
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2457'
ht-degree: 0%

---


# Zoom en línea{#inline-zoom}

El visor de zoom en línea es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra sobre esa imagen estática cuando un usuario pasa el cursor sobre la vista principal o la toca. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

El tipo de visor es 504.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Dirección URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## Uso del visor de zoom en línea {#section-f21ac23d3f6449ad9765588d69584772}

El visor de zoom en línea representa un archivo JavaScript principal y un conjunto de archivos auxiliares (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visor, recursos y CSS en particular) descargados por el visor durante la ejecución.

El visor de zoom en línea se puede utilizar tanto en el modo emergente mediante la página HTML preparada para la producción proporcionada con los visores de servicio de imágenes como en el modo incrustado, donde se integra en una página web de destinatario mediante API documentada.

La configuración y la aplicación de aspectos son similares a las de los demás visores. Puede utilizar CSS personalizada para aplicar la apariencia.

Consulte [Referencia de comandos común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comandos común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de zoom en línea {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visor de zoom en línea admite gestos de un solo toque y de varios toques comunes en otras aplicaciones móviles.

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
   <td colname="col2"> <p> Activa la vista flotante o los cambios entre el nivel de zoom primario y secundario en las muestras, selecciona una nueva miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o barrido horizontal </p> </td> 
   <td colname="col2"> <p> Se desplaza por la lista de muestras en la barra de muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical </p> </td> 
   <td colname="col2"> <p>Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor también admite entrada táctil y entrada de ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad está limitada a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante teclado.

Consulte [Navegación y accesibilidad del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor de zoom en línea {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo en el que se puede hacer clic y que abre el visor en una ventana independiente del explorador. En otros casos, puede ser necesario incrustar el visor directamente en la página de alojamiento. En este último caso, es posible que la página web tenga un diseño de página estático o utilice un diseño interactivo que se muestre de forma diferente en distintos dispositivos o en diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: ventana emergente, incrustación de tamaño fijo e incrustación adaptable.

**Ventana emergente**

En el modo emergente, el visor se abre en una ventana o ficha separada del explorador Web. Toma todo el área de la ventana del navegador y se ajusta cuando se cambia el tamaño de la ventana del navegador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante `window.open()` llamada de JavaScript, un elemento HTML `A` configurado correctamente o de cualquier otra forma adecuada.

Se recomienda utilizar la página HTML lista para usar para el modo emergente denominada `FlyoutViewer.html`. Se encuentra en la subcarpeta [!DNL html5/] de la implementación estándar de los visores de servicio de imágenes:

`<s7viewers_root>/html5/FlyoutViewer.html`

También es necesario configurar el componente FlyoutZoomView para que funcione en el modo de zoom en línea. Se recomienda utilizar el ajuste preestablecido `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` predeterminado para el visor de zoom en línea o un ajuste preestablecido personalizado derivado de él. La personalización visual se puede lograr mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código HTML que abre el visor en una ventana nueva:

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Incrustación de tamaño fijo e incrustación adaptable**

En el modo incrustado, el visor se añade a la página web existente, que puede tener ya contenido de cliente no relacionado con el visor. Normalmente, el visor ocupa solo una parte del espacio de la página web.

El caso de uso principal son las páginas web orientadas para equipos de escritorio o tabletas, y también las páginas web interactivas que ajustan el diseño automáticamente en función del tipo de dispositivo.

El modo de incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta opción es la mejor para las páginas web con un diseño de página estático.

El modo de incrustación de diseño adaptable supone que el visor puede necesitar cambiar el tamaño durante el tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

Al utilizar el modo de incrustación de diseño interactivo con el visor de zoom en línea, asegúrese de especificar puntos de interrupción explícitos para la imagen de vista principal mediante el parámetro `imagereload`. Lo ideal es que los puntos de interrupción coincidan con los puntos de interrupción del ancho del visor según lo dicta el CSS de la página web.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función de la forma en que una página web cambia el tamaño de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, dejando su altura sin restricciones, el visor selecciona automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esto significa que el recurso encaja perfectamente en la vista sin ningún relleno en los lados. Este caso de uso particular es el más común para las páginas web que utilizan marcos de diseño interactivos como Bootstrap, Foundation, etc.

En caso contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellenará solo esa área y seguirá el tamaño proporcionado por el diseño de la página web. Un buen ejemplo de caso de uso es integrar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del navegador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor en la página web.

   La creación de un visor requiere que agregue una etiqueta de script en el encabezado HTML. Antes de usar la API de visor, asegúrese de incluir `FlyoutViewer.js`. `FlyoutViewer.js` se encuentra en la siguiente  [!DNL html5/js/] subcarpeta de la implementación estándar de visores de IS:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Scene7 y se suministra desde el mismo dominio. De lo contrario, se especifica una ruta completa a uno de los servidores de Adobe Scene7 que tienen instalados los visores IS.

Una ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Solo debe hacer referencia al archivo JavaScript `include` del visor principal de la página. No debe hacer referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargarse mediante la lógica del visor en tiempo de ejecución. En particular, no haga referencia directa a la biblioteca `Utils.js` del SDK de HTML5 cargada por el visor desde la ruta de contexto `/s7viewers` (denominada SDK consolidado `include`). El motivo es que la ubicación de `Utils.js` o bibliotecas de visores de tiempo de ejecución similares se administra completamente mediante la lógica del visor y la ubicación cambia entre las versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, la colocación de una referencia directa a cualquier JavaScript `include` secundario utilizado por el visor en la página interrumpe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición de la DIV de contenedor.

   Añada un elemento DIV vacío a la página en la que desea que aparezca el visor. El ID del elemento DIV debe definirse porque este ID se pasa más tarde a la API del visor.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la propiedad CSS `position` se establece en `relative` o `absolute`.

   Es responsabilidad de la página Web especificar el `z-index` apropiado para el elemento DIV del marcador de posición. De este modo, se garantiza que la parte flotante del visor aparezca sobre los demás elementos de la página web.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Configuración del tamaño del visor.

   Este visor muestra miniaturas al trabajar con conjuntos de varios elementos. En los sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal durante la ejecución mediante la API `setAsset()`. Como desarrollador, tiene control sobre cómo gestiona el visor el área de miniaturas en el área inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener el tamaño de vista principal estático y contraer el área del visor exterior, permitiendo así que el contenido de la página web se mueva hacia arriba y, a continuación, utilizar el espacio de la página libre que queda en las miniaturas.

   Para mantener intactos los límites exteriores del visor, defina el tamaño de la clase CSS de nivel superior `.s7flyoutviewer` en unidades absolutas. El cambio de tamaño en CSS se puede colocar directamente en la página HTML o en un archivo CSS de visor personalizado, que posteriormente se asigna a un registro de ajuste preestablecido de visor en Scene7 Publishing System, o se pasa explícitamente mediante el comando style.

   Consulte [Personalización del visor de zoom en línea](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición del tamaño del visor externo estático en una página HTML:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un área de visor exterior fija en la siguiente página de muestra. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html)

   Para que las dimensiones de vista principales sean estáticas, defina el tamaño del visor en unidades absolutas para el componente `Container` SDK interno mediante el selector de CSS `.s7flyoutviewer .s7container`. Además, debe anular el tamaño fijo definido para la clase CSS de nivel superior `.s7flyoutviewer` en la CSS predeterminada del visor, configurándola en `auto`.

   A continuación se muestra un ejemplo de definición del tamaño del visor para el componente `Container` SDK interno, de modo que el área de vista principal no cambie su tamaño al cambiar el recurso:

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

   La siguiente página de muestra muestra el comportamiento del visor con un tamaño de vista principal fijo. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html)

   Además, tenga en cuenta que el CSS del visor predeterminado proporciona un tamaño fijo para su área exterior lista para usar.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.FlyoutViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el campo `containerId` que contiene el nombre del ID de contenedor del visor y el objeto JSON anidado `params` con parámetros de configuración compatibles con el visor. En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl`, el recurso inicial como parámetro `asset`, la ruta de acceso base para cargar CSS como parámetro `contentUrl` y el nombre preestablecido como parámetro `config`. La API de inicialización basada en JSON permite crear y inicio del visor con una sola línea de código.

   Es importante que el contenedor del visor se añada al DOM para que el código del visor pueda encontrar el elemento de contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta `BODY` de cierre o en el evento body `onload()`.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web. Por ejemplo, puede ocultarse con el estilo `display:none` asignado. En este caso, el visor retrasa el proceso de inicialización hasta el momento en que la página web devuelve el elemento de contenedor a la presentación. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de creación de una instancia de visor, pasando las opciones de configuración mínimas necesarias al constructor y llamando al método `init()`. El ejemplo asume que `inlineZoomViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; `http://s7d1.scene7.com/is/image/` es la dirección URL del servicio de imágenes; y `Scene7SharedAssets/ImageSet-Views-Sample` es el recurso:

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

## Incrustación de diseño adaptable con altura ilimitada {#section-056cb574713c4d07be6d07cf3c598839}

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que determina el tamaño de tiempo de ejecución del contenedor `DIV` del visor. En el siguiente ejemplo, supongamos que la página web permite que el contenedor del visor `DIV` ocupe el 40 % del tamaño de la ventana del explorador web, dejando su altura sin restricciones. El código HTML de la página web tendría el siguiente aspecto:

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

Añadir el visor a una página de este tipo es similar a los pasos para la incrustación de tamaño fijo. La única diferencia es que debe anular el tamaño fijo del CSS del visor predeterminado con el tamaño establecido en unidades relativas.

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo con las tres excepciones siguientes:

* añadir el contenedor `DIV` al &quot;titular&quot; `DIV` existente;
* se ha agregado el parámetro `imagereload` con puntos de interrupción explícitos;
* en lugar de establecer un tamaño de visor fijo mediante unidades absolutas, utilice CSS que establezca el visor `width` y `height` en 100% como se muestra a continuación:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del navegador y cómo coincide la proporción de aspecto del visor con el recurso.

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

La siguiente página de ejemplos ilustra los usos más reales del diseño interactivo que se incrusta con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Integración de tamaño flexible con anchura y altura definidas {#section-0a329016f9414d199039776645c693de}

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

El resto de los pasos de incrustación son idénticos a los pasos utilizados para la incrustación de diseño interactivo con altura ilimitada. El ejemplo resultante es el siguiente:

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

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en setter y el constructor no-args. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante métodos de API `setContainerId()`, `setParam()` y `setAsset()`, con llamadas JavaScript independientes.

El siguiente ejemplo ilustra el uso de la incrustación de tamaño fijo con API basada en establecedor:

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

