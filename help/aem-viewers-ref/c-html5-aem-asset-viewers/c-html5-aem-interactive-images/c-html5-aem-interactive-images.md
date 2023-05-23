---
title: Imagen interactiva
description: El visualizador de imágenes interactivo es un visualizador que muestra una sola imagen no ampliable con zonas interactivas en las que se puede hacer clic. El propósito de este visor es implementar una experiencia de "banner de ventas". Es decir, el usuario puede seleccionar un punto interactivo sobre la imagen del titular y ser redirigido a una vista rápida o a una página de detalles del producto en el sitio web. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1720'
ht-degree: 0%

---

# Imagen interactiva{#interactive-image}

El visualizador de imágenes interactivo es un visualizador que muestra una sola imagen no ampliable con zonas interactivas en las que se puede hacer clic. El propósito de este visor es implementar una experiencia de &quot;banner de ventas&quot;. Es decir, el usuario puede seleccionar un punto interactivo sobre la imagen del titular y ser redirigido a una vista rápida o a una página de detalles del producto en el sitio web. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor.

Tipo de visor 508.

## URL de demostración {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## Requisitos del sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso del visualizador de imágenes interactivo {#section-e6c68406ecdc4de781df182bbd8088b4}

El visualizador de imágenes interactivo representa un archivo JavaScript principal y un conjunto de archivos de ayuda (una sola inclusión JavaScript con todos los componentes del SDK del visualizador utilizados por este visualizador, los recursos y el CSS) descargados por el visualizador en tiempo de ejecución.

El visualizador de imágenes interactivo solo se puede utilizar en modo incrustado, donde se integra en la página web de destino mediante la API documentada.

La configuración y el aspecto son similares a los de los otros visores descritos en esta Ayuda. Todo el desollado se logra mediante CSS personalizado.

