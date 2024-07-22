---
title: Vista Favoritos
description: La vista Favoritos consta de una columna de imágenes en miniatura.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 8daf3d19-615b-4d62-a6f5-6a153d193b88
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Vista Favoritos{#favorites-view}

La vista Favoritos consta de una columna de imágenes en miniatura.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

El aspecto del contenedor de vistas de favoritos se controla con el siguiente selector de clases CSS:

```
.s7ecatalogsearchviewer .s7favoritesview
```

La vista administra la posición y la altura de la vista Favoritos; en CSS solo es posible definir la anchura.

**Propiedades CSS de la vista Favoritos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color de fondo </span> </p> </td> 
   <td colname="col2"> <p> Color de fondo de la vista Favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho de la vista. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> margen </span> </p> </td> 
   <td colname="col2"> <p> El tamaño del margen vertical alrededor de cada miniatura. El espaciado de miniaturas real es igual a la suma de los márgenes superior e inferior establecidos para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para configurar el espaciado de diez píxeles.

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
   <td colname="col1"> <p> <span class="codeph"> ancho </span> </p> </td> 
   <td colname="col2"> <p>Ancho de la miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
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
>La miniatura admite el selector de atributos `state`, que se puede utilizar para aplicar diferentes aspectos a diferentes estados de miniaturas. En particular, `state="selected"` corresponde a la miniatura seleccionada recientemente por el usuario. Mientras que `state="default"` corresponde al resto de las miniaturas. Y `state="over"` se usa al pasar el ratón por encima.

Ejemplo: Para configurar miniaturas de 75 x 75 píxeles, tenga un borde predeterminado de gris claro y un borde seleccionado de gris oscuro.

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
   <td colname="col1"> <p> <span class="codeph"> familia de fuentes </span> </p> </td> 
   <td colname="col2"> <p>Nombre de la fuente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamaño de fuente </span> </p> </td> 
   <td colname="col2"> <p>Tamaño de fuente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: configuración de etiquetas con una fuente Helvetica® de 14 píxeles.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
