---
description: El visor flotante es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra en la vista flotante que activa el usuario. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
keywords: responsive
seo-description: El visor flotante es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra en la vista flotante que activa el usuario. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
seo-title: Flotante
solution: Experience Manager
title: Flotante
topic: Dynamic media
uuid: 588e1baa-4165-4aec-8fbe-1a916c0f409f
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---


# Flotante{#flyout}

El visor flotante es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra en la vista flotante que activa el usuario. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Este visor no admite las imágenes que utilizan IR (procesamiento de imágenes) o UGC (contenido generado por el usuario).

El tipo de visor es 504.

Consulte Requisitos y requisitos previos [del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Uso del visor flotante {#section-f21ac23d3f6449ad9765588d69584772}

El visor flotante representa un archivo JavaScript principal y un conjunto de archivos auxiliares (un solo JavaScript incluye todos los componentes del SDK de visor utilizados por este visor, recursos y CSS en particular) descargados por el visor en tiempo de ejecución

El visor flotante solo está diseñado para uso incrustado, lo que significa que está integrado en la página web mediante API documentada. No hay ninguna página web preparada para la producción disponible para el visor flotante.

La configuración y la aplicación de aspectos son similares a las de los demás visores. Puede utilizar CSS personalizada para aplicar la apariencia.

Consulte Referencia [de comandos común a todos los visores: Atributos](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuración y referencia de [comandos comunes a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interactuar con el visor flotante {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visor flotante admite gestos de un solo toque y de varios toque que son comunes en otras aplicaciones móviles.

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
   <td colname="col1"> <p>Barrido o barrido horizontal </p> </td> 
   <td colname="col2"> <p> Se desplaza por la lista de muestras en la barra de muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical </p> </td> 
   <td colname="col2"> <p>Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor también admite entrada táctil y entrada de ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad está limitada a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante teclado.

Consulte Navegación y accesibilidad [del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustación del visor flotante {#section-6bb5d3c502544ad18a58eafe12a13435}

Las diferentes páginas web tienen diferentes necesidades de comportamiento del visor. La página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestra de forma diferente en distintos dispositivos o en diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite dos modos de operación principales: incrustación de tamaño fijo e incrustación de diseño interactivo.

El modo de incrustación de tamaño fijo se utiliza cuando el visor no cambia su tamaño después de la carga inicial. Esta opción es la mejor para las páginas web con un diseño de página estático.

El modo de incrustación de diseño adaptable supone que el visor puede necesitar cambiar el tamaño durante el tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es agregar un visor a una página web que utilice un diseño de página flexible.

Al utilizar el modo de incrustación de diseño interactivo con el visor flotante, asegúrese de especificar puntos de interrupción explícitos para la imagen de vista principal mediante el `imagereload` parámetro . Lo ideal es que los puntos de interrupción coincidan con los puntos de interrupción del ancho del visor según lo dicta el CSS de la página web.

En el modo de incrustación de diseño interactivo, el visor se comporta de forma diferente en función de la forma en que una página web cambia el tamaño de su contenedor `DIV`. Si la página web establece únicamente la anchura del contenedor `DIV`, dejando su altura sin restricciones, el visor selecciona automáticamente la altura según la proporción de aspecto del recurso que se utilice. Esto significa que el recurso encaja perfectamente en la vista sin ningún relleno en los lados. Este caso de uso en particular es el más común para las páginas web que utilizan marcos de diseño interactivos como Bootstrap, Foundation, etc.

En caso contrario, si la página web establece la anchura y la altura del contenedor del visor `DIV`, el visor rellenará solo esa área y seguirá el tamaño proporcionado por la presentación de la página web. Un buen ejemplo de caso de uso es integrar el visor en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del navegador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor en la página web.

   La creación de un visor requiere que agregue una etiqueta de script en el encabezado HTML. Antes de utilizar la API de visor, asegúrese de incluir `FlyoutViewer.js`. `FlyoutViewer.js` se encuentra en la siguiente [!DNL html5/js/] subcarpeta de la implementación estándar de los visores IS:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Adobe Scene7 y se suministra desde el mismo dominio. De lo contrario, debe especificar una ruta de acceso completa a uno de los servidores de Adobe Scene7 que tenga instalados los visores IS.

Una ruta relativa tiene el siguiente aspecto:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Solo debe hacer referencia al archivo JavaScript `include` del visor principal de la página. No debe hacer referencia a ningún archivo JavaScript adicional del código de la página web que pueda descargarse mediante la lógica del visor en tiempo de ejecución. En concreto, no haga referencia directa a la biblioteca del SDK `Utils.js` HTML5 cargada por el visor desde la ruta de `/s7viewers` contexto (el denominado SDK consolidado `include`). El motivo es que la ubicación de las bibliotecas de visores en tiempo de ejecución `Utils.js` o similares está totalmente gestionada por la lógica del visor y la ubicación cambia entre las versiones del visor. Adobe no mantiene versiones anteriores del visor secundario `includes` en el servidor.
>
>
>Como resultado, la colocación de una referencia directa a cualquier JavaScript secundario `include` utilizado por el visor en la página interrumpe la funcionalidad del visor en el futuro cuando se implemente una nueva versión del producto.

1. Definición de la DIV de contenedor.

   Añada un elemento DIV vacío a la página en la que desea que aparezca el visor. El ID del elemento DIV debe definirse porque este ID se pasa más tarde a la API del visor.

   El marcador de posición DIV es un elemento posicionado, lo que significa que la propiedad `position` CSS está definida como `relative` o `absolute`.

   Es responsabilidad de la página web especificar el valor adecuado `z-index` para el elemento DIV del marcador de posición. De este modo, se garantiza que la parte flotante del visor aparezca sobre los demás elementos de la página web.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Configuración del tamaño del visor.

   Este visor muestra miniaturas al trabajar con conjuntos de varios elementos. En los sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal durante la ejecución mediante `setAsset()` API. Como desarrollador, tiene control sobre cómo gestiona el visor el área de miniaturas en el área inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener el tamaño de vista principal estático y contraer el área del visor exterior, permitiendo así que el contenido de la página web se mueva hacia arriba y, a continuación, utilizar el espacio de la página libre que queda en las miniaturas.

   Para mantener intactos los límites exteriores del visor, defina el tamaño de la clase CSS de nivel `.s7flyoutviewer` superior en unidades absolutas. El tamaño en CSS se puede colocar directamente en la página HTML o en un archivo CSS de visor personalizado, que posteriormente se asignará a un registro de ajuste preestablecido de visor en Scene7 Publishing System, o se pasará explícitamente mediante un comando de estilo.

   Consulte [Personalización del visor flotante](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) para obtener más información sobre el estilo del visor con CSS.

   A continuación se muestra un ejemplo de definición del tamaño del visor externo estático en una página HTML:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un área de visor exterior fija en la siguiente página de muestra. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   Para que las dimensiones de la vista principal sean estáticas, defina el tamaño del visor en unidades absolutas para el componente `Container` SDK interno mediante el selector de `.s7flyoutviewer .s7container` CSS. Además, debe anular el tamaño fijo definido para la clase CSS de nivel superior en el CSS del visor predeterminado, configurándolo en `.s7flyoutviewer` `auto`.

   A continuación se muestra un ejemplo de definición del tamaño del visor para el componente `Container` SDK interno, de modo que el área de vista principal no cambie su tamaño al cambiar el recurso:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La siguiente página de muestra muestra el comportamiento del visor con un tamaño de vista principal fijo. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   Además, tenga en cuenta que el CSS del visor predeterminado proporciona un tamaño fijo para su área exterior lista para usar.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.FlyoutViewer` clase, pase toda la información de configuración a su constructor y al `init()` método de llamada en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener el `containerId` `params` campo que contiene el nombre del ID de contenedor del visor y el objeto JSON anidado con parámetros de configuración compatibles con el visor. En este caso, el `params` objeto debe tener al menos la URL del servicio de imágenes pasada como `serverUrl` propiedad y el recurso inicial como `asset` parámetro. La API de inicialización basada en JSON permite crear y inicio del visor con una sola línea de código.

   Es importante que el contenedor del visor se añada al DOM para que el código del visor pueda encontrar el elemento de contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para obtener la máxima compatibilidad, llame al `init()` método justo antes de la `BODY` etiqueta de cierre o en el `onload()` evento body.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web. Por ejemplo, puede ocultarse con `display:none` el estilo asignado. En este caso, el visor retrasa el proceso de inicialización hasta el momento en que la página web devuelve el elemento de contenedor a la presentación. Cuando esto sucede, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de creación de una instancia de visor, pasando las opciones de configuración mínimas necesarias al constructor y llamando al `init()` método. Se supone que el ejemplo `flyoutViewer` es la instancia del visor; `s7viewer` es el nombre del marcador de posición `DIV`; `http://s7d1.scene7.com/is/image/` es la URL del servicio de imágenes; y `Scene7SharedAssets/ImageSet-Views-Sample` es el recurso:

   ```
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   El siguiente código es un ejemplo completo de una página web trivial que incorpora el visor flotante con un tamaño fijo:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Incrustación de diseño adaptable con altura ilimitada {#section-056cb574713c4d07be6d07cf3c598839}

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

Añadir el visor a una página de este tipo es similar a los pasos para la incrustación de tamaño fijo. La única diferencia es que debe anular el tamaño fijo del CSS del visor predeterminado con el tamaño establecido en unidades relativas.

1. Añadir el archivo JavaScript del visor en la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo con las tres excepciones siguientes:

* añadir el contenedor `DIV` al &quot;titular&quot; existente `DIV`;
* se ha añadido `imagereload` un parámetro con puntos de interrupción explícitos;
* en lugar de definir un tamaño de visor fijo mediante unidades absolutas, utilice CSS que establezca la anchura y la altura del visor en 100 %, como se muestra a continuación:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del navegador y cómo coincide la proporción de aspecto del visor con el recurso.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La siguiente página de ejemplos ilustra los usos más reales del diseño interactivo que se incrusta con altura ilimitada:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```

