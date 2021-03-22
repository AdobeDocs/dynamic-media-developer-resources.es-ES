---
description: En este tema se describe la sintaxis de uso de vntc.
seo-description: En este tema se describe la sintaxis de uso de vntc.
seo-title: Uso
solution: Experience Manager
title: Uso
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Uso{#usage}

En este tema se describe la sintaxis de uso de vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* es la ruta y el nombre del archivo que se va a procesar. Puede ser una ruta relativa al directorio de trabajo actual o una ruta absoluta. Debe ser una viñeta, un estilo de archivador o un archivo de estilo de cubrimiento de ventana válido y tener uno de estos sufijos: [!DNL .vnt], [!DNL .vnc] o [!DNL .vnw]. Obligatorio.

*[!DNL destFile]* es la ruta y el nombre del archivo de viñeta de salida. Si no se especifica, el archivo de salida se coloca en la carpeta especificada con `-destpath`. En esta situación, el nombre del archivo se genera automáticamente a partir del nombre del archivo de entrada y un sufijo de tamaño, separados por la cadena especificada con `-separator`. Para las viñetas, el sufijo de tamaño es el ancho de píxeles de la viñeta de salida de una sola resolución, el ancho de la primera vista de una viñeta de salida de varias resoluciones o &quot;0&quot; en el caso de una viñeta piramidal. Para los archivos de estilo de archivador, la resolución de salida se utiliza como sufijo de archivo. *[!DNL destFile]* se ignora cuando  `-info` se especifica .
