---
description: Vignette Converter (vntc) es una utilidad de línea de comandos que se utiliza para preparar contenido creado con Image Authoring para la implementación con procesamiento de imágenes.
seo-description: Vignette Converter (vntc) es una utilidad de línea de comandos que se utiliza para preparar contenido creado con Image Authoring para la implementación con procesamiento de imágenes.
seo-title: Convertidor de viñetas
solution: Experience Manager
title: Convertidor de viñetas
topic: Scene7 Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Convertidor de viñetas{#vignette-converter}

Vignette Converter (vntc) es una utilidad de línea de comandos que se utiliza para preparar contenido creado con Image Authoring para la implementación con procesamiento de imágenes.

[!DNL vntc] se encuentra en [!DNL *[!DNL install_root]*\ImageServing\bin]. Tiene las siguientes capacidades:

* Convierte las viñetas principales en viñetas de producción de una sola resolución, de varias resoluciones o piramidales (consulte Escala de [viñetas](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produce archivadores de producción y ventanas que cubren archivos de estilo (ver `-resolution` y `-jpegquality`).

* Puede producir diferentes versiones de archivos de viñetas, archivadores y archivos de estilo de coberturas de ventanas para utilizarlos con versiones anteriores de Procesamiento de imágenes.
* Extrae imágenes de vista de viñetas, ya sea de resolución completa o de miniaturas (ver `-thumbwidth` y `-image`).
* Extrae propiedades relevantes del archivo de origen (véase `-info`) y las envía a `stdout` o a un archivo de registro opcional (véase `-log`).

Aunque el uso de [!DNL vntc] es opcional, se recomienda encarecidamente para un mejor rendimiento del servidor. [!DNL vntc] también implementa una amplia comprobación de errores y puede evitar graves problemas con el servidor, incluyendo bloqueos, cuando se utiliza con diligencia.

Al generar viñetas de producción, se añade el ancho de píxel de la viñeta de salida (o 0 en el caso de las viñetas piramidales o de varias resoluciones) al nombre del archivo de viñeta de salida generado. Al procesar archivos de estilo archivador, la resolución de salida se anexa al nombre del archivo de salida. Todos los archivos de salida, incluidos los archivos opcionales de miniatura, imagen y registro, así como la viñeta de producción o el archivo de estilo archivador, se colocan en el mismo directorio en el que *[!DNL sourceFile]* se encuentra (a menos que `-destPath` se especifique).

[!DNL vntc] se limita de forma predeterminada a un máximo de 3 GB de memoria. Cuando Vntc llegue a este límite, se detendrá el procesamiento y se producirá un error. Este límite se puede cambiar mediante `-maxmem`.

>[!NOTE]
>
>La herramienta de actualización de viñetas de la creación de imágenes también se puede utilizar para preparar viñetas para su uso. Del mismo modo, la herramienta de creación de contenido puede generar archivos de estilo archivador para su uso con el procesamiento de imágenes. Se utiliza [!DNL vntc] si se va a automatizar el procesamiento. Las herramientas de Creación de imágenes incluyen una interfaz gráfica de usuario, por lo que suelen ser más fáciles de usar de forma interactiva.

## Véase también {#section-3c756bf17b634543904fdd928adeafb2}

Documentación de creación de imágenes
