---
description: Ruta del clip de capa. Especifica una ruta de recorte para la capa actual.
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 1%

---


# clipPath{#clippath}

Ruta del clip de capa. Especifica una ruta de recorte para la capa actual.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nombre de la ruta de acceso incrustada en la imagen de origen de la capa (solo ASCII). </p></td> 
 </tr> 
</table>

Todas las partes de la capa que queden fuera del área definida por `clipPath=` se procesarán con transparencia.

`*``*` pathName es el nombre de una ruta integrada en la imagen de origen de la capa. La ruta se transforma automáticamente para mantener la alineación relativa con el contenido de la imagen. Si se especifica más de un `*`pathName`*`, el servidor recorta la imagen a la intersección de estas rutas. Cualquier `*`pathName`*` no encontrado en la imagen de origen se ignora.

>[!NOTE]
>
>Solo se admiten cadenas ASCII para `*`pathName`*`.

`*``*` pathDefinitionpermite especificar datos de ruta explícitos en coordenadas de píxeles de capa.

Si se especifica `size=` y no 0,0, la capa está presidida. En este caso, las coordenadas de ruta son relativas a la esquina superior izquierda del rectángulo de capa y la capa se coloca en función de `origin=` o de su valor predeterminado. Cualquier región de la ruta fuera del rectángulo de la capa permanece transparente.

Si no se especifica `size=` para un color sólido o una capa de texto, la capa se considera de tamaño automático con la extensión de la ruta que determina su tamaño. Si no se especifica `origin=`, el valor predeterminado es (0,0) del espacio de coordenadas de la ruta. Esto permite especificar las coordenadas de ruta en relación con el origen de la capa 0.

>[!NOTE]
>
>`scale=`no se permiten los  `rotate=`comandos ,  `anchor=` , ni para capas de color sólido autodimensionadas.

`*``*` pathDefinitionacepta una cadena similar al valor del  `d=` atributo del  `<path>` elemento SVG, excepto que se utilizan comas en lugar de espacios para separar valores. `*``*` pathDefinitionpuede incluir una o más subrutas de bucle cerrado.

Los siguientes comandos de ruta son compatibles con `*`pathDefinition`*`:

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
   <td> <p> Inicie una nueva subruta en x,y. </p> </td> 
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
   <td> <p> lina relativa </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y,y</span>} </td> 
   <td> <p> curveto absoluto </p> </td> 
   <td> <p> Dibuje una curva Bezier desde la posición actual hasta x,y. x1,y1 es el punto de control al principio de la curva y x2,y2 es el punto de control al final de la curva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y,y</span>} </td> 
   <td> <p> límite relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> |  <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Cierre la subruta actual con una línea recta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Los comandos en mayúsculas indican que los valores de coordenadas están en posiciones absolutas de píxeles (en relación con la esquina superior izquierda del rectángulo de capa). Los desplazamientos de píxeles siguen comandos en minúsculas en relación con la posición actual.

&#39;m&#39; o &#39;M&#39; siempre inicia una nueva subruta. Las subrutas se cierran automáticamente (con una línea recta) si &quot;Z&quot; o &quot;z&quot; no se especifican al final.

Si una subruta comienza con un movimiento relativo (&quot;m&quot;), es relativa a una de las siguientes opciones:

* El punto de partida de la subruta anterior, si se cerró con &quot;z&quot; o &quot;Z&quot;.
* El punto final de la subruta anterior, si no se cerró explícitamente.
* 0,0, si esta es la primera subruta.

## Propiedades {#section-d4127db0dac54e3cbd44f7ea1e001960}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Las capas de efecto lo ignoran.

`clipPathE=` se ignora si no se encuentra ninguna ruta con el nombre especificado en la imagen de origen de la capa o si el origen de la capa no es una imagen.

## Predeterminado {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Ninguno, para no recortar la capa.

## Véase también {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
