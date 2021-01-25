---
description: Permite a los administradores crear nuevos campos de metadatos para coordinarlos con sistemas gestoras de contenido o para operaciones de plantilla. Algunos ejemplos de campos de metadatos creados incluyen palabras clave, información sobre el autor de la imagen o información del titular de copyright.
seo-description: Permite a los administradores crear nuevos campos de metadatos para coordinarlos con sistemas gestoras de contenido o para operaciones de plantilla. Algunos ejemplos de campos de metadatos creados incluyen palabras clave, información sobre el autor de la imagen o información del titular de copyright.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
topic: Dynamic Media Image Production System API
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 12%

---


# createMetadataField{#createmetadatafield}

Permite a los administradores crear nuevos campos de metadatos para coordinarlos con sistemas gestoras de contenido o para operaciones de plantilla. Algunos ejemplos de campos de metadatos creados incluyen palabras clave, información sobre el autor de la imagen o información del titular de copyright.

Sintaxis

## Tipos de usuarios autorizados {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parámetros {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Entrada (createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre del parámetro </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obligatorio </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Nombre de la compañía a la que pertenece el campo de metadatos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Tipo de recurso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Nombre del campo de metadatos que está creando. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4">Tipo de campo de metadatos. <p>La constante de tipos de campo de metadatos define los tipos disponibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>El valor predeterminado del campo de metadatos que se va a crear (por ejemplo, <span class="codeph"> Scene 7</span>). </p> <p>Los valores predeterminados no se admiten para los tipos de campo de etiqueta y deben omitirse. Si se especifica un valor predeterminado no vacío para un tipo de campo de etiqueta, se mostrará un error. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Oculte o exponga metadatos específicos del sistema IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforce</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Un indicador booleano que indica si el campo de metadatos se fuerza (se valida) cuando se establece el valor. </p> <p>Si se establece en true, se genera un error si se establece un valor no válido en <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Permite crear un conjunto de valores enumerados compartidos al que pueden apuntar las etiquetas seleccionadas. </td> 
  </tr> 
 </tbody> 
</table>

**Salida (createMetadataFieldReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | Sí | Identificador del nuevo campo de metadatos. |

## Ejemplos {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Este ejemplo de código crea un campo de metadatos de tipo cadena llamado `createMetadataField`. La respuesta devuelve el identificador al nuevo campo de metadatos.

**Solicitar**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Respuesta**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

