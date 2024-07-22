---
description: El servicio de imágenes proporciona un preprocesador de solicitudes simple basado en reglas de coincidencia y sustitución de expresiones regulares.
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

El servicio de imágenes proporciona un preprocesador de solicitudes simple basado en reglas de coincidencia y sustitución de expresiones regulares.

Se pueden adjuntar colecciones de reglas (conjuntos de reglas) a cada catálogo de imágenes, incluido el catálogo predeterminado. Las reglas se especifican con archivos con formato XML.

Las reglas de preprocesamiento de solicitudes pueden modificar las partes de la ruta y la consulta de las solicitudes antes de que las procese el analizador de [!DNL Platform Server], incluida la manipulación de la ruta, la adición de comandos, el cambio de valores de comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones de seguridad que normalmente solo se controlan con atributos de catálogo, como la ofuscación de solicitudes, la marca de agua y la limitación del servicio HTTP a direcciones IP de cliente específicas.

Las reglas de preprocesamiento de solicitudes son adecuadas para una variedad de aplicaciones, algunas de las cuales se enumeran a continuación:

* Implemente un mecanismo de *rutas virtuales*, que permita reasignar la ruta de solicitud a rutas de archivo, FTP y HTTP.
* Aplicar selectivamente funciones de seguridad, como marca de agua, filtradas por nombre de imagen o ruta.
* Omitir marcas de agua u otras características de seguridad al acceder al servidor desde direcciones IP específicas.
* Forzar la aplicación de comandos, como `defaultImage=`, a todas las solicitudes o solicitudes que muestran un patrón específico en la ruta de acceso de la dirección URL o en las cadenas de consulta.
* No permitir el uso de comandos que requieren mucha CPU para evitar el uso indebido del servidor.
* Permite que las imágenes de origen se ubiquen en servidores HTTP o FTP sin dejar de especificarlas en la ruta de solicitud, en lugar de `src=`.
* Controle la configuración de calidad de la imagen (como la calidad del JPEG o el enfoque) según la ruta de solicitud o el nombre de la imagen.

Encontrará información detallada sobre la creación, el uso y la administración de conjuntos de reglas en la [Referencia del conjunto de reglas](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Véase también {#see-also}

[Referencia de conjunto de reglas](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [atributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
