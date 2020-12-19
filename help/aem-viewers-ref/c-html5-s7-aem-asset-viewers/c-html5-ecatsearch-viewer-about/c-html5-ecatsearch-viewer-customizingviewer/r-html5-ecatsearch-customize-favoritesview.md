---
description: La vista Favoritos consiste en una columna de imágenes en miniatura.
seo-description: La vista Favoritos consiste en una columna de imágenes en miniatura.
seo-title: Vista Favoritos
solution: Experience Manager
title: Vista Favoritos
topic: Dynamic media
uuid: e9d0380e-3b08-45e4-8419-447df2e8de37
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 2%

---


# Vista Favoritos{#favorites-view}

La vista Favoritos consiste en una columna de imágenes en miniatura.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

El aspecto del contenedor de vista favoritas se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7favoritesview
```

La posición y la altura de la vista Favoritos la gestiona la vista; en CSS solo es posible definir la anchura.

**Propiedades CSS de la vista Favoritos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de la vista Favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la vista. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar una vista Favoritos de 100 píxeles de ancho con un fondo gris semitransparente.

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

El espaciado entre las miniaturas de Favoritos se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**Propiedades CSS de las miniaturas de Favoritos**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Tamaño del margen vertical alrededor de cada miniatura. El espaciado de la miniatura real es igual a la suma de los márgenes superior e inferior que se configuran para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar el espaciado de 10 píxeles.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

El aspecto de la miniatura individual se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**Propiedades CSS de las miniaturas de Favoritos**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Anchura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altura de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borde </span> </p> </td> 
   <td colname="col2"> <p>Borde de la miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura admite el selector de atributos `state`, que puede utilizarse para aplicar diferentes apariencias a distintos estados de miniaturas. En particular, `state="selected"` corresponde a la miniatura seleccionada recientemente por el usuario. `state="default"` corresponde al resto de las miniaturas. Y `state="over"` se utiliza al pasar el ratón por encima.

Ejemplo: para configurar miniaturas de 75 x 75 píxeles, tenga un borde predeterminado de gris claro y un borde seleccionado de color gris oscuro.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

El aspecto de la etiqueta de miniatura se controla con el siguiente selector de clase CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**Propiedades CSS de la etiqueta Favoritos**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nombre de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: para configurar etiquetas con una fuente Helvetica de 14 píxeles.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

