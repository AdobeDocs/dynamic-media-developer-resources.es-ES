---
title: Spin
description: El visualizador de giros es un visualizador de imágenes que proporciona una vista de 360 grados de la imagen o incluso una vista multidimensional si se está utilizando un conjunto de giros adecuado. Tiene herramientas de zoom y giro, compatibilidad con pantalla completa y un botón de cierre opcional. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---

# Spin{#spin}

El visualizador de giros es un visualizador de imágenes que proporciona una vista de 360 grados de la imagen o incluso una vista multidimensional si se está utilizando un conjunto de giros adecuado. Tiene herramientas de zoom y giro, compatibilidad con pantalla completa y un botón de cierre opcional. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor.

Tipo de visor 503.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## Uso del visor de giros {#section-e6c68406ecdc4de781df182bbd8088b4}

Spin Viewer representa un archivo JavaScript principal y un conjunto de archivos de ayuda (una sola inclusión JavaScript con todos los componentes del SDK del visor utilizados por este visor, recursos y CSS) descargados por el visor en tiempo de ejecución.

El visor de giros se puede utilizar en el modo emergente utilizando la página del HTML lista para la producción proporcionada con los visores de IS o en el modo incrustado, donde se integra en la página web de destino mediante la API documentada.

La configuración y el desollado son similares a los de otros visores. Todo el desollamiento se puede lograr a través de CSS personalizado.

