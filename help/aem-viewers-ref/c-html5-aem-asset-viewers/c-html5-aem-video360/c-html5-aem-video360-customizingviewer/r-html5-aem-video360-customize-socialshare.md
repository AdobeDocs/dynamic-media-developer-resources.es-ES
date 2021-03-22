---
description: La herramienta de uso compartido en redes sociales aparece en la esquina superior derecha de forma predeterminada. Consiste en un botón y un panel que se expanden cuando el usuario hace clic o pulsa un botón y contiene herramientas de uso compartido individuales.
seo-description: La herramienta de uso compartido en redes sociales aparece en la esquina superior derecha de forma predeterminada. Consiste en un botón y un panel que se expanden cuando el usuario hace clic o pulsa un botón y contiene herramientas de uso compartido individuales.
seo-title: Uso compartido en medios sociales
solution: Experience Manager
title: Uso compartido en medios sociales
uuid: d7b7e704-6f78-45f9-a82a-14dc6b01e230
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 1%

---


# Uso compartido en medios sociales{#social-share}

La herramienta de uso compartido en redes sociales aparece en la esquina superior derecha de forma predeterminada. Consiste en un botón y un panel que se expanden cuando el usuario hace clic o pulsa un botón y contiene herramientas de uso compartido individuales.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posición y el tamaño de la herramienta de uso compartido en redes sociales en la interfaz de usuario del visor se controlan con lo siguiente:

```
.s7video360viewer .s7socialshare
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

**Ejemplo** : para configurar una herramienta de uso compartido en redes sociales que se posicione a cuatro píxeles de la parte superior y a cinco píxeles de la derecha del contenedor de visor y tenga un tamaño de 28 x 28 píxeles.

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
.s7video360viewer .s7socialshare .s7socialbutton
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
   <td colname="col2"> <p> Sitúe dentro de la ilustración sprite, si se utilizan sprites CSS. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes aspectos a distintos estados de botones.

La información del botón se puede localizar. Consulte [Localización de los elementos de la interfaz de usuario](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Ejemplo** : para configurar un botón de herramienta de uso compartido en redes sociales que muestre una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7video360viewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

El aspecto del panel que contiene los iconos individuales de uso compartido en redes sociales se controla con el siguiente selector de clase CSS:

```
.s7video360viewer .s7socialshare .s7socialsharepanel
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

**Ejemplo** : Configurar un panel para que tenga un color transparente:

```
.s7video360viewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

