---
description: Ruta de clip de capa. Especifica un trazado de recorte para la capa actual.
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 1%

---

# clipPath{#clippath}

Ruta de clip de capa. Especifica un trazado de recorte para la capa actual.

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

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

Partes de la capa que se encuentran fuera del área definida por `clipPath=` son transparentes.

`*`pathName`*` es el nombre de un trazado incrustado en la imagen de origen de la capa. La ruta se transforma automáticamente para mantener la alineación relativa con el contenido de la imagen. Si hay más de uno `*`pathName`*` se especifica, el servidor recorta la imagen a la intersección de estas rutas. Cualquiera `*`pathName`*` no encontrado en la imagen de origen se ignora.

>[!NOTE]
>
>Solo se admiten cadenas ASCII para `*`pathName`*`.

`*`pathDefinition`*` permite especificar datos de ruta explícitos en coordenadas de píxel de capa.

If `size=` se especifica y no 0,0, la capa está presionada. En este caso, las coordenadas de trazado son relativas a la esquina superior izquierda del rectángulo de capa y la capa se coloca basándose en `origin=` o su valor predeterminado. Cualquier región del trazado fuera del rectángulo de capa permanecerá transparente.

If `size=` no se ha especificado para una capa de texto o color sólido, la capa se considera de tamaño propio con la extensión del trazado que determina su tamaño. If `origin=` no se ha especificado, el valor por defecto es (0,0) del espacio de coordenadas de trazado. Esto permite especificar las coordenadas de ruta relativas al origen de la capa 0.

>[!NOTE]
>
>`scale=`, `rotate=`, y `anchor=` no se permiten comandos para capas de color sólido de tamaño propio.

`*`pathDefinition`*` acepta una cadena similar al valor de `d=` atributo del SVG `<path>` , excepto que se utilizan comas en lugar de espacios para separar valores. `*`pathDefinition`*` puede incluir una o más subrutas de bucle cerrado.

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
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> moverla a absoluta </p> </td> 
   <td> <p> Iniciar una nueva subruta en x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> mover a relativo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> línea a absoluta </p> </td> 
   <td> <p> Dibuja una línea desde la posición actual a x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> línea a relativa </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curvatura absoluta </p> </td> 
   <td> <p> Dibujar una curva Bézier desde la posición actual hasta x,y. x1,y1 es el punto de control al principio de la curva y x2,y2 es el punto de control al final de la curva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curva relativa </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Cierre el subtrazado actual con una línea recta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Los comandos en mayúsculas indican que los valores de coordenadas están en posiciones absolutas de píxeles (en relación con la parte superior izquierda del rectángulo de capa). Los desplazamientos de píxeles siguen comandos en minúsculas en relación con la posición actual.

&#39;m&#39; o &#39;M&#39; siempre inicia una nueva subruta. Los subtrazados se cierran automáticamente (con una línea recta) si &#39;Z&#39; o &#39;z&#39; no se especifican al final.

Si una subruta comienza con un movimiento relativo (&#39;m&#39;), es relativa a una de las siguientes opciones:

* El punto de partida de la subruta anterior, si se cerró con &quot;z&quot; o &quot;Z&quot;.
* El punto final de la subruta anterior, si no se cerró explícitamente.
* 0,0, si este es el primer subtrazado.

## Propiedades {#section-d4127db0dac54e3cbd44f7ea1e001960}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Las capas de efectos lo ignoran.

`clipPathE=` se ignora si no se encuentra ninguna ruta con el nombre especificado en la imagen de origen de la capa o si el origen de la capa no es una imagen.

## Predeterminado {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Ninguno, ya que no hay recorte adicional de la capa.

## Véase también {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
