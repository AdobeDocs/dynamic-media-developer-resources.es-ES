---
title: Varios tipos de archivo
description: El visualizador de medios mixtos es un visualizador de medios. Admite conjuntos de medios que contienen imágenes, conjuntos de muestras, conjuntos de giros, vídeos y conjuntos de vídeos adaptables.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2645'
ht-degree: 0%

---

# Varios tipos de archivo{#mixed-media}

El visualizador de medios mixtos es un visualizador de medios. Admite conjuntos de medios que contienen imágenes, conjuntos de muestras, conjuntos de giros, vídeos y conjuntos de vídeos adaptables.

Una miniatura en la parte inferior del visor representa cada elemento del conjunto de medios, junto con su indicador de tipo de recurso. Cuando se selecciona un elemento de conjunto de muestras, aparece una fila secundaria de muestras para permitir la selección de la variación de color dentro del conjunto de muestras. Las imágenes y los elementos del conjunto de muestras admiten el zoom en modo continuo o en línea; los conjuntos de giros admiten el zoom y el giro. Los conjuntos de vídeos y vídeos adaptables admiten todos los controles básicos de reproducción, siempre que se muestren subtítulos opcionales sobre el contenido de vídeo. Un usuario puede cambiar a pantalla completa en cualquier momento haciendo clic en el botón de pantalla completa. El visor tiene un botón de cierre opcional. Está diseñado para funcionar con equipos de escritorio y dispositivos móviles.

El visualizador de medios mixtos utiliza la reproducción de vídeo de flujo HTML5 en formato HLS en su configuración predeterminada siempre que el sistema subyacente lo admita. En los sistemas que no admiten la transmisión por secuencias de HTML5, el visor vuelve a la entrega progresiva de vídeo de HTML5.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

