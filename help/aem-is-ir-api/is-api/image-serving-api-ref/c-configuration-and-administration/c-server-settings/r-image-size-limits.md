---
description: Utilice esta configuración del servidor para establecer los límites de tamaño de imagen.
solution: Experience Manager
title: Límites de tamaño de imagen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
TQID: 'https://experienceleague.adobe.com/-xOEUXOC5tk9b9miYQWTmC73EsZbSo9Zzn8AedEksEI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# Límites de tamaño de imagen{#image-size-limits}

Utilice esta configuración del servidor para establecer los límites de tamaño de imagen.

## IS::MaxMessageSize: límite de tamaño de respuesta {#section-bd942385d4d144cd904003695d72c85e}

Limita el tamaño de los datos que el servidor de imágenes puede enviar a [!DNL Platform Server]. De hecho, esto limita el tamaño de la imagen de respuesta codificada/comprimida que el servicio de imágenes puede devolver al cliente mediante HTTP (Mbytes).

## IS::MaxRenderRgnPixels: límite de tamaño de imagen de salida {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limita el tamaño de las imágenes que puede producir el servidor de imágenes (excluidas las imágenes guardadas en un archivo). Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si una operación de procesamiento supera el límite de tamaño. El valor predeterminado es 16.

## IS::MaxSavePixels: límite de tamaño para guardar en archivos {#section-d1547c4afa88467080ab08356f775e06}

Limita el tamaño de las imágenes que el servidor de imágenes escribe en los archivos con el comando `req=saveToFile`. Valor entero mayor que 0 en millones de píxeles. Se devuelve un error si la operación de guardar el archivo supera ese límite. El valor predeterminado es 100 millones de píxeles.

## IS::MaxNonDsfSize: Límite de tamaño para imágenes de entrada no PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

El tamaño máximo (en píxeles) de las imágenes que no son PTIFF que el servidor de imágenes puede abrir. El servicio de imágenes devuelve un error cuando se intenta acceder a una imagen que no es PTIFF y que supera este límite.

>[!NOTE]
>
>Si establece este valor demasiado alto, puede que el servidor de imágenes no tenga memoria suficiente y se produzcan errores, incluidos bloqueos.
