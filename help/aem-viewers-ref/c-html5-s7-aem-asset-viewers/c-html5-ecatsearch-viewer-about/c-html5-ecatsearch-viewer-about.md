---
description: El visor de búsqueda de catálogos electrónicos es un visor de catálogos que muestra los folletos electrónicos en un pliego o página por página. El catálogo electrónico permite a los usuarios navegar por el catálogo utilizando elementos adicionales de la interfaz de usuario o el modo de miniaturas dedicadas. Los usuarios también pueden acercar cada página para obtener buenos detalles.
keywords: responsive
seo-description: El visor de búsqueda de catálogos electrónicos es un visor de catálogos que muestra los folletos electrónicos en un pliego o página por página. El catálogo electrónico permite a los usuarios navegar por el catálogo utilizando elementos adicionales de la interfaz de usuario o el modo de miniaturas dedicadas. Los usuarios también pueden acercar cada página para obtener buenos detalles.
seo-title: Búsqueda de catálogos electrónicos
solution: Experience Manager
title: Búsqueda de catálogos electrónicos
topic: Dynamic media
uuid: f5ec33bf-e827-4709-9780-6f17096bf306
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2228'
ht-degree: 0%

---


# Búsqueda de catálogos electrónicos{#ecatalog-search}

El visor de búsqueda de catálogos electrónicos es un visor de catálogos que muestra los folletos electrónicos en un pliego o página por página. El catálogo electrónico permite a los usuarios navegar por el catálogo utilizando elementos adicionales de la interfaz de usuario o el modo de miniaturas dedicadas. Los usuarios también pueden acercar cada página para obtener buenos detalles.

Este visor funciona con ecatalogramas y admite mapas de imagen y herramientas de uso compartido en redes sociales opcionales. Cuenta con herramientas de zoom, herramientas de navegación por catálogos, compatibilidad con pantalla completa, miniaturas y un botón de cierre opcional. El visor también es compatible con las herramientas de uso compartido en redes sociales, Imprimir, Descargar y Favoritos. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

El usuario también puede realizar una búsqueda basada en palabras clave o en frases sobre el contenido del catálogo.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

Tipo de visor 513.

