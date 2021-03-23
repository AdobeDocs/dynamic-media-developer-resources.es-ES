---
description: Crea una vista preestablecida que determina lo que puede ver un usuario. El visor puede ser de cualquier tipo disponible en IPS. La vista preestablecida se aplica cuando se publican los recursos.
seo-description: Crea una vista preestablecida que determina lo que puede ver un usuario. El visor puede ser de cualquier tipo disponible en IPS. La vista preestablecida se aplica cuando se publican los recursos.
seo-title: createViewerPreset
solution: Experience Manager
title: createViewerPreset
uuid: 4160d2b0-6147-459f-830a-43c99b8dc196
feature: Dynamic Media Classic,SDK/API,ajustes preestablecidos de visor
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 11%

---


# createViewerPreset{#createviewerpreset}

Crea una vista preestablecida que determina lo que puede ver un usuario. El visor puede ser de cualquier tipo disponible en IPS. La vista preestablecida se aplica cuando se publican los recursos.

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
| `*`companyHandle`*` | `xsd:string` | Sí | El nombre de la empresa que contiene los ajustes preestablecidos de visor y los recursos. |
| `*`folderHandle`*` | `xsd:string` | Sí | El identificador de la carpeta que contiene los recursos. |
| `*`name`*` | `xsd:string` | Sí | Nombre del visor. |
| `*`type`*` | `xsd:string` | Sí | Tipo de visor. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | No | Matriz que contiene nombres, valores y identificadores de imágenes a las que está aplicando ajustes preestablecidos. |

**Salida (createViewerPresetReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | Sí | Gestión del ajuste preestablecido en el visor. |

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

