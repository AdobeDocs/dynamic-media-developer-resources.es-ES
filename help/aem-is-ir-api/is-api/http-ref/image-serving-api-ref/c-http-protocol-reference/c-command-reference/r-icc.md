---
description: Perfil de color de salida.
seo-description: Perfil de color de salida.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

Perfil de color de salida.

`icc= *``*[, *``*[, *``*[, *`objetrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objeto</span></span> </p></td> 
  <td class="stentry"> <p>perfil de color ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> interpretaciónCalidad</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptual|relativo|saturación|absoluto</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 para habilitar, 0 para deshabilitar la compensación de punto negro. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> tramado</span></span> </p></td> 
  <td class="stentry"> <p>1 para activar, 0 para desactivar el tramado. </p></td> 
 </tr> 
</table>

*`object`* especifica el perfil de espacio de color de salida al que se debe convertir la imagen si es diferente al perfil de trabajo. *`profile`* debe ser una `icc::Name` definición válida en el mapa de perfiles ICC de un catálogo de imágenes o catálogo predeterminado, o una ruta relativa a un archivo de perfil (normalmente con [!DNL .icc] o [!DNL .icm] sufijo). See [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)for additional information.

>[!NOTE]
>
>*`object`* no pueden incluir caracteres &#39;,&#39;, aunque estén codificados en HTTP.

*`renderIntent`* permite anular la interpretación predeterminada.

*`blackpointComp`* habilita la compensación de puntos negros si el perfil de salida admite esta función.

>[!NOTE]
>
>No todas las conversiones de color admiten todas *`renderIntent`* las opciones y *`blackpointComp`* . Normalmente, estos ajustes solo se respetan cuando el perfil de salida ICC caracteriza un dispositivo de salida como una impresora o un monitor. Además, algunos perfiles de salida del ICC no admiten todas las *`renderIntent`* opciones.

Nota

*`dither`* activa el tramado (en realidad la difusión de errores), que puede evitar o reducir los artefactos de bandas de color.

## Propiedades {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Solicitar atributo. El servidor devolverá un error si se especifica un tipo de imagen `fmt=` que no coincide con *`profile`*.

*`renderIntent`* y *`blackpointComp`* se omiten si no son compatibles con el perfil ICC especificado. Es más probable que los perfiles de dispositivo de salida CMYK admitan diferentes interpretaciones.

## Predeterminado {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Si la administración de color está habilitada y no `icc=` se especifica, el servidor enviará la imagen convertida al perfil de salida ( `attribute::IccProfile*`) que coincida con el tipo de imagen especificado con `fmt=`.

Si no se especifica, *`renderIntent`* se hereda de `attribute::IccRenderIntent`, *`blackpointComp`* se hereda de `attribute::IccBlackPointCompensation`y *`dither`* se hereda de `attribute::IccDither`.

## Véase también {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[atributo::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [atributo::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [objeto, Color Management, ReferenciaICC,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[FmtEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
