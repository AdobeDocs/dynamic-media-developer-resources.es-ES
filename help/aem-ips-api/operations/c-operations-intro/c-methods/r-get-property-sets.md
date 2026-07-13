---
description: Obtiene los conjuntos de propiedades asociados a un identificador de tipo.
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
TQID: 'https://experienceleague.adobe.com/D2kvkjhVic4Rz-cQPsQoIigz3or1cupYwzOD7rKTGNg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 16%

---

# getPropertySets{#getpropertysets}

Obtiene los conjuntos de propiedades asociados a un identificador de tipo.

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
| typeHandle | `xsd:string` | Sí | El identificador del tipo de conjunto de propiedades. |
| primaryOwnerHandle | `xsd:string` | Sí | Propietario principal de los datos enlazados al objeto de base de datos. |
| secondaryOwnerHandle | `xsd:string` | No | Un propietario secundario opcional de los datos. |

**Salida (getPropertySetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| setArray | `types:PropertySetArray` | Sí | Matriz de conjuntos de propiedades. |

## Ejemplos {#section-1358af974eab4259864910337a6f0bd2}

Este ejemplo de código devuelve conjuntos de propiedades de su propietario principal, especificados por un identificador de tipo.

**Solicitud**

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

