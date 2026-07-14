---
description: Propiedades de vista de capa.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
TQID: 'https://experienceleague.adobe.com/cx-B-BmcEP6vefJY5tsrNMZcwWIKM-pW0CYfP7BjxMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 46
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Propiedades de vista de capa.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| url | `xsd:string` | URL del servidor de imágenes que representa la plantilla. Combina `urlModifier` y `urlPostAp- plyModifier` campos. |
| urlModifier | `xsd:string` | Comandos de protocolo de servicio de imágenes que se aplicarán antes de la solicitud o `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | Comandos de protocolo de servicio de imágenes para aplicar después de `urlModifier` y comandos de solicitud. |

