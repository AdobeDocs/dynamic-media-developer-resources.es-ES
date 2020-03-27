---
description: Modo de ajuste de imagen de respuesta. Especifica cómo se calcula el factor de escala, que se utiliza para escalar la imagen compuesta a la imagen de respuesta cuando el tamaño de respuesta se especifica con wid= y hei= y scl= no está presente.
seo-description: Modo de ajuste de imagen de respuesta. Especifica cómo se calcula el factor de escala, que se utiliza para escalar la imagen compuesta a la imagen de respuesta cuando el tamaño de respuesta se especifica con wid= y hei= y scl= no está presente.
seo-title: Ajuste
solution: Experience Manager
title: Ajuste
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ajuste{#fit}

Modo de ajuste de imagen de respuesta. Especifica cómo se calcula el factor de escala, que se utiliza para escalar la imagen compuesta a la imagen de respuesta cuando el tamaño de respuesta se especifica con wid= y hei= y scl= no está presente.

` fit= *``*, *`modeupscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modo </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ajustar|restringir|recortar|ajustar|ajustar|ajustar|ajustar|ajustar|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

En la siguiente descripción de las opciones de modo, se da por supuesto que *`xScale`* es la relación entre el ancho de la imagen compuesta y el ancho de la imagen de respuesta y *`yScale`* es la relación entre el alto de la imagen compuesta y el alto de la imagen de respuesta.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parámetro </th> 
   <th colname="col2" class="entry"> Definición </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> Ajuste </span> </p> </td> 
   <td colname="col2"> <p>Aplica una escala a la imagen compuesta para que se ajuste al espacio asignado con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span>, con un espacio en blanco mínimo y sin recortes. La imagen de respuesta tendrá el tamaño exacto especificado con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span>. Se aplica el menor de <span class="varname"> xScale </span> e <span class="varname"> yScale </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> restringir </span> </p> </td> 
   <td colname="col2"> <p>Aplica una escala a la imagen compuesta como <span class="codeph"> ajuste </span> para que se ajuste al espacio asignado con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span>, pero la imagen de respuesta real puede ser más pequeña que la especificada con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span> para evitar espacios en blanco. Se aplica el menor de <span class="varname"> xScale </span> e <span class="varname"> yScale </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> recorte </span> </p> </td> 
   <td colname="col2"> <p>Escala la imagen compuesta para que ocupe toda la imagen de respuesta, con un recorte mínimo y sin espacios en blanco. Se aplica el mayor de <span class="varname"> xScale </span> e <span class="varname"> yScale </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ajuste </span> </p> </td> 
   <td colname="col2"> <p>Aplica una escala a la imagen compuesta como <span class="codeph"> recorte </span> para que abarque toda la imagen de respuesta, pero la imagen de respuesta real puede ser mayor que la especificada con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span> para evitar recortes. Se aplica el mayor de <span class="varname"> xScale </span> e <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> estirar </span> </p> </td> 
   <td colname="col2"> <p>Escala la imagen compuesta de forma independiente en x e y para rellenar toda la imagen de respuesta, sin recortes ni espacios en blanco. Esto suele cambiar la proporción de aspecto de la imagen. <span class="varname"> xScale </span> se utiliza para la escala horizontal y <span class="varname"> yScale </span> para la escala vertical. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> xScale </span> para ajustar la imagen horizontalmente, con probablemente recortes o espacios en blanco en la parte superior y/o inferior. Útil para aplicaciones especiales. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> yScale </span> para ajustar la imagen verticalmente, con lo probable de recortar o espacios en blanco a la izquierda o a la derecha. Útil para aplicaciones especiales. </p> </td> 
  </tr> 
 </tbody> 
</table>

Establezca *`upscale`* en &#39;1&#39; para permitir el aumento de escala o en &#39;0&#39; para restringir *`xScale`*y *`yScale`* estar limitado a 1:1. Si la ampliación está desactivada, puede haber espacio en blanco adicional si la imagen compuesta es más pequeña que la imagen de respuesta.

El recorte y el espacio en blanco están centrados de forma predeterminada; su posición se puede controlar con `align=`. El color y la opacidad del relleno de espacio en blanco están determinados por `bgc=`.

## Propiedades {#section-6d7a5a7e18434bca9bc2fdb236af8909}

atributo de Vista. Se aplica independientemente de la configuración de la capa actual. Al menos uno de ellos `wid=` o `hei=` debe especificarse también, de lo contrario se devuelve un error; tanto `wid=` como `hei=` debe especificarse para que los modos de ajuste se comporten como se ha descrito. También se devuelve un error cuando `req=tmb` se especifica.

## Predeterminado {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Véase también {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
