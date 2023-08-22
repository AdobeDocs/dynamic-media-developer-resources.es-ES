---
title: pscan
description: Análisis progresivo del JPEG. El JPEG progresivo muestra una imagen de tal manera que inicialmente muestra una fotografía borrosa o de baja calidad en su totalidad.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# pscan{#pscan}

Análisis progresivo del JPEG. El JPEG progresivo muestra una imagen de tal manera que inicialmente muestra una fotografía borrosa o de baja calidad en su totalidad. A medida que el escaneo continúa, se vuelve más claro a medida que los datos de la imagen se descargan más completamente. Este parámetro permite definir el número de análisis que se deben realizar (3, 4 o 5) para que aparezca toda la imagen.

`pscan=auto|3|4|5`

La velocidad real de cada análisis depende de la velocidad de transmisión del sistema del usuario y del equipo que recibe y descomprime los datos.

`Auto` utiliza la configuración de escaneo calculada por la biblioteca de JPEG independiente y depende del modelo de color. Los valores de `3`, `4`, `5` corresponde a la configuración Análisis que se encuentra en Adobe Photoshop al guardar un archivo de JPEG como pjpeg (JPEG progresivo).

If `pscan` no se ha definido, el valor predeterminado es `auto`.

## Propiedades {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se ignora si el formato de salida no es un JPEG progresivo.

## Predeterminado {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Ejemplo {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Véase también {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
