---
description: En el modo de zoom en línea, la vista principal consiste en la imagen estática, la imagen ampliada mostrada en la vista flotante sobre la imagen estática y el mensaje de sugerencia mostrado sobre la imagen estática.
solution: Experience Manager
title: Vista de zoom flotante
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de medios mixtos
role: Developer,Business Practitioner
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 5%

---

# Vista de zoom flotante{#flyout-zoom-view}

En el modo de zoom en línea, la vista principal consiste en la imagen estática, la imagen ampliada mostrada en la vista flotante sobre la imagen estática y el mensaje de sugerencia mostrado sobre la imagen estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propiedades CSS del área principal del visor**

El aspecto de la vista principal se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de la vista principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para que la vista principal sea transparente:

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

El aspecto del mensaje de sugerencia se controla con el siguiente selector de clase CSS:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

Es posible configurar el estilo de fuente, el aspecto del tamaño y el desplazamiento vertical mediante CSS. Sin embargo, la alineación horizontal la gestiona la lógica del visor. No se admite su anulación mediante CSS con propiedades `left` o `right`.

**Propiedades CSS del mensaje de sugerencia**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS, propiedad </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de relleno del fondo del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Radio del borde de fondo del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento desde la parte inferior de la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Color del texto de la sugerencia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Familia de fuentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidad  </span> </p> </td> 
   <td colname="col2"> <p> Opacidad del fondo del mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> relleno </span> </p> </td> 
   <td colname="col2"> <p> Relleno alrededor del texto del mensaje. </p> </td> 
  </tr> 
 </tbody> 
</table>

El mensaje de sugerencia se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obtener más información.

Ejemplo: para configurar un mensaje de punta semitransparente con una fuente Arial blanca de 12 píxeles, 50 píxeles de desplazamiento desde la parte inferior de la vista principal, el relleno y un borde redondeado:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
