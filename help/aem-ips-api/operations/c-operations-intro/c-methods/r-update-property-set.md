---
description: Utiliza una matriz de propiedades para actualizar un conjunto de propiedades.
seo-description: Utiliza una matriz de propiedades para actualizar un conjunto de propiedades.
seo-title: updatePropertySet
solution: Experience Manager
title: updatePropertySet
topic: Scene7 Image Production System API
uuid: 21a59c5a-7799-4af6-ab9f-b0311f5f7254
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updatePropertySet{#updatepropertyset}

Utiliza una matriz de propiedades para actualizar un conjunto de propiedades.

Sintaxis

## Tipos de usuarios autorizados {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Input (updatePropertySetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | Sí | Controlador del conjunto de propiedades. |
| ` *`replaceProperties`*` | `xsd:string` | No | Se establece en `true` para reemplazar propiedades. |
| ` *`propertyArray`*` | `types:PropertyArray` | Sí | Matriz de propiedades actualizadas para el conjunto de propiedades. |

**Output (updatePropertySetReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Este ejemplo de código actualiza un conjunto de propiedades con propiedades en la matriz de propiedades.

**Solicitar**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**Respuesta**

Ninguno.
