---
title: hei
description: Altura de la imagen de respuesta. Especifica la escala de la imagen procesada para que la altura de la imagen de respuesta no sea mayor que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# hei{#hei}

Altura de la imagen de respuesta. Especifica la escala de la imagen procesada para que la altura de la imagen de respuesta no sea mayor que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Altura de la imagen de respuesta en píxeles (entero bueno que 0). </p></td> 
 </tr> 
</table>

La imagen no se rellena si `wid=` y `hei=` y la anchura/altura es diferente de la proporción de aspecto de la imagen.

`wid=` y `hei=` trabajen juntos para definir el tamaño de la imagen que devuelve el servidor. If `scl=` viene después de `wid=` o `hei=` en la dirección URL, cancela esos comandos y `scl=` define el tamaño de la imagen que devuelve el servidor.

Sin embargo, si `wid=` o `hei=` viene después de `scl=` en la dirección URL, cancelan `scl=` y `wid=`/ `hei=` defina el tamaño de la imagen que devuelve el servidor.

>[!NOTE]
>
>Se devuelve un error si el tamaño de imagen de respuesta calculado o predeterminado es mayor que `attribute::MaxPix`.

## Propiedades {#section-6cbc6acd37c847beab84c896ac25280c}

Puede producirse en cualquier lugar dentro de la solicitud. Cambiar el tamaño de la imagen con `wid=`, `hei=`, o `scl=` no cambia el valor de resolución de impresión incrustado en la imagen de respuesta. Ignorado si `scl=` ocurre después de `wid=` y/o `hei=` en la secuencia de comandos.

## Predeterminado {#section-61043f6c1f5d450883ff9e5eafd95955}

If `wid=`, `hei=`, o `scl=` no se han especificado, la imagen de respuesta se escala para ajustarse al tamaño definido por `attribute::DefaultPix`. If `attribute::DefaultPix` está vacía, la imagen de respuesta tiene el mismo tamaño que la imagen de vista de la viñeta.

## Véase también {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
