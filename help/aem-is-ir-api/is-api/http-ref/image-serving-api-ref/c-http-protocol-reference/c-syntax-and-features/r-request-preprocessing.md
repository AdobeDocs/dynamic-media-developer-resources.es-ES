---
description: El servicio de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de sustitución y coincidencia de expresiones regulares.
solution: Experience Manager
title: Solicitar preprocesamiento
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Solicitar preprocesamiento{#request-preprocessing}

El servicio de imágenes proporciona un preprocesador de solicitudes sencillo basado en reglas de sustitución y coincidencia de expresiones regulares.

Las colecciones de reglas (conjuntos de reglas) se pueden adjuntar a cada catálogo de imágenes, incluido el catálogo predeterminado. Las reglas se especifican con archivos con formato XML.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que las procese [!DNL Platform Server]El analizador de , incluida la manipulación de la ruta, la adición de comandos, el cambio de valores de comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones de seguridad que normalmente se controlan únicamente con atributos de catálogo, como confusión de solicitudes, marca de agua, así como para limitar el servicio HTTP a direcciones IP de cliente específicas.

Las reglas de preprocesamiento de solicitudes son adecuadas para una variedad de aplicaciones, algunas de las cuales se enumeran a continuación:

* Implemente un *rutas virtuales* , que permite volver a asignar la ruta de solicitud a las rutas de archivo, FTP y HTTP.
* Aplicación selectiva de funciones de seguridad, como marca de agua, filtradas por nombre de imagen o ruta.
* Omisión de marcas de agua u otras características de seguridad al acceder al servidor desde direcciones IP específicas.
* Aplicación forzada de comandos, como `defaultImage=`, a todas las solicitudes o a las solicitudes que muestran un patrón específico en la ruta URL o en las cadenas de consulta.
* No permitir el uso de comandos de uso intensivo de CPU para evitar el abuso del servidor.
* Permitir que las imágenes de origen se ubiquen en servidores HTTP o FTP pero especificarlas en la ruta de solicitud en lugar de con `src=`.
* Controle la configuración de calidad de la imagen (como la calidad del JPEG o el enfoque) en función de la ruta de acceso de la solicitud o el nombre de la imagen.

Encontrará información detallada sobre la creación, el uso y la administración de conjuntos de reglas en la [Referencia del conjunto de reglas](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Véase también {#see-also}

[Referencia del conjunto de reglas](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [atributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
