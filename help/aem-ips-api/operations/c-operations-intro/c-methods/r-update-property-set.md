---
description: Utiliza una matriz de propiedades para actualizar un conjunto de propiedades.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

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

**Entrada (updatePropertySetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| setHandle | `xsd:string` | Sí | Handle al conjunto de propiedades. |
| replaceProperties | `xsd:string` | No | Configure como. `true` para reemplazar propiedades. |
| propertyArray | `types:PropertyArray` | Sí | Matriz de propiedades actualizadas para el conjunto de propiedades. |

**Salida (updatePropertySetReturn)**

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
