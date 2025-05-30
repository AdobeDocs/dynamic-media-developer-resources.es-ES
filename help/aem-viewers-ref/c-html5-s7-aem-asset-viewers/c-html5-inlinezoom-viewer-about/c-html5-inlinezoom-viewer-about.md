---
title: Zoom en línea
description: Visor de zoom en línea es un visor de imágenes. Muestra una imagen estática con la versión ampliada sobre esa imagen estática cuando un usuario se desplaza por encima o toca la vista principal. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# Zoom en línea{#inline-zoom}

Visor de zoom en línea es un visor de imágenes. Muestra una imagen estática con la versión ampliada sobre esa imagen estática cuando un usuario se desplaza por encima o toca la vista principal. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor.

Tipo de visor 504.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## Uso del visor de zoom en línea {#section-f21ac23d3f6449ad9765588d69584772}

Visor de zoom en línea representa un archivo JavaScript principal y un conjunto de archivos de ayuda (una sola inclusión JavaScript con todos los componentes SDK del visor utilizados por este visor, recursos y CSS) descargados por el visor durante la ejecución.

El visualizador de zoom en línea se puede utilizar en el modo emergente utilizando la página del HTML lista para la producción proporcionada con los visualizadores del servicio de imágenes o en el modo incrustado, donde se integra en una página web de destino mediante una API documentada.

La configuración y el desollado son similares a los de otros visores. Puede utilizar CSS personalizado para aplicar aspectos.

