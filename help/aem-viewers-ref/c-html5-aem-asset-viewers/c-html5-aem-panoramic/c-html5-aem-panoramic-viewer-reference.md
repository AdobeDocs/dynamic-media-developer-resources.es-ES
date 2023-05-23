---
title: Visor panorámico
description: HTML 5 Visor panorámico es un visor de imágenes que muestra una imagen panorámica. El objetivo de este visor es mostrar un panorama esférico, también conocido como imagen equirectangular. Admite la panorámica automática y la panorámica mediante movimiento giroscópico. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles. El modo de visualización de realidad virtual está disponible en dispositivos móviles compatibles.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 0%

---

# Panorámica{#panoramic}

HTML 5 Visor panorámico es un visor de imágenes que muestra una imagen panorámica. El objetivo de este visor es mostrar un panorama esférico, también conocido como imagen equirectangular. Admite la panorámica automática y la panorámica mediante movimiento giroscópico. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles. El modo de visualización de realidad virtual está disponible en dispositivos móviles compatibles.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Tipo de visor 514.

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Uso del visor panorámico {#section-f21ac23d3f6449ad9765588d69584772}

HTML 5 Visor panorámico representa un archivo JavaScript principal y un conjunto de archivos de ayuda descargados por el visor en tiempo de ejecución. El conjunto de archivos de ayuda es una sola inclusión de JavaScript con todos los componentes del SDK de HTML5 Viewer utilizados por este visor, recursos y CSS en particular.
El visor panorámico HTML5 se puede utilizar en modo emergente utilizando la página del HTML lista para la producción proporcionada con visores IS o en modo incrustado, donde se integra en la página web de destino mediante una API documentada.
La configuración y el desollado son similares a los de los otros visores de HTML5. Todo el desollamiento se puede lograr a través de CSS personalizado.

Consulte [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacción con el visor panorámico HTML5 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visor panorámico HTML5 admite el desplazamiento y la navegación automáticos mediante el movimiento giratorio o de arrastre.

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
   <td colname="col2"> <p>Desplazamiento automático y arrastre para desplazarse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dispositivo táctil </p> </td> 
   <td colname="col2"> <p>Realizar desplazamiento automático y arrastrar para desplazarse de forma predeterminada. Navegue mediante el movimiento giroscópico en el modo de procesamiento de RV (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor admite la entrada táctil y la entrada de ratón en dispositivos Windows con pantalla táctil y ratón; sin embargo, esta compatibilidad se limita únicamente a los exploradores web Chrome, Internet Explorer 11 y Edge.
El Visor panorámico puede procesar imágenes panorámicas en modo de Realidad virtual (VR) especificando el modificador vrrender. Cuando vrrender está habilitado, se muestra una imagen panorámica en pantallas divididas. Un caso de uso común sería servir la imagen en un teléfono móvil montado en unos auriculares de realidad virtual, proporcionando imágenes independientes para cada ojo. El espectador responde al movimiento giroscópico de la cabeza y navega por la imagen.

## Incrustación del visor panorámico HTML5 {#section-6bb5d3c502544ad18a58eafe12a13435}

Las distintas páginas web tienen diferentes necesidades de comportamiento del visualizador. A veces, una página web proporciona un vínculo. Al seleccionar ese vínculo, se abre el visor en una ventana independiente del explorador. En otros casos, puede ser necesario incrustar el visor en la página de alojamiento. En este último caso, la página web puede tener un diseño estático o ser &quot;adaptable&quot; y mostrarse de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: emergente, incrustación de tamaño fijo e incrustación adaptable.

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Ocupa todo el área de la ventana del explorador y se ajusta en caso de que se cambie el tamaño del explorador o la orientación del dispositivo.

Este modo es el más común para dispositivos móviles. La página web carga el visor mediante `window.open()` Llamada de JavaScript, elemento HTML configurado correctamente o cualquier otra forma adecuada.

Se recomienda utilizar una página de HTML predeterminada para el modo de operación emergente. Se llama. [!DNL PanoramicViewer.html] y se encuentra debajo de la [!DNL html5/] de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

La personalización visual se puede lograr aplicando CSS personalizado.

Este es un ejemplo de código de HTML que abre el visor en la nueva ventana:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación adaptable**

En el modo incrustado, el visor se añade a la página web existente, que puede tener ya contenido de clientes no relacionado con el visor. El visor normalmente ocupa solo una parte de los bienes raíces de la página web.

Los casos de uso principales son páginas web orientadas para equipos de escritorio o tabletas, y también páginas web adaptables que ajustan el diseño automáticamente según el tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Este método es la mejor opción para páginas web con diseño estático.

La incrustación interactiva supone que el visualizador debe cambiar de tamaño en tiempo de ejecución en respuesta al cambio de tamaño de su DIV contenedor. El caso de uso más común es añadir un visor a una página web que utiliza un diseño flexible.

En el modo interactivo, el comportamiento del visor varía en función de la forma en que la página web ajusta el tamaño de su contenedor DIV. Si la página web establece únicamente la anchura del DIV contenedor y deja su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso utilizado. Este método garantiza que el recurso se ajuste perfectamente a la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que utilizan marcos de diseño adaptables como Bootstrap, Foundation y similares.

De lo contrario, si la página web establece la anchura y la altura del DIV contenedor del visor, este rellenará esa área y seguirá el tamaño proporcionado por el diseño de página web. Un buen ejemplo es la incrustación del visualizador en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado del HTML. Antes de usar la API de visor, asegúrese de incluir lo siguiente [!DNL PanoramicViewer.js]. El [!DNL PanoramicViewer.js] El archivo se encuentra en [!DNL html5/js/] de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tengan instalados los visores de IIS.

La ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Solo referencia al visor principal JavaScript `include` en la página. No haga referencia a ningún archivo JavaScript adicional en el código de la página web que la lógica del visor pueda descargar durante la ejecución. En concreto, no haga referencia directamente al SDK de HTML5 `Utils.js` biblioteca cargada por el visor desde `/s7viewers` ruta de contexto (denominado SDK consolidado) `include`). El motivo es que la ubicación de `Utils.js` Para bibliotecas de visualizadores en tiempo de ejecución similares, la lógica del visualizador las gestiona completamente y la ubicación cambia entre versiones del visualizador. El Adobe no mantiene las versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, se hace referencia directa a cualquier JavaScript secundario `include` que el usuario utiliza en la página interrumpe la funcionalidad del usuario en el futuro cuando se implemente una nueva versión del producto.

1. Definición del DIV de contenedor.

   Añada un elemento DIV vacío a la página donde desea que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa posteriormente a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El DIV de marcador de posición es un elemento posicionado, lo que significa que la variable `position` La propiedad CSS se establece en `relative` o `absolute`.


   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para `.s7panoramicviewer` clase CSS de nivel superior en unidades absolutas o mediante el modificador `stagesize`.

   El tamaño en CSS se puede ajustar directamente en la página del HTML o en el archivo CSS de visor personalizado, que luego se asigna a un registro de ajuste preestablecido de visor en AOD o se pasa explícitamente mediante el comando de estilo. Consulte Personalización del visor para obtener más información sobre cómo aplicar estilo al visor con CSS. A continuación se muestra un ejemplo de definición del tamaño del visor estático en la página del HTML:

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` El modificador se puede pasar explícitamente con el código de inicialización del visor con la colección params o como una llamada de API como se describe en la sección Referencia de comandos, de esta manera:

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   Se recomienda un enfoque basado en CSS y se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.PanoramicViewer` , pase toda la información de configuración a su constructor y llame a `init(`) en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener un campo containerId que contenga el nombre del ID de contenedor del visor y el objeto JSON de parámetros anidados con parámetros de configuración admitidos por el visor. En este caso, el objeto de parámetros debe tener al menos la URL del servicio de imágenes pasada como `serverUrl` propiedad y recurso inicial como parámetro de recurso. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` método justo antes del cierre `BODY` o en el cuerpo `onload()` evento.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, se puede ocultar usando `display:none` estilo asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar a `init()` método. Este ejemplo supone `panoramicViewer` es la instancia del visor, `s7viewer` es el nombre del marcador de posición `DIV`, [!DNL http://s7d1.scene7.com/is/image/] es la URL del servicio de imágenes y [!DNL Scene7SharedAssets/PanoramicImage-Sample] es el recurso.

   ```html {.line-numbers}
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

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visor panorámico con un tamaño fijo:

   ```html {.line-numbers}
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

**Inserción de diseño interactivo con altura sin restricciones**

Con la incrustación adaptable, la página web normalmente tiene algún tipo de diseño flexible que dicta el tamaño en tiempo de ejecución del DIV contenedor del visualizador. A los efectos de este ejemplo, supongamos que la página web permite que el DIV contenedor del visor ocupe el 80 % del tamaño de la ventana del explorador web, dejando su altura sin restricciones. El código del HTML de la página web puede tener este aspecto:

```html {.line-numbers}
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

Añadir el visor a esta página es similar a la incrustación de tamaño fijo, con la única diferencia de que no es necesario definir explícitamente el tamaño del visor:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del DIV de contenedor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. El DIV de contenedor debe agregarse al DIV de &quot;titular&quot; existente. El siguiente código es un ejemplo completo, puede ver cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo coincide la proporción de aspecto del visor con el recurso.

```html {.line-numbers}
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

La siguiente página de ejemplos ilustra un uso más real de la incrustación de diseño interactivo con una altura sin restricciones:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incrustación de diseño interactivo con anchura y altura definidas**

Si hay un diseño interactivo incrustado con la anchura y la altura definidas, el estilo de la página web es diferente; proporciona ambos tamaños al &quot;titular&quot; `DIV` y céntrelo en la ventana del explorador. Además, la página web establece el tamaño del `HTML` y `BODY` Elemento a 100%:

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

El resto de los pasos de incrustación son idénticos a la incrustación adaptable con altura sin restricciones. El ejemplo resultante es

```html {.line-numbers}
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

**Incrustación mediante una API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. Con esa API, el constructor no toma ningún parámetro y los parámetros de configuración se especifican utilizando `setContainerId()`, `setParam()`, y `setAsset()` Métodos de API con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra la incrustación de tamaño fijo con la API basada en establecedores:

```html {.line-numbers}
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
