---
description: Área de exclusión del flujo de texto. Especifica una o varias regiones que se excluirán del flujo de texto.
solution: Experience Manager
title: textFlowXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 8%

---

# textFlowXPath{#textflowxpath}

Área de exclusión del flujo de texto. Especifica una o varias regiones que se excluirán del flujo de texto.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obtener información adicional, incluida una descripción de *`pathDefinition`*. Si no se especifica ninguna definición de ruta, se ignora `textFlowXPath=`.

## Propiedades {#section-cd1ebb151d4a405fbfc508d46522d686}

Atributo de capa de texto ( solo `textPs=`). Ignorado por otras capas o cuando se especifica sin `textFlowPath=`. Se aplica a `layer=0` si se especifica para `layer=comp`.

## Predeterminado {#section-9405cda904684d829ed12a9e40a4dc46}

Ninguno.

## Véase también {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
