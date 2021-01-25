---
description: Los conjuntos de propiedades son conjuntos de pares nombre-valor específicos de la aplicación que se pueden adjuntar a varios objetos IPS, según el tipo de conjunto de propiedades. Si el tipo de conjunto de propiedades no permite que se adjunten varios conjuntos a un objeto (PropertySetType/allowMultipleisfalse) y el objeto ya tiene un conjunto asociado del mismo tipo, el nuevo conjunto reemplazará al existente.
seo-description: Los conjuntos de propiedades son conjuntos de pares nombre-valor específicos de la aplicación que se pueden adjuntar a varios objetos IPS, según el tipo de conjunto de propiedades. Si el tipo de conjunto de propiedades no permite que se adjunten varios conjuntos a un objeto (PropertySetType/allowMultipleisfalse) y el objeto ya tiene un conjunto asociado del mismo tipo, el nuevo conjunto reemplazará al existente.
seo-title: createPropertySet
solution: Experience Manager
title: createPropertySet
topic: Dynamic Media Image Production System API
uuid: f0b5b951-143f-4a31-bb6b-cdeabdebbcbb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 6%

---


# createPropertySet{#createpropertyset}

Los conjuntos de propiedades son conjuntos de pares nombre-valor específicos de la aplicación que se pueden adjuntar a varios objetos IPS, según el tipo de conjunto de propiedades. Si el tipo de conjunto de propiedades no permite que se adjunten varios conjuntos a un objeto (PropertySetType/allowMultipleisfalse) y el objeto ya tiene un conjunto asociado del mismo tipo, el nuevo conjunto reemplazará al existente.

Sintaxis

## Tipos de usuarios autorizados {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-25258e75f5f3419bad165c797eb6cd8e}

**Entrada (createPropertySetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Sí | El identificador del tipo de conjunto de propiedades. |
| `*`PrimaryOwnerHandle`*` | `xsd:string` | Sí | Identificador del propietario principal del conjunto de propiedades. |
| `*`secondaryOwnerHandle`*` | `xsd:string` | No | Identificador del propietario secundario del conjunto de propiedades. |
| `*`propertyArray`*` | `types:PropertyArray` | Sí | Matriz de propiedades. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Sí | El identificador del nuevo conjunto de propiedades. |

## Ejemplos {#section-4e1f5b2883664bc88f590fcd253df22b}

Este ejemplo de código crea un conjunto de propiedades que contiene nombres y valores de propiedades. La respuesta devuelve un identificador al nuevo conjunto de propiedades.

**Solicitar**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**Respuesta**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```

