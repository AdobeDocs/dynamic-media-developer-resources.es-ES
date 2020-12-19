---
description: El visor de vídeo HTML5 Video360 es un reproductor de vídeo de 360 grados que reproduce flujo continuo y vídeo progresivo de 360 grados codificado en el formato H.264, entregado desde Scene7 Publishing System o desde AEM Dynamic Media.
seo-description: El visor de vídeo HTML5 Video360 es un reproductor de vídeo de 360 grados que reproduce flujo continuo y vídeo progresivo de 360 grados codificado en el formato H.264, entregado desde Scene7 Publishing System o desde AEM Dynamic Media.
seo-title: Video360
solution: Experience Manager
title: Video360
topic: Dynamic media
uuid: b03e6289-e012-4c62-835f-814463a27774
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '2613'
ht-degree: 0%

---


# Video360{#video}

El visor de vídeo HTML5 Video360 es un reproductor de vídeo de 360 grados que reproduce flujo continuo y vídeo progresivo de 360 grados codificado en el formato H.264, entregado desde Scene7 Publishing System o desde AEM Dynamic Media.

Los vídeos de 360 grados, también conocidos como vídeos envolventes o vídeos esféricos, son grabaciones de vídeo en las que se graba una vista en todas las direcciones al mismo tiempo, grabadas con una cámara omnidireccional o una colección de cámaras. Se admiten los conjuntos de vídeos únicos y los conjuntos de vídeos adaptables. El visor también admite el trabajo con flujos de vídeo progresivo y HLS alojados en una ubicación externa.

La proporción de aspecto recomendada para vídeos de 360 es de 2:1. No se admite el sonido espacial. El visor está diseñado para funcionar solo con vídeo de 360°; un intento de reproducir un vídeo que no sea 360 produce una reproducción de vídeo distorsionada.

El visor está diseñado para funcionar tanto en navegadores web de escritorio como móviles compatibles con vídeo HTML5. El visor admite herramientas de uso compartido en redes sociales opcionales.

El visor de vídeo360 utiliza la reproducción de vídeo de flujo HTML5 en formato HLS en su configuración predeterminada siempre que el sistema subyacente lo admita. En sistemas que no admiten el flujo HTML5, el visor vuelve al envío de vídeo progresivo HTML5.

El tipo de visor es 517.

## Direcciones URL de demostración {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Requisitos del sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso del visor de Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

El visor de vídeo HTML5 360 representa un archivo JavaScript principal y un conjunto de archivos auxiliares (un solo JavaScript incluye todos los componentes del SDK de visor HTML5 utilizados por este visor en particular, los recursos y CSS) descargados por el visor en tiempo de ejecución.

El visor de vídeo HTML5 360 se puede utilizar en modo emergente mediante una página HTML preparada para la producción que se proporciona con los visores IS o en modo incrustado, donde se integra en la página web de destinatario mediante API documentada.

La configuración y la aplicación de aspectos son similares a las de los demás visores descritos en esta guía. Todas las apariencias se logran mediante hojas de estilo en cascada (CSS) personalizadas.

