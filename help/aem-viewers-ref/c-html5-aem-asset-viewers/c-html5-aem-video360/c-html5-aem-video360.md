---
title: Video360
description: El visualizador HTML5 Video360 es un reproductor de vídeo de 360 grados que reproduce flujo continuo y vídeo progresivo de 360 codificado en formato H.264, entregado desde Dynamic Media Classic o desde Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2561'
ht-degree: 0%

---

# Video360{#video}

El visualizador HTML5 Video360 es un reproductor de vídeo de 360 grados que reproduce flujo continuo y vídeo progresivo de 360 codificado en formato H.264, entregado desde Dynamic Media Classic o desde Adobe Experience Manager, Dynamic Media.

Los vídeos de 360 grados, también conocidos como vídeos inmersivos o vídeos esféricos, son grabaciones de vídeo en las que se graba una vista en todas las direcciones al mismo tiempo, grabadas con una cámara omnidireccional o una colección de cámaras. Se admiten conjuntos de vídeos adaptables y de vídeo únicos. El visor también admite el trabajo con flujos de vídeo progresivos y HLS alojados en una ubicación externa.

La proporción de aspecto recomendada para el vídeo de 360 es 2:1. No se admite el sonido espacial. El visor está diseñado para trabajar únicamente con vídeo 360; si se intenta reproducir un vídeo que no sea 360, se producirá una reproducción de vídeo distorsionada.

El visor está diseñado para funcionar tanto en exploradores web de escritorio como móviles compatibles con vídeo HTML5. El visor admite herramientas opcionales de uso compartido en redes sociales.

El Visor Video360 utiliza la reproducción de vídeo de flujo HTML5 en formato HLS en su configuración predeterminada siempre que el sistema subyacente admita eso. En sistemas que no admiten el streaming de HTML5, el visor vuelve a recibir la entrega de vídeo progresivo de HTML5.

Tipo de visor 517.

## URL de demostración {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Requisitos del sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso del visor Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer representa un archivo JavaScript principal y un conjunto de archivos de ayuda (una sola inclusión JavaScript con todos los componentes HTML5 Viewer SDK utilizados por este visor, recursos, CSS) descargados por el visor en tiempo de ejecución.

El visualizador HTML5 Video360 se puede utilizar tanto en modo emergente utilizando la página de HTML lista para la producción proporcionada con visores IS como en modo incrustado, donde se integra en la página web de destino mediante una API documentada.

La configuración y el desollado son similares a los de los demás visores descritos en esta guía. Todo el desollado se logra mediante hojas de estilo en cascada personalizadas (CSS).

