---
title: Medios mixtos
description: Visor de medios mixtos es un visor de medios. Admite conjuntos de medios que contienen imágenes, conjuntos de muestras, conjuntos de giros, vídeos y conjuntos de vídeos adaptables.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2581'
ht-degree: 0%

---

# Medios mixtos{#mixed-media}

Visor de medios mixtos es un visor de medios. Admite conjuntos de medios que contienen imágenes, conjuntos de muestras, conjuntos de giros, vídeos y conjuntos de vídeos adaptables.

Una miniatura en la parte inferior del visor representa cada elemento del conjunto de medios, junto con su indicador de tipo de recurso. Cuando se selecciona un elemento del conjunto de muestras, aparece una fila secundaria de muestras para permitir la selección de la variación de color dentro del conjunto de muestras. Las imágenes y los elementos de conjuntos de muestras admiten el zoom en modo continuo o en línea; los conjuntos de giros admiten el zoom y el giro. Los vídeos y los conjuntos de vídeos adaptables admiten todos los controles básicos de reproducción, siempre y cuando se muestren subtítulos opcionales encima del contenido de vídeo. Un usuario puede cambiar a pantalla completa en cualquier momento haciendo clic en el botón de pantalla completa. El visor tiene un botón de cierre opcional. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

El visualizador de medios mixtos utiliza la reproducción de vídeo de flujo HTML5 en formato HLS en su configuración predeterminada siempre que el sistema subyacente admita eso. En sistemas que no admiten el streaming de HTML5, el visor vuelve a recibir la entrega de vídeo progresivo de HTML5.

>[!NOTE]
>
>Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor.

