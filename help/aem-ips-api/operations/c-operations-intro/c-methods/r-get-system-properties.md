---
description: Recupera todas las propiedades del sistema en una sola solicitud.
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 16%

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
| propertyArray | `types:PropertyArray` | Sí | Matriz de propiedades del sistema. |

## Ejemplos {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Este ejemplo de código devuelve una matriz de propiedades del sistema. Respuesta truncada para la brevedad.

**Solicitud**

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
