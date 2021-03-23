---
description: El procesamiento de imágenes admite conversiones de espacio de color basadas en perfiles de espacio de color que se ajustan a la especificación ICC (International Color Consortium).
seo-description: El procesamiento de imágenes admite conversiones de espacio de color basadas en perfiles de espacio de color que se ajustan a la especificación ICC (International Color Consortium).
seo-title: Gestión de color de renderización de imágenes *
solution: Experience Manager
title: Gestión de color de renderización de imágenes *
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---


# Gestión de color de renderización de imágenes *{#image-rendering-color-management}

El procesamiento de imágenes admite conversiones de espacio de color basadas en perfiles de espacio de color que se ajustan a la especificación ICC (International Color Consortium).

**Restricciones**

En este momento solo se admiten los espacios de color CMYK, RGB y escala de grises.

Los archivos de estilo de gabinete (.vnc) y los archivos de estilo de cubiertas de ventanas ( [!DNL .vnw]) no se administran con colores y se supone que existen en el espacio de color de trabajo.

**Véase también**

[International Color Consortium](http://www.color.org/index.xalter) ,  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*` ,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent` ,  `attribute::IccBlackPointCompensation` ,  `attribute::IccDither` , Mapas de perfiles ICC

## Espacios de color predeterminados {#section-8ce27edf42e746febe4654f8f19b9c0c}

Cada catálogo de imágenes (y el catálogo predeterminado) puede definir un conjunto de perfiles ICC. Estos perfiles constituyen los espacios de color predeterminados para este catálogo: una entrada y un perfil de salida para datos de escala de grises, RGB y CMYK ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` y `attribute::IccProfileSrcCmyk`).

El espacio de color predeterminado para una imagen en particular u otro objeto se selecciona de los perfiles predeterminados del catálogo en función del tipo de píxel de la imagen.

## Espacio de color de entrada {#section-660f661a7e954df4b451e34134195276}

Las imágenes de material pueden incrustar perfiles ICC para definir el espacio de color de entrada. Si no hay ningún perfil incrustado en una imagen de origen, se utilizará `attribute::IccProfileSrc*` del catálogo de imágenes correspondiente al tipo de píxel de la imagen de origen. Si este atributo no está definido en el catálogo de imágenes, se utiliza `attribute::IccProfile*`. Si el atributo de catálogo tampoco está definido, la imagen no se administra con colores y solo se aplican transformaciones naïve.

## Espacio de color de trabajo {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Normalmente, el espacio de color de trabajo se define mediante el perfil de color ICC incrustado en la viñeta. Si la viñeta no incluye un perfil, el perfil de entrada RGB predeterminado ( `attribute::IccProfileSrcRgb` del catálogo de sesiones) se utiliza para el espacio de color de trabajo.

Todas las operaciones de renderización se ejecutan en el espacio de color de trabajo.

**Importante:** El perfil ICC para el espacio de color de trabajo debe admitir transformaciones de entrada y salida. Si se utiliza un perfil de sólo salida como espacio de color de trabajo, IR no podrá convertir materiales en él. Este perfil de color puede seguir utilizándose si los materiales existen en el mismo espacio de trabajo. No se podrá aplicar el material en otros espacios de color.

## Valores de color explícitos {#section-31727bf1b23e477ca92572fbbf422d2f}

Se supone que los valores de color RGB especificados con `color=`, `bgc=`, `catalog::BgColor` y `catalog::Color` existen en el espacio de color de trabajo actual.

## Archivos de datos de material {#section-33f7a170a6664c02b8479fb89cc0aea3}

Los archivos de imagen de material (imágenes de textura y calco) pueden tener un tipo de píxel RGB, escala gris o CMYK y pueden incrustar un perfil de color. Si no hay ningún perfil de color incrustado, el espacio de color de entrada predeterminado se asocia a la imagen (por ejemplo, el perfil de color del catálogo de materiales que corresponde al tipo de píxel de la imagen).

Las imágenes de material obtenidas de solicitudes anidadas de Image Serving o Image Rendering suelen incluir un perfil de color. Si no es así, las imágenes se asocian con el espacio de color de entrada predeterminado correspondiente al tipo de píxel.

Si el espacio de color del archivo de imagen es diferente al espacio de color de trabajo, se utiliza la conversión de color precisa para convertir al espacio de color de trabajo. La conversión de tipo no previo se utiliza cuando no hay ningún perfil incrustado y no se define ningún perfil de entrada predeterminado.

Otros archivos de datos de material, como los archivos de estilo de archivador ( [!DNL .vnc]) o los archivos de cubierta de ventanas ( [!DNL .vnw]) no incrustan perfiles de color y siempre se supone que están en el espacio de color de trabajo.

## Espacio de color de salida {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Todas las operaciones de renderización se realizan en el espacio de color de trabajo. Si la solicitud especifica un perfil de color diferente con el comando `icc=`, los datos se convertirán a ese espacio de color justo antes de que se codifique y se devuelvan al cliente. Cuando se deshabilita la gestión del color, se utiliza la conversión ingenua si es necesario para convertir a escala de grises o CMYK.

## Perfiles de color incrustados {#section-5ff733832d38429fbe02b3c1e9bb94a9}

El perfil de color asociado con la imagen representada se puede incrustar en la imagen de respuesta especificando `iccEmbed=` para la solicitud.

Si no se especifica `icc=`, se incrusta el perfil ICC para el espacio de color de trabajo. No hay ningún perfil incrustado si la administración de color está deshabilitada y no se especificó ningún perfil con `icc=`.

## Perfiles ICC {#section-afeb76068b5042adb83261638e450140}

Todos los perfiles de color utilizados por el servidor deben cumplir la especificación ICC. Los archivos de perfil ICC generalmente tienen un sufijo de archivo [!DNL .icc] o [!DNL .icm] y se ubican junto con archivos de datos de material.

Aunque los perfiles de salida se pueden especificar por ruta/nombre de archivo en el comando `icc=`, se recomienda registrar todos los archivos de perfil en el mapa de perfil ICC del catálogo predeterminado o en un catálogo de material específico y utilizar identificadores de acceso directo ( `icc::Name`) en lugar de rutas de archivo.

Los perfiles de trabajo deben estar registrados en el mapa de perfiles ICC del catálogo de materiales o del catálogo predeterminado.
