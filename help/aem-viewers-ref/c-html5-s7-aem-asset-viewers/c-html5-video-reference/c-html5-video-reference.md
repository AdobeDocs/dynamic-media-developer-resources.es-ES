---
title: Vídeo
description: El Visor de vídeo es un reproductor de vídeo que reproduce flujo continuo y vídeo progresivo codificado en formato H.264. Se entrega desde Dynamic Media Classic o Adobe Experience Manager con Dynamic Media.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# Vídeo{#video}

El Visor de vídeo es un reproductor de vídeo que reproduce flujo continuo y vídeo progresivo codificado en formato H.264. Se entrega desde Dynamic Media Classic o desde un Experience Manager con Dynamic Media.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Se admiten conjuntos de vídeos adaptables y de vídeo únicos. Además, el visualizador admite el trabajo con flujos de vídeo progresivos y HLS alojados en ubicaciones externas. Está diseñado para funcionar tanto en exploradores web de escritorio como móviles compatibles con vídeo HTML5. Este visor también admite subtítulos opcionales que se muestran sobre el contenido del vídeo, la navegación por capítulos de vídeo y las herramientas para compartir en medios sociales.

El Visor de vídeo utiliza la reproducción de vídeo de flujo HTML 5 en formato HLS en su configuración predeterminada siempre que el sistema subyacente la admita. En sistemas que no admiten el streaming de HTML 5, el visor vuelve a recibir la entrega de vídeo progresivo de HTML 5.

