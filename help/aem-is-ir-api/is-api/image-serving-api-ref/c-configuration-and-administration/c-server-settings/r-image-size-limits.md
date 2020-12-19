---
description: Utilice esta configuración del servidor para establecer los límites de tamaño de la imagen.
seo-description: Utilice esta configuración del servidor para establecer los límites de tamaño de la imagen.
seo-title: Límites de tamaño de imagen
solution: Experience Manager
title: Límites de tamaño de imagen
topic: Scene7 Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Límites de tamaño de imagen{#image-size-limits}

Utilice esta configuración del servidor para establecer los límites de tamaño de la imagen.

## IS::MaxMessageSize - Límite de tamaño de respuesta {#section-bd942385d4d144cd904003695d72c85e}

Limita el tamaño de los datos que el servidor de imágenes puede enviar al servidor de plataforma. De hecho, esto limita el tamaño de la imagen de respuesta codificada/comprimida que el servicio de imágenes puede devolver al cliente mediante HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Límite de tamaño de imagen de salida {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita el tamaño de las imágenes que puede producir el servidor de imágenes (excluyendo las imágenes guardadas en el archivo). Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si una operación de procesamiento supera el límite de tamaño. El valor predeterminado es 16.

## IS::MaxSavePixels - Límite de tamaño para guardar en archivos {#section-d1547c4afa88467080ab08356f775e06}

Limita el tamaño de las imágenes que el servidor de imágenes escribirá en los archivos con el comando `req=saveToFile`. Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si la operación de guardado de archivos supera ese límite. El valor predeterminado es 100 millones de píxeles.

## IS::MaxNonDsfSize - Límite de tamaño para imágenes de entrada que no son PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

El tamaño máximo (en píxeles) de las imágenes que no son PTIFF que se permite abrir el servidor de imágenes. El servicio de imágenes devolverá un error cuando se intente acceder a una imagen que no sea PTIFF y que supere este límite.

>[!NOTE]
>
>Si este valor se establece en demasiado alto, puede que el servidor de imágenes se quede sin memoria y se produzcan errores, incluidos bloqueos.

