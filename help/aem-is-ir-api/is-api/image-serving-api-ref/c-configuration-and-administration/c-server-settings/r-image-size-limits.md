---
description: Utilice esta configuración del servidor para establecer los límites de tamaño de la imagen.
seo-description: Utilice esta configuración del servidor para establecer los límites de tamaño de la imagen.
seo-title: Límites de tamaño de imagen
solution: Experience Manager
title: Límites de tamaño de imagen
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Límites de tamaño de imagen{#image-size-limits}

Utilice esta configuración del servidor para establecer los límites de tamaño de la imagen.

## IS::MaxMessageSize - Límite de tamaño de respuesta {#section-bd942385d4d144cd904003695d72c85e}

Limita el tamaño de los datos que el servidor de imágenes puede enviar al servidor de Platform. En la práctica, esto limita el tamaño de la imagen de respuesta codificada/comprimida que Image Serving puede devolver al cliente a través de HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Límite de tamaño de imagen de salida {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita el tamaño de las imágenes que puede producir el servidor de imágenes (excluidas las imágenes guardadas en el archivo). Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si una operación de renderización supera el límite de tamaño. El valor predeterminado es 16.

## IS::MaxSavePixels - Límite de tamaño para guardar en archivos {#section-d1547c4afa88467080ab08356f775e06}

Limita el tamaño de las imágenes que el Image Server escribirá en los archivos con el comando `req=saveToFile`. Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si la operación de guardado de archivos supera ese límite. El valor predeterminado es de 100 millones de píxeles.

## IS::MaxNonDsfSize - Límite de tamaño para imágenes de entrada que no sean PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

El tamaño máximo (en píxeles) de imágenes que no son PTIFF que el servidor de imágenes puede abrir. El servicio de imágenes devolverá un error cuando se intente acceder a una imagen que no sea de PTIFF y que supere este límite.

>[!NOTE]
>
>Si establece este valor demasiado alto, puede causar que el servidor de imágenes se vea privado de memoria y provocar errores, incluidos bloqueos.

