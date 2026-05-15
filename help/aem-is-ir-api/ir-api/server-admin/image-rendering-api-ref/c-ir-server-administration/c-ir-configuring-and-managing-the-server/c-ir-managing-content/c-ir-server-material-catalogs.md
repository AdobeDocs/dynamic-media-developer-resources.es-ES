---
description: Los catálogos de material proporcionan muchas opciones de configuración de procesamiento de imágenes.
solution: Experience Manager
title: Catálogos de materiales
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# Catálogos de materiales{#material-catalogs}

Los catálogos de material proporcionan muchas opciones de configuración de procesamiento de imágenes.

Los catálogos de materiales asignan ID de viñeta y material utilizados en las solicitudes a las rutas de archivo reales, pueden almacenar todos los metadatos asociados a los materiales y proporcionar contenedores para las plantillas. Realizan un seguimiento de los perfiles ICC y las macros de comandos.

Solo el componente Java de Image Rendering (ubicado conjuntamente con [!DNL Platform Server]) tiene acceso a los catálogos de materiales. Los archivos de atributos de catálogo deben tener un sufijo [!DNL .ini] y colocarse en la carpeta de catálogo registrada ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). El catálogo de materiales predeterminado ( [!DNL default.ini]) siempre debe estar presente y debe rellenarse con todos los atributos para que el servicio de imágenes funcione correctamente.
