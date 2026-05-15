---
description: Propiedades del archivo PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
TQID: 'https://experienceleague.adobe.com/fM-heKQFWRXUn8QWVxJA1yNJ2aqlozRoK5B-ErzamLA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 45
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

Propiedades del archivo PostScript.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| [!DNL engine] | `xsd:string` | Motor de generación utilizado (consulte &quot;Información de generación&quot; para ver los valores). |
| [!DNL originator] | `types:Asset` | Registro de recursos del recurso principal utilizado en la generación. |
| [!DNL generated] | `types:Asset` | Registro de recursos del recurso generado. |
| attributeArray | `types:GenerationAttributeArray` | Matriz de atributos asociados al proceso de generación. |
