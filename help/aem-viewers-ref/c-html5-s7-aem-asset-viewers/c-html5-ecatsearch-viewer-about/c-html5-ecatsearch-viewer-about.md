---
description: eCatalog Search Viewer es un visor de catálogos que muestra folletos electrónicos distribuidos por extensión o página por página. El catálogo electrónico permite a los usuarios navegar por el catálogo utilizando elementos adicionales de la interfaz de usuario o el modo de miniaturas dedicado. Los usuarios también pueden ampliar todas las páginas para obtener buenos detalles.
keywords: adaptable
solution: Experience Manager
title: Búsqueda en el catálogo electrónico
uuid: f5ec33bf-e827-4709-9780-6f17096bf306
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2191'
ht-degree: 0%

---


# Búsqueda en el catálogo electrónico{#ecatalog-search}

eCatalog Search Viewer es un visor de catálogos que muestra folletos electrónicos distribuidos por extensión o página por página. El catálogo electrónico permite a los usuarios navegar por el catálogo utilizando elementos adicionales de la interfaz de usuario o el modo de miniaturas dedicado. Los usuarios también pueden ampliar todas las páginas para obtener buenos detalles.

Este visor funciona con catálogos electrónicos y admite mapas de imágenes opcionales y herramientas de uso compartido en medios sociales. Tiene herramientas de zoom, herramientas de navegación de catálogo, compatibilidad con pantalla completa, miniaturas y un botón de cierre opcional. El visor también es compatible con las herramientas de uso compartido en medios sociales, Imprimir, Descargar y Favoritos. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.

El usuario también puede realizar una búsqueda basada en palabras clave o en frases en el contenido del catálogo.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

Tipo de visor 513.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demostración de URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## Uso del visor de catálogos electrónicos {#section-e6c68406ecdc4de781df182bbd8088b4}

El visor de búsqueda en catálogo electrónico representa un archivo JavaScript principal y un conjunto de archivos de ayuda (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visor en particular, recursos y CSS) descargados por el visor en tiempo de ejecución

Puede utilizar el visualizador de búsqueda de catálogos electrónicos en modo emergente utilizando una página HTML lista para la producción proporcionada con los visualizadores IS o en modo integrado, donde se integra en la página web de destino mediante API documentada.

