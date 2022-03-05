---
description: El servicio de imágenes admite archivos de gráficos vectoriales escalables (SVG) como datos de origen. Se requiere conformidad con el SVG 1.1.
solution: Experience Manager
title: asistencia al SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# asistencia al SVG{#svg-support}

El servicio de imágenes admite archivos de gráficos vectoriales escalables (SVG) como datos de origen. Se requiere conformidad con el SVG 1.1.

Image Serving solo reconoce el contenido estático del SVG; no se admiten animaciones, secuencias de comandos y otros contenidos interactivos.

Se puede especificar el SVG siempre que se permitan los archivos de imagen (ruta URL, `src=`y `mask=`). Una vez rasterizado el contenido del archivo SVG, se gestiona como una imagen.

De forma similar a las imágenes, los archivos de SVG se pueden especificar como entradas de catálogo de imágenes o como rutas de archivo relativas.

## Variables de sustitución {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` las variables de sustitución pueden incluirse en el archivo SVG en las cadenas de valor `<text>` elementos y cualquier atributo de elemento.

Las variables importantes de la parte de consulta de las solicitudes incrustadas de Image Serving no se sustituyen directamente. En su lugar, todas las definiciones de variables disponibles se anexan a la solicitud, lo que permite que el servicio de imágenes sustituya las variables al analizar la solicitud.

Consulte [Variables de sustitución](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) para obtener más información.

## Referencias de imágenes {#section-a7680f9e6aca4b1a83560637cc9fac66}

Las imágenes pueden insertarse en el SVG mediante la función `<image>` elemento. Imágenes a las que hace referencia el `xlink::href` del `<image>` debe ser una solicitud de servicio de imágenes válida. No se permiten direcciones URL externas.

Especifique una solicitud completa de servicio de imágenes, empezando por `http://`, o una dirección URL relativa, comenzando por `/is/image`. Si se especifica una ruta HTTP completa, el nombre de dominio se elimina de la ruta para convertirse al formato relativo. El uso de una ruta HTTP completa puede ser una ventaja, ya que permite obtener una vista previa del archivo con un procesador de SVG de terceros.

>[!NOTE]
>
>La compatibilidad con el procesamiento de imágenes en esta versión de Image Serving es limitada. La referencia a imágenes desde dentro de un SVG solo debe utilizarse en situaciones en las que las capas y los mecanismos de creación de plantillas tradicionales de Image Serving sean insuficientes para lograr el resultado deseado. En ningún caso debe utilizarse el SVG para generar compositos de varias imágenes.

>[!NOTE]
>
>Las imágenes incrustadas en el SVG no cambian de tamaño automáticamente en este momento. Asegúrese de que todas las referencias de imagen incluyan los comandos de Image Serving necesarios para establecer el tamaño de imagen deseado (p. ej. `wid=`). Si el tamaño de la imagen no está establecido explícitamente, `attribute::DefaultPix` se aplica.

## Gestión de color {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Se supone que todos los valores de color incrustados en archivos de SVG y pasados a plantillas de SVG mediante variables de sustitución existen en la variable `sRgb` espacio de color.

No se realiza ninguna conversión de color cuando las imágenes están incrustadas en el SVG. Para garantizar la fidelidad de color, asegúrese de especificar `icc=sRgb` para todas las solicitudes de imagen incrustadas.

Después de la rasterización, la imagen del SVG participa en la gestión de color como cualquier otra imagen.

## Ejemplo {#section-036cdd45abd449849ee00a8f21788c28}

La siguiente plantilla de SVG ilustra las referencias de imágenes y el uso de variables.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Esta plantilla de SVG puede usarse de la siguiente manera:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restricciones {#section-daa5eccd07204aaf993be41e87822d54}

Los archivos de SVG deben ser independientes y no deben hacer referencia a ningún archivo o recurso secundario, a excepción de las imágenes externas a las que se hace referencia en las solicitudes de servicio de imágenes o representación de imágenes (véase más arriba).

Solo se representa el contenido estático. Animación, funciones interactivas, como botones, etc. puede estar presente, pero no puede procesarse como se espera.

Las especificaciones de color basadas en perfiles ICC no son compatibles en este momento.

`<script>` pueden estar presentes, pero siempre se ignoran.

## Véase también {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Especificación del SVG 1.1](https://www.w3.org/TR/SVG11/)
