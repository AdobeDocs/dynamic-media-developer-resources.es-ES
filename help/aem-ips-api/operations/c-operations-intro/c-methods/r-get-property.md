---
description: Obtiene valores de cadena de propiedades del sistema relacionadas con el portal de imágenes.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
TQID: 'https://experienceleague.adobe.com/loaZvP3tI8neQ6ziLR-xKkkNqGGjD8Mq1jbeC8mJEQo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 10%

---

# getProperty{#getproperty}

Obtiene valores de cadena de propiedades del sistema relacionadas con el portal de imágenes.

Entre las propiedades del sistema compatibles se incluyen:

* `IpsVersion`: número de versión de IPS.
* `IpsImageServerUrl`: prefijo de URL externo completo para el servidor de imágenes IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: prefijo de URL para procesar recursos de SVG.
* `SvgRenderEnabled`: True si `SvgRenderRootUrl` puede procesar los recursos de SVG.

* `UploadPostMaxFileSize`: tamaño máximo (en bytes) de datos de archivo permitido en una carga [!DNL POST]. El sistema rechaza los archivos que superan el límite máximo.

## Tipos de usuarios autorizados {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Entrada (getPropertyParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| nombre | `xsd:string` | Sí | Nombre de la propiedad que se va a obtener. |

**Salida (getPropertyReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| valor | `xsd:string` | Sí | El valor de la propiedad. |

## Ejemplos {#section-3f80a78dd60c404181b34d3a912d7a36}

Este ejemplo de código utiliza una constante de cadena de propiedades IPS para devolver un valor específico. En este ejemplo, la propiedad IPS es la versión del servidor IPS.

**Solicitud**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**Respuesta**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```