Consulte [Referencia de comandos común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comandos común a todos los visores: URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

El contenido de vídeo de 360 requiere una configuración de codificación superior a la del vídeo estándar que no es de 360. En otras palabras, el contenido de 360 debe tener una resolución mayor que el vídeo que no sea de 360 para lograr la misma calidad percibible. Se recomienda considerar los siguientes ajustes preestablecidos de vídeo adaptables para vídeos de 360:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Sin embargo, tenga en cuenta que el servicio de vídeo codificado con una configuración de alta calidad requiere una conexión de ancho de banda alta en el dispositivo del usuario final.

## Interacción con el visor de Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

El visor de vídeo HTML5 Video360 proporciona un conjunto de controles de interfaz de usuario estándar para la reproducción de vídeo, como botón de reproducción/pausa, burbuja de tiempo de vídeo de la barra de desplazamiento, indicador de tiempo de reproducción/tiempo total, control de volumen y botón de pantalla completa. Todos estos controles se agrupan en una barra de control en la parte inferior de la interfaz de usuario del visor.

Tenga en cuenta que en dispositivos táctiles el control de volumen está oculto en la interfaz de usuario, ya que sólo es posible controlar el volumen mediante los botones de hardware del dispositivo.

Cuando el visor funciona en modo emergente, no hay un botón de pantalla completa disponible en la interfaz de usuario.

El visor también admite una serie de herramientas de uso compartido en medios sociales. Están disponibles como un solo botón en la interfaz de usuario que se expande a una barra de herramientas de uso compartido cuando el usuario hace clic o toca en ella. La barra de herramientas de uso compartido contiene un icono para cada tipo de canal de uso compartido admitido, como Facebook, Twitter, uso compartido de correo electrónico, código incrustado y uso compartido de vínculos. Cuando se activan las herramientas de uso compartido de correo electrónico, uso compartido incrustado o uso compartido de vínculos, el visor muestra un cuadro de diálogo modal con el correspondiente formulario de entrada de datos. Cuando se llama a Facebook o Twitter, el visor redirige al usuario a un cuadro de diálogo de uso compartido estándar desde un servicio de medios sociales. Además, cuando se activa una herramienta de uso compartido, la reproducción de vídeo se pausa automáticamente. Las herramientas de uso compartido no están disponibles en modo de pantalla completa debido a las restricciones de seguridad del explorador web.

El visor admite 360 reproducciones de vídeo en auriculares VR (como Oculus Go y Oculus Rift), montajes VR HMD (pantalla montada en el cabezal) y dispositivos no habilitados para VR (como exploradores de escritorio, tabletas y teléfonos móviles no conectados a montajes VR HMD).

No es necesaria ninguna configuración adicional para la vista del contenido de vídeo 360 en los auriculares VR. El visor detecta automáticamente la presencia de auriculares VR y muestra el botón &quot;VR&quot; encima del contenido del vídeo. Al activar este botón &quot;VR&quot; se cambia el procesamiento de vídeo al modo VR. El visor solo admite el procesamiento de VR en navegadores compatibles con WebVR.

Para utilizar montajes HMD de VR, el modificador `Video360Player.vrrender` debe configurarse en `1` en la configuración del visor, lo que fuerza el procesamiento estereoscópico.

En los auriculares VR y los montes VR HMD, el cambio de punto de vista se produce en respuesta al movimiento de auriculares, no se proporciona ningún otro control de reproducción en el modo VR.

Al ver vídeos 360 en dispositivos que no están habilitados para VR, el usuario final puede utilizar el ratón, el tacto o el teclado para controlar la reproducción de vídeo y el punto de vista.

El visor admite entrada táctil y entrada de ratón en dispositivos Windows con pantalla táctil y ratón; sin embargo, esta compatibilidad está limitada a los exploradores web Chrome, Internet Explorer 11 y Edge únicamente.

El visor es totalmente accesible mediante el teclado. Consulte [Navegación y accesibilidad del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor de Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo que, al hacer clic en él, abre el visor en una ventana de explorador independiente. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, es posible que la página web tenga un diseño de página estático o utilice un diseño interactivo que se muestre de forma diferente en distintos dispositivos o en diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: ventana emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

La incrustación de varios vídeos en la misma página es compatible con tabletas y dispositivos móviles. En la mayoría de los casos, solo se puede reproducir un vídeo a la vez. Cuando un usuario inicio de reproducir un vídeo y luego intenta reproducir otro vídeo, el primer vídeo se pone en pausa automáticamente. El vídeo en pausa automática recuerda el tiempo de reproducción actual, de modo que el usuario siempre puede volver a él y reanudar la reproducción. La única excepción es que esta regla está en el navegador Chrome en dispositivos Android 4.x, que pueden reproducir vídeos en paralelo.

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o ficha separada del explorador Web. Toma todo el área de la ventana del navegador y se ajusta en caso de que se cambie el tamaño del navegador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante `window.open()` llamada de JavaScript, elemento HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página HTML lista para usar en el modo de operación emergente. Se denomina [!DNL Video360Viewer.html] y se encuentra en la subcarpeta [!DNL html5/] de la implementación estándar de los visores de IS:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Puede lograr la personalización visual mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código HTML que abre el visor en una ventana nueva:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo incrustado, el visor se agrega a la página web existente, que puede tener ya contenido de cliente no relacionado con el visor. Normalmente, el visor ocupa solo una parte del espacio de una página web.

Los casos de uso principales son páginas web orientadas a equipos de escritorio o tabletas, y también páginas diseñadas con capacidad de respuesta que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta es la mejor opción para las páginas web con un diseño estático.

La incrustación de diseño adaptable supone que el visor puede necesitar cambiar el tamaño en tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, dejando su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para las páginas Web que utilizan marcos de diseño de Web interactivos como Bootstrap, Foundation, etc.

De lo contrario, si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellena esa área y sigue el tamaño que proporciona el diseño de la página web. Un buen ejemplo es la incrustación del visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del navegador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor en la página web.

   La creación de un visor requiere que agregue una etiqueta de script en el encabezado HTML. Antes de usar la API de visor, asegúrese de incluir [!DNL Video360Viewer.js]. El archivo [!DNL Video360Viewer.js] se encuentra en la subcarpeta [!DNL html5/js/] de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se suministra desde el mismo dominio. En caso contrario, especifique una ruta completa a uno de los servidores Adobe Dynamic Media Classic que tenga instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
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

   Para que la función de pantalla completa funcione correctamente en Internet Explorer, asegúrese de que no haya otros elementos en el DOM que tengan un orden de apilamiento superior al del marcador de posición `DIV`.

   A continuación se muestra un ejemplo de un elemento de marcador de posición definido `DIV`:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para la clase CSS de nivel superior `.s7video360viewer` en unidades absolutas o utilizando el modificador `stagesize`.

   Puede colocar el tamaño en CSS directamente en la página HTML o en un archivo CSS de visor personalizado, que posteriormente se asignará a un registro de ajuste preestablecido de visor en AEM Assets (On-demand) o se pasará explícitamente mediante el comando `style`.

   Consulte [Personalización del visor de vídeo360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en la página HTML:

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Puede establecer el modificador `stagesize` en el registro de ajustes preestablecidos de visor en AEM Assets, bajo demanda. O bien, puede pasarlo explícitamente con el código de inicialización del visor con la colección `params` o como una llamada de API como se describe en la sección Referencia de comandos, como se muestra a continuación:

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   En este ejemplo se recomienda un enfoque basado en CSS.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.Video360Viewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener un campo `containerId` que contenga el nombre del ID de contenedor del visor y el objeto JSON anidado `params` con parámetros de configuración admitidos por el visor.

   En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON permite crear y inicio del visor con una sola línea de código, una URL del servidor de vídeo pasada como propiedad `videoserverurl`, un recurso inicial como parámetro `asset` y datos interactivos como propiedad `interactivedata`. La API de inicialización basada en JSON permite crear y inicio del visor con una sola línea de código.

   Es importante que el contenedor del visor se añada al DOM para que el código del visor pueda encontrar el elemento de contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta `BODY` de cierre o en el evento body `onload()`.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web. Por ejemplo, puede ocultarse con el estilo `display:none` asignado. En este caso, el visor retrasa el proceso de inicialización hasta el momento en que la página web devuelve el elemento de contenedor a la presentación. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de creación de una instancia de visor, pasando las opciones de configuración mínimas necesarias al constructor y llamando al método `init()`. El ejemplo asume lo siguiente:

   * La instancia del visor es `video360Viewer`.
   * El nombre del marcador de posición `DIV` es `s7viewer`.
   * La dirección URL del servicio de imágenes es `https://s7d9.scene7.com/is/image`.
   * La dirección URL del servidor de vídeo es `https://s7d9.scene7.com/is/content`.
   * El recurso es `Viewers/space_station_360-AVS`.

   ```
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

   El siguiente código es un ejemplo completo de una página web trivial que incorpora el visor Video360 con un tamaño fijo:

   ```
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

**Incrustación de diseño adaptable con altura ilimitada**

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

Añadir el visor a una página de este tipo es similar a los pasos para la incrustación de tamaño fijo. La única diferencia es que no es necesario definir explícitamente el tamaño del visor.

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición de la DIV de contenedor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Añada la DIV de contenedor a la DIV existente `"holder"`. El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del navegador y cómo coincide la proporción de aspecto del visor con el recurso.

```
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

**Incrustación adaptable con anchura y altura definidas**

En caso de incrustación interactiva con anchura y altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños a la DIV `"holder"` y la centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en 100 por ciento.

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

**Incrustación mediante API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en setter y el constructor no-args. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante métodos de API `setContainerId()`, `setParam()` y `setAsset()` con llamadas JavaScript independientes.

El siguiente ejemplo ilustra el uso de la incrustación de tamaño fijo con la API basada en establecedor:

```
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

