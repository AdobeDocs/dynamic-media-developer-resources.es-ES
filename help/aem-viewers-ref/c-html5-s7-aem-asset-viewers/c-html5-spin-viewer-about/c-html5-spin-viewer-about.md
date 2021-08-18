---
description: El visor de giros es un visor de imágenes que proporciona una vista de 360 grados de la imagen o incluso una vista multidimensional si se utiliza el conjunto de giros apropiado. Tiene herramientas de zoom y giro, compatibilidad con pantalla completa y un botón de cierre opcional. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.
keywords: adaptable
solution: Experience Manager
title: Spin
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: f77dc0c1ac8305037bbb561451317c8e62209cec
workflow-type: tm+mt
source-wordcount: '2138'
ht-degree: 0%

---

# Giro{#spin}

El visor de giros es un visor de imágenes que proporciona una vista de 360 grados de la imagen o incluso una vista multidimensional si se utiliza el conjunto de giros apropiado. Tiene herramientas de zoom y giro, compatibilidad con pantalla completa y un botón de cierre opcional. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

Tipo de visor 503.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Dirección URL de la demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## Uso del visor de giros {#section-e6c68406ecdc4de781df182bbd8088b4}

El visor de giros representa un archivo JavaScript principal y un conjunto de archivos de ayuda (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visor en particular, recursos y CSS) descargados por el visor en tiempo de ejecución.

El visor de giros puede utilizarse tanto en modo emergente mediante la página HTML preparada para la producción que se proporciona con los visores IS como en modo incrustado, donde se integra en la página web de destino mediante API documentada.

