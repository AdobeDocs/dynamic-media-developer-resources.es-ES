---
title: textPath
description: Ruta de texto. Especifica la ruta que se utilizará como línea de base para el texto proporcionado con textPs=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
TQID: 'https://experienceleague.adobe.com/zVKtDOaScVXM-69CquAw4cpc81Wj7X47LLxBf0RdJ6c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 2%

---

# textPath{#textpath}

Ruta de texto. Especifica la ruta que se utilizará como línea de base para el texto proporcionado con textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Datos de ruta. </p></td> 
 </tr> 
</table>

Vea [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obtener información adicional, incluida una descripción de *`pathDefinition`*.

>[!NOTE]
>
>A diferencia de `clipPath=`, las rutas de texto no se cierran automáticamente cuando &#39;z&#39; o &#39;Z&#39; no se especifican al final de una subruta.

*`pathDefinition`* puede incluir varias subrutas. El texto se representa en las subrutas en el orden especificado.

Los comandos RTF `\ql`, `\qc`, `\qr`, `\li` y `\ri` se pueden usar para colocar el texto procesado en la ruta de acceso.

## Propiedades {#section-068137df436c46b9b55d271eb60e7285}

Atributo de capa de texto (`textPs=` solamente). Ignorado por otras capas. Se aplica a `layer=0` si se especifica para `layer=comp`. Se omitirá si `textPs=` están presentes.

Se devuelve un error si una capa incluye `textPath=` y `textFlowPath=`.

## Predeterminado {#section-697b1f2cfc43498080a31327e6eb173d}

Ninguno, para la renderización de texto estándar.

## Véase también {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [Capas de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
