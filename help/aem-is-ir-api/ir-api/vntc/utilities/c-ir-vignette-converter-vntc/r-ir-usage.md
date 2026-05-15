---
title: Uso
description: Este tema describe la sintaxis de uso de vntc.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
TQID: 'https://experienceleague.adobe.com/uNh-n1OEJ5gxWBjLbBNutrNJ1Osae-PEOFBmaKNVf6c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 1%

---

# Uso{#usage}

Este tema describe la sintaxis de uso de vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* es la ruta y el nombre del archivo que se va a procesar. Puede ser una ruta relativa al directorio de trabajo actual o una ruta absoluta. Debe ser una viñeta, un estilo de archivador o un archivo de estilo de recubrimiento de ventana válido y tener uno de los siguientes sufijos:

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

Obligatorio.

*[!DNL destFile]* es la ruta de acceso y el nombre del archivo de viñeta de salida. Si no se especifica, el archivo de salida se coloca en la carpeta especificada con `-destpath`. En esta situación, el nombre de archivo se genera automáticamente a partir del nombre del archivo de entrada y un sufijo de tamaño, separados por la cadena especificada por `-separator`. En el caso de las viñetas, el sufijo de tamaño es la anchura en píxeles de la viñeta de salida de una sola resolución, la anchura de la primera vista de una viñeta de salida de varias resoluciones o &quot;0&quot; si hay una viñeta piramidal. Para archivos de estilo de archivador, la resolución de salida se utiliza como sufijo de archivo. *[!DNL destFile]* se omite cuando se especifica `-info`.
