---
title: textFlowXPath
description: Área de exclusión de flujo de texto. Especifica una o varias regiones que se excluirán del flujo de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# textFlowXPath{#textflowxpath}

Área de exclusión de flujo de texto. Especifica una o varias regiones que se excluirán del flujo de texto.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Datos de ruta. </p></td> 
 </tr> 
</table>

Vea [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obtener información adicional, incluida una descripción de *`pathDefinition`*. Si no se especifica ninguna definición de ruta de acceso, se omite `textFlowXPath=`.

## Propiedades {#section-cd1ebb151d4a405fbfc508d46522d686}

Atributo de capa de texto (`textPs=` solamente). Omitido por otras capas o especificado sin `textFlowPath=`. Se aplica a `layer=0` si se especifica para `layer=comp`.

## Predeterminado {#section-9405cda904684d829ed12a9e40a4dc46}

Ninguno.

## Véase también {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
