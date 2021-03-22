---
description: El visualizador de imágenes interactivo es un visualizador que muestra una sola imagen no ampliable con zonas interactivas en las que se puede hacer clic. El objetivo de este visor es implementar una experiencia de "banner de ventas". Es decir, el usuario puede seleccionar un punto interactivo sobre la imagen del banner y ser redirigido a una vista rápida o a una página de detalles del producto en el sitio web. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.
seo-description: El visualizador de imágenes interactivo es un visualizador que muestra una sola imagen no ampliable con zonas interactivas en las que se puede hacer clic. El objetivo de este visor es implementar una experiencia de "banner de ventas". Es decir, el usuario puede seleccionar un punto interactivo sobre la imagen del banner y ser redirigido a una vista rápida o a una página de detalles del producto en el sitio web. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.
seo-title: Imagen interactiva
solution: Experience Manager
title: Imagen interactiva
uuid: 18b7a0c3-c047-4ce1-8920-1d8ebc1ab60e
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1817'
ht-degree: 0%

---


# Imagen interactiva{#interactive-image}

El visualizador de imágenes interactivo es un visualizador que muestra una sola imagen no ampliable con zonas interactivas en las que se puede hacer clic. El objetivo de este visor es implementar una experiencia de &quot;banner de ventas&quot;. Es decir, el usuario puede seleccionar un punto interactivo sobre la imagen del banner y ser redirigido a una vista rápida o a una página de detalles del producto en el sitio web. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content).

El tipo de visor es 508.

## Demostración de URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html)

## Requisitos del sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso del visualizador de imágenes interactivo {#section-e6c68406ecdc4de781df182bbd8088b4}

El visualizador de imágenes interactivo representa un archivo JavaScript principal y un conjunto de archivos de ayuda (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visualizador en particular, recursos y CSS) descargados por el visualizador en tiempo de ejecución.

El visualizador de imágenes interactivo solo se puede utilizar en modo incrustado, donde se integra en la página web de destino mediante la API documentada.

