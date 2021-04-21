---
description: Vista de escala. Escala la imagen representada según el factor de escala especificado, en relación con la viñeta de resolución completa.
solution: Experience Manager
title: scl
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 3%

---


# scl{#scl}

Vista de escala. Escala la imagen representada según el factor de escala especificado, en relación con la viñeta de resolución completa.

`scl= *`Visitor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> Visitor</span> </span> </p></td> 
  <td class="stentry"> <p>Factor de escala inversa (real, 1,0 o bueno). </p></td> 
 </tr> 
</table>

Si `scl=` viene después de `wid=` o `hei=` en la dirección URL, cancela esos comandos y `scl=` define el tamaño de la imagen devuelta por el servidor.

Sin embargo, si `wid=` o `hei=` va después de `scl=` en la dirección URL, cancelan `scl=` y `wid=`/ `hei=` definen el tamaño de la imagen devuelta por el servidor.

>[!NOTE]
>
>Se devuelve un error si el tamaño de imagen de respuesta calculado o predeterminado es mayor que `attribute::MaxPix`.

## Propiedades {#section-170458cbd6984bd59a3434431258b20f}

Puede ocurrir en cualquier lugar dentro de la solicitud. Se omite si `wid=` o `hei=` se producen después de `scl=` en la secuencia de comandos.

Cambiar el tamaño de la imagen por `scl=` no cambia el valor de resolución de impresión incrustado en la imagen de respuesta.

## Predeterminado {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Si no se especifica `wid=`, `hei=` ni `scl=`, la imagen de respuesta se escala para ajustarse al tamaño definido por `attribute::DefaultPix`. Si `attribute::DefaultPix` está vacío, la imagen de respuesta tiene el mismo tamaño que la imagen de vista de la viñeta.

## Véase también {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3),  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
