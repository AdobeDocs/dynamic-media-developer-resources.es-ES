---
title: Tutorial del SDK del visor
description: El SDK de visor proporciona un conjunto de componentes basados en JavaScript para el desarrollo de visores personalizados. Los visores son aplicaciones basadas en la web que permiten incrustar en las páginas web contenido multimedia enriquecido servido por Adobe Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Tutorial del SDK del visor{#viewer-sdk-tutorial}

El SDK de visor proporciona un conjunto de componentes basados en JavaScript para el desarrollo de visores personalizados. Los visores son aplicaciones basadas en la web que permiten incrustar en las páginas web contenido multimedia enriquecido servido por Adobe Dynamic Media.

Por ejemplo, el SDK proporciona zoom y panorámica interactivos. También proporciona una visualización de 360° y reproducción de vídeo de los recursos que se cargaron en Adobe Dynamic Media a través de la aplicación back-end denominada Dynamic Media Classic.

Aunque los componentes dependen de la funcionalidad de HTML5, están diseñados para funcionar con dispositivos Android™ y Apple iOS, y equipos de escritorio, incluido Internet Explorer y versiones posteriores. Este tipo de experiencia significa que puede proporcionar un único flujo de trabajo para todas las plataformas admitidas.

El SDK consta de componentes de interfaz de usuario que constituyen el contenido del visor. Puede aplicar estilo a estos componentes a través de CSS y de componentes que no sean de interfaz de usuario y que tengan algún tipo de función de apoyo, como la función de recuperación y análisis o el seguimiento de definiciones establecidas. Todos los comportamientos de los componentes se pueden personalizar mediante modificadores que puede especificar de varias formas, por ejemplo, `name=value` en la dirección URL.

Este tutorial incluye el siguiente orden de tareas para ayudarle a crear un visor de zoom básico:

* [Descargar el SDK de visor más reciente de Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Carga del SDK del visor](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Adición de estilo al visor](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Inclusión de Contenedor y ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Adición de componentes de MediaSet y Muestras al visor](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Adición de botones al visor](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Configuración vertical de las muestras](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Descargar el SDK de visor más reciente de Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Descargar el SDK de visor más reciente de Adobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->.

   >[!NOTE]
   >
   >Puede completar este tutorial sin necesidad de descargar el paquete del SDK de visor porque el SDK se carga de forma remota. Sin embargo, el paquete Viewer incluye ejemplos adicionales y una guía de referencia de API que puede ayudarle a crear sus propios visores.

## Carga del SDK del visor {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Comience por configurar una nueva página para desarrollar el visor de zoom básico que va a crear.

   Tenga en cuenta esta nueva página como el código del Bootstrap (o cargador) que utiliza para configurar una aplicación SDK vacía. Abra el editor de texto favorito y pegue el siguiente marcado de HTML en él:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   Agregue el siguiente código JavaScript dentro de la variable `script` para que inicialice la variable `ParameterManager`. Esto le ayuda a prepararse para crear y crear instancias de componentes de SDK dentro del `initViewer` función:

   ```javascript {.line-numbers}
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. Guarde el archivo como una plantilla vacía. Puede utilizar cualquier nombre de archivo que desee.

   Este archivo de plantilla vacío se utilizará como referencia cuando cree visores en el futuro. Esta plantilla funciona localmente y cuando se suministra desde un servidor web.

Ahora, añada estilo al visor.

## Adición de estilo al visor {#section-3783125360a1425eae5a5a334867cc32}

1. Para este visor de página completa que está creando, puede añadir algunos estilos básicos.

   Agregue lo siguiente `style` a la parte inferior del `head`:

   ```html {.line-numbers}
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

Ahora incluya los componentes `Container` y `ZoomView`.

## Inclusión de Contenedor y ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. Crear un visor real incluyendo los componentes `Container` y `ZoomView`.

   Inserte lo siguiente `include` al final del `<head>` element: después de la variable [!DNL Utils.js] se carga el script:

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. Ahora cree variables para hacer referencia a los distintos componentes del SDK.

   Agregue las siguientes variables a la parte superior de la función anónima principal, justo encima `s7sdk.Util.init()`:

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. Inserte lo siguiente dentro del `initViewer` para definir algunos modificadores y crear instancias de los componentes respectivos:

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. Para que el código anterior se ejecute correctamente, agregue una `containerResize` controlador de eventos y una función de ayuda:

   ```javascript {.line-numbers}
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. Previsualice la página para poder ver lo que ha creado. Su página debería tener el siguiente aspecto:

   ![Ejemplo de visor una imagen](assets/viewer-1.jpg)

A continuación, añada los componentes `MediaSet` y `Swatches` al visor.

## Adición de componentes de MediaSet y Muestras al visor {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Para que los usuarios puedan seleccionar imágenes de un conjunto, puede añadir los componentes `MediaSet` y `Swatches`.

   Añada los siguientes SDK:

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Actualice la lista de variables con lo siguiente:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. Crear instancias `MediaSet` y `Swatches` componentes dentro de la variable `initViewer` función.

   Asegúrese de crear una instancia de `Swatches` después de `ZoomView` y `Container` componentes; de lo contrario, el orden de apilamiento oculta la variable `Swatches`:

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Ahora agregue las siguientes funciones de controlador de eventos:

   ```javascript {.line-numbers}
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. Coloque las muestras en la parte inferior del visor agregando el CSS siguiente al `style` elemento:

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Previsualice el visor.

   Observe que las muestras están en la parte inferior izquierda del visor. Para que las muestras tengan el ancho completo del visor, agregue una llamada para cambiar el tamaño manualmente de las muestras cada vez que el usuario cambie el tamaño de su explorador. Agregue lo siguiente a `resizeViewer` función:

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   El visor ahora se parece a la siguiente imagen. Intente cambiar el tamaño de la ventana del navegador del visor y observe el comportamiento resultante.

   ![Ejemplo de visor de dos imágenes](assets/viewer-2.jpg)

Ahora agregue los botones de ampliación, alejamiento y restablecimiento del zoom al visor.

## Adición de botones al visor {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Actualmente, el usuario solo puede ampliar mediante gestos táctiles o de clic. Por lo tanto, agregue al visor algunos botones básicos de control de zoom.

   Añada los siguientes componentes de botón:

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Actualice la lista de variables con lo siguiente:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Crear instancias de botones en la parte inferior de `initViewer` función.

   Recuerde que el orden es importante, a menos que especifique la variable `z-index` en CSS:

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. Ahora, defina algunos estilos básicos para los botones agregando lo siguiente al `style` en la parte superior del archivo :

   ```CSS {.line-numbers}
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. Previsualice el visor. Debería tener el siguiente aspecto:

   ![Ejemplo del visor tres imágenes](assets/viewer-3.jpg)

   A continuación, configure las muestras para que se alineen verticalmente a la derecha.

## Configuración vertical de las muestras {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Puede configurar los modificadores directamente en la variable `ParameterManager` instancia.

   Agregue lo siguiente a la parte superior del `initViewer` para que pueda configurar la variable `Swatches` presentación en miniatura como una sola fila:

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Actualice la siguiente llamada de cambio de tamaño dentro de `resizeViewer`:

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. Edite lo siguiente `s7swatches` regla en `ZoomViewer.css`:

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Previsualice el visor. Tiene el siguiente aspecto:

   ![Ejemplo del visor cuatro imágenes](assets/viewer-4.jpg)

   El visor de zoom básico ya ha finalizado.

   Este tutorial del visor trata los aspectos básicos de lo que proporciona el SDK del visor de Dynamic Media. Al trabajar con el SDK, puede utilizar los distintos componentes estándar para crear y aplicar estilo fácilmente a las experiencias de visualización enriquecidas para las audiencias de destino.
