---
description: El conversor de viñetas (vntc) es una utilidad de línea de comandos que se utiliza para preparar el contenido creado con la creación de imágenes para su implementación con la representación de imágenes.
seo-description: El conversor de viñetas (vntc) es una utilidad de línea de comandos que se utiliza para preparar el contenido creado con la creación de imágenes para su implementación con la representación de imágenes.
seo-title: Conversor de viñetas
solution: Experience Manager
title: Conversor de viñetas
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---


# Conversor de viñetas{#vignette-converter}

El conversor de viñetas (vntc) es una utilidad de línea de comandos que se utiliza para preparar el contenido creado con la creación de imágenes para su implementación con la representación de imágenes.

[!DNL vntc] se encuentra en [!DNL  *[!DNL install_root]*\ImageServing\bin]. Tiene las siguientes capacidades:

* Convierte las viñetas principales en viñetas de producción de una sola resolución, de varias resoluciones o piramidales (consulte [Escala de viñeta](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Genera archivadores de producción y ventanas que cubren archivos de estilo (consulte `-resolution` y `-jpegquality`).

* Puede producir diferentes versiones de archivos de viñetas, archivadores y archivos de estilo de cubiertas de ventanas para su uso con versiones anteriores de Representación de imágenes.
* Extrae imágenes de vista de viñetas, ya sea con resolución completa o miniaturas (consulte `-thumbwidth` y `-image`).
* Extrae propiedades relevantes del archivo de origen (consulte `-info`) y las envía a `stdout` o a un archivo de registro opcional (consulte `-log`).

Aunque el uso de [!DNL vntc] es opcional, se recomienda encarecidamente para el mejor rendimiento del servidor. [!DNL vntc] también implementa una amplia comprobación de errores y puede evitar problemas graves del servidor, incluidos bloqueos, cuando se utiliza con diligencia.

Al generar viñetas de producción, el ancho de píxeles de la viñeta de salida (o 0 en el caso de las viñetas piramidales o de varias resoluciones) se anexa al nombre del archivo de viñeta de salida generado. Al procesar archivos de estilo de archivador, la resolución de salida se anexa al nombre del archivo de salida. Todos los archivos de salida, incluidos los archivos opcionales de miniatura, imagen y registro, así como la viñeta de producción o el archivo de estilo archivador, se colocan en el mismo directorio donde se encuentra *[!DNL sourceFile]* (a menos que se especifique `-destPath`).

[!DNL vntc] se limita de forma predeterminada a como máximo 3 GB de memoria. Cuando Vntc llegue a este límite, detendrá el procesamiento y producirá un error. Este límite se puede cambiar con `-maxmem`.

>[!NOTE]
>
>La herramienta de actualización de viñetas de la creación de imágenes también se puede utilizar para preparar viñetas para su uso. Del mismo modo, la herramienta de creación de contenido puede generar archivos de estilo de archivador para utilizarlos con la representación de imágenes. Utilice [!DNL vntc] si se va a automatizar el procesamiento. Las herramientas de Creación de imágenes incluyen una interfaz gráfica de usuario, por lo que suelen ser más fáciles de utilizar de forma interactiva.

## Véase también {#section-3c756bf17b634543904fdd928adeafb2}

Documentación de creación de imágenes