Tipo de visor 505.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Uso del visualizador de medios mixtos {#section-f21ac23d3f6449ad9765588d69584772}

El visualizador de medios mixtos representa un archivo JavaScript principal y un conjunto de archivos de ayuda (una sola inclusión JavaScript con todos los componentes de SDK del visualizador utilizados por este visualizador, recursos y CSS) descargados por el visualizador en tiempo de ejecución.

Puede utilizar el visualizador de medios mixtos en el modo emergente utilizando la página de HTML lista para la producción proporcionada con los visualizadores de IS. O bien, puede utilizar el visualizador en modo incrustado, donde se integra en una página web de destino mediante la API documentada.

La tarea de configurar y desollar el visor es similar a la de otros visores. Todo el desollado se logra mediante CSS personalizado.

Ver [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visualizador de medios mixtos {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visualizador de medios mixtos admite gestos de un solo toque y de varios toques que son comunes en otras aplicaciones móviles. Cuando el visor no puede procesar un gesto de barrido del usuario, reenvía el evento al explorador web para realizar un desplazamiento de página nativa. Esta funcionalidad permite al usuario navegar por la página incluso si el visor ocupa la mayor parte del área de la pantalla del dispositivo.

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
   <td colname="col2"> <p> Activa la vista flotante o cambia entre el nivel de zoom principal y secundario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pulse dos veces </p> </td> 
   <td colname="col2"> <p>En el modo de zoom continuo <span class="codeph"> de </span>, se amplía un nivel hasta que se alcanza la ampliación máxima y el siguiente gesto de doble toque se restablece al estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tocar y mantener </p> </td> 
   <td colname="col2"> <p> En el modo de zoom <span class="codeph"> dentro de la línea </span>, activa la imagen ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pellizco </p> </td> 
   <td colname="col2"> <p>En el modo de zoom continuo, amplía o reduce la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o gesto horizontal </p> </td> 
   <td colname="col2"> <p> Cuando el recurso actual es un conjunto de giros y la imagen está en estado de restablecimiento, gira a través del conjunto de giros horizontalmente. </p> <p> Cuando el recurso actual es un conjunto de giros o una imagen y la imagen está ampliada, la imagen se mueve horizontalmente. Si la imagen se mueve al borde de la vista y el barrido sigue realizándose en esa dirección, el gesto realiza un desplazamiento de página nativa. </p> <p> Se desplaza por la lista de muestras de la barra de muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deslizar o gesto vertical </p> </td> 
   <td colname="col2"> <p> Si la imagen está en estado de restablecimiento, cambia el ángulo de vista vertical en caso de que se utilice un conjunto de giros multidimensional. En un conjunto de giros unidimensional, o cuando un conjunto de giros multidimensional está en el último o el primer eje, de modo que el barrido vertical no produce un cambio en el ángulo de vista vertical, el gesto realiza un desplazamiento de página nativo. </p> <p> Cuando el recurso actual es un conjunto de giros o una imagen y la imagen está ampliada, la imagen se mueve verticalmente. Si la imagen se mueve al borde de la vista y el barrido sigue realizándose en esa dirección, el gesto realiza un desplazamiento de página nativo. </p> <p> Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor también admite la entrada táctil y la entrada del ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad se limita únicamente a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante el teclado.

Consulte [Navegación y accesibilidad por teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visualizador de medios mixtos {#section-6bb5d3c502544ad18a58eafe12a13435}

Las distintas páginas web tienen diferentes necesidades de comportamiento del visualizador. A veces, una página web proporciona un vínculo que, cuando se selecciona, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el derecho de visor en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de funcionamiento principales: emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

## Acerca del modo emergente {#section-77d5aa03b8b94566958a179b1a2cd474}

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Ocupa todo el área de la ventana del explorador y se ajusta en caso de que cambie el tamaño del explorador o la orientación de un dispositivo móvil.

El modo emergente es el más común en dispositivos móviles. La página web carga el visor mediante la llamada de JavaScript `window.open()`, el elemento HTML `A` configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página de HTML predeterminada para el modo de operación emergente. En este caso, se llama [!DNL MixedMediaViewer.html] y se encuentra dentro de la subcarpeta [!DNL html5/] de su implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Puede conseguir una personalización visual aplicando CSS personalizado.

A continuación se muestra un ejemplo de código HTML que abre el visor en una nueva ventana:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Acerca de la incrustación de tamaño fijo y diseño interactivo {#section-ec86b100ba5943d0b16694268520bbde}

En el modo incrustado, el visor se añade a la página web existente, que puede tener ya contenido de clientes no relacionado con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de una página web.

Los casos de uso principales son páginas web orientadas para equipos de escritorio o tabletas, y también páginas de diseño interactivo que ajustan el diseño automáticamente según el tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta acción es la mejor opción para las páginas web que tienen un diseño estático.

La incrustación de diseño interactivo supone que el visor debe cambiar de tamaño durante la ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es añadir un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente según la forma en que la página web ajusta el tamaño de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV` y deja su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad garantiza que el recurso se ajuste perfectamente a la vista sin ningún relleno en los lados. Este caso de uso es el más común para páginas web que utilizan marcos de diseño adaptable como Bootstrap o Foundation.

De lo contrario, si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellena sólo esa área y sigue el tamaño que proporciona el diseño de página web. Un buen ejemplo es la incrustación del visualizador en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

## Incrustación de tamaño fijo {#section-17d162f76ffa4804b27928f51e7bea1d}

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definir el contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo de JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado de HTML. Antes de usar la API de visor, asegúrese de incluir [!DNL MixedMediaViewer.js]. El archivo [!DNL MixedMediaViewer.js] se encuentra en la subcarpeta [!DNL html5/js/] de su implementación estándar de visores IS:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tengan instalados los visores de IIS.

La ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Solo haga referencia al archivo de JavaScript `include` del visor principal en su página. No haga referencia a ningún archivo JavaScript adicional en el código de la página web que la lógica del visor pueda descargar durante la ejecución. En particular, no haga referencia directamente a la biblioteca HTML5 SDK `Utils.js` cargada por el visor desde la ruta de contexto `/s7viewers` (denominada SDK consolidado `include`). El motivo es que la ubicación de `Utils.js` o bibliotecas similares del visor en tiempo de ejecución está completamente administrada por la lógica del visor y la ubicación cambia entre versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, al establecer una referencia directa a cualquier JavaScript `include` secundario que use el visor en la página, se interrumpe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición del DIV de contenedor.

   Añada un elemento DIV vacío a la página donde desea que aparezca el visor. El elemento DIV debe tener su ID definido, ya que este ID se pasa posteriormente a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El DIV de marcador de posición es un elemento posicionado, lo que significa que la propiedad CSS `position` está establecida en `relative` o `absolute`.

   Asegúrese de que la característica de pantalla completa funciona correctamente en Internet Explorer. Asegúrese de que no haya otros elementos en el DOM que tengan un orden de apilamiento más alto que el DIV de marcador de posición.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Configuración del tamaño del visor

   Este visor muestra miniaturas cuando se trabaja con conjuntos de varios elementos. En sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal durante el tiempo de ejecución mediante la API `setAsset()`. Como desarrollador, tiene control sobre cómo administra el visor el área de miniaturas en la parte inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener el tamaño de la vista principal estático y contraer el área del visor exterior, permitiendo que el contenido de la página web suba. A continuación, utilice los bienes raíces de la página gratuita que se deja desde las miniaturas.

   Para mantener intactos los límites del visor exterior, defina el tamaño de la clase CSS de nivel superior `.s7mixedmediaviewer` en unidades absolutas. El tamaño en CSS se puede ajustar directamente en la página de HTML o en un archivo CSS de visor personalizado, y luego asignarse a un registro de ajuste preestablecido de visor en Dynamic Media Classic, o pasarse explícitamente mediante el comando de estilo.

   Consulte [Personalización del visor de medios mixtos](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición del tamaño del visor exterior estático en una página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un área de visor exterior fija en la siguiente página de muestra. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=es](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=es)

   Para que las dimensiones de la vista principal sean estáticas, defina el tamaño del visor en unidades absolutas para el componente SDK `Container` interno mediante el selector CSS `.s7mixedmediaviewer .s7container` o mediante el modificador `stagesize`.

   A continuación se muestra un ejemplo de definición del tamaño del visor para el componente SDK `Container` interno de modo que el área de vista principal no cambie su tamaño al cambiar el recurso:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La siguiente página de ejemplo muestra el comportamiento del visor con un tamaño de vista principal fijo. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=es](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=es)

   Puede establecer el modificador `stagesize` en el registro de ajustes preestablecidos de visor de Dynamic Media Classic o pasarlo explícitamente con el código de inicialización del visor con la colección `params`. O bien, como una llamada API como se describe en la sección Referencia de comandos de esta Ayuda, como en el siguiente ejemplo:

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Se recomienda un enfoque basado en CSS y se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de la clase `s7viewers.MixedMediaViewer`, pase toda la información de configuración a su constructor y llame al método `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el campo `containerId` que contiene el nombre del ID del contenedor del visor y el objeto JSON `params` anidado con parámetros de configuración compatibles con el visor. En este caso, el objeto `params` debe tener al menos la URL del servicio de imágenes pasada como propiedad `serverUrl`, la URL del servidor de vídeo pasada como propiedad `videoserverurl` y el recurso inicial como parámetro `asset`. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` justo antes de la etiqueta de cierre `BODY` o en el evento `onload()` del cuerpo.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, se puede ocultar usando el estilo `display:none` asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar al método `init()`. El ejemplo supone que `mixedMediaViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; [!DNL http://s7d1.scene7.com/is/image/] es la dirección URL del servicio de imágenes; [!DNL http://s7d1.scene7.com/is/content/] es la dirección URL del servidor de vídeo; y [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] es el recurso:

```html {.line-numbers}
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

El siguiente código es un ejemplo completo de una página web trivial que incrusta el visualizador de medios mixtos con un tamaño fijo:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Inserción adaptable con altura sin restricciones {#section-056cb574713c4d07be6d07cf3c598839}

Con incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que dicta el tamaño de tiempo de ejecución del contenedor del visor `DIV`. En el siguiente ejemplo, supongamos que la página web permite que el contenedor del visor `DIV` ocupe el 40% del tamaño de la ventana del explorador web, sin restringir su altura. El código HTML de la página web tendría el siguiente aspecto:

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

1. Añadir el archivo de JavaScript del visor a la página web.
1. Definición del DIV de contenedor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Agregue el DIV contenedor al DIV `"holder"` existente. El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo la proporción de aspecto del visor coincide con el recurso.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La siguiente página de ejemplos ilustra usos más reales del diseño interactivo incrustado con una altura sin restricciones:

[Demostraciones en vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=es)

## Incrustación de tamaño flexible con anchura y altura definidas {#section-0a329016f9414d199039776645c693de}

Si hay una incrustación de tamaño flexible con la anchura y la altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños al DIV `"holder"` y lo centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y `BODY` en un 100 por ciento.

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

El resto de los pasos de incrustación son idénticos a los pasos utilizados para la incrustación de diseño interactivo con altura sin restricciones. El ejemplo resultante es el siguiente:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incrustación mediante una API basada en Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante los métodos de API `setContainerId()`, `setParam()` y `setAsset()`, con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de incrustación de tamaño fijo con API basada en establecedores:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```
