---
description: Crea una vista preestablecida que determina lo que un usuario puede ver. El visor puede ser de cualquier tipo y estar disponible en IPS. La vista preestablecida se aplica cuando se publican los recursos.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
TQID: 'https://experienceleague.adobe.com/0RlldrqgWyv0YeP-QqtiVqlDpWtGk60mOWf-w9ageYA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 12%

---

# createViewerPreset{#createviewerpreset}

Crea una vista preestablecida que determina lo que un usuario puede ver. El visor puede ser de cualquier tipo y estar disponible en IPS. La vista preestablecida se aplica cuando se publican los recursos.

Sintaxis

## Tipos de usuarios autorizados {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Entrada (createViewerPresetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la empresa que contiene los ajustes preestablecidos y los recursos del visualizador. |
| folderHandle | `xsd:string` | Sí | El identificador de la carpeta que contiene los recursos. |
| nombre | `xsd:string` | Sí | Nombre del visor. |
| tipo | `xsd:string` | Sí | Tipo de visor. |
| configSettingArray | `types:ConfigSettingArray` | No | Matriz que contiene nombres, valores y controladores de las imágenes a las que está aplicando ajustes preestablecidos. |

**Salida (createViewerPresetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | Sí | Control del ajuste preestablecido para el visualizador. |

## Ejemplos {#section-c88ea63536f3461cbe4677ba53f875dd}

Este ejemplo de código crea un ajuste preestablecido de reproductor de vídeo. La respuesta devuelve un identificador al ajuste preestablecido.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Respuesta**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```

