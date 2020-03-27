---
description: vista de escala. Escala la imagen compuesta por el inverso del factor de incidencia.
seo-description: vista de escala. Escala la imagen compuesta por el inverso del factor de incidencia.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

vista de escala. Escala la imagen compuesta por el inverso del factor de incidencia.

`scl= *`filFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> filFactor</span> </p> </td> 
  <td class="stentry"> <p>Factor de escala inversa (bueno real superior a 0,0). </p></td> 
 </tr> 
</table>

No se aplica ninguna escala cuando `scl=1`. *`invFactor`* mayor que 1,0 reduce la escala y menor que 1,0 amplía la imagen compuesta.

Si `scl=` se especifica `wid=` y/o también `hei=` están presentes, la imagen se recorta `wid=` y/o `hei=` después de escalarla.

>[!NOTE]
>
>Se devuelve un error si el tamaño de la imagen de respuesta predeterminada o calculada es mayor que `attribute::MaxPix`.

## Propiedades {#section-60af012719db477db4a4703e9a6da5f5}

Atributo de Vista. Se aplica independientemente de la configuración de la capa actual.

## Predeterminado {#section-32502fa218a24e1f9c65f41c0260b56a}

Si no `wid=`se especifica ni `hei=`ni `scl=` , la imagen de respuesta tendrá el tamaño de la imagen compuesta o `attribute::DefaultPix`, el que sea más pequeño.

## Ejemplo {#section-a33f6239476a4b438d939656ad99aa76}

Consulte el ejemplo en [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) para obtener una aplicación común de `scl=`.

## Véase también {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