Ver [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

El contenido de vídeo 360 requiere ajustes de codificación más altos que el vídeo estándar que no es 360. En otras palabras, el contenido 360 debe tener una resolución mayor que el vídeo no 360 para lograr la misma calidad perceptible. Se recomienda tener en cuenta los siguientes ajustes preestablecidos de vídeo adaptable para vídeo 360:

* 720p, 2.500 kbps
* 1080p, 5000 kbps
* 1440p, 6.600 kbps

Sin embargo, tenga en cuenta que para servir vídeo codificado con estos ajustes de alta calidad se requiere una conexión de alto ancho de banda en el dispositivo de un usuario final.

## Interactuar con el visor de Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

El visor HTML5 Video360 proporciona un conjunto de controles de interfaz de usuario estándar para la reproducción de vídeo, como un botón de reproducción/pausa, una burbuja de tiempo de vídeo de selección manual, un indicador de tiempo de reproducción/tiempo total, un control de volumen y un botón de pantalla completa. Todos estos controles se agrupan en barras de control en la parte inferior de la interfaz de usuario del visor.

En dispositivos táctiles, el control de volumen se oculta de la interfaz de usuario, ya que solo es posible controlar el volumen mediante los botones de hardware del dispositivo.

Cuando el visor funciona en modo emergente, no hay ningún botón de pantalla completa disponible en la interfaz de usuario.

El visualizador también admite varias herramientas de uso compartido de medios sociales. Están disponibles como un solo botón en la interfaz de usuario que se expande hasta una barra de herramientas compartida cuando el usuario hace clic o pulsa en ella. La barra de herramientas para compartir contiene un icono para cada tipo de canal de uso compartido admitido, como Facebook, Twitter, correo electrónico compartido, código compartido incrustado y vínculo compartido. Cuando se activan las herramientas de uso compartido de correo electrónico, de incrustación de recursos compartidos o de vínculo compartido, el visor muestra un cuadro de diálogo modal con el formulario de entrada de datos correspondiente. Cuando se llama a Facebook o Twitter, el visor redirige al usuario a un cuadro de diálogo de uso compartido estándar desde un servicio de medios sociales. Además, cuando se activa una herramienta de uso compartido, la reproducción de vídeo se detiene automáticamente. Las herramientas de uso compartido no están disponibles en el modo de pantalla completa debido a las restricciones de seguridad del explorador web.

El visor admite la reproducción de vídeo 360 en los siguientes casos:

* Auriculares de realidad virtual (como Oculus Go y Oculus Rift)
* Montajes VR HMD (pantalla montada en el cabezal) (como Google Cardboard)
* Dispositivos no habilitados para VR (como navegadores de escritorio, tabletas y teléfonos móviles no conectados a montajes VR HMD)

No es necesaria ninguna configuración adicional para ver contenido de vídeo 360 en auriculares de realidad virtual. El visor detecta automáticamente la presencia de auriculares de realidad virtual y muestra el botón &quot;VR&quot; encima del contenido de vídeo. Al activar este botón &quot;VR&quot;, el procesamiento de vídeo cambia al modo VR. El visor solo admite el procesamiento de RV en exploradores compatibles con WebVR.

Para usar montajes VR HMD, el modificador `Video360Player.vrrender` debe establecerse en `1` en la configuración del visor, lo que fuerza la representación estereoscópica.

En los auriculares de realidad virtual y los soportes VR HMD, el cambio de punto de vista se produce en respuesta al movimiento de los auriculares, no se proporciona ningún otro control de reproducción en el modo VR.

Al ver vídeo 360 en dispositivos que no tienen VR habilitado, el usuario final puede utilizar el ratón, el tacto o el teclado para controlar la reproducción del vídeo y el punto de vista.

El visor admite la entrada táctil y la entrada del ratón en dispositivos Windows con pantalla táctil y ratón; sin embargo, esta compatibilidad se limita únicamente a los exploradores web Chrome, Internet Explorer 11 y Edge.

El visor es totalmente accesible mediante el teclado. Consulte [Navegación y accesibilidad por teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor de Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Las distintas páginas web tienen diferentes necesidades de comportamiento del visualizador. A veces, una página web proporciona un vínculo que, al seleccionarlo, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

La incrustación de varios vídeos en la misma página es compatible con tabletas y dispositivos móviles. Normalmente, sólo se puede reproducir un vídeo a la vez. Cuando un usuario comienza a reproducir un vídeo y luego intenta reproducir otro, el primer vídeo se pausa automáticamente. El vídeo en pausa automática recuerda su tiempo de reproducción actual, por lo que el usuario siempre puede volver a él y reanudar la reproducción. La única excepción a esta regla es el navegador Chrome en dispositivos Android™ 4.x, que puede reproducir vídeos en paralelo.

**Modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Ocupa todo el área de la ventana del explorador y se ajusta en caso de que se cambie el tamaño del explorador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante la llamada de JavaScript `window.open()`, el elemento HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página de HTML predeterminada para el modo de operación emergente. Se llama [!DNL Video360Viewer.html] y se encuentra en la subcarpeta [!DNL html5/] de su implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Puede conseguir una personalización visual aplicando CSS personalizado.

A continuación se muestra un ejemplo de código HTML que abre el visor en una nueva ventana:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo incrustado, el visor se añade a la página web existente, que puede tener ya contenido de clientes no relacionado con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de una página web.

Los casos de uso principales son páginas web orientadas para equipos de escritorio o tabletas, y también páginas diseñadas interactivas que ajustan el diseño automáticamente según el tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Este método es la mejor opción para las páginas web que tienen un diseño estático.

La incrustación de diseño interactivo supone que el visor debe cambiar de tamaño durante la ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es añadir un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente según la forma en que la página web ajusta el tamaño de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV` y deja su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad garantiza que el recurso se ajuste perfectamente a la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que utilizan marcos de diseño web adaptables como Bootstrap y Foundation.

De lo contrario, si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellena sólo esa área y sigue el tamaño que proporciona el diseño de página web. Un buen ejemplo es la incrustación del visualizador en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definir el contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo de JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado de HTML. Antes de usar la API de visor, asegúrese de incluir [!DNL Video360Viewer.js]. El archivo [!DNL Video360Viewer.js] se encuentra en la subcarpeta [!DNL html5/js/] de su implementación estándar de visores IS:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tengan instalados los visores de IIS.

La ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Solo haga referencia al archivo de JavaScript `include` del visor principal en su página. No haga referencia a ningún archivo JavaScript adicional en el código de la página web que la lógica del visor pueda descargar durante la ejecución. En particular, no haga referencia directamente a la biblioteca HTML5 SDK `Utils.js` cargada por el visor desde la ruta de contexto `/s7viewers` (denominada SDK consolidado `include`). El motivo es que la ubicación de `Utils.js` o bibliotecas similares del visor en tiempo de ejecución está completamente administrada por la lógica del visor y la ubicación cambia entre versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, al establecer una referencia directa a cualquier JavaScript `include` secundario que use el visor en la página, se interrumpe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definir el contenedor `DIV`.

   Agregue un elemento `DIV` vacío a la página donde desea que aparezca el visor. El elemento `DIV` debe tener su ID definido, ya que este ID se pasa posteriormente a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El marcador de posición `DIV` es un elemento posicionado, lo que significa que la propiedad CSS `position` está establecida en `relative` o `absolute`.

   Para que la característica de pantalla completa funcione correctamente en Internet Explorer, asegúrese de que no haya otros elementos en el DOM que tengan un orden de apilamiento mayor que el marcador de posición `DIV`.

   A continuación se muestra un ejemplo de un elemento `DIV` de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para la clase CSS de nivel superior `.s7video360viewer` en unidades absolutas o utilizando el modificador `stagesize`.

   Puede establecer el tamaño en CSS directamente en la página de HTML o en un archivo CSS de visor personalizado, que luego se asigna a un registro de ajuste preestablecido de visor en Adobe Experience Manager Assets bajo demanda o se pasa explícitamente mediante el comando `style`.

   Consulte [Personalización del visor de Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en la página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Puede establecer el modificador `stagesize` en el registro de ajustes preestablecidos de visualizador en AEM Assets bajo demanda. O bien, puede pasarlo explícitamente con el código de inicialización del visor con la colección `params`, o como una llamada de API como se describe en la sección Referencia de comandos, de esta manera:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Se recomienda un enfoque basado en CSS y se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.Video360Viewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el campo `containerId` que contiene el nombre del ID del contenedor del visor y el objeto JSON `params` anidado con parámetros de configuración admitidos por el visor.

   En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON le permite crear e iniciar el visor con una sola línea de código, la URL del servidor de vídeo pasada como propiedad de `videoserverurl`, el recurso inicial como parámetro de `asset` y los datos interactivos como propiedad de `interactivedata`. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta de cierre `BODY` o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, se puede ocultar usando el estilo `display:none` asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando esto sucede, la carga del visualizador se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar al método `init()`. El ejemplo supone lo siguiente:

   * La instancia del visor es `video360Viewer`.
   * El nombre del marcador de posición `DIV` es `s7viewer`.
   * La URL del servicio de imágenes es `https://s7d9.scene7.com/is/image`.
   * La URL del servidor de vídeo es `https://s7d9.scene7.com/is/content`.
   * El recurso es `Viewers/space_station_360-AVS`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visor de Video360 con un tamaño fijo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Inserción de diseño interactivo con altura sin restricciones**

Con incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que dicta el tamaño de tiempo de ejecución del contenedor del visor `DIV`. En el siguiente ejemplo, supongamos que la página web permite que el contenedor del visor `DIV` ocupe el 40% del tamaño de la ventana del explorador web, sin restringir su altura. El código HTML de la página web tendría el siguiente aspecto:

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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incrustación interactiva con anchura y altura definidas**

Si hay una incrustación adaptable con anchura y altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños al DIV `"holder"` y lo centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en un 100 por ciento.

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

El resto de los pasos de incrustación son idénticos a los pasos utilizados para la incrustación adaptable con altura sin restricciones. El ejemplo resultante es el siguiente:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incrustación mediante API basada en el establecedor**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante los métodos de API `setContainerId()`, `setParam()` y `setAsset()` con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de la incrustación de tamaño fijo con la API basada en establecedores:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
