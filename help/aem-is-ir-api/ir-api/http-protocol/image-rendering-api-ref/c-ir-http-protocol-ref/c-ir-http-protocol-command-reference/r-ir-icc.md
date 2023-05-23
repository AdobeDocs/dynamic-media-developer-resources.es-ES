---
title: icc
description: Perfil de color de salida.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# icc{#icc}

Perfil de color de salida.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> perfil</span></span> </p></td> 
  <td class="stentry"> <p>Perfil de color ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>perceptual | relativo | saturación | absoluto </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 para activar la compensación de punto negro, 0 para desactivarla. </p></td> 
 </tr> 
</table>

*`profile`* Especifica el perfil del espacio de color de salida al que se debe convertir la imagen procesada si es diferente del perfil de trabajo. *`profile`* Debe ser un válido `icc::Name` definido en el mapa de perfil ICC de un catálogo de imágenes o catálogo predeterminado, o una ruta relativa a un archivo de perfil (normalmente con [!DNL `.icc`] o [!DNL `.icm`] sufijo).

>[!NOTE]
>
>*`profile`* No puede incluir los caracteres &quot;,&quot; aunque tengan codificación HTTP.

*`renderIntent`* Permite anular la interpretación predeterminada.

*`blackpointComp`* Habilita la compensación de punto negro si el perfil de salida admite esta función.

>[!NOTE]
>
>No todas las conversiones de color admiten todas las *`renderIntent`* y *`blackpointComp`* opciones. Normalmente, esta configuración solo se respeta cuando el perfil de salida ICC caracteriza un dispositivo de salida como una impresora o un monitor. Además, algunos perfiles de salida ICC no admiten todas las *`renderIntent`* opciones.

## Propiedades {#section-b4042623a8ea40248c11b2153e5906b1}

Puede producirse en cualquier lugar dentro de la solicitud. Se devuelve un error si el tipo de imagen se especifica con `fmt=` no coincide con *`profile`*.

Ambos *`renderIntent`* y *`blackpointComp`* se ignoran si no son compatibles con el perfil ICC especificado.

Es más probable que los perfiles de dispositivo de salida CMYK admitan distintas intenciones de procesamiento.

## Predeterminado {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Si la administración de color está habilitada y `icc=` no se ha especificado, el servidor envía la imagen convertida al perfil de salida ( `attribute::IccProfile*`) que coincide con el tipo de imagen especificado por `fmt=`.

Si no se especifica, *`renderIntent`* se hereda de `attribute::IccRenderIntent`, y *`blackpointComp`* se hereda de `attribute::IccBlackPointCompensation`.

## Véase también {#section-37ef83149fd74345956a98f633cc0294}

[Gestión de color](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
