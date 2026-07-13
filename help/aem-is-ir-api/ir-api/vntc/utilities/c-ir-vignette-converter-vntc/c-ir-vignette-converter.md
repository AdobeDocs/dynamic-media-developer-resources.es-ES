---
title: Conversor de viñetas
description: El Conversor de viñetas (vntc) es una utilidad de línea de comandos que se utiliza para preparar el contenido creado con la Creación de imágenes para su implementación con el Procesamiento de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
TQID: 'https://experienceleague.adobe.com/NZsbUGCd25rHyvrmt-Rh3XN0p3pHqEtGZrXLp-7JBsc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# Conversor de viñetas{#vignette-converter}

El Conversor de viñetas (vntc) es una utilidad de línea de comandos que se utiliza para preparar el contenido creado con la Creación de imágenes para su implementación con el Procesamiento de imágenes.

[!DNL vntc] está en [!DNL *[!DNL install_root]*\ImageServing\bin]. Tiene las siguientes capacidades:

* Convierte viñetas principales en viñetas de producción piramidales, de resolución múltiple o de una sola resolución (consulte [Escalado de viñetas](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produce archivos de estilo de contenedores y ventanas de producción (vea `-resolution` y `-jpegquality`).

* Produzca diferentes versiones de archivos de estilo de viñetas, archivadores y revestimientos de ventanas para utilizarlos con versiones anteriores de Image Rendering.
* Extrae imágenes de vista de viñetas, ya sea con resolución completa o en miniatura (vea `-thumbwidth` y `-image`).
* Extrae las propiedades relevantes del archivo de origen (consulte `-info`) y las envía a `stdout` o a un archivo de registro opcional (consulte `-log`).

Aunque el uso de [!DNL vntc] es opcional, Adobe recomienda su uso para obtener el mejor rendimiento del servidor. El convertidor de viñetas también implementa una comprobación de errores extensa y puede evitar problemas graves con el servidor, incluidos bloqueos, cuando se utiliza con diligencia.

Al generar viñetas de producción, el ancho de píxel de la viñeta de salida (o 0 si son viñetas piramidales o de varias resoluciones) se anexa al nombre del archivo de viñeta de salida generado. Al procesar archivos de estilo de archivador, la resolución de salida se anexa al nombre del archivo de salida. Todos los archivos de salida, incluidos los archivos de miniaturas, imágenes y registros opcionales y el archivo de viñeta de producción o el archivo de estilo de archivador, se colocan en el mismo directorio en el que se encuentra *[!DNL sourceFile]* (a menos que se especifique `-destPath`).

El conversor de viñetas se limita de forma predeterminada a un máximo de 3 GB de memoria. Cuando vntc alcanza este límite, detiene el procesamiento y produce un error. Este límite se puede cambiar usando `-maxmem`.

>[!NOTE]
>
>La herramienta de actualización de viñetas de Image Authoring también se puede utilizar para preparar viñetas para el uso de procesamiento de imágenes. Del mismo modo, la herramienta de creación de contenido puede generar archivos de estilo contenedor para utilizarlos con el procesamiento de imágenes. Use [!DNL vntc] si el procesamiento va a automatizarse. Las herramientas de Image Authoring incluyen una interfaz gráfica de usuario, por lo que generalmente son más fáciles de usar interactivamente.

## Véase también {#section-3c756bf17b634543904fdd928adeafb2}

Documentación de Image Authoring

