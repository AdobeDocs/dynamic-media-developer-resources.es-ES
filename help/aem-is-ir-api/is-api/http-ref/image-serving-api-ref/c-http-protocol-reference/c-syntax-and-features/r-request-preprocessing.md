---
description: El servicio de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de sustitución y coincidencia de expresiones regulares.
seo-description: El servicio de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de sustitución y coincidencia de expresiones regulares.
seo-title: Solicitar preprocesamiento
solution: Experience Manager
title: Solicitar preprocesamiento
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---


# Solicitar preprocesamiento{#request-preprocessing}

El servicio de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de sustitución y coincidencia de expresiones regulares.

Las colecciones de reglas (conjuntos de reglas) se pueden adjuntar a cada catálogo de imágenes, incluido el catálogo predeterminado. Las reglas se especifican con archivos con formato XML.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que el analizador de Platform Server las procese, lo que incluye la manipulación de la ruta, la adición de comandos, el cambio de los valores de los comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones de seguridad que normalmente se controlan únicamente con atributos de catálogo, como confusión de solicitudes, marca de agua, así como para limitar el servicio HTTP a direcciones IP de cliente específicas.

Las reglas de preprocesamiento de solicitudes son adecuadas para una variedad de aplicaciones, algunas de las cuales se enumeran a continuación:

* Implemente un mecanismo de *rutas virtuales*, que permite reasignar la ruta de solicitud a las rutas de archivo, FTP y HTTP.
* Aplicación selectiva de funciones de seguridad, como marca de agua, filtradas por nombre de imagen o ruta.
* Omisión de marcas de agua u otras características de seguridad al acceder al servidor desde direcciones IP específicas.
* Aplicación forzada de comandos, como `defaultImage=`, a todas las solicitudes o a las solicitudes que muestran un patrón específico en la ruta URL o cadenas de consulta.
* No permitir el uso de comandos de uso intensivo de CPU para evitar el abuso del servidor.
* Permitir que las imágenes de origen se encuentren en servidores HTTP o FTP pero especificarlas en la ruta de solicitud en lugar de con `src=`.
* Controle la configuración de calidad de la imagen (como la calidad JPEG o el enfoque) según la ruta de acceso de la solicitud o el nombre de la imagen.

Encontrará información detallada sobre la creación, el uso y la administración de conjuntos de reglas en la [Referencia del conjunto de reglas](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Véase también {#see-also}

[Referencia](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) del conjunto de reglas,  [atributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
