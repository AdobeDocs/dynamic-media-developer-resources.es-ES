---
description: Filtro de tipo de contenido estático. Especifica una cadena de filtro para el contenido estático entregado mediante /is/content.
solution: Experience Manager
title: tipo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---

# tipo{#type}

Filtro de tipo de contenido estático. Especifica una cadena de filtro para el contenido estático entregado mediante /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Escriba la cadena del filtro. </p></td> 
 </tr> 
</table>

El servidor comparará val con el valor de `catalog::Type` del elemento de contenido estático solicitado. El elemento se devuelve al cliente si los valores coinciden (con distinción de mayúsculas y minúsculas); de lo contrario, se devuelve un error.

## Propiedades {#section-529b088434a44a9f86a64ef548d2925b}

Solo se admite para solicitudes de contenido estático (que no sean de imagen) servidas mediante . Se omite si `catalog::Type` está vacío o no está definido.

## Predeterminado {#section-e9e8f51d0a01452183ccb510efd87d46}

No se aplica ninguna coincidencia de tipo si no se especifica `type=` o está vacío.

## Véase también {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Contenido](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da) estático (no imagen),  [catálogo::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