Consulte Requisitos y requisitos previos [del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## Uso del visor de catálogos electrónicos {#section-e6c68406ecdc4de781df182bbd8088b4}

El visor de búsqueda de catálogos electrónicos representa un archivo JavaScript principal y un conjunto de archivos auxiliares (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visor, recursos y CSS en particular) descargados por el visor en tiempo de ejecución

Puede utilizar el visor de búsqueda de catálogos electrónicos en modo emergente mediante una página HTML preparada para la producción proporcionada con los visores IS o en modo incrustado, donde se integra en la página web de destinatario mediante API documentada.

La configuración y la aplicación de aspectos son similares a las de los demás visores. Todos los aspectos se logran mediante CSS personalizada.

Consulte Referencia [de comandos común a todos los visores: Atributos](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuración y referencia de [comandos comunes a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacción con el visor de búsqueda de catálogos electrónicos {#section-642e66ca38cd4032992840ec6c0b0cd2}

El visor de búsqueda de catálogos electrónicos admite los siguientes gestos táctiles comunes en otras aplicaciones móviles.

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
   <td colname="col2"> <p> Selecciona una nueva miniatura en las muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tocar Doble </p> </td> 
   <td colname="col2"> <p> Amplía un nivel hasta que se alcanza la máxima ampliación. El siguiente gesto de toque de doble restablece el visor al estado de visualización inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pellizcar </p> </td> 
   <td colname="col2"> <p>Acerca o aleja. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o barrido horizontal </p> </td> 
   <td colname="col2"> <p>Se desplaza por la lista de las páginas de catálogo si se utiliza una transición de marco de diapositiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o barrido vertical </p> </td> 
   <td colname="col2"> <p>Cuando la imagen está en estado de restablecimiento, realiza un desplazamiento de página nativo. </p> <p>Cuando las miniaturas están activas, se desplaza por la lista de las miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es posible activar un efecto de animación de volteado de página realista para desplazarse entre las páginas del catálogo. En estos casos, un usuario puede mantener presionada y arrastrar una esquina de página y voltear la página.

Este visor también admite entrada táctil y entrada de ratón en dispositivos Windows con una pantalla táctil y un ratón. Sin embargo, esta compatibilidad está limitada a los exploradores web Chrome, Internet Explorer 11 y Edge.

## Herramientas de uso compartido en medios sociales con el visor de búsqueda de catálogos electrónicos {#section-eb575084a99647c3a9591f439f40b412}

El visor de búsqueda de catálogos electrónicos admite herramientas de uso compartido en redes sociales. Están disponibles como botón en la barra de control principal, que se expande a una barra de herramientas de uso compartido cuando un usuario hace clic o toca en ella.

La barra de herramientas de uso compartido contiene iconos para cada tipo de canal de uso compartido admitido, que incluye Facebook, Twitter, uso compartido de correo electrónico, uso compartido de código incrustado y uso compartido de vínculos. Cuando se activan las herramientas de uso compartido de correo electrónico, uso compartido incrustado o uso compartido de vínculos, el visor muestra un cuadro de diálogo modal con el correspondiente formulario de entrada de datos. Cuando se llama a Facebook o Twitter, el visor redirige al usuario a un cuadro de diálogo de uso compartido estándar desde un servicio social. Las herramientas de uso compartido no están disponibles en modo de pantalla completa debido a las restricciones de seguridad del explorador web.

La función de búsqueda del visor está disponible como icono de cristal en la barra de herramientas principal. Al tocar o hacer clic en el icono, se activa el panel Buscar con un campo de entrada. Después de escribir una palabra clave o frase y pulsar Intro, el visor presenta los resultados de búsqueda en el panel y resalta las palabras encontradas en la vista principal.

## Incrustación del visor de búsqueda de catálogos electrónicos {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo que, al hacer clic en él, abre el visor en una ventana de explorador independiente. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, es posible que la página web tenga un diseño de página estático o utilice un diseño interactivo que se muestre de forma diferente en distintos dispositivos o en diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: ventana emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o ficha separada del explorador Web. Toma todo el área de la ventana del navegador y se ajusta en caso de que se cambie el tamaño del navegador o la orientación del dispositivo móvil.

El modo emergente es el más común para dispositivos móviles. La página web carga el visor mediante una llamada de `window.open()` JavaScript, un elemento `A` HTML configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página HTML lista para usar en el modo de operación emergente. En este caso, se le llama [!DNL eCatalogSearchViewer.html] y se encuentra dentro de la [!DNL html5/] subcarpeta de la implementación estándar de visores IS:

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

Puede lograr la personalización visual mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código HTML que abre el visor en una ventana nueva:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo incrustado, el visor se agrega a la página web existente, que puede tener ya contenido de cliente no relacionado con el visor. Normalmente, el visor ocupa solo una parte del espacio de una página web.

Los casos de uso principales son páginas web orientadas a equipos de escritorio o tabletas, y también páginas diseñadas con capacidad de respuesta que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta es la mejor opción para las páginas web con un diseño estático.

La incrustación de diseño adaptable supone que es posible que el visor tenga que cambiar el tamaño en tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web en su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, dejando su altura sin restricciones, el visor selecciona automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para las páginas web que utilizan marcos de diseño interactivos como Bootstrap, Foundation, etc.

En caso contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellena solo esa área y sigue el tamaño que proporciona el diseño de la página web. Un buen ejemplo es la incrustación del visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del navegador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición de la DIV de contenedor.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor en la página web.

   La creación de un visor requiere que agregue una etiqueta de script en el encabezado HTML. Antes de utilizar la API de visor, asegúrese de incluir [!DNL eCatalogSearchViewer.js]. El [!DNL eCatalogSearchViewer.js] archivo se encuentra en la [!DNL html5/js/] subcarpeta de la implementación estándar de los visores de IS:

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Scene7 y se suministra desde el mismo dominio. De lo contrario, debe especificar una ruta de acceso completa a uno de los servidores de Adobe Scene7 que tenga instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. Definición de la DIV de contenedor.

   Añada un elemento DIV vacío a la página en la que desea que aparezca el visor. El ID del elemento DIV debe estar definido porque este ID se pasa más tarde a la API del visor.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la propiedad `position` CSS está definida como `relative` o `absolute`.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Configuración del tamaño del visor

   Puede definir el tamaño estático del visor, ya sea declarándolo para la clase CSS de nivel `.s7ecatalogsearchviewer` superior en unidades absolutas o utilizando `stagesize` un modificador.

   Puede colocar el tamaño en CSS directamente en la página HTML o en un archivo CSS de visor personalizado, que posteriormente se asignará a un registro de ajuste preestablecido de visor en Scene7 Publishing System, o se pasará explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) de catálogos electrónicos para obtener más información sobre el estilo del visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en una página HTML:

   ```
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede definir el `stagesize` modificador en el registro de ajustes preestablecidos de visor de Scene7 Publishing System o pasarlo explícitamente con el código de inicialización del visor con `params` colección, o como una llamada de API como se describe en la sección Referencia de comandos, como se indica a continuación:

   ```
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.eCatalogSearchViewer` clase, pase toda la información de configuración a su constructor y al `init()` método de llamada en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto tiene el `containerId` `params` campo que contiene el nombre del ID de contenedor del visor y el objeto JSON anidado con parámetros de configuración admitidos por el visor. En este caso, el `params` objeto debe tener al menos la URL del servicio de imágenes pasada como `serverUrl` propiedad y el recurso inicial como `asset` parámetro. La API de inicialización basada en JSON permite crear y inicio del visor con una sola línea de código.

   Es importante que el contenedor del visor se añada al DOM para que el código del visor pueda encontrar el elemento de contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Sin embargo, para obtener la máxima compatibilidad, llame al `init()` método justo antes de la `BODY` etiqueta de cierre o en el `onload()` evento body.

   Al mismo tiempo, el elemento contenedor no debe ser necesariamente parte del diseño de la página web. Por ejemplo, puede ocultarse con `display:none` el estilo asignado. En este caso, el visor retrasa el proceso de inicialización hasta el momento en que la página web devuelve el elemento de contenedor a la presentación. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de creación de una instancia de visor, pasando las opciones de configuración mínimas necesarias al constructor y llamando al `init()` método. Se supone que el ejemplo `eCatalogSearchViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; `http://s7d1.scene7.com/is/image/` es la URL del servicio de imágenes y `Viewers/Pluralist` es el recurso:

   ```
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incorpora el visor de búsqueda de catálogos electrónicos con un tamaño fijo:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incrustación de diseño adaptable con altura ilimitada**

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que determina el tamaño de tiempo de ejecución del contenedor del visor `DIV`. A efectos de este ejemplo, supongamos que la página web permite que el contenedor del visor `DIV` tome el 40 % del tamaño de la ventana del navegador web, dejando su altura sin restricciones. El código HTML de la página web resultante es similar al siguiente:

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

Añadir el visor a una página de este tipo es similar a la incrustación de tamaño fijo. La única diferencia es que no es necesario definir explícitamente el tamaño del visor.

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición de la DIV de contenedor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Añada el contenedor `DIV` al &quot;titular&quot; existente `DIV`. El siguiente código es un ejemplo completo. Puede ver cómo cambia el tamaño del visor cuando se cambia el tamaño del navegador y cómo coincide la proporción de aspecto del visor con el recurso.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La siguiente página de ejemplos ilustra casos de uso más real de diseño interactivo incrustado con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Integración de tamaño flexible con anchura y altura definidas**

En caso de incrustación de tamaño flexible con anchura y altura definidas, el estilo de la página web es diferente. Es decir, proporciona ambos tamaños al &quot;marcador&quot; `DIV` y lo centra en la ventana del navegador. Además, la página web establece el tamaño del elemento `HTML` y en el `BODY` 100 %:

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

El resto de los pasos de incrustación son idénticos al diseño interactivo que se incrusta con altura ilimitada. El ejemplo resultante es el siguiente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incrustación mediante API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en setter y el constructor no-args. Con ese constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante métodos `setContainerId()`, `setParam()`y `setAsset()` API con llamadas JavaScript independientes.

El siguiente ejemplo muestra la incrustación de tamaño fijo con la API basada en establecedor:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "http://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```

