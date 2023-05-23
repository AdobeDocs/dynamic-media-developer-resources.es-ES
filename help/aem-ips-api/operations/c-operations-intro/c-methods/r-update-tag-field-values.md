---
description: Actualiza los valores del diccionario de etiquetas para un campo de etiqueta.
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 15%

---

# updateTagFieldValues{#updatetagfieldvalues}

Actualiza los valores del diccionario de etiquetas para un campo de etiqueta.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Manejo de la compañía. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Controlador de campo de etiqueta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4">Matriz de valores de campo de etiqueta que desea actualizar. <p>Nota: Actualiza solo los valores de las cadenas de etiquetas. No afecta a las asociaciones de recursos. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (updateTagFieldValuesReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | El número de campos de etiqueta actualizados correctamente. |
| warningCount | `xsd:int` | Sí | El número de advertencias generadas cuando la operación intentó actualizar los campos de etiqueta. |
| errorCount | `xsd:int` | Sí | El número de errores generados cuando la operación intentó actualizar los campos de etiqueta. |
| warningDetailArray | `types:TagValueUpdateFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó actualizar los campos de etiqueta. |
| errorDetailArray | `types:TagValueUpdateFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó actualizar los campos de etiqueta. |

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

```java {.line-numbers}
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
