---
title: Administración de fuentes
description: Todas las fuentes a las que se hace referencia en la cadena RTF deben estar disponibles en el archivo de mapa de fuentes del catálogo predeterminado o del catálogo de imágenes actual; de lo contrario, se devuelve un error.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Administración de fuentes{#font-handling}

Todas las fuentes a las que se hace referencia en la cadena RTF deben estar disponibles en el archivo de mapa de fuentes del catálogo predeterminado o del catálogo de imágenes actual; de lo contrario, se devuelve un error.

La mejor calidad para el texto en cursiva y en negrita se logra registrando los archivos de fuente correspondientes. Si no está disponible, el servidor puede sintetizar las caras de fuente en negrita y/o cursiva desde la cara estándar. (Consulte [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

La fuente especificada con `attribute::DefaultFont` se utiliza cuando no se especifica ninguno explícitamente en la cadena RTF.

El servicio de imágenes admite fuentes TrueType, OpenType y Adobe Type 1 (solo Windows).

## Compatibilidad con fuentes Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` admite fuentes Photofont®, con las restricciones siguientes:

* `\cf` se omite en los espacios de texto que especifican una fuente Photofont; las caras de fuente Photofont tienen colores predefinidos
* No se admiten estilos de fuente sintetizados; uso de `\b` y `\i`requerir las entradas de mapa de fuentes correspondientes; de lo contrario, se devuelve un error

* No se admite el flujo de texto vertical
* No se admiten fuentes de fuentes fotográficas con imágenes de 16 bits
* No se admiten fuentes de fuentes fotográficas con varios glifos por imagen
* La conversión de color nativa se aplica a menos que las imágenes de glifo de Photofont incrusten perfiles de color; en este caso, siempre se aplican la interpretación colorimétrica relativa y la compensación de punto negro

Consulte [www.photofont.com](https://www.photofont.com) para obtener más información.

## Véase también {#section-6cb8a802aa044836bbe449d559093f3a}

[Referencia de mapa de fuentes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::FuentePredeterminada](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](https://www.photofont.com)
