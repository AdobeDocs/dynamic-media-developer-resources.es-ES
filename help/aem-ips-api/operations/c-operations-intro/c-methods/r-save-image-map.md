---
description: Cree un nuevo mapa de imagen o edite un mapa existente.
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 15%

---

# saveImageMap{#saveimagemap}

Cree un nuevo mapa de imagen o edite un mapa existente.

Sintaxis

## Tipos de usuarios autorizados {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso.

## Parámetros {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Entrada (saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la empresa con el mapa de imagen que desea guardar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador del recurso de imagen al que pertenece el mapa de imagen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> El identificador del mapa de imagen. Crea un mapa de imagen si es NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Nombre del mapa de imagen que se crea o guarda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Forma de la región. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> region  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Lista de puntos delimitada por comas que definen la región. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> acción  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> <p>El valor <span class="codeph"> href </span> asociado con el mapa de imagen, tal como se especifica en la interfaz IPS. </p> <p>Para obtener el valor <span class="codeph"> href </span>, haga clic en la imagen en la interfaz IPS, copie y pegue la dirección URL en este elemento y, a continuación, dé formato a la dirección URL IPS como dirección URL adecuada. Por ejemplo, <span class="codeph"> y </span> se convierten en <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El orden de la lista de mapas de imágenes (el eje Z). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> enabled  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Salida (saveImageMapReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Sí | El identificador del mapa de imagen nuevo o editado. |

## Ejemplos {#section-fdac488b640f427c8aa3d549c5032851}

Este ejemplo de código crea un nuevo mapa de imagen para un recurso. Utiliza un tipo de forma determinado por una constante de cadena de forma de región y devuelve un controlador al nuevo mapa de imagen.

**Solicitar**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**Respuesta**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```
