---
description: Información del registro de trabajo.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
TQID: 'https://experienceleague.adobe.com/wH0F5TxaTHxn-vP7PTri94WxEa5Bs9Q2-CRnuHdVb3I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

Información del registro de trabajo.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| logMessage | `xsd:string` | Mensajes en el registro de trabajos. |
| logType | `xsd:string` | Tipo de archivo de registro de trabajo. |
| assetName | `xsd:string` | Nombre del recurso en el registro de trabajos (opcional). |
| assetType | `xsd:string` | Elección del tipo de recurso. |
| assetHandle | `xsd:string` | Controlador de recursos al que se hace referencia en el registro de trabajos. |
| auxArray | `types:JobLogDetailAuxArray` | Proporciona información detallada adicional del registro de trabajos más allá de los cinco tipos de registro de trabajos descritos anteriormente. |

