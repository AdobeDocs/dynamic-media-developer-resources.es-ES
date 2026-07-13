---
description: Definición de destino para una acción de clic en el explorador.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
TQID: 'https://experienceleague.adobe.com/x27LpaNACQ5k-n09O-9Bhw7aecAjWQ6wNkLt8XewVXs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

Definición de destino para una acción de clic en el explorador.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| nombre | `xsd:string` | Nombre de la definición del mapa de imagen. |
| shapeType | `xsd:string` | Uno de los valores de forma de región. |
| región | `xsd:string` | Coordenadas de mapa de imagen. El formato se basa en los atributos de etiquetas de HTML `<area>`. |
| action | `xsd:string` | Otros atributos que se incluirán en la etiqueta de HTML `<area>`, incluida la dirección URL `href`. |
| habilitada | `xsd:boolean` | True si el mapa de imagen está habilitado. |

