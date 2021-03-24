---
description: Los conjuntos de propiedades son conjuntos específicos de la aplicación de pares de nombre-valor que se pueden adjuntar a varios objetos IPS, según el tipo de conjunto de propiedades. Si el tipo de conjunto de propiedades no permite que se adjunten varios conjuntos a un objeto (PropertySetType/allowMultipleisfalse) y el objeto ya tiene un conjunto asociado del mismo tipo, el nuevo conjunto sustituirá al existente.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# createPropertySet{#createpropertyset}

Los conjuntos de propiedades son conjuntos específicos de la aplicación de pares de nombre-valor que se pueden adjuntar a varios objetos IPS, según el tipo de conjunto de propiedades. Si el tipo de conjunto de propiedades no permite que se adjunten varios conjuntos a un objeto (PropertySetType/allowMultipleisfalse) y el objeto ya tiene un conjunto asociado del mismo tipo, el nuevo conjunto sustituirá al existente.

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
| `*`primaryOwnerHandle`*` | `xsd:string` | Sí | El identificador del propietario principal del conjunto de propiedades. |
| `*`childOwnerHandle`*` | `xsd:string` | No | El identificador del propietario secundario del conjunto de propiedades. |
| `*`propertyArray`*` | `types:PropertyArray` | Sí | Matriz de propiedades. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Salida (createPropertySetParam)**

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

