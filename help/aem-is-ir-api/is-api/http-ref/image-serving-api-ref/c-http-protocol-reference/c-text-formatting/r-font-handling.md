---
description: Todas las fuentes a las que se hace referencia en la cadena RTF deben estar disponibles en el archivo de asignación de fuentes del catálogo predeterminado o del catálogo de imágenes actual; de lo contrario, se mostrará un error.
seo-description: Todas las fuentes a las que se hace referencia en la cadena RTF deben estar disponibles en el archivo de asignación de fuentes del catálogo predeterminado o del catálogo de imágenes actual; de lo contrario, se mostrará un error.
seo-title: Gestión de fuentes
solution: Experience Manager
title: Gestión de fuentes
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Gestión de fuentes{#font-handling}

Todas las fuentes a las que se hace referencia en la cadena RTF deben estar disponibles en el archivo de asignación de fuentes del catálogo predeterminado o del catálogo de imágenes actual; de lo contrario, se mostrará un error.

La mejor calidad para el texto en cursiva y negrita se logra registrando los archivos de fuente correspondientes. Si no está disponible, el servidor puede sintetizar las caras de fuente negrita y/o cursiva desde la cara estándar. (Véase ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

La cara de fuente especificada con `attribute::DefaultFont` se utiliza cuando no se especifica ninguna en la cadena RTF.

El servicio de imágenes admite fuentes TrueType, OpenType, Adobe Type 1 (solo Windows).

## Compatibilidad con fuentes Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` admite fuentes Photofont®, con las siguientes restricciones:

* `\cf` se ignora en los espacios de texto que especifican una fuente Photofont; Las caras de fuente de fotofuente tienen colores predefinidos
* No se admiten estilos de fuente sintetizados; uso de `\b` y `\i`requerir las entradas correspondientes de asignación de fuentes; de lo contrario, se devuelve un error

* No se admite el flujo de texto vertical
* No se admiten fuentes de fuentes fotográficas con imágenes de 16 bits
* No se admiten fuentes de fuente fotográfica con varios glifos por imagen
* Se aplica la conversión de color naive a menos que las imágenes de glifo de Photofont incorporen perfiles de color; en este caso, siempre se aplican la interpretación colorimétrica relativa y la compensación de punto negro

Consulte ` [www.photofont.com](http://www.photofont.com)` para obtener información adicional.

## Véase también {#section-6cb8a802aa044836bbe449d559093f3a}

[Referencia](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)de mapa de fuente, [atributo::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [atributo::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](http://www.photofont.com)