La configuración y el desollado son similares a los de los demás visores descritos en esta Ayuda. Toda la apariencia se logra mediante CSS personalizada.

Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visualizadores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visualizador de imágenes interactivo {#section-642e66ca38cd4032992840ec6c0b0cd2}

La interacción compatible con el Visor de imágenes de vídeo es la activación de puntos interactivos en sistemas de escritorio. Esta activación se produce al hacer clic y en dispositivos táctiles con un solo toque.

El visor es totalmente accesible mediante teclado.

Consulte [Accesibilidad del teclado y navegación](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visualizador de imágenes interactivo {#section-6bb5d3c502544ad18a58eafe12a13435}

El visualizador de imágenes interactivo está diseñado para incrustarse en la página de alojamiento. Esta página web puede tener un diseño estático o puede ser &quot;interactiva&quot; y mostrarse de forma diferente en distintos dispositivos o en diferentes tamaños de ventana del navegador.

Para satisfacer estas necesidades, el visor admite dos modos de operación principales: incrustación de tamaño fijo e incrustación interactiva.

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo incrustado, el visor se añade a la página web existente. Es posible que esta página web ya tenga contenido de cliente que no esté relacionado con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de una página web.

Los casos de uso principales son páginas web orientadas a equipos de escritorio o tabletas, y páginas diseñadas con capacidad de respuesta que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta es la mejor opción para páginas web con diseño estático.

La incrustación de diseño interactivo supone que el visor puede tener que cambiar el tamaño durante la ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web para su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, sin restringir su altura, el visor elige automáticamente su altura según la proporción de aspecto del recurso utilizado. Esta funcionalidad garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para las páginas web que usan marcos de diseño web interactivos como Bootstrap, Foundation, etc.

De lo contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellena solo esa área. También sigue el tamaño que proporciona el diseño de página web. Un buen ejemplo es integrar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Integración de tamaño fijo**

Para añadir el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   Para crear un visor es necesario agregar una etiqueta de script en el encabezado HTML. Antes de utilizar la API del visor, asegúrese de incluir [!DNL InterativeImage.js]. El archivo [!DNL InteractiveImage.js] se encuentra en la subcarpeta [!DNL html5/js/] de la implementación estándar de los visores IS:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se suministra desde el mismo dominio. De lo contrario, se especifica una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tienen instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Solo debe hacer referencia al archivo JavaScript `include` del visor principal de la página. No debe hacer referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargar la lógica del visor durante la ejecución. En concreto, no haga referencia directamente a la biblioteca `Utils.js` del SDK de HTML5 cargada por el visor desde la ruta de contexto `/s7viewers` (denominada SDK consolidado `include`). El motivo es que la ubicación de las `Utils.js` o bibliotecas de visores de tiempo de ejecución similares se administra completamente mediante la lógica del visor y la ubicación cambia entre las versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, poner una referencia directa a cualquier JavaScript `include` secundario que utilice el visor en la página rompe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del contenedor `DIV`.

   Agregue un elemento vacío `DIV` a la página en la que desea que aparezca el visor. El elemento `DIV` debe tener su ID definido, ya que este ID se pasa más tarde a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El marcador de posición `DIV` es un elemento posicionado, lo que significa que la propiedad `position` CSS está establecida en `relative` o `absolute`.

   A continuación se muestra un ejemplo de un elemento de marcador de posición definido `DIV`:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para la clase CSS de nivel superior `.s7interactiveimage` en unidades absolutas o utilizando el modificador `stagesize`.

   Puede colocar el tamaño en CSS directamente en la página HTML o en un archivo CSS de visor personalizado, que más tarde se asigna a un registro preestablecido de visor en AEM Assets bajo demanda o se pasa explícitamente mediante el comando `style`.

   Consulte [Vídeo](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obtener más información sobre cómo diseñar el visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en la página HTML:

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Puede pasar explícitamente el modificador `stagesize` con el código de inicialización del visor con la colección `params` o como una llamada de API como se describe en la sección Referencia de comandos, de esta manera:

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Se recomienda un enfoque basado en CSS que se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.InteractiveImage`, pase toda la información de configuración a su constructor e invoque el método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener un campo `containerId` que contenga el nombre del ID del contenedor de visor y el objeto `params` JSON anidado con parámetros de configuración admitidos por el visor. En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON le permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor de visor agregado al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación del DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta `BODY` de cierre o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de página web todavía. Por ejemplo, puede ocultarse utilizando el estilo `display:none` asignado. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web vuelve a poner el elemento contenedor en el diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   El siguiente es un ejemplo de creación de una instancia de visor, pasando al constructor las opciones de configuración mínimas necesarias y llamando al método `init()`. El ejemplo supone que `interactiveImage` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` es la URL del servicio de imágenes y `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` es el recurso:

   ```
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

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visor de imágenes de vídeo con un tamaño fijo:

   ```
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

**Diseño interactivo con altura ilimitada**

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible en su lugar que dicta el tamaño de tiempo de ejecución del contenedor del visor `DIV`. En el siguiente ejemplo, supongamos que la página web permite que el contenedor `DIV` del visor tome el 40% del tamaño de la ventana del explorador web. Y su altura no está restringida. El código HTML de la página web tendría el siguiente aspecto:

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

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Agregue el contenedor `DIV` al `"holder"` `DIV` existente. El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo la proporción de aspecto del visor coincide con el recurso.

```
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

La página de ejemplos siguientes ilustra más usos reales de la incrustación de diseño interactivo con altura ilimitada:

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html)

**Incrustación de tamaño flexible con anchura y altura definidas**

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

El resto de los pasos de incrustación son idénticos a los pasos utilizados para la incrustación interactiva con altura ilimitada. El ejemplo resultante es el siguiente:

```
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

**Incrustación mediante API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor no-args. El uso de este constructor de API no toma ningún parámetro y se especifican parámetros de configuración mediante métodos de API `setContainerId()`, `setParam()` y `setAsset()` con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de incrustación de tamaño fijo con la API basada en definidores:

```
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

