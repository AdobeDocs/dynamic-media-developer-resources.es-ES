---
title: enredar
description: Ver anchura. Especifica la anchura de la imagen de respuesta (ver imagen) cuando fit= no está presente en la solicitud.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
TQID: 'https://experienceleague.adobe.com/n6U4pPJuxOo3rX2nU7EYsnevrCPBzoYq5SiQvrr5t20'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 274
ht-degree: 1%

---

# enredar{#wid}

Ver anchura. Especifica la anchura de la imagen de respuesta (ver imagen) cuando fit= no está presente en la solicitud.

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Ancho de la imagen en píxeles (int mayor que 0). </p> </td> 
 </tr> 
</table>

Si se especifican `hei=` y `scl=`, la imagen compuesta se puede recortar según el atributo `align=`. Cuando `fit=` está presente, `wid=` especifica el ancho de imagen de respuesta exacto, mínimo o máximo; consulte la descripción de `fit=` para obtener detalles.

Si no se especifica `scl=`, la imagen compuesta se ajustará para ajustarse. Si se especifican `wid=` y `hei=`, y no se especifica `scl=`, la imagen se ajustará para ajustarse por completo al rectángulo de anchura/altura, dejando tan poca área de fondo expuesta como sea posible. En este caso, la imagen se coloca dentro del rectángulo de vista según el atributo `align=`.

>[!NOTE]
>
>Se devuelve un error si el tamaño de imagen de respuesta calculado o predeterminado es mayor que `attribute::MaxPix`.

## Predeterminado {#section-976d4c8554a34c899f85d172f6ac6f58}

Si no se especifican `wid=`, `hei=` ni `scl=`, la imagen de respuesta tendrá el tamaño de la imagen compuesta o `attribute::DefaultPix`, el que sea menor.

## Propiedades {#section-c93b7ce1b0d2475f80b06264b45d1285}

Ver atributo. Se aplica independientemente de la configuración de capa actual.

## Ejemplo {#section-82bc98b7c15a451bbe9b915d414c0470}

Solicite una imagen para que quepa en un rectángulo de 200 x 200; alinee la imagen en la parte superior derecha si no es cuadrada. Cualquier área del fondo está llena con `attribute::BkgColor`.

` http:// *`Servidor`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

La misma imagen, entregada a una anchura fija de 200 píxeles, pero con una altura variable para mantener la proporción de aspecto de la imagen. En este caso, la imagen devuelta nunca tendrá áreas de relleno de fondo. En este caso, `align=` no tendría ningún efecto.

` http:// *`Servidor`*/myRootId/myImageId?wid=200`

## Véase también {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
