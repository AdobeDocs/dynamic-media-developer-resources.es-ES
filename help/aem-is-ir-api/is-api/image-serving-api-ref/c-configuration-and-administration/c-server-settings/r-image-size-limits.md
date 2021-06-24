---
description: Utilice esta configuración del servidor para establecer los límites de tamaño de la imagen.
solution: Experience Manager
title: Límites de tamaño de imagen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '234'
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

## IS::MaxNonDsfSize - Límite De Tamaño Para Imágenes De Entrada Que No Sean PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

El tamaño máximo (en píxeles) de imágenes que no son PTIFF que el servidor de imágenes puede abrir. El servicio de imágenes devolverá un error cuando se intente acceder a una imagen que no sea de PTIFF y que supere este límite.

>[!NOTE]
>
>Si establece este valor demasiado alto, puede causar que el servidor de imágenes se vea privado de memoria y provocar errores, incluidos bloqueos.
