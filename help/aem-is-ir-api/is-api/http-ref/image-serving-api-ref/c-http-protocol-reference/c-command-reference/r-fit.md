---
description: Modo de ajuste de imagen de respuesta. Especifica cómo se calcula el factor de escala, que se utiliza para escalar la imagen compuesta a la imagen de respuesta cuando el tamaño de respuesta se especifica con wid= y hei= y scl= no está presente.
solution: Experience Manager
title: Ajuste
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 2%

---


# Ajuste{#fit}

Modo de ajuste de imagen de respuesta. Especifica cómo se calcula el factor de escala, que se utiliza para escalar la imagen compuesta a la imagen de respuesta cuando el tamaño de respuesta se especifica con wid= y hei= y scl= no está presente.

` fit= *``*, *`modeupscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|restricción|recorte|ajuste|estiramiento|ajuste|vfit  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

En la siguiente descripción de las opciones de modo, se supone que *`xScale`* es la relación entre el ancho de la imagen compuesta y el ancho de la imagen de respuesta y *`yScale`* es la relación entre la altura de la imagen compuesta y la altura de la imagen de respuesta.

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
   <td colname="col2"> <p>Escala la imagen compuesta para que se ajuste al espacio asignado con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span>, con un espacio en blanco mínimo y sin recortes. La imagen de respuesta tendrá el tamaño exacto especificado con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span>. Se aplica la escala <span class="varname"> xScale </span> menor y <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> restricción  </span> </p> </td> 
   <td colname="col2"> <p>Escala la imagen compuesta como <span class="codeph"> ajustar </span> para que se ajuste al espacio asignado con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span>, pero la imagen de respuesta real puede ser más pequeña de lo especificado con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span> para evitar espacios en blanco. Se aplica la escala <span class="varname"> xScale </span> menor y <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> recorte </span> </p> </td> 
   <td colname="col2"> <p>Escala la imagen compuesta para que rellene toda la imagen de respuesta con un recorte mínimo y sin espacios en blanco. Se aplica el mayor de <span class="varname"> xScale </span> y <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ajuste </span> </p> </td> 
   <td colname="col2"> <p>Escala la imagen compuesta como <span class="codeph"> recortar </span> para que abarque toda la imagen de respuesta, pero la imagen de respuesta real puede ser mayor de lo especificado con <span class="codeph"> wid= </span> y <span class="codeph"> hei= </span> para evitar recortes. Se aplica el mayor de <span class="varname"> xScale </span> y <span class="varname"> yScale </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> estirar  </span> </p> </td> 
   <td colname="col2"> <p>Escala la imagen compuesta de forma independiente en x e y para rellenar toda la imagen de respuesta, sin recortes ni espacios en blanco. Esto suele cambiar la relación de aspecto de la imagen. <span class="varname"> xScale  </span> se utiliza para escalado horizontal y  <span class="varname"> yScale  </span> para escalado vertical. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit  </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> xScale </span> para ajustar la imagen horizontalmente, con probablemente recorte o espacio en blanco en la parte superior o inferior. Útil para aplicaciones especiales. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit  </span> </p> </td> 
   <td colname="col2"> <p>Aplica <span class="varname"> yScale </span> para ajustar la imagen verticalmente, con probablemente recorte o espacio en blanco a la izquierda y/o a la derecha. Útil para aplicaciones especiales. </p> </td> 
  </tr> 
 </tbody> 
</table>

Configure *`upscale`* en &quot;1&quot; para permitir el aumento de escala o en &quot;0&quot; para restringir que *`xScale`*y *`yScale`* se limiten a 1:1. Si se desactiva el escalado ascendente, pueden estar presentes espacios en blanco adicionales si la imagen compuesta es menor que la imagen de respuesta.

El recorte y los espacios en blanco están centrados de forma predeterminada; su posición se puede controlar con `align=`. El color y la opacidad del relleno del espacio en blanco están determinados por `bgc=`.

## Propiedades {#section-6d7a5a7e18434bca9bc2fdb236af8909}

Ver atributo. Se aplica independientemente de la configuración de capa actual. También se debe especificar al menos uno de `wid=` o `hei=`; de lo contrario, se devuelve un error; se deben especificar `wid=` y `hei=` para que los modos de ajuste se comporten como se describe. También se devuelve un error cuando se especifica `req=tmb`.

## Predeterminado {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## Véase también {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
