---
description: Ruta de texto. Especifica la ruta que se utilizará como línea de base para el texto proporcionado con textPs=.
seo-description: Ruta de texto. Especifica la ruta que se utilizará como línea de base para el texto proporcionado con textPs=.
seo-title: textPath
solution: Experience Manager
title: textPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a2f0047b-ad62-4605-a723-b43d53fbea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# textPath{#textpath}

Ruta de texto. Especifica la ruta que se utilizará como línea de base para el texto proporcionado con textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obtener información adicional, incluida una descripción de *`pathDefinition`*.

>[!NOTE]
>
>A diferencia de `clipPath=`, las rutas de texto no se cierran automáticamente cuando no se especifica &#39;z&#39; o &#39;Z&#39; al final de una subruta.

*`pathDefinition`* puede incluir varias subrutas. El texto se representa en las subrutas en el orden especificado.

Los comandos RTF `\ql`, `\qc`, `\qr`, `\li` y `\ri` pueden utilizarse para colocar el texto procesado a lo largo de la ruta.

## Propiedades {#section-068137df436c46b9b55d271eb60e7285}

Atributo de capa de texto ( `textPs=` solamente). Omitido por otras capas. Se aplica a `layer=0` si se especifica para `layer=comp`. Se omite si `textPs=` está presente.

Se devuelve un error si una capa incluye `textPath=` y `textFlowPath=`.

## Predeterminado {#section-697b1f2cfc43498080a31327e6eb173d}

Ninguno, para la representación de texto estándar.

## Véase también {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), capas  [de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
