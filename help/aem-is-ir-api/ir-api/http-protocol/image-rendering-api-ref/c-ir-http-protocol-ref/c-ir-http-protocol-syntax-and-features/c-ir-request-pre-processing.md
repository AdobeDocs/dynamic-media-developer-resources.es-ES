---
title: Solicitar procesamiento previo
description: El procesamiento de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de sustitución y coincidencia de expresiones regulares.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Solicitar procesamiento previo{#request-pre-processing}

El procesamiento de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de sustitución y coincidencia de expresiones regulares.

Se pueden adjuntar colecciones de reglas (conjuntos de reglas) a cada catálogo de materiales, incluido el catálogo predeterminado. Las reglas se especifican con archivos con formato XML.

Las reglas de preprocesamiento de solicitudes pueden modificar las partes de las solicitudes de ruta y consulta antes de que el analizador de procesamiento de imágenes las procese. Este precepto incluye la manipulación de la ruta de acceso, la adición de comandos, el cambio de valores de comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones que normalmente solo se controlan con atributos de catálogo, como configurar el tamaño predeterminado de la imagen de respuesta o limitar el servicio HTTP a direcciones IP de cliente específicas.

Las reglas de preprocesamiento de solicitudes son adecuadas para varias aplicaciones, algunas de las cuales se enumeran a continuación:

* Implementación de un *rutas virtuales* mecanismo, que permite reasignar la ruta de solicitud a las rutas de archivo, FTP y HTTP.
* No permitir el uso de comandos de uso intensivo de la CPU para evitar el uso indebido del servidor.
* Controle la configuración de calidad de la imagen (como la calidad del JPEG o el enfoque) según la ruta de solicitud o el nombre de la imagen.

Encontrará información detallada sobre cómo crear, utilizar y administrar conjuntos de reglas en la Referencia del conjunto de reglas.

Consulte también Referencia de conjunto de reglas, attribute::RuleSetFile