La configuración y el desollado son similares a los de los demás visores. Todo el desliz se puede lograr mediante CSS personalizada.

Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visualizadores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visualizador de giros {#section-642e66ca38cd4032992840ec6c0b0cd2}

El visor de giros admite los siguientes gestos táctiles que son comunes en otras aplicaciones móviles. Cuando el usuario no puede procesar el gesto de barrido de un usuario, envía el evento al explorador web para que realice un desplazamiento de página nativo. Esta funcionalidad permite al usuario navegar por la página aunque el visor ocupe la mayor parte del área de la pantalla del dispositivo.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Doble toque </p> </td> 
   <td colname="col2"> <p> Amplía un nivel hasta alcanzar la ampliación máxima. El siguiente gesto de doble toque restablece el visor al estado de visualización inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pellizcar </p> </td> 
   <td colname="col2"> <p>Amplía o reduce la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido horizontal o deslizamiento </p> </td> 
   <td colname="col2"> <p> Si la imagen está en estado de restablecimiento, gira horizontalmente por el conjunto. </p> <p> Si la imagen se amplía, la imagen se mueve horizontalmente. Si la imagen se mueve al borde de la vista y aún se realiza un barrido en esa dirección, el gesto realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical o flexión </p> </td> 
   <td colname="col2"> <p> Si la imagen está en estado de restablecimiento, cambia el ángulo de vista vertical en caso de que se utilice un conjunto de giros multidimensional. En un conjunto de giros unidimensional, el gesto realiza un desplazamiento de página nativo. O bien, cuando un conjunto de giros multidimensional está en el último o el primer eje para que el barrido vertical no genere un cambio en el ángulo de visión vertical, el gesto también realiza un desplazamiento de página nativo. </p> <p> Si la imagen se amplía, la imagen se mueve verticalmente. Si la imagen se mueve al borde de la vista y aún se realiza un barrido en esa dirección, el gesto realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>El visor también admite entrada táctil y entrada de ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad está limitada únicamente a los navegadores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante teclado.

Consulte [Accesibilidad del teclado y navegación](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visualizador de giros {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo que, cuando se hace clic, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o en diferentes tamaños de ventana del navegador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: elemento emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

**Acerca del modo emergente**

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Toma todo el área de la ventana del explorador y se ajusta en caso de que se cambie el tamaño del explorador o de que se cambie la orientación de un dispositivo móvil.

El modo emergente es el más común para los dispositivos móviles. La página web carga el visor utilizando `window.open()` llamada de JavaScript, el elemento HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página HTML predeterminada para el modo de operación emergente. En este caso, se denomina [!DNL SpinViewer.html] y se encuentra dentro de la subcarpeta [!DNL html5/] de la implementación estándar de los visores IS:

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Puede lograr la personalización visual mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código HTML que abre el visor en una nueva ventana:

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**Acerca del modo de incrustación de tamaño fijo y el modo de incrustación de diseño interactivo**

En el modo integrado, el visor se añade a la página web existente, que puede tener ya contenido de cliente no relacionado con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de una página web.

Los casos de uso principales son páginas web orientadas a equipos de escritorio o tabletas, así como páginas de diseño adaptables que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta acción es la mejor opción para páginas web con diseño estático.

La incrustación de diseño interactivo supone que el visor debe cambiar el tamaño en tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web para su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, sin restringir su altura, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para las páginas web que usan marcos de diseño interactivo como Bootstrap o Foundation.

De lo contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellena solo esa área y sigue el tamaño que proporciona el diseño de la página web. Un buen ejemplo puede ser la incrustación del visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Integración de tamaño fijo**

Para agregar el visor de giros a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   Para crear un visor es necesario agregar una etiqueta de script en el encabezado HTML. Antes de usar la API de visor, asegúrese de incluir `SpinViewer.js`. `SpinViewer.js` se encuentra en la  [!DNL html5/js/] subcarpeta de la implementación estándar de IS-Viewers:

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores Dynamic Media de Adobe y se suministra desde el mismo dominio. De lo contrario, se especifica una ruta completa a uno de los servidores Dynamic Media de Adobe que tienen instalados los visores IS.

   La ruta relativa tiene el siguiente aspecto:

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Solo haga referencia al archivo JavaScript `include` del visor principal de la página. No haga referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargar la lógica del visor durante la ejecución. En concreto, no haga referencia directamente a la biblioteca `Utils.js` del SDK de HTML5 cargada por el visor desde la ruta de contexto `/s7viewers` (denominada SDK consolidado `include`). El motivo es que la ubicación de las `Utils.js` o bibliotecas de visores de tiempo de ejecución similares se administra completamente mediante la lógica del visor y la ubicación cambia entre las versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
   >
   >
   >Como resultado, poner una referencia directa a cualquier JavaScript `include` secundario que utilice el visor en la página rompe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del contenedor DIV.

   Agregue un elemento DIV vacío a la página donde desee que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa más tarde a la API del visor.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la propiedad `position` CSS está establecida en `relative` o `absolute`.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Configuración del tamaño del visor

   Puede establecer el tamaño estático del visor declarándolo para la clase CSS de nivel superior `.s7spinviewer` en unidades absolutas o utilizando el modificador `stagesize`.

   Puede colocar el tamaño en CSS directamente en la página HTML o en un archivo CSS de visor personalizado. Posteriormente se asigna a un registro preestablecido de visualizador en Dynamic Media Classic o se pasa explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor de giros](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) para obtener más información sobre cómo diseñar el visor con CSS.

   A continuación se muestra un ejemplo de definición de un tamaño de visor estático en una página HTML:

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede establecer el modificador `stagesize` en el registro preestablecido de visualizador en Dynamic Media Classic. O bien, puede pasarlo explícitamente con el código de inicialización del visor con la colección `params` o como una llamada de API como se describe en la sección Referencia del comando, como se indica a continuación:

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   Se recomienda un enfoque basado en CSS que se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.SpinViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto tiene un campo `containerId` que contiene el nombre del ID del contenedor de visor y el objeto `params` JSON anidado con parámetros de configuración compatibles con el visor. En este caso del objeto `params`, debe tener al menos la URL del servicio de imágenes pasada como propiedad `serverUrl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON le permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor de visor agregado al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación del DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta `BODY` de cierre o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe ser necesariamente parte del diseño de la página web todavía. Por ejemplo, puede ocultarse con el estilo `display:none` asignado. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web vuelve a poner el elemento contenedor en el diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   El siguiente es un ejemplo de creación de una instancia de visor, pasando las opciones de configuración mínimas necesarias al constructor y llamando al método `init()`. En el ejemplo se supone que `spinViewer` es la instancia del visor, `s7viewer` es el nombre del marcador de posición `DIV`, [!DNL http://s7d1.scene7.com/is/image/] es la URL del servicio de imágenes y [!DNL Scene7SharedAssets/SpinSet_Sample] es el recurso.

   ```
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

   El siguiente código es un ejemplo completo de una página web trivial que incorpora el visor de giros con un tamaño fijo:

   ```
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

La siguiente página de ejemplos ilustra casos de uso más reales de incrustación de diseño interactivo con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Integración de tamaño flexible con anchura y altura definidas**

Si hay una incrustación de tamaño flexible con anchura y altura definidas, el estilo de la página web es diferente. Es decir, proporciona ambos tamaños al &quot; titular&quot; `DIV` y lo centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en 100%:

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

**Incrustación mediante API basada en Setter**

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor no-args. Con ese constructor de API no toma ningún parámetro y se especifican parámetros de configuración mediante métodos de API `setContainerId()`, `setParam()` y `setAsset()` con llamadas de JavaScript independientes.

El siguiente ejemplo muestra la incrustación de tamaño fijo con la API basada en establecedor:

```
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
