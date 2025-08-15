---
description: El servicio de imágenes admite archivos de gráficos vectoriales escalables (SVG) como datos de origen. Se requiere la conformidad con SVG 1.1.
solution: Experience Manager
title: Compatibilidad con SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Compatibilidad con SVG{#svg-support}

El servicio de imágenes admite archivos de gráficos vectoriales escalables (SVG) como datos de origen. Se requiere la conformidad con SVG 1.1.

El servicio de imágenes solo reconoce contenido estático de SVG; no se admiten animaciones, scripts ni otro contenido interactivo.

Se puede especificar SVG donde se permitan los archivos de imagen (ruta de acceso de la dirección URL, `src=` y `mask=`). Una vez rasterizado el contenido del archivo SVG, se gestiona como una imagen.

De forma similar a las imágenes, los archivos SVG se pueden especificar como entradas de catálogo de imágenes o como rutas de archivo relativas.

## Variables de sustitución {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` variables de sustitución pueden incluirse en el archivo SVG en los elementos de cadenas de valor `<text>` y en cualquier atributo de elemento.

Las variables importantes en la parte de consulta de las solicitudes del servicio de imágenes incrustadas no se sustituyen directamente. En su lugar, todas las definiciones de variables disponibles se anexan a la solicitud, lo que permite al servicio de imágenes sustituir variables al analizar la solicitud.

Consulte [Variables de sustitución](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) para obtener más información.

## Referencias de imagen {#section-a7680f9e6aca4b1a83560637cc9fac66}

Las imágenes se pueden insertar en SVG usando el elemento `<image>`. Las imágenes a las que hace referencia el atributo `xlink::href` del elemento `<image>` deben ser solicitudes de servicio de imágenes válidas. No se permiten direcciones URL externas.

Especifique una solicitud de servicio de imágenes completa, que comience por `http://`, o una dirección URL relativa, que comience por `/is/image`. Si se especifica una ruta HTTP completa, el nombre de dominio se elimina de la ruta para convertirlo al formato relativo. El uso de una ruta HTTP completa puede ser beneficioso, ya que permite previsualizar el archivo con un procesador SVG de terceros.

>[!NOTE]
>
>La compatibilidad con el procesamiento de imágenes en esta versión del servicio de imágenes es limitada. Las referencias a imágenes desde SVG solo deben utilizarse en situaciones en las que los mecanismos tradicionales de asignación de capas y creación de plantillas del servicio de imágenes no sean suficientes para lograr el resultado deseado. SVG no debe utilizarse en ningún caso para generar composiciones de varias imágenes.

>[!NOTE]
>
>Las imágenes incrustadas en SVG no cambian de tamaño automáticamente en este momento. Asegúrese de que todas las hrefs de imagen incluyan los comandos necesarios del servicio de imágenes para establecer el tamaño de imagen deseado (por ejemplo, `wid=`). Si el tamaño de la imagen no se establece explícitamente, se aplica `attribute::DefaultPix`.

## Gestión de color {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Se supone que todos los valores de color incrustados en archivos SVG y pasados a plantillas de SVG mediante variables de sustitución existen en el espacio de color `sRgb`.

No se realiza ninguna conversión de color cuando las imágenes están incrustadas en SVG. Para garantizar la fidelidad del color, asegúrese de especificar `icc=sRgb` para todas las solicitudes de imagen incrustadas.

Después de la rasterización, la imagen de SVG participa en la administración de color como cualquier otra imagen.

## Ejemplo {#section-036cdd45abd449849ee00a8f21788c28}

La siguiente plantilla de SVG ilustra las referencias de imagen y el uso de variables.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Esta plantilla de SVG se puede utilizar de la siguiente manera:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restricciones {#section-daa5eccd07204aaf993be41e87822d54}

Los archivos SVG deben ser independientes y no deben hacer referencia a ningún archivo o recurso secundario, excepto a las imágenes externas a las que se hace referencia con solicitudes de servicio o procesamiento de imágenes (ver arriba).

Solo se procesa el contenido estático. Animación, funciones interactivas, como botones, etc. puede estar presente, pero no procesarse según lo esperado.

Las especificaciones de color basadas en perfiles ICC no son compatibles en este momento.

`<script>` elementos pueden estar presentes, pero siempre se omiten.

## Véase también {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [máscara=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [especificación de SVG 1.1](https://www.w3.org/TR/SVG11/)
