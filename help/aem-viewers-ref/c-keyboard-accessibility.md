---
title: Navegación y accesibilidad del teclado
description: Todas las funciones expuestas en la interfaz de visor Zoom básico, Catálogo electrónico, Búsqueda en el catálogo electrónico, Flotante, Zoom en línea, Medios mixtos, Giro, Vídeo, Zoom, Dimensional (3D), Carrusel, Imagen interactiva, Vídeo interactivo y Vídeo360 son accesibles mediante el teclado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Navegación y accesibilidad del teclado{#keyboard-accessibility-and-navigation}

Todas las funciones expuestas en la interfaz de visor Zoom básico, Catálogo electrónico, Búsqueda en el catálogo electrónico, Flotante, Zoom en línea, Medios mixtos, Giro, Vídeo, Zoom, Carrusel, Dimensional (3D), Imagen interactiva, Vídeo interactivo y Vídeo360 son accesibles mediante el teclado.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Navegación y accesibilidad del teclado {#topic-f5650e9493404e55a3627c8d1366b861}

Todas las funciones expuestas en la interfaz de visor Zoom básico, Catálogo electrónico, Búsqueda en el catálogo electrónico, Flotante, Zoom en línea, Medios mixtos, Giro, Vídeo, Zoom, Carrusel, Dimensional (3D), Imagen interactiva, Vídeo interactivo y Vídeo360 son accesibles mediante el teclado.

Un usuario final puede navegar entre los elementos de la interfaz de usuario del visor con las pulsaciones de teclas **[!UICONTROL Tab]** y **[!UICONTROL Mayús+Tab]**. Al usar **[!UICONTROL Tab]**, el foco de entrada se mueve al siguiente elemento de la interfaz de usuario en el orden de tabulación; al usar **[!UICONTROL Mayús+Tab]**, el foco de entrada se vuelve a colocar en el elemento de interfaz de usuario anterior. La inversión del enfoque sigue la ubicación natural del elemento de la interfaz de usuario en la pantalla y se mueve de izquierda a derecha y, a continuación, de arriba a abajo.

Según la configuración del sistema operativo y del explorador web, el elemento de interfaz de usuario que tiene el enfoque de entrada recibe una indicación de enfoque visual. Por ejemplo, el indicador visual puede ser un borde delgado representado alrededor del elemento de interfaz de usuario.

Es posible deshabilitar o personalizar dicho resaltado de enfoque en el visor CSS. En la tabla de contenido de este sistema de ayuda, bajo un nombre de visor específico (por ejemplo, Zoom básico o Vídeo interactivo), haga clic en **Personalizar *nombre del visor*** >**&#x200B; Enfoque destacado &#x200B;**.

Las pulsaciones de teclas compatibles con los elementos de la interfaz de usuario del visor individual son, en la mayoría de los casos, obvias y fáciles de descubrir.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Acción </p> </th> 
   <th colname="col2" class="entry"> <p>Pulsación </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activar componentes de botón </p> </td> 
   <td colname="col2"> <p>Tecla Intro o Espacio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ampliar o reducir </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> o <span class="uicontrol"> - </span>, respectivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Restablecimiento de zoom </p> </td> 
   <td colname="col2"> <p>Clave Esc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Panorámica </p> </td> 
   <td colname="col2"> <p>Tecla de flecha arriba, abajo, izquierda o derecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Giro de una imagen de 360 grados </p> </td> 
   <td colname="col2"> <p>Utilice las teclas de flecha cuando la imagen esté en estado de restablecimiento. </p> <p>Utilice las teclas de flecha arriba o abajo cuando trabaje con conjuntos de giros multidimensionales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Selección de muestras de producto </p> </td> 
   <td colname="col2"> <p>Tecla de flecha arriba, abajo, izquierda o derecha; tecla Inicio o Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activación de muestra de producto </p> </td> 
   <td colname="col2"> <p>Tecla Intro o Espacio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo y vídeo interactivo, rebobinado gradual </p> </td> 
   <td colname="col2"> <p>Tecla de flecha izquierda o arriba. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo y vídeo interactivo, avance rápido </p> </td> 
   <td colname="col2"> <p>Tecla de flecha derecha o abajo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo y vídeo interactivo, ir al principio o al final </p> </td> 
   <td colname="col2"> <p>Tecla Inicio o Fin, respectivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo y vídeo interactivo, controlar el nivel de volumen cuando el foco está en el regulador </p> </td> 
   <td colname="col2"> <p>Tecla de flecha arriba, abajo, izquierda o derecha; tecla Inicio o Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo y vídeo interactivo, volumen mutable </p> </td> 
   <td colname="col2"> <p>Teclas de flecha, inicio y final para controlar el nivel de volumen cuando el foco está en la parte deslizante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>En vídeo, cuando se muestra el cuadro de diálogo modal, la inversión de enfoque se limita únicamente a los controles del cuadro de diálogo. </p> </td> 
   <td colname="col2"> <p>Esc para cerrar el cuadro de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrusel, cambiar imagen del titular en la vista principal </p> </td> 
   <td colname="col2"> <p>Tecla de flecha izquierda o derecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrusel, selección de punto interactivo y activación de punto interactivo </p> </td> 
   <td colname="col2"> <p>Selección de punto interactivo: tecla de flecha arriba, abajo, izquierda o derecha </p> <p>Activación de punto interactivo: espacio o tecla Intro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, cambie la imagen de la página en la vista principal </p> </td> 
   <td colname="col2"> <p> Teclas de flecha izquierda o derecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, selección de miniaturas </p> </td> 
   <td colname="col2"> <p>Teclas de flecha; Inicio y Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, activación de muestras </p> </td> 
   <td colname="col2"> <p>Tecla Intro o Espacio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, selección de puntos interactivos </p> </td> 
   <td colname="col2"> <p>Teclas de flecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, activación </p> </td> 
   <td colname="col2"> <p>Teclas Intro o Espacio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, activar componentes desplegables </p> </td> 
   <td colname="col2"> <p> Tecla de flecha abajo; Espacio o Intro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, cuando el enfoque está en el panel desplegable </p> </td> 
   <td colname="col2"> <p>Utilice las teclas de flecha para seleccionar un elemento específico en el panel antes de activarlo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, cuando se muestra un cuadro de diálogo modal, el recorrido del enfoque se limita únicamente a los controles del cuadro de diálogo. </p> </td> 
   <td colname="col2"> <p>Esc para cerrar el cuadro de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>
