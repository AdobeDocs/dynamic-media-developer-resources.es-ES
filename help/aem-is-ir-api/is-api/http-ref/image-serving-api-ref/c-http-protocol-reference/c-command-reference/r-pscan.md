---
description: Análisis progresivo JPEG. JPEG progresivo muestra una imagen de tal manera que inicialmente muestra una foto borrosa/de baja calidad en su totalidad. A medida que continúa el análisis, se vuelve más claro a medida que los datos de la imagen se descargan de forma más completa. Este parámetro le permite establecer el número de exploraciones que necesita (3, 4 o 5) para que aparezca toda la imagen.
solution: Experience Manager
title: pscan
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 2%

---

# pscan{#pscan}

Análisis progresivo JPEG. JPEG progresivo muestra una imagen de tal manera que inicialmente muestra una foto borrosa/de baja calidad en su totalidad. A medida que continúa el análisis, se vuelve más claro a medida que los datos de la imagen se descargan de forma más completa. Este parámetro le permite establecer el número de exploraciones que necesita (3, 4 o 5) para que aparezca toda la imagen.

`pscan=auto|3|4|5`

La velocidad real de cada escaneo depende de la velocidad de transmisión del sistema del usuario y del ordenador que recibe y descomprime los datos.

`Auto` utiliza la configuración de exploración calculada por la biblioteca JPEG independiente y depende del modelo de color. Los valores de `3`, `4`, `5` corresponden a la configuración de análisis que se encuentra en Adobe Photoshop al guardar un archivo JPEG como pjpeg (JPEG progresivo).

Si `pscan` no está establecido, el valor predeterminado es `auto`.

## Propiedades {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se omite si el formato de salida no es JPEG progresivo.

## Predeterminado {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Ejemplo {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Véase también {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
