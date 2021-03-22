---
description: Todas las funciones expuestas en la interfaz de visor de Zoom básico, Catálogo electrónico, Búsqueda en catálogo electrónico, Flotante, Zoom en línea, Medios mixtos, Giro, Vídeo, Zoom, Dimensión (3D), Carrusel, Imagen interactiva, Vídeo interactivo y Video360 son accesibles mediante teclado.
solution: Experience Manager
title: Navegación y accesibilidad del teclado
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Accesibilidad y navegación por teclado{#keyboard-accessibility-and-navigation}

Todas las funciones expuestas en la interfaz de visor de Zoom básico, Catálogo electrónico, Búsqueda en catálogo electrónico, Flotante, Zoom en línea, Medios mixtos, Giro, Vídeo, Zoom, Carrusel, Dimensional (3D), Imagen interactiva, Vídeo interactivo y Video360 son accesibles mediante teclado.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Accesibilidad y navegación por teclado {#topic-f5650e9493404e55a3627c8d1366b861}

Todas las funciones expuestas en la interfaz de visor de Zoom básico, Catálogo electrónico, Búsqueda en catálogo electrónico, Flotante, Zoom en línea, Medios mixtos, Giro, Vídeo, Zoom, Carrusel, Dimensional (3D), Imagen interactiva, Vídeo interactivo y Video360 son accesibles mediante teclado.

Un usuario final puede navegar entre los elementos de la interfaz de usuario del visor utilizando las pulsaciones de teclas **[!UICONTROL Tab]** y **[!UICONTROL Shift+Tab]**. Al utilizar **[!UICONTROL Tab]** se avanza el enfoque de entrada al siguiente elemento de la interfaz de usuario en el orden de tabulación; el uso de **[!UICONTROL Shift+Tab]** devuelve el enfoque de entrada al elemento de interfaz de usuario anterior. El enfoque transversal sigue la ubicación del elemento de la interfaz de usuario natural en la pantalla y se mueve de izquierda a derecha y, a continuación, de arriba a abajo.

Dependiendo de la configuración del sistema operativo y del explorador web, el elemento de la interfaz de usuario que tenga el enfoque de entrada puede recibir una indicación de enfoque visual. Por ejemplo, el indicador visual puede ser un borde delgado representado alrededor del elemento de la interfaz de usuario.

Es posible desactivar o personalizar este resaltado de enfoque en el visor CSS. En la tabla de contenido de este sistema de Ayuda, bajo un nombre de visor específico (por ejemplo, Zoom básico o Vídeo interactivo), haga clic en **Personalización *nombre del visor*** >** Resaltado de enfoque **.

Las pulsaciones de teclas admitidas por los elementos de la interfaz de usuario del visor individual son, en la mayoría de los casos, obvias y fáciles de descubrir.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Acción </p> </th> 
   <th colname="col2" class="entry"> <p>Tecla </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activar componentes de botón </p> </td> 
   <td colname="col2"> <p>Tecla Space o Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Acercar o alejar </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> +  </span> o  <span class="uicontrol"> -  </span>, respectivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Restablecimiento de zoom </p> </td> 
   <td colname="col2"> <p>Clave Esc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Desplazamiento </p> </td> 
   <td colname="col2"> <p>Tecla de flecha arriba, abajo, izquierda o derecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Giro de una imagen de 360 grados </p> </td> 
   <td colname="col2"> <p>Utilice las teclas de flecha cuando la imagen esté en estado de restablecimiento. </p> <p>Utilice las teclas de flecha arriba o abajo para trabajar con conjuntos de giros multidimensionales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Selección de muestra de producto </p> </td> 
   <td colname="col2"> <p>tecla de flecha arriba, abajo, izquierda o derecha; Clave principal o final. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activación de muestra de producto </p> </td> 
   <td colname="col2"> <p>Tecla Space o Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e vídeo interactivo, rebobinado gradual </p> </td> 
   <td colname="col2"> <p>Tecla de flecha izquierda o arriba. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e vídeo interactivo, avance rápido </p> </td> 
   <td colname="col2"> <p>Tecla de flecha derecha o abajo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e vídeo interactivo, vaya al principio o al final </p> </td> 
   <td colname="col2"> <p>Clave principal o final, respectivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e vídeo interactivo, controle el nivel de volumen cuando el enfoque está en el control deslizante </p> </td> 
   <td colname="col2"> <p>tecla de flecha arriba, abajo, izquierda o derecha; Clave principal o final. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e vídeo interactivo, volumen mutable </p> </td> 
   <td colname="col2"> <p>Teclas de flecha, inicio y fin para controlar el nivel de volumen cuando el enfoque está en su parte deslizante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo, cuando se muestra el cuadro de diálogo modal, el enfoque transversal se limita solo a los controles de cuadro de diálogo. </p> </td> 
   <td colname="col2"> <p>Clave Esc para cerrar el cuadro de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrusel, cambiar la imagen del banner en la vista principal </p> </td> 
   <td colname="col2"> <p>Tecla de flecha izquierda o derecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrusel, selección de puntos interactivos y activación de puntos interactivos </p> </td> 
   <td colname="col2"> <p>Selección de puntos interactivos: flecha arriba, abajo, izquierda o derecha </p> <p>Activación de puntos interactivos: Tecla Space o Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, cambiar la imagen de página en la vista principal </p> </td> 
   <td colname="col2"> <p> Teclas de flecha izquierda o derecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, selección de miniaturas </p> </td> 
   <td colname="col2"> <p>teclas de flecha; Clave principal y final. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, activación de muestras </p> </td> 
   <td colname="col2"> <p>Tecla Space o Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, selección de puntos interactivos </p> </td> 
   <td colname="col2"> <p>Teclas de flecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, activación </p> </td> 
   <td colname="col2"> <p>Teclas Space o Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, activación de componentes desplegables </p> </td> 
   <td colname="col2"> <p> tecla de flecha abajo; Space o Enter key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, cuando el enfoque está en el panel desplegable </p> </td> 
   <td colname="col2"> <p>Utilice las teclas de flecha para seleccionar un elemento específico del panel antes de activarlo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo electrónico, cuando se muestra un cuadro de diálogo modal, el enfoque transversal se limita solo a los controles de cuadro de diálogo. </p> </td> 
   <td colname="col2"> <p>Clave Esc para cerrar el cuadro de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

