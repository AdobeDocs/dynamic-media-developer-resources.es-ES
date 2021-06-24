---
description: Vista de escala. Escala la imagen compuesta por la inversa del factor de incidencia.
solution: Experience Manager
title: scl
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---

# scl{#scl}

Vista de escala. Escala la imagen compuesta por la inversa del factor de incidencia.

`scl= *`Visitor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Visitor</span> </p> </td> 
  <td class="stentry"> <p>Factor de escala inversa (bueno real distinto de 0,0). </p></td> 
 </tr> 
</table>

No se aplica ninguna escala cuando `scl=1`. *`invFactor`* mayor que 1,0 baja escala y menor que 1,0 amplía la imagen compuesta.

Si se especifica `scl=` y `wid=` o `hei=` también están presentes, la imagen se recorta a `wid=` o `hei=` después del escalado.

>[!NOTE]
>
>Se devuelve un error si el tamaño de imagen de respuesta calculado o predeterminado es mayor que `attribute::MaxPix`.

## Propiedades {#section-60af012719db477db4a4703e9a6da5f5}

Ver atributo. Se aplica independientemente de la configuración de capa actual.

## Predeterminado {#section-32502fa218a24e1f9c65f41c0260b56a}

Si no se especifican `wid=`, `hei=` ni `scl=`, la imagen de respuesta tendrá el tamaño de la imagen compuesta o `attribute::DefaultPix`, el que sea más pequeño.

## Ejemplo {#section-a33f6239476a4b438d939656ad99aa76}

Consulte el ejemplo en [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) para obtener una aplicación común de `scl=`.

## Véase también {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
