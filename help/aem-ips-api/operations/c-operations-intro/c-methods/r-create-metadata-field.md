---
description: Permite a los administradores crear nuevos campos de metadatos para coordinarlos con sistemas de administración de contenido o para operaciones de plantilla. Algunos ejemplos de campos de metadatos creados incluyen palabras clave, información sobre el autor de la imagen o información sobre el titular de los derechos de autor.
seo-description: Permite a los administradores crear nuevos campos de metadatos para coordinarlos con sistemas de administración de contenido o para operaciones de plantilla. Algunos ejemplos de campos de metadatos creados incluyen palabras clave, información sobre el autor de la imagen o información sobre el titular de los derechos de autor.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
feature: Dynamic Media Classic,SDK/API,Metadatos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 12%

---


# createMetadataField{#createmetadatafield}

Permite a los administradores crear nuevos campos de metadatos para coordinarlos con sistemas de administración de contenido o para operaciones de plantilla. Algunos ejemplos de campos de metadatos creados incluyen palabras clave, información sobre el autor de la imagen o información sobre el titular de los derechos de autor.

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
   <td colname="col4"> Nombre de la empresa a la que pertenece el campo de metadatos. </td> 
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
   <td colname="col4"> <p>El valor predeterminado del campo de metadatos que se va a crear (por ejemplo, <span class="codeph"> Scene 7</span>). </p> <p>Los valores predeterminados no son compatibles con los tipos de campo de etiqueta y deben omitirse. Si se especifica un valor predeterminado no vacío para un tipo de campo de etiqueta, se devolverá un error. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Ocultar o exponer metadatos específicos del sistema IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Un indicador booleano que indica si el campo de metadatos se aplica (validado) cuando se establece el valor. </p> <p>Si se establece en true, se genera un error si se establece un valor no válido en <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Permite crear un conjunto de valores enumerados compartidos a los que las etiquetas seleccionadas pueden apuntar. </td> 
  </tr> 
 </tbody> 
</table>

**Salida (createMetadataFieldReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | Sí | El identificador del nuevo campo de metadatos. |

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

