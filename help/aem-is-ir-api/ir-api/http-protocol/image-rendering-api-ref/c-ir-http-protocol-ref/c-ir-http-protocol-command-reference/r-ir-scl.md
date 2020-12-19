---
description: Vista de escala. Ajusta la escala de la imagen procesada según el factor de escala especificado, en relación con la viñeta de resolución completa.
seo-description: Vista de escala. Ajusta la escala de la imagen procesada según el factor de escala especificado, en relación con la viñeta de resolución completa.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---


# scl{#scl}

Vista de escala. Ajusta la escala de la imagen procesada según el factor de escala especificado, en relación con la viñeta de resolución completa.

`scl= *`filFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filFactor</span> </span> </p></td> 
  <td class="stentry"> <p>Factor de escala inversa (real, 1,0 o bueno). </p></td> 
 </tr> 
</table>

Si `scl=` va después de `wid=` o `hei=` en la dirección URL, cancela esos comandos y `scl=` define el tamaño de la imagen devuelta por el servidor.

Sin embargo, si `wid=` o `hei=` va después de `scl=` en la dirección URL, cancelan `scl=` y `wid=`/ `hei=` definen el tamaño de la imagen devuelta por el servidor.

>[!NOTE]
>
>Se devuelve un error si el tamaño de la imagen de respuesta predeterminada o calculada es mayor que `attribute::MaxPix`.

## Propiedades {#section-170458cbd6984bd59a3434431258b20f}

Puede ocurrir en cualquier lugar dentro de la solicitud. Se omite si `wid=` o `hei=` se producen después de `scl=` en la secuencia de comandos.

Al cambiar el tamaño de la imagen por `scl=` no se cambia el valor de resolución de impresión incrustado en la imagen de respuesta.

## Predeterminado {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Si no se especifica ni `wid=`, `hei=` ni `scl=`, la imagen de respuesta se ajusta al tamaño definido por `attribute::DefaultPix`. Si `attribute::DefaultPix` está vacío, la imagen de respuesta tiene el mismo tamaño que la imagen de vista de la viñeta.

## Véase también {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3),  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
