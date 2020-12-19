---
description: Área de exclusión de flujo de texto. Especifica una o varias regiones para excluir del flujo de texto.
seo-description: Área de exclusión de flujo de texto. Especifica una o varias regiones para excluir del flujo de texto.
seo-title: textFlowXPath
solution: Experience Manager
title: textFlowXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: ce833ae7-e774-4954-a521-b6247e75f6eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 7%

---


# textFlowXPath{#textflowxpath}

Área de exclusión de flujo de texto. Especifica una o varias regiones para excluir del flujo de texto.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obtener información adicional, incluida una descripción de *`pathDefinition`*. Si no se especifica ninguna definición de ruta, se omite `textFlowXPath=`.

## Propiedades {#section-cd1ebb151d4a405fbfc508d46522d686}

Atributo de capa de texto ( `textPs=` solamente). Omitido por otras capas o cuando se especifica sin `textFlowPath=`. Se aplica a `layer=0` si se especifica para `layer=comp`.

## Predeterminado {#section-9405cda904684d829ed12a9e40a4dc46}

Ninguno.

## Véase también {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
