---
title: pscan
description: Análisis progresivo de JPEG. Progressive JPEG muestra una imagen de tal manera que inicialmente muestra una fotografía borrosa o de baja calidad en su totalidad.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
TQID: 'https://experienceleague.adobe.com/NhxrMkCLJuVcoakGVk7akMWm6Po9a-CSSegTqHLXMbo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 2%

---

# pscan{#pscan}

Análisis progresivo de JPEG. Progressive JPEG muestra una imagen de tal manera que inicialmente muestra una fotografía borrosa o de baja calidad en su totalidad. A medida que el escaneo continúa, se vuelve más claro a medida que los datos de la imagen se descargan más completamente. Este parámetro permite definir el número de análisis que se deben realizar (3, 4 o 5) para que aparezca toda la imagen.

`pscan=auto|3|4|5`

La velocidad real de cada análisis depende de la velocidad de transmisión del sistema del usuario y del equipo que recibe y descomprime los datos.

`Auto` utiliza la configuración de digitalización calculada por la biblioteca independiente de JPEG y depende del modelo de color. Los valores de `3`, `4`, `5` corresponden a la configuración de análisis encontrada en Adobe Photoshop al guardar un archivo JPEG como pjpeg (JPEG progresivo).

Si `pscan` no está establecido, el valor predeterminado es `auto`.

## Propiedades {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se ignora si el formato de salida no es JPEG progresivo.

## Predeterminado {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Ejemplo {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Véase también {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
