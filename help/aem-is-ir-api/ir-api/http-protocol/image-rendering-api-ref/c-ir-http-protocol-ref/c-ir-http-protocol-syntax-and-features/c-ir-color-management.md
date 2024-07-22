---
description: El procesamiento de imágenes admite conversiones del espacio de color basadas en perfiles del espacio de color que se ajustan a la especificación ICC (International Color Consortium).
solution: Experience Manager
title: Administración de color de procesamiento de imágenes *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# Administración de color de procesamiento de imágenes *{#image-rendering-color-management}

El procesamiento de imágenes admite conversiones del espacio de color basadas en perfiles del espacio de color que se ajustan a la especificación ICC (International Color Consortium).

**Restricciones**

En este momento solo se admiten espacios de color CMYK, RGB y de escala de grises.

Los archivos de estilo de los contenedores (.vnc) y los archivos de estilo de las cubiertas de las ventanas ( [!DNL .vnw]) no se administran por colores y se supone que existen en el espacio de color de trabajo.

**Ver también**

[Consorcio Internacional del Color](https://www.color.org/index.xalter) , [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , Mapas de perfil ICC

## Espacios de color predeterminados {#section-8ce27edf42e746febe4654f8f19b9c0c}

Cada catálogo de imágenes (y el catálogo predeterminado) puede definir un conjunto de perfiles ICC. Estos perfiles constituyen los espacios de color predeterminados para este catálogo: un perfil de entrada y uno de salida para los datos de escala de grises, RGB y CMYK ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` y `attribute::IccProfileSrcCmyk`).

El espacio de color predeterminado para una imagen u otro objeto concreto se selecciona de los perfiles predeterminados del catálogo en función del tipo de píxel de la imagen.

## Espacio de color de entrada {#section-660f661a7e954df4b451e34134195276}

Las imágenes de material pueden incrustar perfiles ICC para definir el espacio de color de entrada. Si no hay ningún perfil incrustado en una imagen de origen, se utiliza `attribute::IccProfileSrc*` del catálogo de imágenes aplicable correspondiente al tipo de píxel de la imagen de origen. Si este atributo no está definido en el catálogo de imágenes, se utiliza `attribute::IccProfile*`. Si ese atributo de catálogo tampoco está definido, la imagen no se administra con colores y solo se aplican transformaciones naïve.

## Espacio de color de trabajo {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Normalmente, el espacio de color de trabajo se define mediante el perfil de color ICC incrustado en la viñeta. Si la viñeta no incluye un perfil, se utiliza el perfil de entrada predeterminado del RGB ( `attribute::IccProfileSrcRgb` del catálogo de sesiones) para el espacio de color de trabajo.

Todas las operaciones de procesamiento se ejecutan en el espacio de color de trabajo.

**Importante:** El perfil ICC para el espacio de color de trabajo debe admitir transformaciones de entrada y salida. Si se utiliza un perfil de sólo salida como espacio de color de trabajo, IR no puede convertir materiales en él. Este perfil de color podrá seguir utilizándose si existen materiales en el mismo espacio de color de trabajo. Error al intentar aplicar materiales en otros espacios de color.

## Valores de color explícitos {#section-31727bf1b23e477ca92572fbbf422d2f}

Se supone que los valores de color de RGB especificados con `color=`, `bgc=`, `catalog::BgColor` y `catalog::Color` existen en el espacio de color de trabajo actual.

## Archivos de datos de material {#section-33f7a170a6664c02b8479fb89cc0aea3}

Los archivos de imagen de material (imágenes de textura y calcomanía) pueden tener un tipo de píxel RGB, de escala de grises o CMYK y pueden incrustar un perfil de color. Si no hay ningún perfil de color incrustado, el espacio de color de entrada predeterminado se asocia a la imagen (por ejemplo, el perfil de color del catálogo de materiales que corresponde al tipo de píxel de la imagen).

Las imágenes materiales obtenidas de las solicitudes anidadas de servicio o procesamiento de imágenes suelen incluir un perfil de color. Si no es así, las imágenes se asocian al espacio de color de entrada predeterminado correspondiente al tipo de píxel.

Si el espacio de color del archivo de imagen es diferente del espacio de color de trabajo, se utiliza una conversión de color precisa para convertirlo al espacio de color de trabajo. La conversión de tipo nativa se utiliza cuando no hay ningún perfil incrustado ni se define ningún perfil de entrada predeterminado.

Otros archivos de datos de material, como los archivos de estilo de archivador ( [!DNL .vnc]) o los archivos de cobertura de ventana ( [!DNL .vnw]) no incrustan perfiles de color y siempre se supone que están en el espacio de color de trabajo.

## Espacio de color de salida {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Todas las operaciones de procesamiento tienen lugar en el espacio de color de trabajo. Si la solicitud especifica un perfil de color diferente con el comando `icc=`, los datos se convierten a ese espacio de color justo antes de codificarse y devolverse al cliente. Cuando la gestión de color está desactivada, se utiliza la conversión naïve si es necesario para convertir a escala de grises o CMYK.

## Perfiles de color incrustados {#section-5ff733832d38429fbe02b3c1e9bb94a9}

El perfil de color asociado con la imagen procesada se puede incrustar en la imagen de respuesta especificando `iccEmbed=` para la solicitud.

Si no se especifica `icc=`, se incrusta el perfil ICC para el espacio de color de trabajo. No hay ningún perfil incrustado si la administración de color está deshabilitada y no se especificó ningún perfil con `icc=`.

## Perfiles ICC {#section-afeb76068b5042adb83261638e450140}

Todos los perfiles de color utilizados por el servidor deben cumplir con la especificación ICC. Los archivos de perfil ICC suelen tener un sufijo de archivo [!DNL .icc] o [!DNL .icm] y se ubican con archivos de datos de material.

Aunque los perfiles de salida se pueden especificar por ruta/nombre de archivo en el comando `icc=`, se recomienda registrar todos los archivos de perfil en el mapa de perfiles ICC del catálogo predeterminado o de un catálogo de materiales específico y utilizar identificadores de acceso directo ( `icc::Name`) en lugar de rutas de archivo.

Los perfiles de trabajo deben registrarse en el mapa de perfiles ICC del catálogo de materiales o del catálogo predeterminado.
