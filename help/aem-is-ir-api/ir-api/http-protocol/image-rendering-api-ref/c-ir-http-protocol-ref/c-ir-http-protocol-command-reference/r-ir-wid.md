---
description: Responder el ancho de la imagen. Especifica la escala de la imagen procesada para que la imagen de respuesta no sea más alta que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.
seo-description: Responder el ancho de la imagen. Especifica la escala de la imagen procesada para que la imagen de respuesta no sea más alta que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# wid{#wid}

Responder el ancho de la imagen. Especifica la escala de la imagen procesada para que la imagen de respuesta no sea más alta que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Ancho de la imagen en píxeles (int bueno que 0). </p></td> 
 </tr> 
</table>

La imagen no se rellena si se especifican `wid=` y `hei=` y `wid`/ `hei` es diferente a la proporción de aspecto de la imagen.

`wid=` y  `hei=` trabajar juntos para definir el tamaño de la imagen que devuelve el servidor. Si `scl=` va después de `wid=` o `hei=` en la dirección URL, cancela esos comandos y `scl=` define el tamaño de la imagen devuelta por el servidor.

Sin embargo, si `wid=` o `hei=` va después de `scl=` en la dirección URL, cancelan `scl=` y `wid=`/ `hei=` definen el tamaño de la imagen devuelta por el servidor.

>[!NOTE]
>
>Se devuelve un error si el tamaño de la imagen de respuesta predeterminada o calculada es mayor que `attribute::MaxPix`.

## Propiedades {#section-2d067c6d371748e19cb157684700a49d}

Puede ocurrir en cualquier lugar dentro de la solicitud. Al cambiar el tamaño de la imagen por `wid=`, `hei=` o `scl=` no se cambia el valor de resolución de impresión incrustado en la imagen de respuesta. Se omite si `scl=` se produce después de `wid=` o `hei=` en la secuencia de comandos.

## Predeterminado {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Si no se especifica ni `wid=`, `hei=` ni `scl=`, la imagen de respuesta se ajusta al tamaño definido por `attribute::DefaultPix`. Si `attribute::DefaultPix` está vacío, la imagen de respuesta tendrá el mismo tamaño que la imagen de vista de la viñeta.

## Véase también {#section-450dfc12b1d440e2a3172a69d91db51f}

[atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
