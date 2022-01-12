---
title: Visor panorámico
description: HTML5 Panoramic Viewer es un visor de imágenes que muestra una imagen panorámica. El objetivo de este visor es mostrar un panorama esférico, también conocido como imagen equirectangular. Es compatible con la planeación y la panorámica automáticas mediante el movimiento giroscópico. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles. El modo de visualización de la realidad virtual está disponible en dispositivos móviles compatibles.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 0%

---

# Panorámica{#panoramic}

HTML5 Panoramic Viewer es un visor de imágenes que muestra una imagen panorámica. El objetivo de este visor es mostrar un panorama esférico, también conocido como imagen equirectangular. Es compatible con la planeación y la panorámica automáticas mediante el movimiento giroscópico. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles. El modo de visualización de la realidad virtual está disponible en dispositivos móviles compatibles.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Tipo de visor 514.

## Dirección URL de la demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Uso del visor panorámico {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramic Viewer representa un archivo JavaScript principal y un conjunto de archivos de ayuda descargados por el visor durante la ejecución. El conjunto de archivos de ayuda es una única inclusión JavaScript con todos los componentes de SDK de visor HTML5 utilizados por este visor, recursos y CSS en particular.
El visor panorámico de HTML5 se puede utilizar tanto en modo emergente mediante la página HTML lista para la producción que se proporciona con los visualizadores IS como en modo incrustado, donde se integra en la página web de destino mediante API documentada.
La configuración y el desollado son similares a los de los otros visores HTML5. Todo el desliz se puede lograr mediante CSS personalizada.

Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visualizadores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor panorámico HTML5 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panoramic Viewer admite el desplazamiento automático y la navegación mediante arrastre o movimiento giroscópico.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Navegación </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ordenador </p> </td> 
   <td colname="col2"> <p>Panorámica automática y arrastre para navegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dispositivo táctil </p> </td> 
   <td colname="col2"> <p>Panorámica automática y arrastre para desplazarse de forma predeterminada. Navegue por el movimiento giroscópico en el modo de procesamiento VR (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor admite la entrada táctil y la entrada de ratón en dispositivos Windows con pantalla táctil y ratón; sin embargo, esta compatibilidad se limita solo a los navegadores web Chrome, Internet Explorer 11 y Edge.
El visor panorámico puede procesar imágenes panorámicas en modo Realidad virtual (VR) especificando el modificador vrrender. Cuando está habilitada la representación, se muestra una imagen panorámica en pantallas divididas. Un caso de uso común sería servir la imagen en un teléfono móvil montado en un auricular de realidad virtual, proporcionando imágenes separadas para cada ojo. El espectador responde al movimiento giroscópico de la cabeza y navega por la imagen.

## HTML de incrustación 5 Visor panorámico {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo. Al seleccionar ese vínculo, se abre el visor en una ventana independiente del explorador. En otros casos, puede ser necesario integrar el visor en la página de alojamiento. En este último caso, la página web puede tener un diseño estático o ser &quot;interactiva&quot; y mostrarse de forma diferente en distintos dispositivos o en diferentes tamaños de ventana del navegador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: ventana emergente, incrustación de tamaño fijo e incrustación interactiva.

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Toma todo el área de la ventana del navegador y se ajusta en caso de que el navegador cambie de tamaño o la orientación del dispositivo cambie.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante `window.open()` Llamada de JavaScript, elemento de HTML configurado correctamente o de cualquier otra manera adecuada.

Se recomienda utilizar una página HTML predeterminada para el modo de operación emergente. Se llama [!DNL PanoramicViewer.html] y se encuentra debajo de la variable [!DNL html5/] subcarpeta de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

La personalización visual se puede lograr aplicando CSS personalizada.

Este es un ejemplo de código de HTML que abre el visor en la nueva ventana:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación interactivo**

En el modo integrado, el visor se añade a la página web existente, que puede tener ya algún contenido de cliente no relacionado con el visor. Normalmente, el visor solo ocupa una parte del espacio de la página web.

Los casos de uso principales son páginas web orientadas a equipos de escritorio o tabletas, y también páginas web adaptables que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Este método es la mejor opción para páginas web con diseño estático.

La incrustación interactiva supone que el visor debe cambiar el tamaño en tiempo de ejecución como respuesta al cambio de tamaño de su contenedor DIV. El caso de uso más común es agregar un visor a una página web que utiliza un diseño flexible.

En el modo interactivo, el visor se comporta de forma diferente en función del tamaño de la página web según el contenedor DIV. Si la página web establece únicamente la anchura del contenedor DIV, sin restringir su altura, el visor elige automáticamente su altura según la proporción de aspecto del recurso utilizado. Este método garantiza que el recurso se ajuste perfectamente a la vista sin ningún relleno en los lados. Este caso de uso es el más común para las páginas web que usan marcos de diseño interactivos como Bootstrap, Fundación, etc.

De lo contrario, si la página web establece la anchura y la altura del contenedor DIV del visor, el visor rellena esa área y sigue el tamaño proporcionado por el diseño de la página web. Un buen ejemplo es integrar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Integración de tamaño fijo**

Para añadir el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   Para crear un visor es necesario agregar una etiqueta de script en el encabezado del HTML. Antes de utilizar la API del visor, asegúrese de incluir [!DNL PanoramicViewer.js]. La variable [!DNL PanoramicViewer.js] el archivo se encuentra debajo de [!DNL html5/js/] subcarpeta de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se suministra desde el mismo dominio. De lo contrario, se especifica una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tienen instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Solo haga referencia al JavaScript del visor principal `include` en la página. No haga referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargar la lógica del visor durante la ejecución. En particular, no haga referencia directa al SDK de HTML5 `Utils.js` biblioteca cargada por el visor desde `/s7viewers` ruta de contexto (denominado SDK consolidado) `include`). La razón es que la ubicación de `Utils.js` o bibliotecas de visores de tiempo de ejecución similares se gestionan completamente mediante la lógica del visor y la ubicación cambia entre las versiones del visor. El Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, poner una referencia directa a cualquier JavaScript secundario `include` utilizado por el visor en la página rompe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del contenedor DIV.

   Agregue un elemento DIV vacío a la página donde desee que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa más tarde a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la variable `position` La propiedad CSS se establece en `relative` o `absolute`.


   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para `.s7panoramicviewer` clase CSS de nivel superior en unidades absolutas o utilizando el modificador `stagesize`.

   El tamaño en CSS se puede colocar directamente en la página HTML o en el archivo CSS del visor personalizado, que más tarde se asigna a un registro preestablecido de visualizador en AOD o se pasa explícitamente mediante el comando Estilo. Consulte Personalización del visor para obtener más información sobre cómo diseñar el visor con CSS. A continuación se muestra un ejemplo de definición del tamaño del visor estático en la página de HTML:

   ```
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` El modificador se puede pasar explícitamente con el código de inicialización del visualizador con la colección params o como una llamada de API como se describe en la sección Referencia de comandos, de esta manera:

   ```
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   Se recomienda el enfoque basado en CSS, que se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.PanoramicViewer` clase , pase toda la información de configuración a su constructor e invoque `init(`) en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener un campo containerId que contenga el nombre del ID del contenedor del visor y el objeto JSON de parámetros anidados con parámetros de configuración admitidos por el visor. En este caso, el objeto params debe tener al menos la URL de servicio de imágenes pasada como `serverUrl` y el recurso inicial como parámetro de recurso. La API de inicialización basada en JSON le permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor de visor agregado al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación del DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame a la función `init()` justo antes del cierre `BODY` o en el cuerpo `onload()` evento.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, puede ocultarse usando `display:none` estilo asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web vuelve a poner el elemento contenedor en el diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   El siguiente es un ejemplo de creación de una instancia de visor, pasar al constructor las opciones de configuración mínimas necesarias y llamar a la función `init()` método. Este ejemplo asume `panoramicViewer` es la instancia del visor, `s7viewer` es el nombre del marcador de posición `DIV`, [!DNL http://s7d1.scene7.com/is/image/] es la URL del servicio de imágenes y [!DNL Scene7SharedAssets/PanoramicImage-Sample] es el recurso.

   ```
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incorpora el visor panorámico con un tamaño fijo:

   ```
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**Diseño interactivo con altura ilimitada**

Con la incrustación interactiva, la página web normalmente tiene algún tipo de diseño flexible en su lugar, lo que dicta el tamaño en tiempo de ejecución del contenedor DIV del visor. A los efectos de este ejemplo, supongamos que la página web permite que el contenedor DIV del visor tome el 80 % del tamaño de la ventana del explorador web, dejando su altura sin restricciones. El código del HTML de la página web podría tener este aspecto:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 
```

Añadir el visor a esta página es similar a la incrustación de tamaño fijo, con la única diferencia de que no necesita definir explícitamente el tamaño del visor:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor DIV.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. El contenedor DIV debe añadirse al DIV &quot;titular&quot; existente. El siguiente código es un ejemplo completo: puede ver cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo coincide la proporción de aspecto del visor con el recurso.

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

La siguiente página de ejemplos ilustra un uso más real del diseño interactivo incrustado con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Diseño interactivo con anchura y altura definidas**

Si hay un diseño interactivo incrustado con la anchura y la altura definidas, el estilo de la página web es diferente; proporciona ambos tamaños al &quot;soporte&quot; `DIV` y céntrela en la ventana del explorador. Además, la página web establece el tamaño de la variable `HTML` y `BODY` al 100%:

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

El resto de pasos de incrustación son idénticos a la incrustación interactiva con altura ilimitada. El ejemplo resultante es

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**Incrustación mediante API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor no-args. Con esa API, el constructor no toma ningún parámetro y los parámetros de configuración se especifican usando `setContainerId()`, `setParam()`y `setAsset()` Métodos de API con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra la incrustación de tamaño fijo con la API basada en establecedor:

```
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
