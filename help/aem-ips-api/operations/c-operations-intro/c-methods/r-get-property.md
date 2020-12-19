---
description: Obtiene valores de cadena de las propiedades del sistema relacionadas con el portal de imágenes.
seo-description: Obtiene valores de cadena de las propiedades del sistema relacionadas con el portal de imágenes.
seo-title: getProperty
solution: Experience Manager
title: getProperty
topic: Scene7 Image Production System API
uuid: 38ea08a6-c948-4a01-bc9a-d1609197224e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# getProperty{#getproperty}

Obtiene valores de cadena de las propiedades del sistema relacionadas con el portal de imágenes.

Las propiedades del sistema admitidas son:

* `IpsVersion`:: Número de versión de IPS.
* `IpsImageServerUrl`:: Prefijo de URL externo completo para el servidor de imágenes IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`:: Prefijo URL para procesar recursos SVG.
* `SvgRenderEnabled`:: True si los recursos SVG se pueden representar mediante  `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`:: Tamaño máximo (en bytes) de los datos de archivo permitidos en una carga  [!DNL POST]. El sistema rechaza los archivos que superen el límite máximo.

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

**Input (getPropertyParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`name`*` | `xsd:string` | Sí | Nombre de la propiedad que se va a obtener. |

**Output (getPropertyReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`basado en IP`*` | `xsd:string` | Sí | El valor de la propiedad. |

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

