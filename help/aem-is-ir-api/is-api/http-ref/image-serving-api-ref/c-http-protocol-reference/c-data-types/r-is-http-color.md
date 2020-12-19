---
description: Valores de color. Puede especificar valores de color mediante notación hexadecimal, una lista separada por comas de valores de componentes o decimales.
seo-description: Valores de color. Puede especificar valores de color mediante notación hexadecimal, una lista separada por comas de valores de componentes o decimales.
seo-title: color
solution: Experience Manager
title: color
topic: Scene7 Image Serving - Image Rendering API
uuid: 61308b8e-eaac-4b2e-8500-2f9efa8a6ce8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 14%

---


# color{#color}

Valores de color. Puede especificar valores de color mediante notación hexadecimal, una lista separada por comas de valores de componentes o decimales.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> gray</span>[,<span class="varname"> alpha</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>,<span class="varname"> verde</span>,<span class="varname"> azul</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cian</span>,  <span class="varname"> magenta</span>,  <span class="varname"> amarillo</span>,  <span class="varname"> negro</span>[,alfa]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rojo</span>,  <span class="varname"> verde</span>,  <span class="varname"> azul</span>,  <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>valor del componente de color (0...255, decimal) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cian</span>,  <span class="varname"> magenta</span>,  <span class="varname"> amarillo</span>,  <span class="varname"> negro</span>,  <span class="varname"> alfa</span></span> </p></td> 
  <td class="stentry"> <p>Valor del componente de color CMYK (0,100 %, decimal int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gris</span>,  <span class="varname"> alfa</span></span> </p> </td> 
  <td class="stentry"> <p>valor del componente de color gris (0...100%, decimal) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>valor de color gris hexadecimal (GG) de dos dígitos empaquetado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>gris hexadecimal de cuatro dígitos empaquetado con valor de color alfa (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>valor de color RGB hexadecimal de seis dígitos empaquetado (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>valor de color hexadecimal RGBA (RRGGBBAA) o CMYK (CCMMYKK) empaquetado de ocho dígitos (si se especifica con el sufijo 'k') </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>CMYK hexadecimal de diez dígitos empaquetado con valor alfa (CCYYMKKAA) </p> </td> 
 </tr> 
</table>

Los valores de componentes decimales para los colores RGB están en el rango 0...255. Los valores de los componentes decimales para CMYK y gris están en el rango 0,100%. Todos los valores de componentes hexadecimales están en el rango 0...0xFF.

Se supone que los valores de los componentes de color son independientes del valor alfa (no se multiplican previamente).

Todos los valores de color, prefijos y sufijos no distinguen entre mayúsculas y minúsculas.

El sufijo de tipo &#39;k&#39; es necesario para los valores de color CMYK. Se puede especificar un sufijo de tipo opcionalmente para los valores de color RGB y gris.

El prefijo &#39;0x&#39; es necesario para los valores de color gris hexadecimales.

El sufijo &#39;s&#39; especifica que el valor de color está asociado con el espacio de color de entrada (origen) correspondiente al tipo de píxel del valor de color (definido con `attribute::IccProfileSrc*`). Si este sufijo no está presente, el valor de color se asocia al espacio de color de salida (destino) (definido con `icc=` o `attribute::IccProfile*`).

## Predeterminado {#section-737082a7da544acca8092a48d88480e7}

Si no se especifica explícitamente un valor alfa, se supone que es 255, 0xFF o 100% (completamente opaco).

## Ejemplos {#section-4ac69026349949f8b595a6d4a9ce474d}

Algunos ejemplos de especificadores de color válidos, así como el tipo de píxel, el valor de color, el valor alfa y el espacio de color predeterminado correspondientes:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>color</i> </b> </th> 
   <th class="entry"> <b>Tipo de píxel</b> </th> 
   <th class="entry"> <b>Valor de color</b> </th> 
   <th class="entry"> <b>Valor alfa</b> </th> 
   <th class="entry"> <b>Espacio de color predeterminado  </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0,100,200,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160,177,194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100S </p> </td> 
   <td> <p>gris </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75 g </p> </td> 
   <td> <p>gris </p> </td> 
   <td> <p>50 % </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>gris </p> </td> 
   <td> <p>44 % </p> </td> 
   <td> <p>44 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>gris </p> </td> 
   <td> <p>87 % </p> </td> 
   <td> <p>93 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26 KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14 % </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

El espacio de color de salida especificado con `icc=` se aplica en lugar del espacio de color predeterminado cuando el tipo de píxel de un color de salida corresponde al tipo de píxel de la imagen de salida.
