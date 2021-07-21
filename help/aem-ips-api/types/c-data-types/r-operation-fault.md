---
description: Mensaje detallado que responde a una de las URL proporcionadas en la solicitud de invalidación de CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 11%

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
