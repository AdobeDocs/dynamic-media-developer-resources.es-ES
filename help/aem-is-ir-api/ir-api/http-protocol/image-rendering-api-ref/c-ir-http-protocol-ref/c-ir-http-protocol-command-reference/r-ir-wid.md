---
title: enredar
description: Ancho de imagen de respuesta. Especifica la escala de la imagen procesada para que la imagen de respuesta no sea más alta que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# enredar{#wid}

Ancho de imagen de respuesta. Especifica la escala de la imagen procesada para que la imagen de respuesta no sea más alta que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Ancho de la imagen en píxeles (int mayor que 0). </p></td> 
 </tr> 
</table>

La imagen no se rellena si se han especificado `wid=` y `hei=`, y `wid`/ `hei` es diferente de la proporción de aspecto de la imagen.

`wid=` y `hei=` trabajan juntos para definir el tamaño de la imagen que devuelve el servidor. Si `scl=` va después de `wid=` o `hei=` en la dirección URL, cancela esos comandos y `scl=` define el tamaño de la imagen que devuelve el servidor.

Sin embargo, si `wid=` o `hei=` van después de `scl=` en la dirección URL, cancelan `scl=` y `wid=`/ `hei=` definen el tamaño de la imagen devuelta por el servidor.

>[!NOTE]
>
>Se devuelve un error si el tamaño de imagen de respuesta calculado o predeterminado es mayor que `attribute::MaxPix`.

## Propiedades {#section-2d067c6d371748e19cb157684700a49d}

Puede producirse en cualquier lugar dentro de la solicitud. Al cambiar el tamaño de la imagen con `wid=`, `hei=` o `scl=`, no se cambia el valor de resolución de impresión incrustado en la imagen de respuesta. Se omite si `scl=` se produce después de `wid=` o `hei=` en la secuencia de comandos.

## Predeterminado {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Si no se especifica `wid=`, `hei=` o `scl=`, la imagen de respuesta se ajustará para ajustarse al tamaño definido por `attribute::DefaultPix`. Si `attribute::DefaultPix` está vacío, la imagen de respuesta tendrá el mismo tamaño que la imagen de vista de la viñeta.

## Véase también {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
