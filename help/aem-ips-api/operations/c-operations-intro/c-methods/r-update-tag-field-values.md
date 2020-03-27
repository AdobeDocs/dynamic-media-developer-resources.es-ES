---
description: Actualiza los valores del diccionario de etiquetas de un campo de etiqueta.
seo-description: Actualiza los valores del diccionario de etiquetas de un campo de etiqueta.
seo-title: updateTagFieldValues
solution: Experience Manager
title: updateTagFieldValues
topic: Scene7 Image Production System API
uuid: 21689469-a0dd-480b-82ba-ebd12956ff8f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateTagFieldValues{#updatetagfieldvalues}

Actualiza los valores del diccionario de etiquetas de un campo de etiqueta.

Sintaxis

## Tipos de usuarios autorizados {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-0a3a4bab026746238c9d4009caf42e94}

**Entrada (updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obligatorio </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador de Compañía. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador del campo de etiqueta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4">Matriz de valores de campo de etiqueta que desea actualizar. <p>Nota:  Actualiza únicamente los valores de las cadenas de etiquetas. No afecta a las asociaciones de recursos. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (updateTagFieldValuesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sí | El número de campos de etiqueta actualizados correctamente. |
| ` *`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó actualizar los campos de etiquetas. |
| ` *`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó actualizar los campos de etiquetas. |
| ` *`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | No | Matriz de detalles asociada a los recursos que generaron advertencias cuando la operación intentó actualizar los campos de etiquetas. |
| ` *`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | No | Matriz de detalles asociada a los recursos que generaron errores cuando la operación intentó actualizar los campos de etiquetas. |

## Ejemplos {#section-bb4dcf97044c4675974c9b8d27674001}

**Solicitar**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**Respuesta**

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```

