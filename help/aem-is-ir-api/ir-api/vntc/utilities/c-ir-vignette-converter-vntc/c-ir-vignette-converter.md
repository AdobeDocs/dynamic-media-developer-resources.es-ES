---
title: Conversor de viñetas
description: El Conversor de viñetas (vntc) es una utilidad de línea de comandos que se utiliza para preparar el contenido creado con la Creación de imágenes para su implementación con el Procesamiento de imágenes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Conversor de viñetas{#vignette-converter}

El Conversor de viñetas (vntc) es una utilidad de línea de comandos que se utiliza para preparar el contenido creado con la Creación de imágenes para su implementación con el Procesamiento de imágenes.

[!DNL vntc] está en [!DNL *[!DNL install_root]*\ImageServing\bin]. Tiene las siguientes capacidades:

* Convierte viñetas principales en viñetas de producción de una sola resolución, varias resoluciones o piramidales (consulte [Escala de viñeta](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produce archivos de estilo de armario y ventana de producción (consulte `-resolution` y `-jpegquality`).

* Produzca diferentes versiones de archivos de estilo de viñetas, archivadores y revestimientos de ventanas para utilizarlos con versiones anteriores de Image Rendering.
* Extrae imágenes de vista de viñetas, ya sea con resolución completa o en miniatura (consulte `-thumbwidth` y `-image`).
* Extrae las propiedades relevantes del archivo de origen (consulte `-info`) y los envía a `stdout` o un archivo de registro opcional (consulte `-log`).

Mientras que el uso de [!DNL vntc] es opcional, Adobe recomienda su uso para obtener el mejor rendimiento del servidor. El convertidor de viñetas también implementa una comprobación de errores extensa y puede evitar problemas graves con el servidor, incluidos bloqueos, cuando se utiliza con diligencia.

Al generar viñetas de producción, el ancho de píxel de la viñeta de salida (o 0 si son viñetas piramidales o de varias resoluciones) se anexa al nombre del archivo de viñeta de salida generado. Al procesar archivos de estilo de archivador, la resolución de salida se anexa al nombre del archivo de salida. Todos los archivos de salida, incluidos los archivos opcionales de miniaturas, imágenes y registros y el archivo de estilo de archivador o viñeta de producción, se colocan en el mismo directorio donde *[!DNL sourceFile]* se encuentra (a menos que `-destPath` se ha especificado).

El conversor de viñetas se limita de forma predeterminada a un máximo de 3 GB de memoria. Cuando vntc alcanza este límite, detiene el procesamiento y produce un error. Este límite se puede cambiar utilizando `-maxmem`.

>[!NOTE]
>
>La herramienta de actualización de viñetas de Image Authoring también se puede utilizar para preparar viñetas para el uso de procesamiento de imágenes. Del mismo modo, la herramienta de creación de contenido puede generar archivos de estilo contenedor para utilizarlos con el procesamiento de imágenes. Uso [!DNL vntc] si se va a automatizar el procesamiento. Las herramientas de Image Authoring incluyen una interfaz gráfica de usuario, por lo que generalmente son más fáciles de usar interactivamente.

## Véase también {#section-3c756bf17b634543904fdd928adeafb2}

Documentación de Image Authoring
