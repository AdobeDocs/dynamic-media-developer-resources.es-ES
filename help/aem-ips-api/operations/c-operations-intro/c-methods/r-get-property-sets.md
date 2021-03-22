---
description: Obtiene conjuntos de propiedades asociados a un control de tipo.
seo-description: Obtiene conjuntos de propiedades asociados a un control de tipo.
seo-title: getPropertySets
solution: Experience Manager
title: getPropertySets
uuid: fa3cadb3-92b3-4ffb-ac1e-87a01b98bcb2
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 16%

---


# getPropertySets{#getpropertysets}

Obtiene conjuntos de propiedades asociados a un control de tipo.

Sintaxis

## Tipos de usuarios autorizados {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-d8da2847e77e4a95a4441d9848cac775}

**Entrada (getPropertySetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Sí | El identificador del tipo de conjunto de propiedades. |
| `*`primaryOwnerHandle`*` | `xsd:string` | Sí | Propietario principal de los datos enlazados al objeto de base de datos. |
| `*`childOwnerHandle`*` | `xsd:string` | No | Un propietario secundario opcional de los datos. |

**Salida (getPropertySetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`setArray`*` | `types:PropertySetArray` | Sí | Conjunto de conjuntos de propiedades. |

## Ejemplos {#section-1358af974eab4259864910337a6f0bd2}

Este ejemplo de código devuelve conjuntos de propiedades de su propietario principal, especificados por un identificador de tipo .

**Solicitar**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**Respuesta**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```

