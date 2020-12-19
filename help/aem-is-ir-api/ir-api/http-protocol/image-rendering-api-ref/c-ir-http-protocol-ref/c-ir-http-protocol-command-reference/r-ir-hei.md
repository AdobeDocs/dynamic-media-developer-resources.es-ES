---
description: Responder la altura de la imagen. Especifica la escala de la imagen representada de modo que la altura de la imagen de respuesta no sea mayor que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.
seo-description: Responder la altura de la imagen. Especifica la escala de la imagen representada de modo que la altura de la imagen de respuesta no sea mayor que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# hei{#hei}

Responder la altura de la imagen. Especifica la escala de la imagen representada de modo que la altura de la imagen de respuesta no sea mayor que el valor especificado, manteniendo al mismo tiempo la proporción de aspecto de la imagen.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Responder la altura de la imagen en píxeles (entero bueno a 0). </p></td> 
 </tr> 
</table>

La imagen no se rellena si se especifican `wid=` y `hei=` y la anchura y altura es diferente a la proporción de aspecto de la imagen.

`wid=` y  `hei=` trabajar juntos para definir el tamaño de la imagen que devuelve el servidor. Si `scl=` va después de `wid=` o `hei=` en la dirección URL, cancela esos comandos y `scl=` define el tamaño de la imagen devuelta por el servidor.

Sin embargo, si `wid=` o `hei=` va después de `scl=` en la dirección URL, cancelan `scl=` y `wid=`/ `hei=` definen el tamaño de la imagen devuelta por el servidor.

>[!NOTE]
>
>Se devuelve un error si el tamaño de la imagen de respuesta predeterminada o calculada es mayor que `attribute::MaxPix`.

## Propiedades {#section-6cbc6acd37c847beab84c896ac25280c}

Puede ocurrir en cualquier lugar dentro de la solicitud. Al cambiar el tamaño de la imagen por `wid=`, `hei=` o `scl=` no se cambia el valor de resolución de impresión incrustado en la imagen de respuesta. Se omite si `scl=` se produce después de `wid=` y/o `hei=` en la secuencia de comandos.

## Predeterminado {#section-61043f6c1f5d450883ff9e5eafd95955}

Si no se especifica ni `wid=`, `hei=` ni `scl=`, la imagen de respuesta se ajusta al tamaño definido por `attribute::DefaultPix`. Si `attribute::DefaultPix` está vacío, la imagen de respuesta tiene el mismo tamaño que la imagen de vista de la viñeta.

## Véase también {#section-7ba51379f1e2421c92d3592d20a37734}

[atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
