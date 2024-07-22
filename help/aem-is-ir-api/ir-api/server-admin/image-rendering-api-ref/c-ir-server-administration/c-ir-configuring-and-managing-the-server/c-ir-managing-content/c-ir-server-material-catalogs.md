---
description: Los catálogos de material proporcionan muchas opciones de configuración de procesamiento de imágenes.
solution: Experience Manager
title: Catálogos de materiales
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Catálogos de materiales{#material-catalogs}

Los catálogos de material proporcionan muchas opciones de configuración de procesamiento de imágenes.

Los catálogos de materiales asignan ID de viñeta y material utilizados en las solicitudes a las rutas de archivo reales, pueden almacenar todos los metadatos asociados a los materiales y proporcionar contenedores para las plantillas. Realizan un seguimiento de los perfiles ICC y las macros de comandos.

Solo el componente Java de Image Rendering (ubicado conjuntamente con [!DNL Platform Server]) tiene acceso a los catálogos de materiales. Los archivos de atributos de catálogo deben tener un sufijo [!DNL .ini] y colocarse en la carpeta de catálogo registrada ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). El catálogo de materiales predeterminado ( [!DNL default.ini]) siempre debe estar presente y debe rellenarse con todos los atributos para que el servicio de imágenes funcione correctamente.
