---
title: Gestión de color del servicio de imágenes
description: Image Serving admite conversiones de espacio de color basadas en perfiles de espacio de color que se ajustan a la especificación ICC (International Color Consortium).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 0%

---

# Gestión de color del servicio de imágenes{#image-serving-color-management}

Image Serving admite conversiones de espacio de color basadas en perfiles de espacio de color que se ajustan a la especificación ICC (International Color Consortium).

## Espacios de color predeterminados {#section-8cfe60808bce49968091995e4e521dba}

Cada catálogo de imágenes (y el catálogo predeterminado) puede definir un conjunto de perfiles ICC que constituyen los espacios de color predeterminados para este catálogo: un perfil de entrada y otro de salida para datos de escala gris, RGB y CMYK. Consulte
[atributo::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[atributo::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[atributo::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[atributo::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[atributo::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[atributo::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Espacio de color de entrada {#section-9f08e2c1b6aa4fe4815be174972c1944}

Las imágenes de origen pueden incrustar perfiles ICC para definir el espacio de color de entrada. Si no hay ningún perfil incrustado en una imagen de origen, `attribute::IccProfileSrc*` del catálogo de imágenes correspondiente al tipo de píxel de la imagen de origen se utiliza. Si este atributo no está definido en el catálogo de imágenes, `attribute::IccProfile*` se utiliza. Si el atributo de catálogo tampoco está definido, la imagen no se administra con colores y solo se aplican transformaciones naïve.

## Espacio de color de salida {#section-b517bca622b64dcfa7defba6035d0716}

El espacio de color del resultado de la imagen final de una solicitud se define con la variable `icc=` comando. If `icc=` no se especifica, el espacio de color de salida predeterminado (del catálogo principal de la solicitud) que corresponde al tipo de píxel de la imagen de salida se utiliza como espacio de color de salida. Si no se define ningún perfil de salida en el catálogo principal o predeterminado y si la capa base es una imagen con un perfil incrustado que coincide con el tipo de píxel de salida, ese perfil se utiliza para el espacio de color de salida. De lo contrario, el espacio de color de salida permanece sin definir: solo se aplican conversiones de color naïve al convertir entre tipos de píxeles y no se puede incrustar ningún perfil de color en la imagen de salida.

El espacio de color de salida de una solicitud de servicio de imágenes anidada/incrustada siempre es el mismo que el espacio de color de salida de la solicitud externa de incrustación.

## Colores sólidos {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Valores de color especificados con `color=`, `bgcolor=`o el comando RTF `\iscolortbl` se asocian al espacio de color de entrada si el valor de color incluye el sufijo &quot;S&quot;; en caso contrario, se asocian al espacio de color de salida. Valores de color especificados con `bgc=` o los comandos RTF `\colortbl` y `\cmykcolortbl` siempre están asociados al espacio de color de salida predeterminado o real correspondiente.

>[!NOTE]
>
>En este momento, `bgc=` no participa completamente en la gestión de color: el sufijo &quot;S&quot; se ignora cuando se especifica con `bgc=`, y la conversión naïve se aplica cuando el tipo de píxel del valor de color especificado con `bgc=` difiere del tipo de píxel de la imagen de salida. De lo contrario, `bgc=` está asociado con el espacio de color de salida real.

## Solicitudes anidadas e incrustadas {#section-bdda638c31504f26a77e51ebb1ea6e3b}

El espacio de color de salida para solicitudes IS anidadas y solicitudes IR incrustadas se establece automáticamente en el espacio de color de salida de la solicitud externa, a menos que la solicitud anidada especifique un espacio de color de salida explícito con `icc=`. Además, las solicitudes anidadas/incrustadas también heredan los espacios de color de salida predeterminados del catálogo principal de la solicitud exterior, para garantizar una gestión coherente de los valores de color sólido.

## Conversión de espacio de color {#section-ca87b80b8e364ea59d8a92d87121b0fb}

El servicio de imágenes suele intentar retrasar las conversiones de color durante el procesamiento. Si todas las capas de una imagen tienen el mismo espacio de color de capa, la conversión al espacio de color de salida se realiza después de la combinación y el escalado final. Si hay varios espacios de color de capa, cada capa se transforma al espacio de color de salida antes de la fusión.

>[!NOTE]
>
>Los comandos `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`y `op_saturation=` son operaciones de RGB. Estas operaciones mantienen la fidelidad de color solo si el espacio de color de la capa tiene un tipo de píxel RGB. Si no es un RGB, los datos se convierten a RGB mediante la conversión de color naïve y el resultado tendrá una fidelidad de color limitada. El espacio de color de la capa para estas capas debe considerarse indeterminado.

Las opciones de conversión de color se proporcionan con `icc=` o si `icc=` no se ha especificado, con `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`y `attribute::IccDither`.

## Incrustación de perfiles de color {#section-261ebbae5ce046589a776ca972380052}

El perfil de color ICC del espacio de color de salida, si está disponible, se puede incrustar en la imagen de respuesta especificando `iccEmbed=`.

## Administración de perfiles ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Todos los perfiles de color utilizados por el servidor deben cumplir la especificación ICC. Los archivos de perfil ICC suelen tener un [!DNL .icc] o [!DNL .icm] sufijo de archivo y se ubican junto con archivos de datos de imagen.

Mientras que los perfiles de salida se pueden especificar por ruta/nombre de archivo en la variable `icc=` , se recomienda registrar todos los archivos de perfil en el mapa de perfiles ICC del catálogo o catálogo de imágenes predeterminado y utilizar identificadores de acceso directo ( `icc::Name`) en lugar de rutas de archivo.

Todos los perfiles ICC a los que se hace referencia en `catalog::IccProfile` y `attribute::IccProfile*` debe estar registrado en el mapa de perfiles ICC de la imagen o del catálogo predeterminado.

## Restricciones {#section-fb50ede40b124b89b30679da29782ab5}

En este momento solo se admiten los espacios de color CMYK, RGB y escala de grises.

## Perfiles de color ICC incluidos {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Serving incluye la mayoría de los perfiles ICC de Adobe estándar en el catálogo de imágenes predeterminado. Se puede acceder a estos perfiles mediante sus nombres comunes (por ejemplo, como se ve en Photoshop) o con un identificador algo más corto. La siguiente tabla enumera todos los perfiles ICC estándar. Al hacer referencia a un perfil en la variable `icc=` por su nombre común, los espacios deben codificarse como `%20`.

Se pueden agregar perfiles adicionales a los perfiles estándar, ya sea al catálogo predeterminado o a un catálogo de imágenes específico. Consulte la [Referencia de mapa de perfil ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) para obtener más información.

>[!NOTE]
>
>La siguiente tabla se aplica a *Dynamic Media híbrido* solo (con `dynamicmedia` modo de ejecución).

|Identificador|Nombre común|Nombre de archivo| |— |— |— | |**RGB**||| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|RGB de Apple|AppleRGB.icc| |`CIERGB`|RGB CIE|CIERGB.icc| |`ColorMatchRGB`|RGB ColorMatch|ColorMatchRGB.icc| |`NTSC`|NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto`|RGB ProPhoto|ProPhoto.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm| |`WideGamutRGB`|RGB de gama amplia|WideGamutRGB.icc| |**CMYK**||| |`CoatedFogra27`|FOGRA27 recubierto (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|FOGRA39 recubierto (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|Europa ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc| |`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale Uncovered v2|EuroscaleUncovered.icc| |`JapanColorCoated`|Color japonés 2001 recubierto|Color japonés2001recubierto.icc| |`JapanColorNewspaper`|Diario japonés color 2002|JapanColor2002Newspaper.icc| |`JapanColorUncoated`|Color japonés 2001 sin recubrir|Color japonés2001Sin recubrir.icc| |`JapanColorWebCoated`|Color japonés 2003 Web recubierto|Color japonés2003WebCoated.icc| |`JapanWebCoated`|Japón Web Coated (Ad)|JapónWebCoated.icc| |`NewsprintSNAP2007`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc| |`PS4Default`|CMYK predeterminado de Photoshop 4|Photoshop4DefaultCMYK.icc| |`PS5Default`|CMYK predeterminado de Photoshop 5|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|EE.UU. Captura de hojas v2|USSheetfeedCoated.icc| |`SheetfedUncoated`|EE.UU. Captura de pantalla v2 no recubierto|USSheetfeedUncovered.icc| |`UncoatedFogra29`|FOGRA29 no recubierto (ISO 12647-2:2004)|UncoveredFOGRA29.icc| |`WebCoated`|EE.UU. Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`WebCoatedGrade3`|Documento Web Coated SWOP 2006 Grado 3|WebCoatedSWOP2006Grado3.icc| |`WebCoatedGrade5`|Documento Web Coated SWOP 2006 Grado 5|WebCoatedSWOP2006Grado5.icc| |`WebUncoated`|EE.UU. Web Uncovered v2|USWebUncovered.icc|

La siguiente tabla se aplica a *Servicio de imágenes de Dynamic Media Classic* y *Dynamic Media* (se está ejecutando en `dynamicmedia_scene7` modo de ejecución).

|Identificador|Nombre común|Nombre de archivo| |— |— |— | |**RGB**||| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|RGB de Apple|AppleRGB.icc| |`CIERGB|CIE RGB`|CIERGB.icc| |`ColorMatchRGB`|RGB ColorMatch|ColorMatchRGB.icc| |`NTSC`|NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto RGB`|RGB ProPhoto|RGB ProPhoto.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm| |`WideGamutRGB`|RGB de gama amplia|WideGamutRGB.icc| |**CMYK**||| |`CoatedFogra27`|FOGRA27 recubierto (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|FOGRA39 recubierto (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|Europa ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc| |`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale Uncovered v2|EuroscaleUncovered.icc| |`JapanColorCoated`|Color japonés 2001 recubierto|Color japonés2001recubierto.icc| |`JapanColorNewspaper`|Diario japonés color 2002|JapanColor2002Newspaper.icc| |`JapanColorUncoated`|Color japonés 2001 sin recubrir|Color japonés2001Sin recubrir.icc| |`Japan Color 2003 Web Coated`|Color japonés 2003 Web recubierto|Color japonés2003WebCoated.icc| |`JapanWebCoated`|Japón Web Coated (Ad)|JapónWebCoated.icc| |`PS4Default`|CMYK predeterminado de Photoshop 4|Photoshop4DefaultCMYK.icc| |`PS5Default`|CMYK predeterminado de Photoshop 5|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|EE.UU. Captura de hojas v2|USSheetfeedCoated.icc| |`SheetfedUncoated`|EE.UU. Captura de pantalla v2 no recubierto|USSheetfeedUncovered.icc| |`UncoatedFogra29`|FOGRA29 no recubierto (ISO 12647-2:2004)|UncoveredFOGRA29.icc| |`US Newsprint (SNAP 2007)`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc| |`WebCoated`|EE.UU. Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`Web Coated SWOP 2006 Grade 3 Paper`|Documento Web Coated SWOP 2006 Grado 3|WebCoatedSWOP2006Grado3.icc| |`Web Coated SWOP Grade 5 Paper`|Documento Web Coated SWOP 2006 Grado 5|WebCoatedSWOP2006Grado5.icc| |`WebUncoated`|EE.UU. Web Uncovered v2|USWebUncovered.icc|

## Véase también {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [atributo::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [atributo::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [atributo::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [Referencia de mapa de perfil ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