Tipo de visor 506.

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Uso del visor de vídeo {#section-f21ac23d3f6449ad9765588d69584772}

Visor de vídeo representa un archivo JavaScript principal y un conjunto de archivos de ayuda (un solo JavaScript incluido con todos los componentes del SDK del visor utilizados por este visor, los recursos y CSS descargados por el visor en tiempo de ejecución).

Puede utilizar el Visor de vídeo en modo emergente utilizando la página de HTML lista para la producción proporcionada con visores IS. O bien, puede utilizar el visualizador en modo incrustado, donde se integra en una página web de destino mediante la API documentada.

La tarea de configurar y desollar el visor es similar a la de otros visores. Todo el desollado se logra mediante CSS personalizado.

Ver [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de vídeo {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El Visor de vídeo proporciona un conjunto de controles de interfaz de usuario estándar para la reproducción de vídeo, como un botón de reproducción/pausa, una burbuja de tiempo de vídeo de selección manual de vídeo, un indicador de tiempo de reproducción/tiempo total, un control de volumen, un botón de pantalla completa y un conmutador de subtítulos. Todos estos controles se agrupan en una barra de control en la parte inferior de la interfaz de usuario del visor.

En dispositivos táctiles, el control de volumen se oculta de la interfaz de usuario, ya que solo es posible controlar el volumen mediante los botones de hardware.

Cuando el visor funciona en modo emergente, el botón de pantalla completa no está disponible en la interfaz de usuario.

Es posible navegar por el contenido de un vídeo rápidamente cuando se activa el capítulo de vídeo. Los capítulos de vídeo se muestran como marcadores en la pista de selección manual de vídeo y muestran el título del capítulo y la descripción asociada al pasar el ratón por encima o con un solo toque en los sistemas táctiles. Los usuarios pueden buscar un capítulo determinado seleccionando un marcador de capítulo o la burbuja de descripción del capítulo.

El visor admite tanto la entrada táctil como la entrada del ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad se limita únicamente a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante el teclado.

Consulte [Navegación y accesibilidad por teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Herramientas de uso compartido de medios sociales con el Visor de vídeos {#section-907d316fe1da4b87abb9775f02464704}

El Visor de vídeo es compatible con las herramientas de uso compartido de medios sociales. Están disponibles como un solo botón en la interfaz de usuario que se expande hasta una barra de herramientas compartida cuando el usuario hace clic o pulsa en ella.

La barra de herramientas de uso compartido contiene un icono para cada tipo de canal de uso compartido admitido, como Facebook, Twitter, correo electrónico compartido, código compartido incrustado y vínculo compartido. Cuando se activan las herramientas de uso compartido de correo electrónico, de incrustación de recursos compartidos o de vínculo compartido, el visor muestra un cuadro de diálogo modal con el formulario de entrada de datos correspondiente. Cuando se llama a Facebook o a un Twitter, el visor redirige al usuario a un cuadro de diálogo de uso compartido estándar desde un servicio de medios sociales. Además, cuando se activa una herramienta de uso compartido, la reproducción de vídeo se detiene automáticamente.

Las herramientas de uso compartido no están disponibles en el modo de pantalla completa debido a las restricciones de seguridad del explorador web.

## Incrustación del visor de vídeo {#section-6bb5d3c502544ad18a58eafe12a13435}

Las distintas páginas web tienen diferentes necesidades de comportamiento del visualizador. A veces, una página web proporciona un vínculo que, al seleccionarlo, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

La incrustación de varios vídeos en la misma página es compatible con tabletas y dispositivos móviles. Normalmente, sólo se puede reproducir un vídeo a la vez. Cuando un usuario comienza a reproducir un vídeo y luego intenta reproducir otro, el primer vídeo se pausa automáticamente. El vídeo en pausa automática recuerda su tiempo de reproducción actual, por lo que el usuario siempre puede volver a él y reanudar la reproducción. La única excepción a esta regla es el navegador Chrome en dispositivos Android™ 4.x, que puede reproducir vídeos en paralelo.

**Modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Ocupa todo el área de la ventana del explorador y se ajusta en caso de que se cambie el tamaño del explorador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante la llamada de JavaScript `window.open()`, el elemento de HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página de HTML predeterminada para el modo de operación emergente. Se llama [!DNL VideoViewer.html] y se encuentra en la subcarpeta [!DNL html5/] de su implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Puede conseguir una personalización visual aplicando CSS personalizado.

A continuación se muestra un ejemplo de código de HTML que abre el visor en una nueva ventana:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación adaptable**

En el modo incrustado, el visor se añade a la página web existente, que puede tener ya contenido de clientes no relacionado con el visor. Normalmente, el visor ocupa solo una parte de los bienes raíces de la página web.

Los casos de uso principales son páginas web orientadas para equipos de escritorio o tabletas, y también páginas de diseño interactivo que ajustan el diseño automáticamente según el tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta opción es la mejor para las páginas web que tienen un diseño de página estático.

La incrustación de diseño interactivo supone que el visor debe cambiar su tamaño en tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es añadir el visor a una página web que utiliza un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente según la forma en que la página web cambie el tamaño de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV` y deja su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Este método garantiza que el recurso se ajuste perfectamente a la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que utilizan un marco de diseño interactivo como Bootstrap o Foundation.

De lo contrario, si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellenará sólo esa área y seguirá el tamaño proporcionado por el diseño de la página web. Un buen ejemplo es la incrustación del visualizador en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definir el contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo de JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado del HTML. Antes de usar la API de visor, asegúrese de incluir [!DNL FlyoutViewer.js]. El archivo [!DNL FlyoutViewer.js] se encuentra en la subcarpeta [!DNL html5/js/] de su implementación estándar de visores IS:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tengan instalados los visores de IIS.

La ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Solo haga referencia al archivo de JavaScript `include` del visor principal en su página. No haga referencia a ningún archivo JavaScript adicional en el código de la página web que la lógica del visor pueda descargar durante la ejecución. En particular, no haga referencia directamente a la biblioteca `Utils.js` del SDK de HTML5 cargada por el visor desde la ruta de contexto `/s7viewers` (denominado SDK consolidado `include`). El motivo es que la ubicación de `Utils.js` o bibliotecas similares del visor en tiempo de ejecución está completamente administrada por la lógica del visor y la ubicación cambia entre versiones del visor. El Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, al establecer una referencia directa a cualquier JavaScript `include` secundario que use el visor en la página, se interrumpe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del DIV de contenedor.

   Añada un elemento DIV vacío a la página donde desea que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa posteriormente a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El DIV de marcador de posición es un elemento posicionado, lo que significa que la propiedad CSS `position` está establecida en `relative` o `absolute`.

   Asegúrese de que la característica de pantalla completa funciona correctamente en Internet Explorer. Asegúrese de que no haya otros elementos en el DOM que tengan un orden de apilamiento más alto que el DIV de marcador de posición.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para la clase CSS de nivel superior `.s7videoviewer` en unidades absolutas o utilizando el modificador `stagesize`.

   Puede colocar el tamaño en CSS directamente en la página del HTML o en un archivo CSS de visor personalizado. Posteriormente, se asigna a un registro de ajuste preestablecido de visualizador en Dynamic Media Classic o se pasa explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor de vídeo](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) para obtener más información sobre cómo aplicar estilo al visor mediante CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en una página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede establecer el modificador `stagesize` en el registro de ajustes preestablecidos de visor de Dynamic Media Classic o pasarlo explícitamente con el código de inicialización del visor con la colección `params`. O bien, como una llamada API como se describe en la sección Referencia de comandos, como en el siguiente ejemplo:

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   Se recomienda un enfoque basado en CSS y se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.VideoViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el campo `containerId` que contiene el nombre del ID del contenedor del visor y el objeto JSON `params` anidado con parámetros de configuración admitidos por el visor. En este caso, el objeto `params` debe tener al menos la URL del servicio de imágenes pasada como propiedad `serverUrl`, la URL del servidor de vídeo pasada como propiedad `videoserverurl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta de cierre `BODY` o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, se puede ocultar usando el estilo `display:none` asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar al constructor las opciones de configuración mínimas necesarias y llamar al método `init()`. En este ejemplo se supone que `videoViewer` es la instancia del visor, `s7viewer` es el nombre del marcador de posición `DIV`, [!DNL http://s7d1.scene7.com/is/image/] es la dirección URL del servicio de imágenes, [!DNL http://s7d1.scene7.com/is/content/] es la dirección URL del servidor de vídeo y [!DNL Scene7SharedAssets/Glacier_Climber_MP4] es el recurso.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visualizador de vídeo con un tamaño fijo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Inserción de diseño interactivo con altura sin restricciones**

Con el diseño interactivo incrustado, la página web normalmente tiene algún tipo de diseño flexible que dicta el tamaño en tiempo de ejecución del contenedor del visor `DIV`. A efectos de este ejemplo, supongamos que la página web permite que el contenedor del visor `DIV` ocupe el 40% del tamaño de la ventana del explorador web, sin restringir su altura. El código del HTML de la página web tendría el siguiente aspecto:

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

Añadir el visor a una página de este tipo es similar a la incrustación de tamaño fijo; la única diferencia es que no necesita definir explícitamente el tamaño del visor.

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definición del DIV de contenedor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Agregar el contenedor `DIV` al &quot;titular&quot; `DIV` existente. El siguiente código es un ejemplo completo. Puede ver cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo coincide la proporción de aspecto del visor con el recurso.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La siguiente página de ejemplos ilustra un uso más real de la incrustación de diseño interactivo con una altura sin restricciones:

[Demostraciones en vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=es)

**Incrustación de diseño interactivo con anchura y altura definidas**

Si hay un diseño interactivo incrustado con la anchura y la altura definidas, el estilo de la página web es diferente; proporciona ambos tamaños al &quot;titular&quot; `DIV` y lo centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en 100%:

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

Los pasos de incrustación restantes son idénticos a la incrustación de diseño interactivo con altura sin restricciones. El ejemplo resultante es el siguiente:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Incrustación mediante API basada en el establecedor**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. Con esa API, el constructor no toma ningún parámetro y los parámetros de configuración se especifican utilizando los métodos API `setContainerId()`, `setParam()` y `setAsset()` con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra la incrustación de tamaño fijo con la API basada en establecedores:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
