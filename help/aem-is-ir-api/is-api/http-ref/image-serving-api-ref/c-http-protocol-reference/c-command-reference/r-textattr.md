---
description: Atributos de capa de texto. Especifica atributos adicionales para capas de texto que no están disponibles como comandos rtf.
seo-description: Atributos de capa de texto. Especifica atributos adicionales para capas de texto que no están disponibles como comandos rtf.
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 1%

---


# textAttr{#textattr}

Atributos de capa de texto. Especifica atributos adicionales para capas de texto que no están disponibles como comandos rtf.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>Proporciona un medio para escalar la capa de texto sin cambiar el tamaño de fuente. Los valores de resolución más altos aumentan el tamaño del texto procesado en relación con el tamaño del lienzo; los valores más pequeños reducen el tamaño del texto. Resolución de texto en puntos por pulgada (int bueno a 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing  </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla el modo de suavizado empleado por el motor de procesamiento de texto. </p> <p> <span class="codeph"> off | norma | crujiente | agudo | fuerte | suave  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> apagado </span> </p> </td> 
      <td class="stentry"> <p>Desactive el suavizado de texto. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm  </span> </p> </td> 
      <td class="stentry"> <p>Activar el modo de suavizado de texto estándar (predeterminado). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> crujiente  </span> </p> </td> 
      <td class="stentry"> <p>Seleccione el modo de suavizado de Photoshop <span class="codeph"> crujiente </span> ( <span class="codeph"> textPs= </span> solamente). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> enfocado  </span> </p> </td> 
      <td class="stentry"> <p>Seleccione el modo de suavizado de Photoshop <span class="codeph"> agudo </span> ( <span class="codeph"> textPs= </span> solamente). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fuerte </span> </p> </td> 
      <td class="stentry"> <p>Seleccione el modo de suavizado de Photoshop <span class="codeph"> fuerte </span> ( <span class="codeph"> textPs= </span> solamente). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla cómo se utiliza el res al procesar el texto </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>Utilice la resolución especificada. </p> <p>Se utiliza si el texto se va a representar con un tamaño exacto en relación con el lienzo de composición. El texto se puede recortar al tamaño de la capa (si se especifica) si el cuadro de texto es demasiado pequeño. Esta es la única opción <span class="varname"> resMode </span> admitida por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>Ajuste la resolución automáticamente para rellenar mejor el rectángulo de la capa con el texto. </p> <p>Se utiliza para ajustar automáticamente el tamaño del texto de modo que el cuadro de texto se rellene en la medida de lo posible, sin riesgo de truncamiento. Si el ajuste de palabras está activado, el texto se puede volver a ajustar en la resolución final. <span class="varname"> res  </span> se omite si  <span class="codeph"> autoRes  </span> está seleccionado. No compatible con <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>Utilizar la resolución especificada; disminuya si es necesario para evitar que el texto se trunque al rectángulo de la capa. </p> <p>Se utiliza para representar el texto con la resolución exacta especificada, siempre que no se produzca ningún recorte. En caso de recorte, la resolución se reduce automáticamente para garantizar que todo el texto esté contenido completamente dentro del cuadro de texto. Si el ajuste de palabras está activado, el texto se puede volver a ajustar en la resolución final. No compatible con <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Si el tamaño de la capa de texto no se especifica con size= o si solo se especifica la anchura, se omiten los valores 'autoRes' y 'maxRes' y se utiliza la resolución especificada para representar el texto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica el modo de ajuste. </p> <p> <span class="codeph"> ajustar | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>Desactive el ajuste de palabras. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> ajuste </span> </p> </td> 
      <td class="stentry"> <p>Habilite el ajuste de palabras estándar. </p> <p>Rompe palabras largas si es necesario. <span class="codeph"> textPs=  </span> solo admite  <span class="codeph"> ajuste  </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>Habilitar ajuste de palabras sin saltos. </p> <p>Nunca se rompe una palabra, incluso si se trunca al final. Generalmente se utiliza junto con <span class="codeph"> autoRes </span> o <span class="codeph"> maxRes </span> para asegurar que las palabras largas nunca se rompan. </p> </td> 
     </tr> 
    </table> </p> <p>Tanto <span class="codeph"> envuelven </span> como <span class="codeph"> nbwrap </span> automáticamente en límites de palabras y guiones. </p> </td> 
 </tr> 
</table>

## Propiedades {#section-114ca0b8585b403c873e2251478ad1d5}

Atributo de capa de texto. Omitido por capas de imagen, color sólido y efecto. Se aplica a `layer=0` si se especifica para `layer=comp`.

## Predeterminado {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Véase también {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
