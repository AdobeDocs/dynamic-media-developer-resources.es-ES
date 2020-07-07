---
description: El servicio de imágenes admite archivos de gráficos vectoriales escalables (SVG) como datos de origen. Se requiere la conformidad con SVG 1.1.
seo-description: El servicio de imágenes admite archivos de gráficos vectoriales escalables (SVG) como datos de origen. Se requiere la conformidad con SVG 1.1.
seo-title: Compatibilidad con SVG
solution: Experience Manager
title: Compatibilidad con SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# Compatibilidad con SVG{#svg-support}

El servicio de imágenes admite archivos de gráficos vectoriales escalables (SVG) como datos de origen. Se requiere la conformidad con SVG 1.1.

El servicio de imágenes solo reconoce el contenido SVG estático; no se admiten animaciones, secuencias de comandos y otros contenidos interactivos.

Se puede especificar SVG siempre que se permitan los archivos de imagen (ruta de URL, `src=`y `mask=`). Después de rasterizar el contenido del archivo SVG, se gestiona como una imagen.

De forma similar a las imágenes, los archivos SVG se pueden especificar como entradas de catálogo de imágenes o como rutas de archivos relativas.

## Variables de sustitución {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` las variables de sustitución pueden incluirse en el archivo SVG en los elementos de cadenas de valor `<text>` y en cualquier atributo de elemento.

Las variables importantes de la parte de consulta de las solicitudes incrustadas de servicio de imágenes no se sustituyen directamente. En su lugar, todas las definiciones de variables disponibles se anexan a la solicitud, lo que permite que el servicio de imágenes reemplace las variables al analizar la solicitud.

Consulte Variables [de sustitución](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) para obtener información adicional.

## Referencias de imagen {#section-a7680f9e6aca4b1a83560637cc9fac66}

Las imágenes se pueden insertar en SVG mediante el `<image>` elemento . Las imágenes a las que hace referencia el `xlink::href` atributo del `<image>` elemento deben ser solicitudes válidas de servicio de imágenes. No se permiten direcciones URL extranjeras.

Especifique una solicitud de servicio de imágenes completa, comenzando por `http://`o una dirección URL relativa, comenzando por `/is/image`. Si se especifica una ruta HTTP completa, el nombre de dominio se eliminará de la ruta para convertirlo al formato relativo. El uso de una ruta HTTP completa puede resultar ventajoso, ya que permite previsualizar el archivo con un procesador SVG de terceros.

>[!NOTE]
>
>La compatibilidad con el procesamiento de imágenes en esta versión del servicio de imágenes es limitada. Las imágenes de referencia desde SVG solo se deben usar en situaciones en las que los mecanismos tradicionales de creación de capas y plantillas del servicio de imágenes no sean suficientes para lograr el resultado deseado. Bajo ninguna circunstancia debe utilizarse SVG para generar composiciones de varias imágenes.

>[!NOTE]
>
>Las imágenes incrustadas en SVG no cambian de tamaño automáticamente en este momento. Asegúrese de que todas las referencias de imagen incluyen los comandos de servicio de imágenes necesarios para definir el tamaño de imagen deseado (p. ej. `wid=`). Si el tamaño de la imagen no se establece explícitamente, se aplicará `attribute::DefaultPix` .

## Color management {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Se supone que todos los valores de color incrustados en archivos SVG y pasados a plantillas SVG mediante variables de sustitución existen en el espacio de `sRgb` color.

No se realiza ninguna conversión de color cuando las imágenes se incrustan en el SVG. Para garantizar la fidelidad del color, asegúrese de especificar `icc=sRgb` para todas las solicitudes de imagen incrustadas.

Después de la rasterización, la imagen SVG participa en la gestión de color como cualquier otra imagen.

## Ejemplo {#section-036cdd45abd449849ee00a8f21788c28}

La siguiente plantilla SVG ilustra las referencias de imagen y el uso de variables.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Esta plantilla SVG puede utilizarse de la siguiente manera:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

Los archivos SVG deben ser independientes y no deben hacer referencia a ningún archivo o recurso secundario, a excepción de las imágenes externas a las que se hace referencia con solicitudes de servicio de imágenes o de procesamiento de imágenes (véase más arriba).

Solo se representa el contenido estático. Animación, funciones interactivas, como botones, etc. puede estar presente pero no puede procesarse como se espera.

Las especificaciones de color basadas en perfil ICC no son compatibles en este momento.

`<script>` los elementos pueden estar presentes pero siempre se omiten.

## Véase también {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), especificación [SVG 1.1](http://www.w3.org/TR/SVG11/)
