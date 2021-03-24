---
description: Mensaje detallado que responde a una de las URL proporcionadas en la solicitud de invalidación de CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 10%

---


# OperationFault{#operationfault}

Mensaje detallado que responde a una de las URL proporcionadas en la solicitud de invalidación de CDN.

**Admitido desde**

4.5.0, parche 2011-02

## Parámetros {#section-cf4b0c923cef4c14869319af73ace58b}

| ** Nombre** | ** Tipo** | ** Descripción** |
|---|---|---|
| `*`código`*` | `xsd:int` | Código de error proporcionado desde la CDN |
| `*`razón`*` | `xsd:string` | Mensaje de error proporcionado desde la CDN |