La configuración y el desollado son similares a los de los demás visores. Toda la apariencia se logra mediante CSS personalizada.

Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visualizadores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de búsqueda de catálogos electrónicos {#section-642e66ca38cd4032992840ec6c0b0cd2}

El visor de búsqueda de catálogos electrónicos admite los siguientes gestos táctiles que son comunes en otras aplicaciones móviles.

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
   <td colname="col1"> <p>Doble toque </p> </td> 
   <td colname="col2"> <p> Amplía un nivel hasta alcanzar la ampliación máxima. El siguiente gesto de doble toque restablece el visor al estado de visualización inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pellizcar </p> </td> 
   <td colname="col2"> <p>Amplía o reduce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido horizontal o deslizamiento </p> </td> 
   <td colname="col2"> <p>Se desplaza por la lista de páginas del catálogo si se utiliza una transición de marco de diapositiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical o flexión </p> </td> 
   <td colname="col2"> <p>Cuando la imagen se encuentra en estado de restablecimiento, realiza un desplazamiento de página nativo. </p> <p>Cuando las miniaturas están activas, se desplaza por la lista de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es posible habilitar un efecto realista de animación de volteado de página para desplazarse entre las páginas del catálogo. En estos casos, un usuario puede mantener y arrastrar una esquina de página y voltear la página.

Este visor también admite la entrada táctil y la entrada de ratón en dispositivos Windows con una pantalla táctil y un ratón. Sin embargo, esta compatibilidad está limitada únicamente a los navegadores web Chrome, Internet Explorer 11 y Edge.

## Herramientas de uso compartido en medios sociales con el visor de búsqueda de catálogos electrónicos {#section-eb575084a99647c3a9591f439f40b412}

El visor de búsqueda de catálogos electrónicos es compatible con las herramientas de uso compartido en redes sociales. Están disponibles como un botón en la barra de control principal que se expande a una barra de herramientas de uso compartido cuando un usuario hace clic o pulsa sobre él.

La barra de herramientas para compartir contiene iconos para cada tipo de canal de uso compartido admitido, que incluye Facebook, Twitter, uso compartido de correo electrónico, uso compartido de código incrustado y uso compartido de vínculos. Cuando se activan las herramientas de uso compartido por correo electrónico, uso compartido incrustado o uso compartido de vínculos, el visor muestra un cuadro de diálogo modal con un formulario de entrada de datos correspondiente. Cuando se llama a Facebook o Twitter, el visor redirige al usuario a un cuadro de diálogo estándar de uso compartido desde un servicio social. Las herramientas de uso compartido no están disponibles en el modo de pantalla completa debido a las restricciones de seguridad del explorador web.

La función Buscar del espectador está disponible como un icono de cristal en la barra de herramientas principal. Al tocar o hacer clic en el icono, se activa el panel Buscar con un campo de entrada. Después de escribir una palabra clave o frase y de pulsar Intro, el visor presenta los resultados de búsqueda en el panel y resalta las palabras encontradas en la vista principal.

## Incrustación del visor de búsqueda de catálogos electrónicos {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo que, cuando se hace clic, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o en diferentes tamaños de ventana del navegador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: elemento emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Toma todo el área de la ventana del explorador y se ajusta en caso de que se cambie el tamaño del explorador o de que se cambie la orientación de un dispositivo móvil.

El modo emergente es el más común para los dispositivos móviles. La página web carga el visor utilizando `window.open()` llamada de JavaScript, el elemento HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página HTML predeterminada para el modo de operación emergente. En este caso, se denomina [!DNL eCatalogSearchViewer.html] y se encuentra dentro de la subcarpeta [!DNL html5/] de la implementación estándar de los visores IS:

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

Puede lograr la personalización visual mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código HTML que abre el visor en una nueva ventana:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo integrado, el visor se añade a la página web existente, que puede tener ya contenido de cliente no relacionado con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de una página web.

Los casos de uso principales son páginas web orientadas a equipos de escritorio o tabletas, y también páginas diseñadas con capacidad de respuesta que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta es la mejor opción para páginas web con diseño estático.

La incrustación de diseño interactivo supone que el visor puede tener que cambiar el tamaño durante la ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web para su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, sin restringir su altura, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que usan marcos de diseño interactivos como Bootstrap, Fundación, etc.

De lo contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellena solo esa área y sigue el tamaño que proporciona el diseño de la página web. Un buen ejemplo es integrar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Integración de tamaño fijo**

Para añadir el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor DIV.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   Para crear un visor es necesario agregar una etiqueta de script en el encabezado HTML. Antes de utilizar la API del visor, asegúrese de incluir [!DNL eCatalogSearchViewer.js]. El archivo [!DNL eCatalogSearchViewer.js] se encuentra en la subcarpeta [!DNL html5/js/] de la implementación estándar de los visores IS:

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores Dynamic Media de Adobe y se suministra desde el mismo dominio. De lo contrario, se especifica una ruta completa a uno de los servidores Dynamic Media de Adobe que tienen instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. Definición del contenedor DIV.

   Agregue un elemento DIV vacío a la página donde desee que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa más tarde a la API del visor.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la propiedad `position` CSS está establecida en `relative` o `absolute`.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para la clase CSS de nivel superior `.s7ecatalogsearchviewer` en unidades absolutas o utilizando el modificador `stagesize`.

   Puede colocar el tamaño en CSS directamente en la página HTML o en un archivo CSS de visor personalizado, que después se asigna a un registro preestablecido de visor en Dynamic Media Classic, o se pasa explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor de catálogos electrónicos](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obtener más información sobre cómo diseñar el visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en una página HTML:

   ```
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede establecer el modificador `stagesize` en el registro preestablecido de visualizador en Dynamic Media Classic, o pasarlo explícitamente con el código de inicialización del visualizador con la colección `params` o como una llamada de API como se describe en la sección Referencia de comandos, como se indica a continuación:

   ```
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.eCatalogSearchViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto tiene el campo `containerId` que contiene el nombre del ID del contenedor de visor y el objeto `params` JSON anidado con parámetros de configuración admitidos por el visor. En este caso, el objeto `params` debe tener al menos la dirección URL del servicio de imágenes pasada como propiedad `serverUrl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON le permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor de visor agregado al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación del DOM hasta el final de la página web. Sin embargo, para obtener la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta `BODY` de cierre o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe ser necesariamente parte del diseño de página web aún. Por ejemplo, puede ocultarse utilizando el estilo `display:none` asignado. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web vuelve a poner el elemento contenedor en el diseño. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   El siguiente es un ejemplo de creación de una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar al método `init()`. El ejemplo supone que `eCatalogSearchViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; `http://s7d1.scene7.com/is/image/` es la URL del servicio de imágenes y `Viewers/Pluralist` es el recurso:

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

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visor de búsqueda de catálogos electrónicos con un tamaño fijo:

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

**Diseño interactivo con altura ilimitada**

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible en su lugar que dicta el tamaño de tiempo de ejecución del contenedor del visor `DIV`. Para los fines de este ejemplo, supongamos que la página web permite que el contenedor `DIV` del visor tome el 40% del tamaño de la ventana del explorador web, sin restringir su altura. El código HTML de la página web resultante tiene el siguiente aspecto:

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

Añadir el visor a una página de este tipo es similar a la incrustación de tamaño fijo, con la única diferencia de que no es necesario definir explícitamente el tamaño del visor.

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor DIV.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Añada el contenedor `DIV` al &quot;soporte&quot; `DIV` existente. El siguiente código es un ejemplo completo. Puede ver cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo coincide la relación de aspecto del visor con el recurso.

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

La siguiente página de ejemplos ilustra casos de uso más reales de incrustación de diseño interactivo con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Integración de tamaño flexible con anchura y altura definidas**

En caso de incrustación de tamaño flexible con anchura y altura definidas, el estilo de la página web es diferente. Es decir, proporciona ambos tamaños al &quot; titular&quot; `DIV` y lo centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en 100%:

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

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor no-args. Con ese constructor de API no toma ningún parámetro y se especifican parámetros de configuración mediante métodos de API `setContainerId()`, `setParam()` y `setAsset()` con llamadas de JavaScript independientes.

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

