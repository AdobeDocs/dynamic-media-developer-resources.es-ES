---
description: El visor de medios mixtos es un visor de medios. Admite conjuntos de medios que contienen imágenes, conjuntos de muestras, conjuntos de giros, vídeos y conjuntos de vídeos adaptables.
keywords: responsive
seo-description: El visor de medios mixtos es un visor de medios. Admite conjuntos de medios que contienen imágenes, conjuntos de muestras, conjuntos de giros, vídeos y conjuntos de vídeos adaptables.
seo-title: Varios tipos de archivo
solution: Experience Manager
title: Varios tipos de archivo
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Varios tipos de archivo{#mixed-media}

El visor de medios mixtos es un visor de medios. Admite conjuntos de medios que contienen imágenes, conjuntos de muestras, conjuntos de giros, vídeos y conjuntos de vídeos adaptables.

Una miniatura en la parte inferior del visor representa cada elemento de conjunto de medios, junto con su indicador de tipo de recurso. Cuando se selecciona un elemento de conjunto de muestras, aparece una fila secundaria de muestras para permitir la selección de la variación de color dentro del conjunto de muestras. Las imágenes y los elementos del conjunto de muestras admiten el zoom en modo continuo o en línea; los conjuntos de giros admiten el zoom y el giro. Los vídeos y los conjuntos de vídeos adaptables admiten todos los controles de reproducción básicos siempre que se muestren los subtítulos opcionales encima del contenido del vídeo. Un usuario puede cambiar a pantalla completa en cualquier momento haciendo clic en el botón de pantalla completa. El visor tiene un botón de cierre opcional. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

El visor de medios mixtos utiliza la reproducción de vídeo de flujo HTML5 en formato HLS en su configuración predeterminada siempre que el sistema subyacente lo admita. En sistemas que no admiten el flujo HTML5, el visor vuelve al envío de vídeo progresivo HTML5.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

Tipo de visor 505.

Consulte Requisitos y requisitos previos [del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Uso del visor de medios mixtos {#section-f21ac23d3f6449ad9765588d69584772}

El visor de medios mixtos representa un archivo JavaScript principal y un conjunto de archivos auxiliares (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visor concreto, recursos y CSS) descargados por el visor en tiempo de ejecución.

Puede utilizar el visor de medios mixtos en modo emergente mediante la página HTML preparada para la producción que se proporciona con los visores IS. O bien, puede utilizar el visor en modo incrustado, donde se integra en una página web de destinatario mediante la API documentada.

La tarea de configurar y aplicar aspectos al visor es similar a la de otros visores. Todos los aspectos se logran mediante CSS personalizada.

Consulte Referencia [de comandos común a todos los visores: Atributos](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuración y referencia de [comandos comunes a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor de medios mixtos {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visor de medios mixtos admite gestos de un solo toque y de varios toque, que son comunes en otras aplicaciones móviles. Cuando el visor no puede procesar el gesto de barrido de un usuario, reenvía el evento al navegador web para realizar un desplazamiento de página nativo. Esta funcionalidad permite al usuario navegar por la página aunque el visor ocupe la mayor parte del área de la pantalla del dispositivo.

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
   <td colname="col1"> <p>Tocar Doble </p> </td> 
   <td colname="col2"> <p>Cuando se encuentra en <span class="codeph"> el modo de </span> zoom continuo, se amplía un nivel hasta alcanzar el máximo de ampliación, el siguiente gesto de toque de doble se restablece al estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tocar y mantener </p> </td> 
   <td colname="col2"> <p> Cuando se encuentra en <span class="codeph"> modo </span> de zoom en línea, activa la imagen ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pellizcar </p> </td> 
   <td colname="col2"> <p>Cuando se encuentra en modo de zoom continuo, amplía o reduce la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o barrido horizontal </p> </td> 
   <td colname="col2"> <p> Cuando el recurso actual es un conjunto de giros y la imagen está en estado de restablecimiento, gira horizontalmente por el conjunto de giros. </p> <p> Cuando el recurso actual es un conjunto de giros o una imagen y la imagen se amplía, la imagen se mueve horizontalmente. Si la imagen se mueve al borde de la vista y el barrido se sigue realizando en esa dirección, el gesto realiza un desplazamiento de página nativo. </p> <p> Se desplaza por la lista de muestras en la barra de muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido o barrido vertical </p> </td> 
   <td colname="col2"> <p> Si la imagen está en estado de restablecimiento, cambia el ángulo de vista vertical en caso de que se utilice un conjunto de giros multidimensional. En un conjunto de giros unidimensional, o cuando un conjunto de giros multidimensional se encuentra en el último o primer eje, de modo que el barrido vertical no dé como resultado un cambio en el ángulo de vista vertical, el gesto realiza un desplazamiento de página nativo. </p> <p> Cuando el recurso actual es un conjunto de giros o una imagen y la imagen se amplía, la imagen se mueve verticalmente. Si la imagen se mueve al borde de la vista y el barrido se sigue realizando en esa dirección, el gesto realiza un desplazamiento de página nativo. </p> <p> Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor también admite entrada táctil y entrada de ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad está limitada a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante teclado.

Consulte Navegación y accesibilidad [del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación de un visor de medios mixtos {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. A veces, una página web proporciona un vínculo que, al hacer clic en él, abre el visor en una ventana de explorador independiente. En otros casos, es necesario incrustar el visor directamente en la página de alojamiento. En este último caso, es posible que la página web tenga un diseño de página estático o utilice un diseño interactivo que se muestre de forma diferente en distintos dispositivos o en diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite tres modos de operación principales: ventana emergente, incrustación de tamaño fijo e incrustación de diseño interactivo.

## Acerca del modo emergente {#section-77d5aa03b8b94566958a179b1a2cd474}

En el modo emergente, el visor se abre en una ventana o ficha separada del explorador Web. Toma todo el área de la ventana del navegador y se ajusta en caso de que se cambie el tamaño del navegador o la orientación del dispositivo móvil.

El modo emergente es el más común para dispositivos móviles. La página web carga el visor mediante una llamada de `window.open()` JavaScript, un elemento `A` HTML configurado correctamente o cualquier otro método adecuado.

Se recomienda utilizar una página HTML lista para usar en el modo de operación emergente. En este caso, se le llama [!DNL MixedMediaViewer.html] y se encuentra dentro de la [!DNL html5/] subcarpeta de la implementación estándar de visores IS:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Puede lograr la personalización visual mediante la aplicación de CSS personalizada.

A continuación se muestra un ejemplo de código HTML que abre el visor en una ventana nueva:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Acerca de la incrustación de diseño adaptable y de tamaño fijo {#section-ec86b100ba5943d0b16694268520bbde}

En el modo incrustado, el visor se agrega a la página web existente, que puede tener ya contenido de cliente no relacionado con el visor. Normalmente, el visor ocupa solo una parte del espacio de una página web.

Los casos de uso principales son las páginas web orientadas a equipos de escritorio o tabletas, y también las páginas de diseño adaptables que ajustan el diseño automáticamente en función del tipo de dispositivo.

La incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta es la mejor opción para las páginas web con un diseño estático.

La incrustación de diseño adaptable supone que es posible que el visor tenga que cambiar el tamaño en tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función del tamaño de la página web en su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, dejando su altura sin restricciones, el visor selecciona automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad garantiza que el recurso encaje perfectamente en la vista sin ningún relleno en los lados. Este caso de uso es el más común para las páginas web que utilizan marcos de diseño interactivos como Bootstrap, Foundation, etc.

En caso contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellena solo esa área y sigue el tamaño que proporciona el diseño de la página web. Un buen ejemplo es la incrustación del visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del navegador web.

## Incrustación de tamaño fijo {#section-17d162f76ffa4804b27928f51e7bea1d}

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor en la página web.

   La creación de un visor requiere que agregue una etiqueta de script en el encabezado HTML. Antes de utilizar la API de visor, asegúrese de incluir [!DNL MixedMediaViewer.js]. El [!DNL MixedMediaViewer.js] archivo se encuentra en la [!DNL html5/js/] subcarpeta de la implementación estándar de los visores de IS:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Scene7 y se suministra desde el mismo dominio. De lo contrario, debe especificar una ruta de acceso completa a uno de los servidores de Adobe Scene7 que tenga instalados los visores IS.

La ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Solo debe hacer referencia al archivo JavaScript `include` del visor principal de la página. No debe hacer referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargarse mediante la lógica del visor en tiempo de ejecución. En concreto, no haga referencia directa a la biblioteca del SDK `Utils.js` HTML5 cargada por el visor desde la ruta de `/s7viewers` contexto (el denominado SDK consolidado `include`). El motivo es que la ubicación de las bibliotecas de visores en tiempo de ejecución `Utils.js` o similares está totalmente gestionada por la lógica del visor y la ubicación cambia entre las versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, la colocación de una referencia directa a cualquier JavaScript secundario `include` utilizado por el visor en la página interrumpe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición de la DIV de contenedor.

   Añada un elemento DIV vacío a la página en la que desea que aparezca el visor. El ID del elemento DIV debe estar definido porque este ID se pasa más tarde a la API del visor. El DIV tiene su tamaño especificado mediante CSS.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la propiedad `position` CSS está definida como `relative` o `absolute`.

   Asegúrese de que la función de pantalla completa funciona correctamente en Internet Explorer. Compruebe que no hay otros elementos en el DOM que tengan un orden de apilamiento superior al del marcador de posición DIV.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Configuración del tamaño del visor

   Este visor muestra miniaturas al trabajar con conjuntos de varios elementos. En los sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal durante la ejecución mediante `setAsset()` API. Como desarrollador, tiene control sobre cómo gestiona el visor el área de miniaturas en la parte inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener el tamaño de vista principal estático y contraer el área del visor exterior, permitiendo que el contenido de la página web se mueva hacia arriba y, a continuación, utilizar el espacio de la página libre que queda en las miniaturas.

   Para mantener intactos los límites exteriores del visor, defina el tamaño de la clase CSS de nivel `.s7mixedmediaviewer` superior en unidades absolutas. El tamaño en CSS se puede colocar directamente en la página HTML o en un archivo CSS de visor personalizado, que posteriormente se asignará a un registro de ajuste preestablecido de visor en Scene7 Publishing System, o se pasará explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) de medios mixtos para obtener más información sobre el estilo del visor con CSS.

   A continuación se muestra un ejemplo de definición del tamaño del visor externo estático en una página HTML:

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un área de visor exterior fija en la siguiente página de muestra. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   Para que las dimensiones de la vista principal sean estáticas, defina el tamaño del visor en unidades absolutas para el componente `Container` SDK interno mediante el selector `.s7mixedmediaviewer .s7container` de CSS o mediante `stagesize` un modificador.

   A continuación se muestra un ejemplo de definición del tamaño del visor para el componente `Container` SDK interno, de modo que el área de vista principal no cambie su tamaño al cambiar el recurso:

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La siguiente página de muestra muestra el comportamiento del visor con un tamaño de vista principal fijo. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   Puede definir el `stagesize` modificador en el registro de ajustes preestablecidos de visor de Scene7 Publishing System o pasarlo explícitamente con el código de inicialización del visor con `params` colección, o como una llamada de API como se describe en la sección Referencia de comandos de esta Ayuda, como se muestra a continuación:

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   En este ejemplo se recomienda un enfoque basado en CSS.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.MixedMediaViewer` clase, pase toda la información de configuración a su constructor y al `init()` método de llamada en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el `containerId` `params` campo que contiene el nombre del ID de contenedor del visor y el objeto JSON anidado con parámetros de configuración compatibles con el visor. En este caso, el `params` objeto debe tener al menos la URL del servicio de imágenes pasada como `serverUrl` propiedad, la URL del servidor de vídeo se pasa como `videoserverurl` propiedad y el recurso inicial como `asset` parámetro. La API de inicialización basada en JSON permite crear y inicio del visor con una sola línea de código.

   Es importante que el contenedor del visor se añada al DOM para que el código del visor pueda encontrar el elemento de contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al `init()` método justo antes de la `BODY` etiqueta de cierre o en el `onload()` evento body.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web. Por ejemplo, puede ocultarse con `display:none` el estilo asignado. En este caso, el visor retrasa el proceso de inicialización hasta el momento en que la página web devuelve el elemento de contenedor a la presentación. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de creación de una instancia de visor, pasando las opciones de configuración mínimas necesarias al constructor y llamando al `init()` método. Se supone que el ejemplo `mixedMediaViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; [!DNL http://s7d1.scene7.com/is/image/] es la dirección URL del servicio de imágenes; [!DNL http://s7d1.scene7.com/is/content/] es la URL del servidor de vídeo; y [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] es el recurso:

```
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

El siguiente código es un ejemplo completo de una página web trivial que incorpora el visor de medios mixtos con un tamaño fijo:

```
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

## Incrustación interactiva con altura sin restricciones {#section-056cb574713c4d07be6d07cf3c598839}

Con la incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que determina el tamaño de tiempo de ejecución del contenedor del visor `DIV`. En el siguiente ejemplo, suponga que la página web permite que el contenedor del visor `DIV` represente el 40 % del tamaño de la ventana del navegador web, dejando su altura sin restricciones. El código HTML de la página web tendría el siguiente aspecto:

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

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición de la DIV de contenedor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo. Añada el contenedor DIV al `"holder"` DIV existente. El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del navegador y cómo coincide la proporción de aspecto del visor con el recurso.

```
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

La siguiente página de ejemplos ilustra los usos más reales del diseño interactivo que se incrusta con altura ilimitada:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## Integración de tamaño flexible con anchura y altura definidas {#section-0a329016f9414d199039776645c693de}

En caso de incrustación de tamaño flexible con anchura y altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños a la `"holder"` DIV y la centra en la ventana del explorador. Además, la página web establece el tamaño del elemento `HTML` y el `BODY` elemento en 100 por ciento.

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

El resto de los pasos de incrustación son idénticos a los pasos utilizados para la incrustación de diseño interactivo con altura ilimitada. El ejemplo resultante es el siguiente:

```
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

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en setter y el constructor no-args. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante métodos `setContainerId()`, `setParam()`y `setAsset()` API, con llamadas JavaScript independientes.

El siguiente ejemplo ilustra el uso de la incrustación de tamaño fijo con API basada en establecedor:

```
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