Consulte [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visualizador de imágenes interactivo {#section-642e66ca38cd4032992840ec6c0b0cd2}

La interacción que admite el visualizador de imágenes de vídeo es la activación de puntos interactivos en sistemas de escritorio. Esta activación se produce al hacer clic y en dispositivos táctiles con un solo toque.

El visor es totalmente accesible mediante el teclado.

Consulte [Navegación y accesibilidad del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visualizador de imágenes interactivo {#section-6bb5d3c502544ad18a58eafe12a13435}

El visualizador de imágenes interactivo está incrustado en la página de alojamiento. Esta página web puede tener un diseño estático o puede ser &quot;adaptable&quot; y mostrarse de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador.

Para satisfacer estas necesidades, el visor admite dos modos de operación principales: incrustación de tamaño fijo e incrustación adaptable.

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo incrustado, el visor se agrega a la página web existente. Es posible que esta página web ya tenga algunos contenidos de clientes no relacionados con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de una página web.

Los casos de uso principales son páginas web orientadas para equipos de escritorio o tabletas, y páginas con diseño interactivo que ajustan el diseño automáticamente según el tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Este método es la mejor opción para las páginas web que tienen un diseño estático.

La incrustación de diseño interactivo supone que el visualizador debe cambiar de tamaño durante la ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es añadir un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente según la forma en que la página web ajusta el tamaño de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`Sin embargo, y sin restricciones de altura, el visualizador elige automáticamente su altura según la relación de aspecto del recurso utilizado. Esta funcionalidad garantiza que el recurso se ajuste perfectamente a la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que utilizan marcos de diseño web adaptables como Bootstrap y Foundation.

En caso contrario, si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellena solo esa área. También sigue el tamaño que proporciona el diseño de página web. Un buen ejemplo es la incrustación del visualizador en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado del HTML. Antes de usar la API de visor, asegúrese de incluir lo siguiente [!DNL InterativeImage.js]. El [!DNL InteractiveImage.js] El archivo se encuentra en [!DNL html5/js/] de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tengan instalados los visores de IIS.

La ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Solo referencia al visor principal JavaScript `include` en la página. No haga referencia a ningún archivo JavaScript adicional en el código de la página web que la lógica del visor pueda descargar durante la ejecución. En concreto, no haga referencia directamente al SDK de HTML5 `Utils.js` biblioteca cargada por el visor desde `/s7viewers` ruta de contexto (denominado SDK consolidado) `include`). El motivo es que la ubicación de `Utils.js` Para bibliotecas de visualizadores en tiempo de ejecución similares, la lógica del visualizador las gestiona completamente y la ubicación cambia entre versiones del visualizador. El Adobe no mantiene las versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, se hace referencia directa a cualquier JavaScript secundario `include` que el usuario utiliza en la página interrumpe la funcionalidad del usuario en el futuro cuando se implemente una nueva versión del producto.

1. Definición del contenedor `DIV`.

   Añadir un vacío `DIV` a la página donde desea que aparezca el visor. El `DIV` debe tener su ID definido, ya que este ID se pasa posteriormente a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El marcador de posición `DIV` es un elemento posicionado, lo que significa que la variable `position` La propiedad CSS se establece en `relative` o `absolute`.

   El siguiente es un ejemplo de marcador de posición definido `DIV` elemento:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para `.s7interactiveimage` clase CSS de nivel superior en unidades absolutas o utilizando `stagesize` modificador.

   Puede poner el tamaño en CSS directamente en la página del HTML. O bien, puede colocar el tamaño en un archivo CSS de visor personalizado, que luego se asigna a un registro de ajuste preestablecido de visor en Adobe Experience Manager Assets: bajo demanda o se pasa explícitamente mediante `style` comando.

   Consulte [Vídeo](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en la página del HTML:

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Puede pasar explícitamente el `stagesize` modificador con el código de inicialización del visor con `params` o como una llamada API como se describe en la sección Referencia de comandos, de esta manera:

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Se recomienda un enfoque basado en CSS y se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.InteractiveImage` , pase toda la información de configuración a su constructor y llame a `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener `containerId` campo que contiene el nombre del ID de contenedor del visor y el valor anidado `params` Objeto JSON con parámetros de configuración admitidos por el visor. En este caso, la variable `params` el objeto debe tener al menos la URL del servicio de imágenes pasada como `serverUrl` y el recurso inicial como `asset` parámetro. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` método justo antes del cierre `BODY` o en el cuerpo `onload()` evento.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, se puede ocultar usando `display:none` estilo asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando este evento se produce, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar a `init()` método. El ejemplo supone `interactiveImage` es la instancia del visualizador; `s7viewer` es el nombre del marcador de posición `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` es la URL del servicio de imágenes y `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` es el recurso:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visualizador de imágenes de vídeo con un tamaño fijo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Inserción de diseño interactivo con altura sin restricciones**

Con incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que dicta el tamaño de tiempo de ejecución del contenedor del visualizador `DIV`. En el siguiente ejemplo, supongamos que la página web permite el contenedor del visor `DIV` para obtener el 40 % del tamaño de la ventana del explorador web. Y, su altura se deja sin restricciones. El código del HTML de la página web tendría el siguiente aspecto:

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

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Añadir el contenedor `DIV` a la existente `"holder"` `DIV`. El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo la proporción de aspecto del visor coincide con el recurso.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La siguiente página de ejemplos ilustra usos más reales del diseño interactivo incrustado con una altura sin restricciones:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**Incrustación de tamaño flexible con anchura y altura definidas**

Si hay una incrustación de tamaño flexible con la anchura y la altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños a la `"holder"` DIV y centrarlo en la ventana del explorador. Además, la página web establece el tamaño del `HTML` y `BODY` elemento al 100 por ciento.

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
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Incrustación mediante una API basada en el establecedor**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante `setContainerId()`, `setParam()`, y `setAsset()` Métodos de API con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de la incrustación de tamaño fijo con la API basada en establecedores:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```
