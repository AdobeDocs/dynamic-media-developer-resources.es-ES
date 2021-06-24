---
description: Resolución de impresión. Anula el valor de resolución de impresión incrustado en la imagen de respuesta.
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# printRes{#printres}

Resolución de impresión. Anula el valor de resolución de impresión incrustado en la imagen de respuesta.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Resolución de impresión (dpi). </p></td> 
 </tr> 
</table>

La resolución de impresión se define normalmente por `catalog::PrintResolution` en el caso de una entrada de catálogo; de lo contrario, por el valor de resolución de impresión incrustado en la imagen de origen. En el caso de una plantilla o imagen compuesta en capas, la resolución de impresión predeterminada incrustada en el archivo de respuesta es la resolución de impresión de la imagen de capa con el número de capa más bajo.

La configuración de la resolución de impresión no cambia el tamaño de píxeles de la imagen de respuesta.

## Propiedades {#section-03c7910ebe234804a319e5d0d8ef3a74}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual.

## Predeterminado {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` o la resolución de impresión incrustada en la imagen de origen.

## Véase también {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catálogo::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
