---
description: El procesamiento de imágenes proporciona un preprocesador de solicitud simple basado en reglas de coincidencia y sustitución de expresiones regulares.
seo-description: El procesamiento de imágenes proporciona un preprocesador de solicitud simple basado en reglas de coincidencia y sustitución de expresiones regulares.
seo-title: Solicitud de preprocesamiento *
solution: Experience Manager
title: Solicitud de preprocesamiento *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ef69ea23-753c-40c8-9edd-eab9c8820c98
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Solicitud de preprocesamiento *{#request-pre-processing}

El procesamiento de imágenes proporciona un preprocesador de solicitud simple basado en reglas de coincidencia y sustitución de expresiones regulares.

Las colecciones de reglas (conjuntos de reglas) se pueden adjuntar a cada catálogo de materiales, incluido el catálogo predeterminado. Las reglas se especifican con archivos con formato XML.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que el analizador de procesamiento de imágenes las procese, incluida la manipulación de la ruta, la adición de comandos, el cambio de valores de comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones que normalmente solo se controlan con atributos de catálogo, como establecer el tamaño de imagen de respuesta predeterminado o limitar el servicio HTTP a direcciones IP de cliente específicas.

Las reglas de preprocesamiento de solicitudes son adecuadas para una variedad de aplicaciones, algunas de las cuales se enumeran a continuación:

* Implementar un mecanismo *paths virtuales*, que permite reasignar la ruta de la solicitud a las rutas de archivo, FTP y HTTP.
* No permitir el uso de comandos con uso intensivo de CPU para evitar el uso indebido del servidor.
* Controle los ajustes de calidad de imagen (como la calidad JPEG o el enfoque) en función de la ruta de acceso de la solicitud o del nombre de la imagen.

Encontrará información detallada sobre la creación, el uso y la administración de conjuntos de reglas en la Referencia del conjunto de reglas.

Consulte también Referencia de conjunto de reglas, atributo::RuleSetFile
