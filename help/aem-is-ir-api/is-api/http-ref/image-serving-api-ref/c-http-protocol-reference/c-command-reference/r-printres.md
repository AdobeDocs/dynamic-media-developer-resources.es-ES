---
title: printRes
description: Resolución de impresión. Anula el valor de resolución de impresión incrustado en la imagen de respuesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# printRes{#printres}

Resolución de impresión. Anula el valor de resolución de impresión incrustado en la imagen de respuesta.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Resolución de impresión (ppp). </p></td> 
 </tr> 
</table>

La resolución de impresión se define normalmente por `catalog::PrintResolution` si es una entrada de catálogo, de lo contrario, por el valor de resolución de impresión incrustado en la imagen de origen. Si hay una plantilla o una imagen compuesta con capas, la resolución de impresión predeterminada incrustada en el archivo de respuesta es la resolución de impresión de la imagen de capa con el número de capa más bajo.

La configuración de la resolución de impresión no cambia el tamaño en píxeles de la imagen de respuesta.

## Propiedades {#section-03c7910ebe234804a319e5d0d8ef3a74}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual.

## Predeterminado {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
O la resolución de impresión incrustada en la imagen de origen.

## Véase también {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
