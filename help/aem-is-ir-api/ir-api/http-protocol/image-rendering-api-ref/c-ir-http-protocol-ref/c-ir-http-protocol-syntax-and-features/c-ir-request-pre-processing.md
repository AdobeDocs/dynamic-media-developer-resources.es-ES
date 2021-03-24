---
description: El procesamiento de imágenes proporciona un preprocesador de solicitud simple basado en reglas de sustitución y coincidencia de expresiones regulares.
solution: Experience Manager
title: Solicitud de preprocesamiento *
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Solicitar procesamiento previo *{#request-pre-processing}

El procesamiento de imágenes proporciona un preprocesador de solicitud simple basado en reglas de sustitución y coincidencia de expresiones regulares.

Las colecciones de reglas (conjuntos de reglas) se pueden adjuntar a cada catálogo de material, incluido el catálogo predeterminado. Las reglas se especifican con archivos con formato XML.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que las procese el analizador de procesamiento de imágenes, incluida la manipulación de la ruta, la adición de comandos, la modificación de los valores de los comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones que normalmente se controlan únicamente con atributos de catálogo, como configurar el tamaño de imagen de respuesta predeterminado o limitar el servicio HTTP a direcciones IP de cliente específicas.

Las reglas de preprocesamiento de solicitudes son adecuadas para una variedad de aplicaciones, algunas de las cuales se enumeran a continuación:

* Implemente un mecanismo de *rutas virtuales*, que permite reasignar la ruta de solicitud a las rutas de archivo, FTP y HTTP.
* No permitir el uso de comandos de uso intensivo de CPU para evitar el abuso del servidor.
* Controle la configuración de calidad de la imagen (como la calidad JPEG o el enfoque) según la ruta de acceso de la solicitud o el nombre de la imagen.

Encontrará información detallada sobre la creación, el uso y la administración de conjuntos de reglas en la Referencia del conjunto de reglas.

Consulte también Referencia de conjunto de reglas, atributo::RuleSetFile
