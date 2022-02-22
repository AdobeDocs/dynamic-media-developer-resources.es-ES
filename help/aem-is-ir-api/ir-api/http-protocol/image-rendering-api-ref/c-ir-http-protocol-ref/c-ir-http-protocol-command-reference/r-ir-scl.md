---
title: scl
description: Vista de escala. Escala la imagen representada según el factor de escala especificado, en relación con la viñeta de resolución completa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '174'
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

If `scl=` viene después de `wid=` o `hei=` en la dirección URL, cancela esos comandos y `scl=` define el tamaño de la imagen que devuelve el servidor.

Sin embargo, si `wid=` o `hei=` viene después de `scl=` en la URL, cancelan `scl=` y `wid=`/ `hei=` defina el tamaño de la imagen que devuelve el servidor.

>[!NOTE]
>
>Se devuelve un error si el tamaño de imagen de respuesta calculado o predeterminado es mayor que `attribute::MaxPix`.

## Propiedades {#section-170458cbd6984bd59a3434431258b20f}

Puede ocurrir en cualquier lugar dentro de la solicitud. Ignorado si `wid=` o `hei=` occur after `scl=` en la secuencia de comandos.

Cambiar el tamaño de la imagen con `scl=` no cambia el valor de resolución de impresión incrustado en la imagen de respuesta.

## Predeterminado {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

If `wid=`, `hei=`o `scl=` no se especifican, la imagen de respuesta se escala para ajustarse al tamaño definido por `attribute::DefaultPix`. If `attribute::DefaultPix` está vacía, la imagen de respuesta tiene el mismo tamaño que la imagen de vista de la viñeta.

## Véase también {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