Consulte [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de giros {#section-642e66ca38cd4032992840ec6c0b0cd2}

El visor de giros admite los siguientes gestos táctiles, que son comunes en otras aplicaciones móviles. Cuando el visor no puede procesar un gesto de barrido del usuario, reenvía el evento al explorador web para realizar un desplazamiento de página nativa. Esta funcionalidad permite al usuario navegar por la página incluso si el visor ocupa la mayor parte del área de la pantalla del dispositivo.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Pulse dos veces </p> </td> 
   <td colname="col2"> <p> Aumenta el tamaño de un nivel hasta que se alcanza el máximo de aumento. El siguiente gesto de doble toque restablece al visor al estado de visualización inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pellizco </p> </td> 
   <td colname="col2"> <p>Aumenta o reduce la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o gesto horizontal </p> </td> 
   <td colname="col2"> <p> Si la imagen está en estado de restablecimiento, gira horizontalmente por el conjunto. </p> <p> Si la imagen se amplía, la mueve horizontalmente. Si la imagen se mueve al borde de la vista y aún se realiza un barrido en esa dirección, el gesto realiza un desplazamiento de página nativa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deslizar o gesto vertical </p> </td> 
   <td colname="col2"> <p> Si la imagen está en estado de restablecimiento, cambia el ángulo de vista vertical en caso de que se utilice un conjunto de giros multidimensional. En un conjunto de giros unidimensional, el gesto realiza un desplazamiento de página nativo. O bien, cuando un conjunto de giros multidimensional está en el último o en el primer eje para que el barrido vertical no genere un cambio en el ángulo de vista vertical, el gesto también realiza un desplazamiento de página nativo. </p> <p> Si la imagen se amplía, la mueve verticalmente. Si la imagen se mueve al borde de la vista y aún se realiza un barrido en esa dirección, el gesto realiza un desplazamiento de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El visor también admite la entrada táctil y la entrada del ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad se limita únicamente a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante el teclado.

Consulte [Navegación y accesibilidad del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor de giros {#section-6bb5d3c502544ad18a58eafe12a13435}

Las distintas páginas web tienen diferentes necesidades de comportamiento del visualizador. A veces, una página web proporciona un vínculo que, cuando se selecciona, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el derecho de visor en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de funcionamiento principales: emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Ocupa todo el área de la ventana del explorador y se ajusta en caso de que cambie el tamaño del explorador o la orientación de un dispositivo móvil.

El modo emergente es el más común en dispositivos móviles. La página web carga el visor mediante `window.open()` Llamada de JavaScript, correctamente configurada `A` elemento HTML o cualquier otro método adecuado.

Se recomienda utilizar una página de HTML predeterminada para el modo de operación emergente. En este caso, se llama [!DNL SpinViewer.html] y se encuentra dentro de [!DNL html5/] de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Puede conseguir una personalización visual aplicando CSS personalizado.

A continuación se muestra un ejemplo de código de HTML que abre el visor en una nueva ventana:

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo incrustado, el visor se añade a la página web existente, que puede tener ya contenido de clientes no relacionado con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de una página web.

Los casos de uso principales son páginas web orientadas para equipos de escritorio o tabletas, y también páginas de diseño interactivo que ajustan el diseño automáticamente según el tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta acción es la mejor opción para las páginas web que tienen un diseño estático.

La incrustación de diseño interactivo supone que el visualizador debe cambiar de tamaño durante la ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es añadir un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente según la forma en que la página web ajusta el tamaño de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`Sin embargo, y sin restricciones de altura, el visualizador elige automáticamente su altura según la relación de aspecto del recurso utilizado. Esta funcionalidad garantiza que el recurso se ajuste perfectamente a la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que utilizan marcos de diseño adaptable como Bootstrap o Foundation.

En caso contrario, si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellena solo esa área y sigue el tamaño que proporciona el diseño de página web. Un buen ejemplo puede ser la incrustación del visualizador en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Incrustación de tamaño fijo**

Para añadir el visor de giros a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado del HTML. Antes de usar la API de visor, asegúrese de incluir lo siguiente `SpinViewer.js`. `SpinViewer.js` se encuentra debajo de [!DNL html5/js/] de la implementación estándar de IS-Viewers:

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Dynamic Media de Adobe y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Dynamic Media de Adobe que tengan instalados los visores de IIS.

   La ruta relativa tiene el siguiente aspecto:

   ```html {.line-numbers}
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Solo referencia al visor principal JavaScript `include` en la página. No haga referencia a ningún archivo JavaScript adicional en el código de la página web que la lógica del visor pueda descargar durante la ejecución. En concreto, no haga referencia directamente al SDK de HTML5 `Utils.js` biblioteca cargada por el visor desde `/s7viewers` ruta de contexto (denominado SDK consolidado) `include`). El motivo es que la ubicación de `Utils.js` Para bibliotecas de visualizadores en tiempo de ejecución similares, la lógica del visualizador las gestiona completamente y la ubicación cambia entre versiones del visualizador. El Adobe no mantiene las versiones anteriores del visor secundario `includes` en el servidor.
   >
   >
   >Como resultado, se hace referencia directa a cualquier JavaScript secundario `include` que el usuario utiliza en la página interrumpe la funcionalidad del usuario en el futuro cuando se implemente una nueva versión del producto.

1. Definición del DIV de contenedor.

   Añada un elemento DIV vacío a la página donde desea que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa posteriormente a la API del visor.

   El DIV de marcador de posición es un elemento posicionado, lo que significa que la variable `position` La propiedad CSS se establece en `relative` o `absolute`.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para `.s7spinviewer` clase CSS de nivel superior en unidades absolutas o utilizando `stagesize` modificador.

   Puede colocar el tamaño en CSS directamente en la página del HTML o en un archivo CSS de visor personalizado. Posteriormente, se asigna a un registro de ajuste preestablecido de visualizador en Dynamic Media Classic o se pasa explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor de giros](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en una página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede configurar las variables `stagesize` modificador en el registro de ajuste preestablecido de visor en Dynamic Media Classic. O bien, puede pasarlo explícitamente con el código de inicialización del visor con `params` o como una llamada API como se describe en la sección Referencia de comandos, como se muestra a continuación:

   ```html {.line-numbers}
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   Se recomienda un enfoque basado en CSS y se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.SpinViewer` , pase toda la información de configuración a su constructor y llame a `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto tiene `containerId` que contiene el nombre del ID de contenedor del visor y el campo anidado `params` Objeto JSON con parámetros de configuración compatibles con el visor. En este caso de `params` debe tener al menos la URL del servicio de imágenes pasada como `serverUrl` propiedad y recurso inicial como `asset` parámetro. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` método justo antes del cierre `BODY` o en el cuerpo `onload()` evento.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web. Por ejemplo, se puede ocultar utilizando la variable `display:none` estilo asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar a `init()` método. El ejemplo supone `spinViewer` es la instancia del visor, `s7viewer` es el nombre del marcador de posición `DIV`, [!DNL http://s7d1.scene7.com/is/image/] es la URL del servicio de imágenes y [!DNL Scene7SharedAssets/SpinSet_Sample] es el recurso.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visor de giros con un tamaño fijo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Inserción de diseño interactivo con altura sin restricciones**

Con incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que dicta el tamaño de tiempo de ejecución del contenedor del visualizador `DIV`. A efectos de este ejemplo, supongamos que la página web permite el contenedor del visor `DIV` para ocupar el 40 % del tamaño de la ventana del explorador web, sin restringir su altura. El código de HTML de página web resultante tiene el siguiente aspecto:

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

Añadir el visor a una página de este tipo es similar a la incrustación de tamaño fijo, con la única diferencia de que no es necesario definir explícitamente el tamaño del visor.

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del DIV de contenedor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Añadir el contenedor `DIV` al &quot;titular&quot; existente `DIV`. El siguiente código es un ejemplo completo. Puede ver cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo coincide la proporción de aspecto del visor con el recurso.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La siguiente página de ejemplos ilustra casos de uso más reales de incrustación de diseño interactivo con altura sin restricciones:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incrustación de tamaño flexible con anchura y altura definidas**

Si hay una incrustación de tamaño flexible con la anchura y la altura definidas, el estilo de la página web es diferente. Es decir, proporciona ambos tamaños al &quot;titular&quot; `DIV` y lo centra en la ventana del explorador. Además, la página web establece el tamaño del `HTML` y `BODY` Elemento a 100%:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incrustación mediante una API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. Con ese constructor de API no toma ningún parámetro y los parámetros de configuración se especifican utilizando `setContainerId()`, `setParam()`, y `setAsset()` Métodos de API con llamadas de JavaScript independientes.

El siguiente ejemplo muestra la incrustación de tamaño fijo con la API basada en establecedores:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
