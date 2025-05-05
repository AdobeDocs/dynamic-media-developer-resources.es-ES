---
description: Mensaje detallado que responde a una de las direcciones URL proporcionadas en la solicitud de invalidación de la CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 5%

---

# [!DNL OperationFault]{#operationfault}

Mensaje detallado que responde a una de las direcciones URL proporcionadas en la solicitud de invalidación de la CDN.

**Admitido Desde**

4.5.0, parche 2011-02

## Parámetros {#section-cf4b0c923cef4c14869319af73ace58b}

| **&#x200B; nombre** | **&#x200B; tipo** | **&#x200B; descripción** |
|---|---|---|
| código | `xsd:int` | Código de error proporcionado desde la CDN |
| razón | `xsd:string` | Mensaje de error proporcionado desde la CDN |
