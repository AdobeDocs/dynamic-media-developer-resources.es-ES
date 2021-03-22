---
description: Todas las fuentes a las que se hace referencia en la cadena RTF deben estar disponibles en el archivo de asignación de fuentes del catálogo predeterminado o del catálogo de imágenes actual; de lo contrario, se devuelve un error.
seo-description: Todas las fuentes a las que se hace referencia en la cadena RTF deben estar disponibles en el archivo de asignación de fuentes del catálogo predeterminado o del catálogo de imágenes actual; de lo contrario, se devuelve un error.
seo-title: Administración de fuentes
solution: Experience Manager
title: Administración de fuentes
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# Tratamiento de fuentes{#font-handling}

Todas las fuentes a las que se hace referencia en la cadena RTF deben estar disponibles en el archivo de asignación de fuentes del catálogo predeterminado o del catálogo de imágenes actual; de lo contrario, se devuelve un error.

La mejor calidad para el texto en cursiva y negrita se consigue registrando los archivos de fuente correspondientes. Si no está disponible, el servidor puede sintetizar las caras de fuente en negrita o cursiva desde la cara estándar. (Véase ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

La fuente especificada con `attribute::DefaultFont` se utiliza cuando no se especifica ninguna explícitamente en la cadena RTF.

Image Serving es compatible con las fuentes TrueType, OpenType y Adobe Type 1 (solo Windows).

## Compatibilidad con fuentes Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` admite fuentes Photofont®, con las restricciones siguientes:

* `\cf` se ignora en los espacios de texto que especifican una fuente Photofont; Las caras de fuentes fotográficas tienen colores predefinidos
* No se admiten estilos de fuente sintetizados; el uso de `\b` y `\i`requieren las entradas correspondientes del mapa de fuente; de lo contrario, se devuelve un error

* No se admite el flujo de texto vertical
* No se admiten fuentes de fuentes fotográficas con imágenes de 16 bits
* No se admiten fuentes de fuentes fotográficas con varios glifos por imagen
* La conversión de color naive se aplica a menos que las imágenes de glifo de Photofont incrusten perfiles de color; en este caso, siempre se aplican la intención de procesamiento colorimétrico relativo y la compensación de punto negro

Consulte ` [www.photofont.com](http://www.photofont.com)` para obtener más información.

## Véase también {#section-6cb8a802aa044836bbe449d559093f3a}

[Referencia](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d) de mapa de fuente,  [atributo::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [atributo::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