Tipo de visor 505.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Dirección URL de la demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Uso del visualizador de medios mixtos {#section-f21ac23d3f6449ad9765588d69584772}

El visualizador de medios mixtos representa un archivo JavaScript principal y un conjunto de archivos de ayuda (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visualizador en particular, recursos y CSS) descargados por el visualizador en tiempo de ejecución.

Puede utilizar el visualizador de medios mixtos en modo emergente utilizando la página HTML lista para la producción que se proporciona con los visualizadores IS. O bien, puede utilizar el visor en modo incrustado, donde se integra en una página web de destino mediante la API documentada.

La tarea de configurar y desollar el visor es similar a la de otros visores. Toda la apariencia se logra mediante CSS personalizada.

Consulte [Referencia de comando común a todos los visores: Atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visualizadores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visualizador de medios mixtos {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visualizador de medios mixtos es compatible con gestos de un solo toque y de varios toque comunes en otras aplicaciones móviles. Cuando el usuario no puede procesar el gesto de barrido de un usuario, envía el evento al explorador web para que realice un desplazamiento de página nativo. Esta funcionalidad permite al usuario navegar por la página aunque el visor ocupe la mayor parte del área de la pantalla del dispositivo.

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
   <td colname="col2"> <p> Activa la vista flotante o los cambios entre el nivel de zoom primario y el secundario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doble toque </p> </td> 
   <td colname="col2"> <p>Cuando <span class="codeph"> continuo </span> modo de zoom, reduce un nivel hasta alcanzar la ampliación máxima, el siguiente gesto de doble toque se restablece al estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tocar y mantener </p> </td> 
   <td colname="col2"> <p> Cuando <span class="codeph"> inline </span> zoom, activa la imagen ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pellizcar </p> </td> 
   <td colname="col2"> <p>Cuando se encuentra en modo de zoom continuo, amplía o reduce la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido horizontal o deslizamiento </p> </td> 
   <td colname="col2"> <p> Cuando el recurso actual es un conjunto de giros y la imagen está en estado de restablecimiento, gira horizontalmente por el conjunto de giros. </p> <p> Cuando el recurso actual es un conjunto de giros o una imagen y la imagen se amplía, la imagen se mueve horizontalmente. Si la imagen se mueve al borde de la vista y el barrido se sigue realizando en esa dirección, el gesto realiza un desplazamiento de página nativo. </p> <p> Se desplaza por la lista de muestras de la barra de muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical o flexión </p> </td> 
   <td colname="col2"> <p> Si la imagen está en estado de restablecimiento, cambia el ángulo de vista vertical en caso de que se utilice un conjunto de giros multidimensional. En un conjunto de giros unidimensionales, o cuando un conjunto de giros multidimensional está en el último o el primer eje, de modo que el barrido vertical no genere un cambio en el ángulo de visión vertical, el gesto realiza el desplazamiento nativo de la página. </p> <p> Cuando el recurso actual es un conjunto de giros o una imagen y la imagen se amplía, la imagen se mueve verticalmente. Si la imagen se mueve al borde de la vista y el barrido se sigue realizando en esa dirección, el gesto realiza el desplazamiento de la página nativo. </p> <p> Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor también admite entrada táctil y entrada de ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad está limitada únicamente a los navegadores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante teclado.

Consulte [Navegación y accesibilidad del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustar visualizador de medios mixtos {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo que, cuando se selecciona, abre el visor en una ventana independiente del explorador. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, la página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o en diferentes tamaños de ventana del navegador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: elemento emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

## Acerca del modo emergente {#section-77d5aa03b8b94566958a179b1a2cd474}

En el modo emergente, el visor se abre en una ventana o pestaña independiente del explorador web. Toma todo el área de la ventana del explorador y se ajusta en caso de que se cambie el tamaño del explorador o de que se cambie la orientación de un dispositivo móvil.

El modo emergente es el más común para los dispositivos móviles. La página web carga el visor mediante `window.open()` Llamada de JavaScript, correctamente configurada `A` elemento HTML o cualquier otro método adecuado.

Se recomienda utilizar una página de HTML predeterminada para el modo de operación emergente. En este caso, se llama [!DNL MixedMediaViewer.html] y se encuentra dentro de la variable [!DNL html5/] subcarpeta de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Puede lograr la personalización visual mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código de HTML que abre el visor en una nueva ventana:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Acerca de la incrustación de diseño interactivo y de tamaño fijo {#section-ec86b100ba5943d0b16694268520bbde}

En el modo integrado, el visor se añade a la página web existente, que puede tener ya contenido de cliente no relacionado con el visor. Normalmente, el visor solo ocupa una parte de los bienes raíces de una página web.

Los casos de uso principales son páginas web orientadas a equipos de escritorio o tabletas, así como páginas de diseño adaptables que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta acción es la mejor opción para páginas web con diseño estático.

La incrustación de diseño interactivo supone que el visor debe cambiar el tamaño durante la ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web y su contenedor `DIV`. Si la página web establece solo la anchura del contenedor `DIV`, dejando su altura sin restricciones, el visor elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para las páginas web que usan marcos de diseño interactivo como Bootstrap o Foundation.

De lo contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellena solo esa área y sigue el tamaño que proporciona el diseño de la página web. Un buen ejemplo es integrar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

## Incrustación de tamaño fijo {#section-17d162f76ffa4804b27928f51e7bea1d}

Para añadir el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   Para crear un visor es necesario agregar una etiqueta de script en el encabezado del HTML. Antes de utilizar la API del visor, asegúrese de incluir [!DNL MixedMediaViewer.js]. La variable [!DNL MixedMediaViewer.js] el archivo se encuentra debajo de [!DNL html5/js/] subcarpeta de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Dynamic Media Classic y se suministra desde el mismo dominio. De lo contrario, se especifica una ruta completa a uno de los servidores de Adobe Dynamic Media Classic que tienen instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
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

   Asegúrese de que la función de pantalla completa funciona correctamente en Internet Explorer. Compruebe que no haya otros elementos en el DOM que tengan un orden de apilamiento superior al DIV del marcador de posición.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Configuración del tamaño del visor

   Este visor muestra miniaturas al trabajar con conjuntos de varios elementos. En los sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal durante el tiempo de ejecución mediante `setAsset()` API. Como desarrollador, tiene control sobre cómo el visor gestiona el área de miniaturas en la parte inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener el tamaño de la vista principal estático y contraer el área del visor exterior, lo que permite que el contenido de la página web aumente. A continuación, utilice el espacio de página libre que queda en las miniaturas.

   Para mantener intactos los límites exteriores del visor, defina el tamaño de `.s7mixedmediaviewer` clase CSS de nivel superior en unidades absolutas. El tamaño en CSS se puede colocar directamente en la página HTML o en un archivo CSS de visor personalizado, y posteriormente se puede asignar a un registro preestablecido de visor en Dynamic Media Classic, o pasar explícitamente utilizando el comando Estilo.

   Consulte [Personalización del visualizador de medios mixtos](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición del tamaño estático del visor exterior en una página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un área fija del visor exterior en la siguiente página de muestra. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html)

   Para que las dimensiones de la vista principal sean estáticas, defina el tamaño del visor en unidades absolutas para el `Container` Componente SDK que utiliza `.s7mixedmediaviewer .s7container` Selector de CSS, o bien utilizando `stagesize` modificador.

   A continuación, se muestra un ejemplo de definición del tamaño del visor para el `Container` Componente SDK para que el área de vista principal no cambie su tamaño al cambiar el recurso:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La siguiente página de muestra muestra el comportamiento del visor con un tamaño fijo de vista principal. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html)

   Puede configurar la variable `stagesize` en el registro preestablecido de visualizador en Dynamic Media Classic o páselo explícitamente con el código de inicialización del visualizador con `params` colección. O bien, como una llamada de API como se describe en la sección Referencia de comandos de esta Ayuda, como se muestra a continuación:

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Se recomienda un enfoque basado en CSS que se utiliza en este ejemplo.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.MixedMediaViewer` clase , pase toda la información de configuración a su constructor e invoque `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener la variable `containerId` campo que contiene el nombre del ID del contenedor del visor y anidado `params` objeto JSON con parámetros de configuración compatibles con el visor. En este caso, la variable `params` debe tener al menos la dirección URL del servidor de imágenes transferida como `serverUrl` , la URL del servidor de vídeo se transfiere como `videoserverurl` propiedad y activo inicial como `asset` parámetro. La API de inicialización basada en JSON le permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor de visor agregado al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación del DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame a la función `init()` justo antes del cierre `BODY` o en el cuerpo `onload()` evento.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, puede ocultarse usando `display:none` estilo asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web vuelve a poner el elemento contenedor en el diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de creación de una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar a la función `init()` método. El ejemplo asume `mixedMediaViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; [!DNL http://s7d1.scene7.com/is/image/] es la URL del servicio de imágenes; [!DNL http://s7d1.scene7.com/is/content/] es la URL del servidor de vídeo; y [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] es el recurso:

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

## Incrustación interactiva con altura ilimitada {#section-056cb574713c4d07be6d07cf3c598839}

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible en su lugar que dicta el tamaño de tiempo de ejecución del contenedor del visor `DIV`. Para el siguiente ejemplo, supongamos que la página web permite el contenedor del visor `DIV` para tomar el 40% del tamaño de la ventana del explorador web, sin restringir su altura. El código del HTML de la página web tendría el siguiente aspecto:

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
1. Definición del contenedor DIV.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Agregue el DIV de contenedor a la `"holder"` DIV. El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo la proporción de aspecto del visor coincide con el recurso.

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

La página de ejemplos siguientes ilustra más usos reales de la incrustación de diseño interactivo con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Integración de tamaño flexible con anchura y altura definidas {#section-0a329016f9414d199039776645c693de}

Si hay una incrustación de tamaño flexible con anchura y altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños a la variable `"holder"` DIV y lo centra en la ventana del explorador. Además, la página web establece el tamaño de la variable `HTML` y `BODY` al 100 por ciento.

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

El resto de los pasos de incrustación son idénticos a los pasos utilizados para el diseño interactivo incrustado con altura ilimitada. El ejemplo resultante es el siguiente:

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

## Incrustación mediante API basada en Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor no-args. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican usando `setContainerId()`, `setParam()`y `setAsset()` métodos de API, con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de incrustación de tamaño fijo con API basada en establecedor:

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
