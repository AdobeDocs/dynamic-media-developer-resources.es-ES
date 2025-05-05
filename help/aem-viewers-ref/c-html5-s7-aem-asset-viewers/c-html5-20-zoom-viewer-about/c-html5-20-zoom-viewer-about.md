---
title: Zoom
description: Visor de zoom es un visor de imágenes que muestra una imagen ampliable. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Tiene herramientas de zoom, soporte de pantalla completa, muestras y un botón de cierre opcional. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2343'
ht-degree: 0%

---

# Zoom{#zoom}

Visor de zoom es un visor de imágenes que muestra una imagen ampliable. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Tiene herramientas de zoom, soporte de pantalla completa, muestras y un botón de cierre opcional. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor.

Tipo de visor 502.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Uso del visor de zoom {#section-e6c68406ecdc4de781df182bbd8088b4}

Visor de zoom representa un archivo JavaScript principal y un conjunto de archivos de ayuda (una sola inclusión JavaScript con todos los componentes SDK del visor utilizados por este visor, recursos y CSS en particular) descargados por el visor en tiempo de ejecución.

Puede utilizar el visualizador de zoom en modo emergente mediante una página de HTML lista para la producción proporcionada con visores IS o en modo incrustado, donde se integra en la página web de destino mediante una API documentada.

La configuración y el desollado son similares a los de otros visores. Todo el desollado se logra mediante CSS personalizado.

Ver [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de zoom {#section-642e66ca38cd4032992840ec6c0b0cd2}

El visor de zoom admite los siguientes gestos táctiles, que son comunes en otras aplicaciones móviles. Cuando el visor no puede procesar el gesto de deslizamiento del usuario, reenvía el evento al explorador web para realizar el desplazamiento de la página nativa. Este tipo de funcionalidad permite al usuario navegar por la página incluso si el visor ocupa la mayor parte del área de la pantalla del dispositivo.

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
   <td colname="col2"> <p> Selecciona una nueva miniatura en las muestras. En la vista principal, oculta o revela los elementos de la interfaz de usuario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pulse dos veces </p> </td> 
   <td colname="col2"> <p> Aumenta el tamaño de un nivel hasta que se alcanza el máximo de aumento. El siguiente gesto de doble toque restablece al visor al estado de visualización inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pellizco </p> </td> 
   <td colname="col2"> <p>Amplía o reduce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o gesto horizontal </p> </td> 
   <td colname="col2"> <p> Se desplaza por la lista de muestras de la barra de muestras. </p> <p> Si la imagen está en estado de restablecimiento y el parámetro <span class="codeph"> frametransition </span> está establecido en slide, el recurso se cambia con la animación de slide. Para otros modos de <span class="codeph"> frametransition </span>, el gesto realiza un desplazamiento de página nativo. </p> <p> Si la imagen se amplía, la mueve horizontalmente. Si la imagen se mueve al borde de la vista y se realiza un barrido en la misma dirección, el gesto realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical </p> </td> 
   <td colname="col2"> <p> Si la imagen está en estado de restablecimiento, el gesto realiza un desplazamiento de página nativo. </p> <p> Cuando se amplía la imagen, esta se mueve verticalmente. Si la imagen se mueve al borde de la vista y se realiza un barrido en la misma dirección, el gesto realiza un desplazamiento de página nativo. </p> <p> Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor admite tanto la entrada táctil como la entrada del ratón en dispositivos Windows con una pantalla táctil y un ratón. Sin embargo, esta compatibilidad se limita únicamente a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante el teclado.

Consulte [Navegación y accesibilidad por teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor de zoom {#section-6bb5d3c502544ad18a58eafe12a13435}

Las distintas páginas web tienen diferentes necesidades de comportamiento del visualizador. A veces, una página web proporciona un vínculo que, cuando se selecciona, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de funcionamiento principales: emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

**Modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Ocupa todo el área de la ventana del explorador y se ajusta en caso de que se cambie el tamaño del explorador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante la llamada de JavaScript `window.open()`, el elemento de HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página de HTML predeterminada para el modo de operación emergente. La página de HTML predeterminada se llama `ZoomViewer.html` y se encuentra en la subcarpeta `html5/` de su implementación estándar de visores de servicio de Internet (IS-Viewers), como se muestra a continuación:

`<s7viewers_root>/html5/ZoomViewer.html`

Aplique CSS personalizado para lograr un aspecto personalizado para la página.

A continuación se muestra un ejemplo de código de HTML que abre el visor en la nueva ventana:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo incrustado, el visor se añade a la página web existente, que puede tener ya contenido de clientes no relacionado con el visor. Normalmente, el visor ocupa solo una parte de los bienes raíces de la página web.

Los casos de uso principales son páginas web orientadas para equipos de escritorio o tabletas, y también páginas diseñadas interactivas que ajustan el diseño automáticamente, según el tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta opción es la mejor opción para las páginas web que tienen un diseño estático.

El modo de incrustación de diseño interactivo supone que es necesario cambiar el tamaño del visor durante el tiempo de ejecución debido al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es añadir un visor a una página web que utilice un diseño flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente según la forma en que la página web ajusta el tamaño de su contenedor `DIV`. Si la página web solo establece la anchura del contenedor `DIV` y deja su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta lógica garantiza que el recurso se ajuste perfectamente a la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que utilizan marcos de diseño adaptables, como Bootstrap y Foundation.

Si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellena ese área y sigue el tamaño que proporciona la página web. Por ejemplo, al incrustar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

## Incrustación de tamaño fijo {#section-44f365e6c0dd40709467a459afa82a7f}

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definición del DIV de contenedor.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo de JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado del HTML. Antes de usar la API de visor, asegúrese de incluir [!DNL ZoomViewer.js]. El archivo [!DNL ZoomViewer.js] se encuentra en la subcarpeta [!DNL html5/js/] de su implementación estándar de visores IS:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tengan instalados los visores de IIS.

La ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Configuración del tamaño del visor.

   Este visor muestra miniaturas cuando se trabaja con conjuntos de varios elementos; en los sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal en tiempo de ejecución mediante la API `setAsset()`. Como desarrollador, tiene control sobre cómo administra el visor el área de miniaturas en la parte inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener el tamaño de la vista principal estático y contraer el área del visor exterior, permitiendo que el contenido de la página web se mueva hacia arriba, y utilizar los bienes raíces en pantalla libre que quedan de las miniaturas.

   Para mantener intactos los límites del visor exterior, defina el tamaño de la clase CSS de nivel superior `.s7zoomviewer` en unidades absolutas. El tamaño en CSS se puede ajustar directamente en la página del HTML. O bien, se puede colocar en un archivo CSS de visor personalizado, que luego se asigna a un registro de ajuste preestablecido de visor en Dynamic Media Classic o se pasa explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor de zoom](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor externo estático en una página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un visor exterior fijo en el siguiente ejemplo. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=es](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=es)

   Para que las dimensiones de la vista principal sean estáticas, defina el tamaño del visor en unidades absolutas para el componente SDK `Container` interno mediante el selector CSS `.s7zoomviewer` `.s7container` o mediante el modificador `stagesize`.

   A continuación se muestra un ejemplo de definición del tamaño del visor para el componente SDK `Container` interno de modo que el área de vista principal no cambie su tamaño al cambiar el recurso:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La siguiente página de demostración muestra el comportamiento del visor con un tamaño de vista principal fijo. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=es](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=es)

   Puede establecer el modificador `stagesize` en el registro de ajuste preestablecido de visualizador en Dynamic Media Classic. O bien, puede pasarlo explícitamente con el código de inicialización del visor con la colección `params` o como una llamada de API como se describe en la sección Referencia de comandos de esta Ayuda, como en el ejemplo siguiente:

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   Se recomienda un enfoque basado en CSS y se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.ZoomViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor.

   La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el campo `containerId` que contiene el nombre del ID del contenedor del visor y el objeto JSON `params` anidado con parámetros de configuración compatibles con el visor. En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta de cierre `BODY` o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, se puede ocultar usando el estilo `display:none` asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar al método `init()`. En este ejemplo se supone que `zoomViewer` es la instancia del visor, `s7viewer` es el nombre del DIV del marcador de posición, `http://s7d1.scene7.com/is/image/` es la dirección URL del servicio de imágenes y `Scene7SharedAssets/ImageSet-Views-Sample` es el recurso.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visualizador de vídeo con un tamaño fijo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Inserción de diseño interactivo con altura sin restricciones {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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

Añadir el visor a una página de este tipo es similar a los pasos para la incrustación de tamaño fijo. La única diferencia es que no es necesario definir explícitamente el tamaño del visor.

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definición del DIV de contenedor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Agregue el DIV contenedor al DIV `"holder"` existente. El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo la proporción de aspecto del visor coincide con el recurso.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La siguiente página de ejemplos ilustra usos más reales del diseño interactivo incrustado con una altura sin restricciones:

[Demostraciones en vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Incrustación de tamaño flexible con anchura y altura definidas {#section-3674e6c032594441a6576b7fb1de6e64}

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## Incrustación mediante API basada en establecedores {#section-44e014925f24418b900696003855c0a9}

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante los métodos de API `setContainerId()`, `setParam()` y `setAsset()` con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de incrustación de tamaño fijo con API basada en establecedores:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
