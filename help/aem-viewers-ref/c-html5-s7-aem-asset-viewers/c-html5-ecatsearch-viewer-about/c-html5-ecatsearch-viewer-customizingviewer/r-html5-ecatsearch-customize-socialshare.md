---
title: Uso compartido social
description: La herramienta Compartir en redes sociales aparece en la esquina superior izquierda de forma predeterminada. Consiste en un botón y un panel que se expande cuando el usuario hace clic o pulsa un botón y contiene herramientas de uso compartido individuales.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5cac6c86-08fb-46fd-bab0-ab77154eb770
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Uso compartido social{#social-share}

La herramienta Compartir en redes sociales aparece en la esquina superior izquierda de forma predeterminada. Consiste en un botón y un panel que se expande cuando el usuario hace clic o pulsa un botón y contiene herramientas de uso compartido individuales.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La posición y el tamaño de la herramienta de uso compartido en redes sociales de la interfaz de usuario del visor se controlan de la siguiente manera:

```
.s7ecatalogsearchviewer .s7socialshare
```

**Propiedades CSS de la herramienta de uso compartido en redes sociales**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margen superior </span> </p> </td> 
   <td colname="col2"> <p> Desplazamiento desde la parte superior de la barra de control. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> Distancia al siguiente botón de la izquierda o al lado izquierdo de la barra de control si este botón es el primero de una fila. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p> Ancho de la herramienta de uso compartido en redes sociales. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura de la herramienta de uso compartido en redes sociales. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configure una herramienta de uso compartido en redes sociales que esté colocada a cuatro píxeles de la parte superior y a cinco píxeles de la derecha del contenedor del visor y cuyo tamaño sea de 28 x 28 píxeles.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

El aspecto del botón de la herramienta de uso compartido en redes sociales se controla con el siguiente selector de clases CSS:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**Propiedades CSS del botón social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagen de fondo </span> </p> </td> 
   <td colname="col2"> <p> Imagen que se muestra para un estado de botón determinado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posición de fondo </span> </p> </td> 
   <td colname="col2"> <p> Coloque dentro del icono de ilustración si se utilizan iconos CSS. </p> <p>Consulte también <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botón es compatible con el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de botones.

La información del objeto del botón se puede localizar. Consulte [Localización de elementos de la interfaz de usuario](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obtener más información.

Ejemplo: configure un botón de la herramienta de uso compartido en redes sociales que muestre una imagen diferente para cada uno de los cuatro estados de botón diferentes.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

El aspecto del panel que contiene los iconos individuales de uso compartido en medios sociales se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

**Propiedades CSS del panel de uso compartido en redes sociales**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p>Color de fondo del panel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Configuración de un panel para que tenga un color transparente:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
