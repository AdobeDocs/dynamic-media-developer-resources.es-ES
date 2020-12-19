---
description: Ruta del clip de capa. Especifica una ruta de clip para la capa actual.
seo-description: Ruta del clip de capa. Especifica una ruta de clip para la capa actual.
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Scene7 Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# clipPath{#clippath}

Ruta del clip de capa. Especifica una ruta de clip para la capa actual.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nombre de la ruta incrustada en la imagen de origen de la capa (solo ASCII). </p></td> 
 </tr> 
</table>

Todas las partes de la capa que queden fuera del área definida por `clipPath=` se mostrarán transparentes.

` *``*` pathName es el nombre de un trazado incrustado en la imagen de origen de la capa. La ruta se transforma automáticamente para mantener la alineación relativa con el contenido de la imagen. Si se especifica más de un ` *`pathName`*`, el servidor recorta la imagen a la intersección de estas rutas. Se ignora cualquier ` *`pathName`*` no encontrado en la imagen de origen.

>[!NOTE]
>
>Solo se admiten cadenas ASCII para ` *`pathName`*`.

` *``*` pathDefinitionpermite especificar datos de ruta explícitos en coordenadas de píxeles de capa.

Si se especifica `size=` y no 0,0, la capa estará presidida. En este caso, las coordenadas de trazado son relativas a la esquina superior izquierda del rectángulo de capa y la capa se coloca en función de `origin=` o su valor predeterminado. Todas las regiones del trazado situadas fuera del rectángulo de la capa permanecen transparentes.

Si no se especifica `size=` para una capa de texto o color sólido, la capa se considera de tamaño propio con la extensión de la ruta que determina su tamaño. Si no se especifica `origin=`, el valor predeterminado es (0,0) del espacio de coordenadas de ruta. Esto permite especificar las coordenadas de ruta con relación al origen de la capa 0.

>[!NOTE]
>
>`scale=`no se permiten  `rotate=`ni  `anchor=` comandos para capas de color sólido de tamaño propio.

` *``*` pathDefinitionacepta una cadena similar al valor del  `d=` atributo del  `<path>` elemento SVG, excepto que se utilizan comas en lugar de espacios para separar valores. ` *``*` pathDefinitionpuede incluir uno o más subpaths de bucle cerrado.

Los siguientes comandos de ruta se admiten en ` *`pathDefinition`*`:

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Comando</b> </th> 
   <th class="entry"> <b> Nombre</b> </th> 
   <th class="entry"> <b> Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> moveto absoluto </p> </td> 
   <td> <p> Inicio un nuevo subtrazado en x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
   <td> <p> moveto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absoluto </p> </td> 
   <td> <p> Dibuje una línea desde la posición actual hasta x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y,y</span>} </td> 
   <td> <p> curveto absoluto </p> </td> 
   <td> <p> Dibuje una curva Bézier desde la posición actual hasta x,y. x1,y1 es el punto de control al principio de la curva y x2,y2 es el punto de control al final de la curva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y,y</span>} </td> 
   <td> <p> curveto relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> |  <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Cierre el subtrazado actual con una línea recta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Los comandos en mayúsculas indican que los valores de las coordenadas están en posiciones absolutas de píxeles (en relación con la esquina superior izquierda del rectángulo de la capa). Los desplazamientos de píxeles siguen comandos en minúsculas en relación con la posición actual.

&#39;m&#39; o &#39;M&#39; siempre inicio una nueva subruta. Las subrutas se cierran automáticamente (con una línea recta) si no se especifica &#39;Z&#39; o &#39;z&#39; al final.

Si un subtrazado comienza con un movimiento relativo (&#39;m&#39;), es relativo a uno de los siguientes:

* El punto de inicio del subtrazado anterior, si se cerró con &#39;z&#39; o &#39;Z&#39;.
* El punto final del subtrazado anterior, si no se cerró explícitamente.
* 0,0, si es la primera subruta.

## Propiedades {#section-d4127db0dac54e3cbd44f7ea1e001960}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Las capas de efectos lo ignoran.

`clipPathE=` se omite si no se encuentra ninguna ruta con el nombre especificado en la imagen de origen de la capa o si el origen de la capa no es una imagen.

## Predeterminado {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Ninguno, para que no se recorte la capa.

## Véase también {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
