---
description: Crea un formato de imagen.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# saveImageFormat{#saveimageformat}

Crea un formato de imagen.

>[!NOTE]
>
>El valor del campo `urlModifier` debe constar de un XML válido. Por ejemplo, cambie `&` a `&`. Obtenga el valor `urlModfier` de la interfaz de usuario de IPS.

## Tipos de usuarios autorizados {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Entrada (saveImageFormatParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con el formato de imagen con el que desea trabajar. |
| `*`imageFormatHandle`*` | `xsd:string` | No | El controlador de formato de imagen que desea guardar. |
| `*`name`*` | `xsd:string` | Sí | Nombre del formato de imagen. |
| `*`urlModifier`*` | `xsd:string` | Sí | Puede ser cualquier cadena de consulta de protocolo IPS. La forma más sencilla de generar un modificador de URL es crear uno con la interfaz de usuario IPS y luego cortar y pegar la cadena de consulta. |

**Salida (saveImageFormatReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`imageFormatHandle`*` | `xsd:string` | Sí | Gestionar al formato de imagen. |

## Ejemplos {#section-c7bd733212ef494297a97093f3af193f}

Este ejemplo de código crea un formato de imagen. En este ejemplo, `urlModifier` estaba determinado por su valor en la interfaz de usuario IPS con un formato HTML válido.

**Solicitar**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**Respuesta**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```
