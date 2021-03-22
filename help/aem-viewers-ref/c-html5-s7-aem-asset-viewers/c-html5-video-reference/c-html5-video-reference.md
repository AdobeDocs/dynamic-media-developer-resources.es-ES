---
description: El visor de vídeo es un reproductor de vídeo que reproduce flujo continuo y vídeo progresivo codificado en formato H.264. Se entrega desde Dynamic Media Classic o AEM Dynamic Media.
keywords: adaptable
solution: Experience Manager
title: Vídeo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2383'
ht-degree: 0%

---


# Vídeo{#video}

El visor de vídeo es un reproductor de vídeo que reproduce flujo continuo y vídeo progresivo codificado en formato H.264. Se entrega desde Dynamic Media Classic o AEM Dynamic Media.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Se admiten conjuntos de vídeo único y adaptable. Además, el visor admite el trabajo con flujos de vídeo progresivos y HLS alojados en ubicaciones externas. Está diseñado para funcionar tanto en exploradores web de escritorio como móviles que admiten vídeo HTML5. Este visor también admite subtítulos optativos que se muestran sobre el contenido de vídeo, la navegación por capítulos de vídeo y las herramientas de uso compartido en redes sociales.

El visor de vídeo utiliza la reproducción de vídeo de flujo HTML5 en formato HLS en su configuración predeterminada siempre que el sistema subyacente lo admita. En los sistemas que no admiten la transmisión por secuencias HTML5, el visor vuelve a la entrega de vídeo progresivo HTML5.

Tipo de visor 506.

## Demostración de URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Uso del visualizador de vídeo {#section-f21ac23d3f6449ad9765588d69584772}

El visor de vídeo representa un archivo JavaScript principal y un conjunto de archivos de ayuda, un solo JavaScript incluye todos los componentes del SDK de visor que utiliza este visor, recursos y CSS descargados por el visor en tiempo de ejecución.

Puede utilizar el visualizador de vídeo en modo emergente utilizando la página HTML preparada para la producción que se proporciona con los visualizadores IS. O bien, puede utilizar el visor en modo incrustado, donde se integra en una página web de destino mediante la API documentada.

