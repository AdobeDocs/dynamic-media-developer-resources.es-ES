---
description: Obtiene valores de cadena de propiedades del sistema relacionadas con Image Portal.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 11%

---


# getProperty{#getproperty}

Obtiene valores de cadena de propiedades del sistema relacionadas con Image Portal.

Entre las propiedades del sistema compatibles se incluyen:

* `IpsVersion`: Número de versión IPS.
* `IpsImageServerUrl`: Prefijo de URL externo completo para el servidor de imágenes IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: Prefijo URL para procesar recursos SVG.
* `SvgRenderEnabled`: True si  `SvgRenderRootUrl` puede representar los recursos SVG.

* `UploadPostMaxFileSize`: Tamaño máximo (en bytes) de los datos de archivo permitidos en una carga  [!DNL POST]. El sistema rechaza los archivos que superen el límite máximo.

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
| `*`name`*` | `xsd:string` | Sí | Nombre de la propiedad que se va a obtener. |

**Salida (getPropertyReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`basado en IP`*` | `xsd:string` | Sí | El valor de la propiedad. |

## Ejemplos {#section-3f80a78dd60c404181b34d3a912d7a36}

Este ejemplo de código utiliza una constante de cadena Propiedades IPS para devolver un valor específico. En este ejemplo, la propiedad IPS es la versión del servidor IPS.

**Solicitar**

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