Ver [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de zoom en línea {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visor de zoom en línea admite gestos de un solo toque y de varios toques que son comunes en otras aplicaciones móviles.

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
   <td colname="col2"> <p> Activa la vista flotante o cambia entre el nivel de zoom principal y secundario en las muestras y selecciona una nueva miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o gesto horizontal </p> </td> 
   <td colname="col2"> <p> Se desplaza por la lista de muestras de la barra de muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical </p> </td> 
   <td colname="col2"> <p>Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor también admite la entrada táctil y la entrada del ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad se limita únicamente a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante el teclado.

Consulte [Navegación y accesibilidad por teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor de zoom en línea {#section-6bb5d3c502544ad18a58eafe12a13435}

Las distintas páginas web tienen diferentes necesidades de comportamiento del visualizador. A veces, una página web proporciona un vínculo en el que se puede hacer clic para abrir el visor en una ventana independiente del explorador. En otros casos, puede ser necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de funcionamiento principales: emergente, incrustación de tamaño fijo e incrustación adaptable.

**Elemento emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Ocupa todo el área de la ventana del explorador y se ajusta cuando se cambia el tamaño de la ventana del explorador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante la llamada de JavaScript `window.open()`, el elemento de HTML `A` configurado correctamente o cualquier otra forma adecuada.

Se recomienda usar la página de HTML predeterminada para el modo emergente denominado `FlyoutViewer.html`. Se encuentra en la subcarpeta [!DNL html5/] de su implementación estándar de Image Serving-Viewers:

`<s7viewers_root>/html5/FlyoutViewer.html`

También es necesario tener configurado el componente FlyoutZoomView para que funcione en el modo de zoom en línea. Se recomienda utilizar el ajuste preestablecido predeterminado `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` para el visor de zoom en línea o un ajuste preestablecido personalizado derivado de él. La personalización visual se puede lograr aplicando CSS personalizado.

El siguiente es un ejemplo de código de HTML que abre el visor en una nueva ventana:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Incrustación de tamaño fijo e incrustación adaptable**

En el modo incrustado, el visor se añade a la página web existente, que puede tener ya contenido de clientes no relacionado con el visor. El visor normalmente ocupa solo una parte de los bienes raíces de la página web.

Los casos de uso principales son páginas web orientadas para equipos de escritorio o tabletas, y también páginas web adaptables que ajustan el diseño automáticamente según el tipo de dispositivo.

El modo de incrustación de tamaño fijo se utiliza cuando el visualizador no cambia su tamaño después de su carga inicial. Esta opción es perfecta para las páginas web que tienen un diseño de página estático.

El modo de incrustación de diseño interactivo supone que el visor debe cambiar de tamaño durante el tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es añadir un visor a una página web que utilice un diseño de página flexible.

Cuando utilice el modo de incrustación de diseño interactivo con el Visor de zoom en línea, asegúrese de especificar puntos de interrupción explícitos para la imagen de vista principal mediante el parámetro `imagereload`. Lo ideal es que combine los puntos de interrupción con los puntos de interrupción de anchura del visor según lo dictado por la página web de CSS.

En el modo de incrustación de diseño interactivo, el comportamiento del visor varía en función del tamaño del contenedor de página web `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV` y deja su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad significa que el recurso se adapta perfectamente a la vista sin ningún relleno en los lados. Este caso de uso en particular es el más común para las páginas web que utilizan marcos de diseño adaptable como Bootstrap o Foundation.

De lo contrario, si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellenará únicamente ese área y seguirá el tamaño proporcionado por el diseño de página web. Un buen ejemplo de uso es la incrustación del visualizador en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definir el contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo de JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado del HTML. Antes de usar la API de visor, asegúrese de incluir `FlyoutViewer.js`. `FlyoutViewer.js` se encuentra en la siguiente subcarpeta [!DNL html5/js/] de su implementación estándar de visores IS:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Dynamic Media de Adobe y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Dynamic Media de Adobe que tengan instalados los visores de IIS.

Una ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Solo haga referencia al archivo de JavaScript `include` del visor principal en su página. No haga referencia a ningún archivo JavaScript adicional en el código de la página web que la lógica del visor pueda descargar durante la ejecución. En particular, no haga referencia directamente a la biblioteca `Utils.js` del SDK de HTML5 cargada por el visor desde la ruta de contexto `/s7viewers` (denominado SDK consolidado `include`). El motivo es que la ubicación de `Utils.js` o bibliotecas similares del visor en tiempo de ejecución está completamente administrada por la lógica del visor y la ubicación cambia entre versiones del visor. El Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, al establecer una referencia directa a cualquier JavaScript `include` secundario que use el visor en la página, se interrumpe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del DIV de contenedor.

   Añada un elemento DIV vacío a la página donde desea que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa posteriormente a la API del visor.

   El DIV de marcador de posición es un elemento posicionado, lo que significa que la propiedad CSS `position` está establecida en `relative` o `absolute`.

   Es responsabilidad de la página web especificar el `z-index` correcto para el elemento DIV del marcador de posición. Al hacerlo, se asegura de que la parte flotante del visor aparezca sobre los demás elementos de la página web.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Configuración del tamaño del visor.

   Este visor muestra miniaturas cuando se trabaja con conjuntos de varios elementos. En sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal durante el tiempo de ejecución mediante la API `setAsset()`. Como desarrollador, tiene control sobre cómo administra el visor el área de miniaturas en el área inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener el tamaño de la vista principal estático y contraer el área del visor exterior, dejando que el contenido de la página web suba, y luego utilizar los bienes raíces de la página libre que quedan de las miniaturas.

   Para mantener intactos los límites del visor exterior, defina el tamaño de la clase CSS de nivel superior `.s7flyoutviewer` en unidades absolutas. El tamaño en CSS se puede ajustar directamente en la página del HTML o en un archivo CSS de visor personalizado, y luego asignarse a un registro de ajuste preestablecido de visor en Dynamic Media Classic, o pasarse explícitamente mediante el comando de estilo.

   Consulte [Personalización del visor de zoom en línea](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición del tamaño del visor exterior estático en una página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un área de visor exterior fija en la siguiente página de muestra. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html?lang=es](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html?lang=es)

   Para que las dimensiones de la vista principal sean estáticas, defina el tamaño del visor en unidades absolutas para el componente SDK `Container` interno mediante el selector CSS `.s7flyoutviewer .s7container`. Además, debe anular el tamaño fijo definido para la clase CSS de nivel superior `.s7flyoutviewer` en el visor CSS predeterminado, estableciéndolo en `auto`.

   A continuación se muestra un ejemplo de definición del tamaño del visor para el componente SDK `Container` interno de modo que el área de vista principal no cambie su tamaño al cambiar el recurso:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La siguiente página de ejemplo muestra el comportamiento del visor con un tamaño de vista principal fijo. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html?lang=es](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html?lang=es)

   Además, el visor CSS predeterminado proporciona un tamaño fijo para su área exterior de forma predeterminada.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.FlyoutViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el campo `containerId` que contiene el nombre del ID del contenedor del visor y el objeto JSON `params` anidado con parámetros de configuración compatibles con el visor. En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl`; el recurso inicial como parámetro `asset`, la ruta base para cargar CSS como parámetro `contentUrl` y el nombre del ajuste preestablecido como parámetro `config`. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta de cierre `BODY` o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, se puede ocultar usando el estilo `display:none` asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar al método `init()`. El ejemplo supone que `inlineZoomViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; `http://s7d1.scene7.com/is/image/` es la dirección URL del servicio de imágenes; y `Scene7SharedAssets/ImageSet-Views-Sample` es el recurso:

   ```html {.line-numbers}
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

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visor de zoom en línea con un tamaño fijo:

   ```html {.line-numbers}
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

## Inserción de diseño interactivo con altura sin restricciones {#section-056cb574713c4d07be6d07cf3c598839}

Con incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que dicta el tamaño de tiempo de ejecución del contenedor del visor `DIV`. En el siguiente ejemplo, supongamos que la página web permite que el contenedor del visor `DIV` ocupe el 40% del tamaño de la ventana del explorador web, sin restringir su altura. El código del HTML de la página web tendría el siguiente aspecto:

```html {.line-numbers}
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

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definir el contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo con las tres excepciones siguientes:

* agregar el contenedor `DIV` al &quot;contenedor&quot; `DIV` existente;
* se agregó el parámetro `imagereload` con puntos de interrupción explícitos;
* en lugar de establecer un tamaño de visor fijo mediante unidades absolutas, utilice CSS que establezca el visor `width` y `height` en el 100% como se muestra a continuación:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo la proporción de aspecto del visor coincide con el recurso.

```html {.line-numbers}
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

La siguiente página de ejemplos ilustra usos más reales del diseño interactivo incrustado con una altura sin restricciones:

[Demostraciones en vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=es)

## Incrustación de tamaño flexible con anchura y altura definidas {#section-0a329016f9414d199039776645c693de}

Si hay una incrustación de tamaño flexible con la anchura y la altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños al DIV `"holder"` y lo centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en un 100 por ciento.

```html {.line-numbers}
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

El resto de los pasos de incrustación son idénticos a los pasos utilizados para la incrustación de diseño interactivo con altura sin restricciones. El ejemplo resultante es el siguiente:

```html {.line-numbers}
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

## Incrustación mediante una API basada en Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante los métodos de API `setContainerId()`, `setParam()` y `setAsset()`, con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de incrustación de tamaño fijo con API basada en establecedores:

```html {.line-numbers}
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