La tarea de configurar y desollar el visor es similar a la de otros visores. Toda la apariencia se logra mediante CSS personalizada.

Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visualizadores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visualizador de vídeo {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visor de vídeo proporciona un conjunto de controles de interfaz de usuario estándar para la reproducción de vídeo, como un botón de reproducción/pausa, una burbuja de tiempo de vídeo de depurador, un indicador de tiempo de reproducción/tiempo total, un control de volumen, un botón de pantalla completa y un botón de subtítulos. Todos estos controles se agrupan en una barra de control en la parte inferior de la interfaz de usuario del visor.

En dispositivos táctiles, el control de volumen está oculto en la interfaz de usuario, ya que solo es posible controlar el volumen mediante los botones de hardware.

Cuando el visor funciona en modo emergente, el botón de pantalla completa no está disponible en la interfaz de usuario.

Es posible navegar rápidamente por el contenido de un vídeo cuando se activa el capítulo de vídeo. Los capítulos del vídeo se muestran como marcadores en la pista de desplazamiento de vídeo y muestran el título del capítulo y la descripción asociada al pasar el ratón sobre ellos o al tocar los sistemas táctiles. Los usuarios pueden buscar un capítulo en particular haciendo clic en un marcador de capítulo o tocando la burbuja de descripción del capítulo.

El visor admite la entrada táctil y la entrada de ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad está limitada únicamente a los navegadores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante teclado.

Consulte [Accesibilidad del teclado y navegación](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Herramientas de uso compartido en redes sociales con el Visor de vídeos {#section-907d316fe1da4b87abb9775f02464704}

El visualizador de vídeo es compatible con las herramientas de uso compartido de medios sociales Están disponibles como un solo botón en la interfaz de usuario que se expande a una barra de herramientas de uso compartido cuando el usuario hace clic o pulsa en ella.

La barra de herramientas de uso compartido contiene un icono para cada tipo de canal de uso compartido compatible, como Facebook, Twitter, uso compartido de correo electrónico, uso compartido de código incrustado y uso compartido de vínculos. Cuando se activan las herramientas de uso compartido por correo electrónico, uso compartido incrustado o uso compartido de vínculos, el visor muestra un cuadro de diálogo modal con un formulario de entrada de datos correspondiente. Cuando se llama a Facebook o Twitter, el visor redirige al usuario a un cuadro de diálogo estándar de uso compartido desde un servicio de medios sociales. Además, cuando se activa una herramienta de uso compartido, la reproducción de vídeo se pone en pausa automáticamente.

Las herramientas de uso compartido no están disponibles en el modo de pantalla completa debido a las restricciones de seguridad del explorador web.

## Incrustación del visualizador de vídeo {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo que, cuando se hace clic, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o en diferentes tamaños de ventana del navegador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: ventana emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

La incrustación de varios vídeos en la misma página se admite en tabletas y dispositivos móviles. En la mayoría de los casos, solo se puede reproducir un vídeo a la vez. Cuando un usuario comienza a reproducir un vídeo y luego intenta reproducir otro, el primer vídeo se pone en pausa automáticamente. El vídeo que se pausó automáticamente recuerda su tiempo de reproducción actual, de modo que el usuario siempre pueda volver a él y reanudar la reproducción. La única excepción en esta regla es el navegador Chrome en dispositivos Android 4.x, que pueden reproducir vídeos en paralelo.

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Toma todo el área de la ventana del explorador y se ajusta en caso de que se cambie el tamaño del explorador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor utilizando `window.open()` llamada de JavaScript, el elemento HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página HTML predeterminada para el modo de operación emergente. Se denomina [!DNL VideoViewer.html] y se encuentra en la subcarpeta [!DNL html5/] de la implementación estándar de los visores IS:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Puede lograr la personalización visual mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código HTML que abre el visor en una nueva ventana:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación interactivo**

En el modo integrado, el visor se añade a la página web existente, que puede tener ya contenido de cliente no relacionado con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de la página web.

El caso de uso principal son páginas web orientadas a equipos de escritorio o tabletas, así como páginas de diseño adaptables que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta opción es la mejor para páginas web con un diseño de página estático.

La incrustación de diseño interactivo supone que el visor puede tener que cambiar el tamaño en tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar el visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web para su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, sin restringir su altura, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Este método garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que utilizan un marco de diseño interactivo como Bootstrap, Foundation, etc.

De lo contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellena solo esa área y sigue el tamaño proporcionado por el diseño de la página web. Un buen ejemplo es integrar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Integración de tamaño fijo**

Para añadir el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   Para crear un visor es necesario agregar una etiqueta de script en el encabezado HTML. Antes de utilizar la API del visor, asegúrese de incluir [!DNL FlyoutViewer.js]. El archivo [!DNL FlyoutViewer.js] se encuentra en la subcarpeta [!DNL html5/js/] de la implementación estándar de los visores IS:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se suministra desde el mismo dominio. De lo contrario, se especifica una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tienen instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Solo debe hacer referencia al archivo JavaScript `include` del visor principal de la página. No debe hacer referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargar la lógica del visor durante la ejecución. En concreto, no haga referencia directamente a la biblioteca `Utils.js` del SDK de HTML5 cargada por el visor desde la ruta de contexto `/s7viewers` (denominada SDK consolidado `include`). El motivo es que la ubicación de las `Utils.js` o bibliotecas de visores de tiempo de ejecución similares se administra completamente mediante la lógica del visor y la ubicación cambia entre las versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, poner una referencia directa a cualquier JavaScript `include` secundario que utilice el visor en la página rompe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del contenedor DIV.

   Agregue un elemento DIV vacío a la página donde desee que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa más tarde a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la propiedad `position` CSS está establecida en `relative` o `absolute`.

   Asegúrese de que la función de pantalla completa funciona correctamente en Internet Explorer. Compruebe que no haya otros elementos en el DOM que tengan un orden de apilamiento superior al DIV del marcador de posición.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para la clase CSS de nivel superior `.s7videoviewer` en unidades absolutas o utilizando el modificador `stagesize`.

   El tamaño en CSS se puede colocar directamente en la página HTML o en un archivo CSS de visor personalizado, que más tarde se asigna a un registro preestablecido de visor en Dynamic Media Classic o se pasa explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor de vídeo](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) para obtener más información sobre cómo diseñar el visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en una página HTML:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede establecer el modificador `stagesize` en el registro preestablecido de visualizador en Dynamic Media Classic, o pasarlo explícitamente con el código de inicialización del visualizador con la colección `params` o como una llamada de API como se describe en la sección Referencia del comando , como se muestra a continuación:

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   Se recomienda un enfoque basado en CSS que se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.VideoViewer`, pase toda la información de configuración a su constructor e invoque el método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener un campo `containerId` que contenga el nombre del ID del contenedor de visor y el objeto `params` JSON anidado con parámetros de configuración admitidos por el visor. En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl`, la dirección URL del servidor de vídeo transferida como propiedad `videoserverurl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON le permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor de visor agregado al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación del DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta `BODY` de cierre o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de página web todavía. Por ejemplo, puede ocultarse utilizando el estilo `display:none` asignado. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web vuelve a poner el elemento contenedor en el diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   El siguiente es un ejemplo de creación de una instancia de visor, pasar al constructor las opciones de configuración mínimas necesarias y llamar al método `init()`. En este ejemplo se supone que `videoViewer` es la instancia del visor, `s7viewer` es el nombre del marcador de posición `DIV`, [!DNL http://s7d1.scene7.com/is/image/] es la URL del servicio de imágenes, [!DNL http://s7d1.scene7.com/is/content/] es la URL del servidor de vídeo y [!DNL Scene7SharedAssets/Glacier_Climber_MP4] es el recurso.

   ```
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

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visor de vídeo con un tamaño fijo:

   ```
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

**Diseño interactivo con altura ilimitada**

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible en su lugar que dicta el tamaño en tiempo de ejecución del contenedor del visor `DIV`. Para los fines de este ejemplo, supongamos que la página web permite que el contenedor `DIV` del visor tome el 40% del tamaño de la ventana del explorador web, sin restringir su altura. El código HTML de la página web tendría el siguiente aspecto:

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

Añadir el visor a una página de este tipo es muy similar a la incrustación de tamaño fijo; la única diferencia es que no es necesario definir explícitamente el tamaño del visor.

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor DIV.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Agregue el contenedor `DIV` al &quot; titular&quot; `DIV` existente. El siguiente código es un ejemplo completo. Puede ver cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo coincide la relación de aspecto del visor con el recurso.

```
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

La siguiente página de ejemplos ilustra un uso más real del diseño interactivo incrustado con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Diseño interactivo con anchura y altura definidas**

En caso de que el diseño interactivo se incruste con la anchura y la altura definidas, el estilo de la página web es diferente; proporciona ambos tamaños al &quot; holder&quot; `DIV` y céntrelo en la ventana del navegador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en 100%:

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

Los pasos de incrustación restantes son idénticos a la incrustación de diseño interactivo con altura ilimitada. El ejemplo resultante es el siguiente:

```
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

**Incrustación mediante API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor no-args. Con esa API, el constructor no toma ningún parámetro y los parámetros de configuración se especifican usando métodos de API `setContainerId()`, `setParam()` y `setAsset()` con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra la incrustación de tamaño fijo con la API basada en establecedor:

```
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

