---
title: icc
description: Perfil de color de salida.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 3%

---

# icc{#icc}

Perfil de color de salida.

`icc= *`objeto`*[, *`renderIntent`*[, *`blackpointComp`*[, *`estremecimiento`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objeto</span> </span> </p></td> 
  <td class="stentry"> <p>Perfil de color ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptual|relativo|saturación|absoluto</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 para activar la compensación de punto negro, 0 para desactivarla. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> estremecimiento</span></span> </p></td> 
  <td class="stentry"> <p>1 para activar el tramado y 0 para desactivarlo. </p></td> 
 </tr> 
</table>

El valor *`object`* especifica el perfil del espacio de color de salida al que se debe convertir la imagen si es diferente del perfil de trabajo. El valor *`profile`* debe ser un válido `icc::Name` definido en el mapa de perfil ICC de un catálogo de imágenes o catálogo predeterminado, o una ruta relativa a un archivo de perfil (normalmente con [!DNL .icc] o [!DNL .icm] sufijo). Consulte [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) para obtener más información.

>[!NOTE]
>
>El valor *`object`* no puede incluir los caracteres &quot;,&quot; aunque tengan codificación HTTP.

El valor *`renderIntent`* permite anular la interpretación predeterminada.

El valor *`blackpointComp`* activa la compensación de punto negro si el perfil de salida admite esta función.

>[!NOTE]
>
>No todas las conversiones de color admiten todas las *`renderIntent`* y *`blackpointComp`* opciones. Normalmente, esta configuración solo se respeta cuando el perfil de salida ICC caracteriza un dispositivo de salida como una impresora o un monitor. Además, algunos perfiles de salida ICC no admiten todas las *`renderIntent`* opciones.

Nota

El modificador *`dither`* habilita el tramado (en realidad difusión por error), que puede evitar o reducir los defectos de las bandas de colores.

## Propiedades {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Atributo de solicitud. El servidor devuelve un error si se especifica un tipo de imagen con `fmt=` que no coincide *`profile`*.

Los modificadores *`renderIntent`* y *`blackpointComp`* se ignoran si no son compatibles con el perfil ICC especificado. Es más probable que los perfiles de dispositivo de salida CMYK admitan distintas intenciones de procesamiento.

## Predeterminado {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Si la administración de color está habilitada y `icc=` no se ha especificado, el servidor envía la imagen convertida al perfil de salida ( `attribute::IccProfile*`) que coincide con el tipo de imagen especificado por `fmt=`.

Si no se especifica, *`renderIntent`* se hereda de `attribute::IccRenderIntent`, *`blackpointComp`* se hereda de `attribute::IccBlackPointCompensation`, y *`dither`* se hereda de `attribute::IccDither`.

## Véase también {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Gestión de color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [Referencia de mapa de perfiles ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
