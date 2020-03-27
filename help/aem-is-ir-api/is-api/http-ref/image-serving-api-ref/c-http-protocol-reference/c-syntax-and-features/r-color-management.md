---
description: El servicio de imágenes admite conversiones de espacio de color basadas en perfiles de espacio de color que se ajustan a la especificación ICC (International Color Consortium).
seo-description: El servicio de imágenes admite conversiones de espacio de color basadas en perfiles de espacio de color que se ajustan a la especificación ICC (International Color Consortium).
seo-title: Gestión de color del servicio de imágenes
solution: Experience Manager
title: Gestión de color del servicio de imágenes
topic: Scene7 Image Serving - Image Rendering API
uuid: 6291372e-ec4c-4fbd-bffc-b55b1bf2f8cf
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Gestión de color del servicio de imágenes{#image-serving-color-management}

El servicio de imágenes admite conversiones de espacio de color basadas en perfiles de espacio de color que se ajustan a la especificación ICC (International Color Consortium).

## Espacios de color predeterminados {#section-8cfe60808bce49968091995e4e521dba}

Cada catálogo de imágenes (y el catálogo predeterminado) puede definir un conjunto de perfiles ICC que constituyen los espacios de color predeterminados para este catálogo: una entrada y un perfil de salida para los datos en escala de grises, RGB y CMYK. See ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, and ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Espacio de color de entrada {#section-9f08e2c1b6aa4fe4815be174972c1944}

Las imágenes de origen pueden incrustar perfiles ICC para definir el espacio de color de entrada. Si no hay ningún perfil incrustado en una imagen de origen, se utilizará `attribute::IccProfileSrc*` el catálogo de imágenes correspondiente al tipo de píxel de la imagen de origen. Si este atributo no está definido en el catálogo de imágenes, `attribute::IccProfile*` se utiliza. Si el atributo de catálogo tampoco está definido, la imagen no se gestiona con colores y solo se aplicarán transformaciones naïve.

## Espacio de color de salida {#section-b517bca622b64dcfa7defba6035d0716}

El espacio de color del resultado final de la imagen de una solicitud se define con el `icc=` comando. Si no `icc=` se especifica, el espacio de color de salida predeterminado (del catálogo principal de la solicitud) que corresponde al tipo de píxel de la imagen de salida se utiliza como espacio de color de salida. Si no hay ningún perfil de salida definido en el catálogo principal o predeterminado, y si la capa base es una imagen con un perfil incrustado que coincide con el tipo de píxel de salida, ese perfil se utiliza para el espacio de color de salida. De lo contrario, el espacio de color de salida permanece sin definir: solo se aplicarán conversiones de color naïve al convertir entre tipos de píxeles y no se podrá incrustar ningún perfil de color en la imagen de salida.

El espacio de color de salida de una solicitud de servicio de imágenes anidada/incrustada siempre es el mismo que el espacio de color de salida de la solicitud externa de incrustación.

## Colores sólidos {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Los valores de color especificados con `color=`, `bgcolor=`o el comando RTF `\iscolortbl` se asociarán con el espacio de color de entrada si el valor de color incluye el sufijo &#39;S&#39;; de lo contrario, se asociarán con el espacio de color de salida. Los valores de color especificados con `bgc=` o los comandos RTF `\colortbl` y siempre `\cmykcolortbl` están asociados con el espacio de color de salida predeterminado o real correspondiente.

>[!NOTE]
>
>En este momento, `bgc=` no participa completamente en la administración de color: el sufijo &#39;S&#39; se ignora cuando se especifica con `bgc=`, y la conversión ingenua se aplica cuando el tipo de píxel del valor de color especificado con `bgc=` difiere del tipo de píxel de la imagen de salida. De lo contrario, `bgc=` se asocia al espacio de color de salida real.

## Solicitudes anidadas e incrustadas {#section-bdda638c31504f26a77e51ebb1ea6e3b}

El espacio de color de salida para solicitudes IS anidadas y solicitudes IR incrustadas se establece automáticamente en el espacio de color de salida de la solicitud externa, a menos que la solicitud anidada especifique un espacio de color de salida explícito con `icc=`. Además, las solicitudes anidadas o incrustadas también heredan los espacios de color de salida predeterminados del catálogo principal de la solicitud externa, para garantizar una gestión coherente de los valores de color sólido.

## Conversión de espacio de color {#section-ca87b80b8e364ea59d8a92d87121b0fb}

El servicio de imágenes suele intentar retrasar las conversiones de color durante el procesamiento. Si todas las capas de una imagen tienen el mismo espacio de color de capa, la conversión al espacio de color de salida se realiza después de la combinación y la escala final. Si hay varios espacios de color de capa, cada capa se transforma en el espacio de color de salida antes de la combinación.

>[!NOTE]
>
>Los comandos `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`y `op_saturation=` son operaciones RGB. Estas operaciones mantienen la fidelidad de color sólo si el espacio de color de la capa tiene un tipo de píxel RGB. Si no es RGB, los datos se convierten a RGB mediante conversión de color naïve y el resultado tendrá una fidelidad de color limitada. El espacio de color de la capa para dichas capas debe considerarse indeterminado.

Las opciones de conversión de color se proporcionan con `icc=` o, si no `icc=` se especifica, con `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`y `attribute::IccDither`.

## Incrustación de perfiles de color {#section-261ebbae5ce046589a776ca972380052}

El perfil de color ICC del espacio de color de salida, si está disponible, se puede incrustar en la imagen de respuesta especificando `iccEmbed=`.

## Administración de perfiles ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Todos los perfiles de color utilizados por el servidor deben cumplir la especificación ICC. Los archivos de perfil ICC suelen tener un sufijo [!DNL .icc] o [!DNL .icm] de archivo y se ubican junto con los archivos de datos de imagen.

Aunque los perfiles de salida se pueden especificar por ruta/nombre de archivo en el `icc=` comando, se recomienda registrar todos los archivos de perfil en el mapa de Perfil ICC del catálogo o catálogo de imágenes predeterminado y utilizar identificadores de acceso directo ( `icc::Name`) en lugar de rutas de archivo.

Todos los perfiles ICC a los que se hace referencia en `catalog::IccProfile` y en `attribute::IccProfile*` deben registrarse en el mapa de Perfiles ICC de la imagen o del catálogo predeterminado.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

En este momento solo se admiten espacios de color CMYK, RGB y escala de grises.

## perfiles de color ICC incluidos {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

El servicio de imágenes incluye la mayoría de los perfiles ICC de Adobe en el catálogo de imágenes predeterminado. Se puede acceder a estos perfiles por sus nombres comunes (por ejemplo, como se ve en Photoshop) o con un identificador algo más corto. La siguiente tabla lista todos los perfiles ICC estándar. Al hacer referencia a un perfil del `icc=` comando por su nombre común, los espacios deben codificarse como `%20`.

Pueden agregarse perfiles adicionales a los perfiles estándar, ya sea al catálogo predeterminado o a un catálogo de imágenes específico. Consulte la Referencia [del mapa de Perfiles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ICC para obtener más información.

>[!NOTE]
>
>La siguiente tabla se aplica solo a *Dynamic Media Hybrid* (se ejecuta en modo de `dynamicmedia` ejecución).

|Identificador|Nombre común|Nombre de archivo||—|—|—||**RGB**|||`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB`|CIE RGB|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC (1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto`|ProPhoto RGB|ProPhoto.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|Rgb Perfil de espacio de color.icm||`WideGamutRGB`|RGB de gama amplia|WideGamutRGB.icc||**CMYK**|||`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc||`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Uncover v2|EuroscaleUncover.icc||`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc||`JapanColorUncoated`|Japan Color 2001 sin estucar|JapanColor2001Uncover.icc||`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc||`NewsprintSNAP2007`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc||`PS4Default`|Photoshop 4 CMYK predeterminado|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5 CMYK predeterminado|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|EE.UU. Sheetfeed Coated v2|USSheetfeedCoated.icc||`SheetfedUncoated`|EE.UU. Sheetfeed Uncover v2|USSheetfeedUnsquare.icc||`UncoatedFogra29`|FOGRA29 no recubierta (ISO 12647-2:2004)|FOGRA29.icc||`WebCoated`|EE.UU. Web Coated (SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`WebCoatedGrade3`|Papel Web Coated SWOP 2006 Grado 3|WebCoatedSWOP2006Grado3.icc||`WebCoatedGrade5`|Papel Web Coated SWOP 2006 Grado 5|WebCoatedSWOP2006Grado5.icc||`WebUncoated`|EE.UU. Web No recubierta v2|USWebUnsquare.icc|

La siguiente tabla se aplica al servicio *de imágenes de* Dynamic Media Classic (Scene7) y a los medios *dinámicos* (que se ejecutan en modo de `dynamicmedia_scene7` ejecución).

|Identificador|Nombre común|Nombre de archivo||—|—|—||**RGB**|||`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB|CIE RGB`|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC (1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|Rgb Perfil de espacio de color.icm||`WideGamutRGB`|RGB de gama amplia|WideGamutRGB.icc||**CMYK**|||`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc||`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Uncover v2|EuroscaleUncover.icc||`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc||`JapanColorUncoated`|Japan Color 2001 sin estucar|JapanColor2001Uncover.icc||`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc||`PS4Default`|Photoshop 4 CMYK predeterminado|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5 CMYK predeterminado|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|EE.UU. Sheetfeed Coated v2|USSheetfeedCoated.icc||`SheetfedUncoated`|EE.UU. Sheetfeed Uncover v2|USSheetfeedUnsquare.icc||`UncoatedFogra29`|FOGRA29 no recubierta (ISO 12647-2:2004)|FOGRA29.icc||`US Newsprint (SNAP 2007)`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc||`WebCoated`|EE.UU. Web Coated (SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`Web Coated SWOP 2006 Grade 3 Paper`|Papel Web Coated SWOP 2006 Grado 3|WebCoatedSWOP2006Grado3.icc||`Web Coated SWOP Grade 5 Paper`|Papel Web Coated SWOP 2006 Grado 5|WebCoatedSWOP2006Grado5.icc||`WebUncoated`|EE.UU. Web No recubierta v2|USWebUnsquare.icc|

## Véase también {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](http://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [atributo::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*, [atributo::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*, [atributo::IccIntentIntent, atributo::IccPointCompensationBlack](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[ Asistente, InccAttribute: IccDitherError, OtrosError Referencia de Mapa de Perfil ICC,color=,bgc=, *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
