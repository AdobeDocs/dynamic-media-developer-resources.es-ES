---
description: Obtiene conjuntos de propiedades asociados a un identificador de tipo.
seo-description: Obtiene conjuntos de propiedades asociados a un identificador de tipo.
seo-title: getPropertySets
solution: Experience Manager
title: getPropertySets
topic: Scene7 Image Production System API
uuid: fa3cadb3-92b3-4ffb-ac1e-87a01b98bcb2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPropertySets{#getpropertysets}

Obtiene conjuntos de propiedades asociados a un identificador de tipo.

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

**Input (getPropertySetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | Sí | El identificador del tipo de conjunto de propiedades. |
| ` *`PrimaryOwnerHandle`*` | `xsd:string` | Sí | El propietario principal de los datos enlazados al objeto de base de datos. |
| ` *`secondaryOwnerHandle`*` | `xsd:string` | No | Un propietario secundario opcional de los datos. |

**Output (getPropertySetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`setArray`*` | `types:PropertySetArray` | Sí | Conjunto de conjuntos de propiedades. |

## Ejemplos {#section-1358af974eab4259864910337a6f0bd2}

Este ejemplo de código devuelve conjuntos de propiedades de su propietario principal, especificados por un identificador de tipo.

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

