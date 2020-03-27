---
description: Devuelve la configuración IPS de una compañía específica.
seo-description: Devuelve la configuración IPS de una compañía específica.
seo-title: getCompanySettings
solution: Experience Manager
title: getCompanySettings
topic: Scene7 Image Production System API
uuid: 28ee706d-aaef-45a1-9655-3805f158cdc3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getCompanySettings{#getcompanysettings}

Devuelve la configuración IPS de una compañía específica.

Sintaxis

## Tipos de usuarios autorizados {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-e146f479c2744baa8f68be8c8848c97f}

**Entrada (getCompanySettingsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía cuya configuración desea recuperar. |

**Salida (getCompanySettingsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`configuración`*` | `types:CompanySettings` | Sí | Configuración de Compañía. |

## Ejemplos {#section-191f78995ecf473a95eadf7296204fd7}

Este ejemplo de código devuelve todos los ajustes IPS de una compañía específica.

**Solicitar**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**Respuesta**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```

