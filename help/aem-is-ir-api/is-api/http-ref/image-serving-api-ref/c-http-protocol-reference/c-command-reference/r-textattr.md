---
title: textAttr
description: Atributos de capa de texto. Especifica atributos adicionales para las capas de texto que no están disponibles como comandos rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# textAttr{#textattr}

Atributos de capa de texto. Especifica atributos adicionales para las capas de texto que no están disponibles como comandos rtf.

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>Proporciona un medio para cambiar el tamaño de la capa de texto sin cambiar el tamaño de la fuente. Los valores de resolución más altos aumentan el tamaño del texto procesado en relación con el tamaño del lienzo; los valores más pequeños reducen el tamaño del texto. Resolución de texto en puntos por pulgada (int mayor que 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> suavizado </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla el modo de suavizado empleado por el motor de renderización de texto. </p> <p> <span class="codeph"> desactivado | norma | crujiente | afilado | fuerte | suavizar </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> de </span> </p> </td> 
      <td class="stentry"> <p>Deshabilite el suavizado de texto. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
      <td class="stentry"> <p>Active el modo de suavizado de texto estándar (predeterminado). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nítidas </span> </p> </td> 
      <td class="stentry"> <p>Seleccione el modo de suavizado de Photoshop <span class="codeph"> nítido </span> ( <span class="codeph"> textPs= </span> solamente). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> sostenido </span> </p> </td> 
      <td class="stentry"> <p>Seleccione el modo de suavizado de Photoshop <span class="codeph"> sharp </span> ( <span class="codeph"> textPs= </span> solamente). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> </span> fuerte </p> </td> 
      <td class="stentry"> <p>Seleccione el modo de suavizado de Photoshop <span class="codeph"> con </span> seguro ( <span class="codeph"> textPs= </span> solamente). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla el uso de res al representar el texto </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Utilizar la resolución especificada. </p> <p>Utilícelo si el texto se va a representar en un tamaño exacto en relación con el lienzo compuesto. El texto se puede recortar al tamaño de la capa (si se especifica) si el cuadro de texto es demasiado pequeño. Esta es la única opción <span class="varname"> resMode </span> compatible con <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Ajuste la resolución automáticamente para rellenar mejor la capa con el texto. </p> <p>Utilícelo para ajustar automáticamente el tamaño del texto de modo que el cuadro de texto se rellene en la medida de lo posible, sin riesgo de truncamiento. Si el ajuste de texto está habilitado, el texto se puede ajustar de nuevo a la resolución final. La res </span> <span class="varname"> se omite si se selecciona <span class="codeph"> autoRes </span>. No admitido por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Utilice la resolución especificada; reduzca si es necesario para evitar que el texto se trunque a la capa recta. </p> <p>Se utiliza para representar texto con la resolución especificada, siempre que no se produzca ningún recorte. Si hay recorte, la resolución se reduce automáticamente para garantizar que todo el texto esté contenido completamente dentro del cuadro de texto. Si el ajuste de texto está habilitado, el texto se puede ajustar de nuevo a la resolución final. No admitido por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Si el tamaño de la capa de texto no se especifica con size= o si solo se especifica la anchura, se omiten los ajustes 'autoRes' y 'maxRes'. En estos casos, la resolución especificada se utiliza para representar el texto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica el modo de ajuste. </p> <p> Ajuste de <span class="codeph"> | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Desactive el ajuste de palabras. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> ajustar </span> </p> </td> 
      <td class="stentry"> <p>Activar ajuste de palabras estándar. </p> <p>Si es necesario, rompe palabras largas. <span class="codeph"> textPs= </span> solo admite el ajuste <span class="codeph"> </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Activar ajuste de palabras de no separación. </p> <p>Nunca rompe una palabra, incluso si se trunca al final. Se suele usar con <span class="codeph"> autoRes </span> o <span class="codeph"> maxRes </span> para garantizar que las palabras largas nunca se rompan. </p> </td> 
     </tr> 
    </table> </p> <p>Tanto el ajuste <span class="codeph"> como </span> y <span class="codeph"> se ajustan automáticamente en </span> los límites de palabras y guiones. </p> </td> 
 </tr> 
</table>

## Propiedades {#section-114ca0b8585b403c873e2251478ad1d5}

Atributo de capa de texto. Ignorado por las capas de imagen, color sólido y efecto. Se aplica a `layer=0` si se especifica para `layer=comp`.

## Predeterminado {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Véase también {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
