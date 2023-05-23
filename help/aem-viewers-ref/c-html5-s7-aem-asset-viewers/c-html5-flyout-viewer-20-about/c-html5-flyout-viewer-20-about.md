---
title: Flotante
description: El visor flotante es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra en la vista flotante que activa un usuario. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# Flotante{#flyout}

El visor flotante es un visor de imágenes. Muestra una imagen estática con la versión ampliada que se muestra en la vista flotante que activa un usuario. Este visor funciona con conjuntos de imágenes y la navegación se realiza mediante muestras. Está diseñado para trabajar en equipos de escritorio y dispositivos móviles.

>[!NOTE]
>
>Las imágenes que utilizan IR (Image Rendering) o UGC (User-Generated Content) no son compatibles con este visor.

Tipo de visor 504.

Consulte [Requisitos y requisitos previos del sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demostración {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Uso del visor flotante {#section-f21ac23d3f6449ad9765588d69584772}

Visor flotante representa un archivo JavaScript principal y un conjunto de archivos de ayuda (una sola inclusión JavaScript con todos los componentes SDK del visor utilizados por este visor, recursos y CSS) descargados por el visor en tiempo de ejecución

El visualizador flotante solo está diseñado para uso incrustado, lo que significa que se integra en la página web mediante una API documentada. No hay ninguna página web lista para la producción disponible para el visor flotante.

La configuración y el desollado son similares a los de otros visores. Puede utilizar CSS personalizado para aplicar aspectos.

Consulte [Referencia de comando común a todos los visores: atributos de configuración](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) y [Referencia de comando común a todos los visores: URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interacción con el visor flotante {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

El visor flotante admite gestos de un solo toque y de varios toques que son comunes en otras aplicaciones móviles.

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
   <td colname="col1"> <p>Barrido o gesto horizontal </p> </td> 
   <td colname="col2"> <p> Se desplaza por la lista de muestras de la barra de muestras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Barrido vertical </p> </td> 
   <td colname="col2"> <p>Si el gesto se realiza dentro del área de muestras, realiza un desplazamiento de página nativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

El visor también admite la entrada táctil y la entrada del ratón en dispositivos Windows con pantalla táctil y ratón. Sin embargo, esta compatibilidad se limita únicamente a los exploradores web Chrome, Internet Explorer 11 y Edge.

Este visor es totalmente accesible mediante el teclado.

Consulte [Navegación y accesibilidad del teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incrustar visor flotante {#section-6bb5d3c502544ad18a58eafe12a13435}

Las distintas páginas web tienen diferentes necesidades de comportamiento del visualizador. La página web puede tener un diseño de página estático o utilizar un diseño interactivo que se muestre de forma diferente en diferentes dispositivos o para diferentes tamaños de ventana del explorador. Para satisfacer estas necesidades, el visor admite dos modos de operación principales: incrustación de tamaño fijo e incrustación de diseño interactivo.

El modo de incrustación de tamaño fijo se utiliza cuando el visualizador no cambia su tamaño después de su carga inicial. Esta opción es perfecta para las páginas web que tienen un diseño de página estático.

El modo de incrustación de diseño interactivo supone que el visor debe cambiar de tamaño durante el tiempo de ejecución en respuesta al cambio de tamaño de su contenedor `DIV`. El caso de uso más común es añadir un visor a una página web que utilice un diseño de página flexible.

Cuando utilice el modo de incrustación de diseño interactivo con el visor flotante, asegúrese de especificar puntos de interrupción explícitos para la imagen de vista principal mediante el `imagereload` parámetro. Lo ideal es que combine los puntos de interrupción con los puntos de interrupción de anchura del visor según lo dictado por la página web de CSS.

En el modo de incrustación de diseño interactivo, el visualizador se comporta de forma diferente según la forma en que se utilice un contenedor de página web `DIV` tiene el tamaño adecuado. Si la página web establece únicamente la anchura del contenedor `DIV`Sin restringir su altura, el visualizador elige automáticamente su altura según la proporción de aspecto del recurso que se utilice. Esta funcionalidad significa que el recurso se adapta perfectamente a la vista sin ningún relleno en los lados. Este caso de uso en particular es el más común para las páginas web que utilizan marcos de diseño adaptable como Bootstrap y Foundation.

En caso contrario, si la página web establece tanto la anchura como la altura del contenedor del visor `DIV`, el visor rellena únicamente ese área y sigue el tamaño indicado en el diseño de la página web. Un buen ejemplo de uso es la incrustación del visualizador en una superposición modal, donde el tamaño de la superposición depende del tamaño de la ventana del explorador web.

**Incrustación de tamaño fijo**

Para agregar el visor a una página web, haga lo siguiente:

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

1. Añadir el archivo JavaScript del visor a la página web.

   La creación de un visor requiere que añada una etiqueta de script en el encabezado del HTML. Antes de usar la API de visor, asegúrese de incluir lo siguiente `FlyoutViewer.js`. `FlyoutViewer.js` está en lo siguiente [!DNL html5/js/] de la implementación estándar de IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puede utilizar una ruta relativa si el visor está implementado en uno de los servidores de Dynamic Media de Adobe y se proporciona desde el mismo dominio. De lo contrario, especifique una ruta completa a uno de los servidores de Dynamic Media de Adobe que tengan instalados los visores de IIS.

Una ruta relativa tiene el siguiente aspecto:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
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

   Es responsabilidad de la página web especificar la `z-index` para el elemento DIV de marcador de posición. Al hacerlo, se asegura de que la parte flotante del visor aparezca sobre los demás elementos de la página web.

   A continuación se muestra un ejemplo de un elemento DIV de marcador de posición definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Configuración del tamaño del visor.

   Este visor muestra miniaturas cuando se trabaja con conjuntos de varios elementos. En sistemas de escritorio, las miniaturas se colocan debajo de la vista principal. Al mismo tiempo, el visor permite el intercambio del recurso principal durante el tiempo de ejecución mediante `setAsset()` API. Como desarrollador, tiene control sobre cómo administra el visor el área de miniaturas en el área inferior cuando el nuevo recurso solo tiene un elemento. Es posible mantener intacto el tamaño del visor exterior y permitir que la vista principal aumente su altura y ocupe el área de miniaturas. O bien, puede mantener el tamaño de la vista principal estático y contraer el área del visor exterior, dejando que el contenido de la página web suba, y luego utilizar los bienes raíces de la página libre que quedan de las miniaturas.

   Para mantener intactos los límites del visor exterior, defina el tamaño para `.s7flyoutviewer` clase CSS de nivel superior en unidades absolutas. El tamaño en CSS se puede ajustar directamente en la página del HTML o en un archivo CSS de visor personalizado, asignarse posteriormente a un registro de ajuste preestablecido de visor en Dynamic Media Classic o pasarse explícitamente mediante el comando de estilo.

   Consulte [Personalizar visor flotante](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) para obtener más información sobre cómo aplicar estilo al visor con CSS.

   A continuación se muestra un ejemplo de definición del tamaño del visor exterior estático en una página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puede ver el comportamiento con un área de visor exterior fija en la siguiente página de muestra. Tenga en cuenta que cuando cambia entre conjuntos, el tamaño del visor exterior no cambia:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   Para que las dimensiones de la vista principal sean estáticas, defina el tamaño del visor en unidades absolutas para la vista interna `Container` Componente de SDK que utiliza `.s7flyoutviewer .s7container` Selector de CSS. Además, debe anular el tamaño fijo definido para `.s7flyoutviewer` clase CSS de nivel superior en el visor CSS predeterminado, configurándola como `auto`.

   A continuación, se muestra un ejemplo de definición del tamaño del visor para el dispositivo interno `Container` Componente del SDK para que el área de vista principal no cambie su tamaño al cambiar el recurso:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La siguiente página de ejemplo muestra el comportamiento del visor con un tamaño de vista principal fijo. Tenga en cuenta que cuando cambia entre conjuntos, la vista principal permanece estática y el contenido de la página web se mueve verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   Además, el visor CSS predeterminado proporciona un tamaño fijo para su área exterior de forma predeterminada.

1. Creación e inicialización del visor.

   Cuando haya completado los pasos anteriores, cree una instancia de `s7viewers.FlyoutViewer` , pase toda la información de configuración a su constructor y llame a `init()` en una instancia de visor. La información de configuración se pasa al constructor como un objeto JSON. Como mínimo, este objeto debe tener `containerId` campo que contiene el nombre del ID de contenedor del visor y el valor anidado `params` Objeto JSON con parámetros de configuración compatibles con el visor. En este caso, la variable `params` el objeto debe tener al menos la URL del servicio de imágenes pasada como `serverUrl` y el recurso inicial como `asset` parámetro. La API de inicialización basada en JSON permite crear e iniciar el visor con una sola línea de código.

   Es importante tener el contenedor del visor añadido al DOM para que el código del visor pueda encontrar el elemento contenedor por su ID. Algunos exploradores retrasan la creación de DOM hasta el final de la página web. Para conseguir la máxima compatibilidad, llame al método `init()` método justo antes del cierre `BODY` o en el cuerpo `onload()` evento.

   Al mismo tiempo, el elemento contenedor no debe formar parte necesariamente del diseño de la página web todavía. Por ejemplo, se puede ocultar usando `display:none` estilo asignado a él. En este caso, el visor retrasa su proceso de inicialización hasta el momento en que la página web devuelve el elemento contenedor al diseño. Cuando se produce esta acción, la carga del visor se reanuda automáticamente.

   A continuación se muestra un ejemplo de cómo crear una instancia de visor, pasar las opciones de configuración mínimas necesarias al constructor y llamar a `init()` método. El ejemplo supone `flyoutViewer` es la instancia del visualizador; `s7viewer` es el nombre del marcador de posición `DIV`; `http://s7d1.scene7.com/is/image/` es la URL del servicio de imágenes; y `Scene7SharedAssets/ImageSet-Views-Sample` es el recurso:

   ```html {.line-numbers}
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

   El siguiente código es un ejemplo completo de una página web trivial que incrusta el visor flotante con un tamaño fijo:

   ```html {.line-numbers}
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

## Inserción de diseño interactivo con altura sin restricciones {#section-056cb574713c4d07be6d07cf3c598839}

Con incrustación de diseño interactivo, la página web normalmente tiene algún tipo de diseño flexible que dicta el tamaño de tiempo de ejecución del contenedor del visualizador `DIV`. En el siguiente ejemplo, supongamos que la página web permite el contenedor del visor `DIV` para ocupar el 40 % del tamaño de la ventana del explorador web, sin restringir su altura. El código del HTML de la página web tendría el siguiente aspecto:

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

Añadir el visor a una página de este tipo es similar a los pasos para la incrustación de tamaño fijo. La única diferencia es que debe anular el tamaño fijo del CSS del visor predeterminado con el tamaño establecido en unidades relativas.

1. Añadir el archivo JavaScript del visor a la página web.
1. Definición del contenedor `DIV`.
1. Configuración del tamaño del visor.
1. Creación e inicialización del visor.

Todos los pasos anteriores son los mismos que con la incrustación de tamaño fijo con las tres excepciones siguientes:

* añadir el contenedor `DIV` al &quot;titular&quot; existente `DIV`;
* añadido `imagereload` parámetro con puntos de interrupción explícitos;
* en lugar de establecer un tamaño de visor fijo mediante unidades absolutas, utilice CSS que establece el ancho y el alto del visor en el 100 %, como se muestra a continuación:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

El siguiente código es un ejemplo completo. Observe cómo cambia el tamaño del visor cuando se cambia el tamaño del explorador y cómo la proporción de aspecto del visor coincide con el recurso.

```html {.line-numbers}
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

La siguiente página de ejemplos ilustra usos más reales del diseño interactivo incrustado con una altura sin restricciones:

[Demostraciones en directo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Ubicación de demostración alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Incrustación de tamaño flexible con anchura y altura definidas {#section-0a329016f9414d199039776645c693de}

Si hay una incrustación de tamaño flexible con la anchura y la altura definidas, el estilo de la página web es diferente. Proporciona ambos tamaños a la `"holder"` DIV y lo centra en la ventana del explorador. Además, la página web establece el tamaño del `HTML` y `BODY` elemento al 100 por ciento.

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

## Incrustación mediante una API basada en Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

En lugar de utilizar la inicialización basada en JSON, es posible utilizar la API basada en establecedores y el constructor sin argumentos. El uso de este constructor de API no toma ningún parámetro y los parámetros de configuración se especifican mediante `setContainerId()`, `setParam()`, y `setAsset()` Métodos de API, con llamadas de JavaScript independientes.

El siguiente ejemplo ilustra el uso de incrustación de tamaño fijo con API basada en establecedores:

```html {.line-numbers}
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
