---
title: Uso
description: Este tema describe la sintaxis de uso de vntc.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '158'
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

*[!DNL destFile]* es la ruta y el nombre del archivo de viñeta de salida. Si no se especifica, el archivo de salida se coloca en la carpeta especificada con `-destpath`. En esta situación, el nombre de archivo se genera automáticamente a partir del nombre del archivo de entrada y un sufijo de tamaño, separados por la cadena especificada por `-separator`. En el caso de las viñetas, el sufijo de tamaño es la anchura en píxeles de la viñeta de salida de una sola resolución, la anchura de la primera vista de una viñeta de salida de varias resoluciones o &quot;0&quot; si hay una viñeta piramidal. Para archivos de estilo de archivador, la resolución de salida se utiliza como sufijo de archivo. *[!DNL destFile]* se ignora cuando `-info` se ha especificado.
