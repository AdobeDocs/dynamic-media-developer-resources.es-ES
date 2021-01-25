---
description: El servicio de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de coincidencia y sustitución de expresiones regulares.
seo-description: El servicio de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de coincidencia y sustitución de expresiones regulares.
seo-title: Preprocesamiento de solicitud
solution: Experience Manager
title: Preprocesamiento de solicitud
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Preprocesamiento de solicitud{#request-preprocessing}

El servicio de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de coincidencia y sustitución de expresiones regulares.

Las colecciones de reglas (conjuntos de reglas) se pueden adjuntar a cada catálogo de imágenes, incluido el catálogo predeterminado. Las reglas se especifican con archivos con formato XML.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que el analizador de Platform Server las procese, incluida la manipulación de la ruta, la adición de comandos, el cambio de valores de comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones de seguridad que normalmente se controlan únicamente con atributos de catálogo, como confusión de solicitudes, marcado de agua, así como limitar el servicio HTTP a direcciones IP de clientes específicas.

Las reglas de preprocesamiento de solicitudes son adecuadas para una variedad de aplicaciones, algunas de las cuales se enumeran a continuación:

* Implementar un mecanismo *paths virtuales*, que permite reasignar la ruta de la solicitud a las rutas de archivo, FTP y HTTP.
* Aplicación selectiva de funciones de seguridad, como la marca de agua, filtradas por nombre de imagen o ruta.
* Omitir marcas de agua u otras características de seguridad al acceder al servidor desde direcciones IP específicas.
* Obligar la aplicación de comandos, como `defaultImage=`, a todas las solicitudes o a aquellas que exhiban un patrón específico en la ruta de URL o en las cadenas de consulta.
* No permitir el uso de comandos con uso intensivo de CPU para evitar el uso indebido del servidor.
* Permitir que las imágenes de origen se encuentren en servidores HTTP o FTP mientras se siguen especificando en la ruta de solicitud en lugar de `src=`.
* Controle los ajustes de calidad de imagen (como la calidad JPEG o el enfoque) en función de la ruta de acceso de la solicitud o del nombre de la imagen.

Encontrará información detallada sobre la creación, el uso y la administración de conjuntos de reglas en la [Referencia del conjunto de reglas](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Véase también {#see-also}

[Referencia](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) del conjunto de reglas,  [atributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
