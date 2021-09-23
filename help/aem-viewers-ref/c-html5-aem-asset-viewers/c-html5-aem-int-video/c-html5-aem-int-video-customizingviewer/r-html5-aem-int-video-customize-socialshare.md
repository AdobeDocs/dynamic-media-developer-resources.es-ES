---
title: Uso compartido en medios sociales
description: La herramienta de uso compartido en redes sociales aparece en la esquina superior derecha de forma predeterminada. Consiste en un botón y un panel que se expanden cuando el usuario hace clic o pulsa un botón y contiene herramientas de uso compartido individuales.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ad544a12-d2a4-45c9-9e76-e0bf96901725
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Uso compartido en medios sociales{#social-share}

La herramienta de uso compartido en redes sociales aparece en la esquina superior derecha de forma predeterminada. Consiste en un botón y un panel que se expanden cuando el usuario hace clic o pulsa un botón y contiene herramientas de uso compartido individuales.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posición y el tamaño de la herramienta de uso compartido en redes sociales en la interfaz de usuario del visor se controlan con lo siguiente:

```
.s7interactivevideoviewer .s7socialshare
```

**Propiedades CSS de la herramienta de uso compartido en redes sociales**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior </span> </p> </td> 
   <td colname="col2"> <p> Posición vertical de la herramienta de uso compartido en redes sociales en relación con el contenedor del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> izquierda </span> </p> </td> 
   <td colname="col2"> <p> Posición horizontal de la herramienta de uso compartido en redes sociales en relación con el contenedor del visor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Ancho de la herramienta de uso compartido en redes sociales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la herramienta de uso compartido en redes sociales. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example}

Configurar una herramienta de uso compartido en redes sociales que se coloca a cuatro píxeles de la parte superior y a cinco píxeles de la derecha del contenedor de visor y cuyo tamaño es de 28 x 28 píxeles.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

El aspecto del botón de la herramienta de uso compartido en redes sociales se controla con el siguiente selector de clases CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**Propiedades CSS del botón de herramienta de uso compartido en redes sociales**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo  </span> </p> </td> 
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Ejemplo {#example-1}

Para configurar un botón de herramienta de uso compartido en redes sociales que muestre una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

El aspecto del panel que contiene los iconos individuales de uso compartido en redes sociales se controla con el siguiente selector de clase CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
```

**Propiedades CSS del panel de uso compartido en redes sociales**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#example-2}

Para configurar un panel con un color transparente:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
