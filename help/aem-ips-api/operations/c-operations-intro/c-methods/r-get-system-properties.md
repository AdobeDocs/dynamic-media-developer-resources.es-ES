---
description: Recupera todas las propiedades del sistema en una sola solicitud.
seo-description: Recupera todas las propiedades del sistema en una sola solicitud.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
topic: Scene7 Image Production System API
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getSystemProperties{#getsystemproperties}

Recupera todas las propiedades del sistema en una sola solicitud.

Sintaxis

## Tipos de usuarios autorizados {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parámetros {#section-b2a4fb7068424223aec87c50f0586d73}

**Entrada (getSystemPropertiesParam)**

Ninguno.

**Salida (getSystemPropertiesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`propertyArray`*` | `types:PropertyArray` | Sí | Matriz de propiedades del sistema. |

## Ejemplos {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Este ejemplo de código devuelve una matriz de propiedades del sistema. Respuesta truncada para la brevedad.

**Solicitar**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**Respuesta**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```

