---
description: Filtros que ayudan a definir criterios de búsqueda para que las búsquedas sean más eficientes.
solution: Experience Manager
title: SearchFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---


# SearchFilter{#searchfilter}

Filtros que ayudan a definir criterios de búsqueda para que las búsquedas sean más eficientes.

Sintaxis

## Parámetros {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> carpeta</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Especifique la carpeta que desee buscar. Déjelo en blanco para buscar en toda la compañía. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Configúrelo en: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> Verdadero</span>: Para buscar la carpeta con nombre y todas las subcarpetas. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> Falso</span>: Para buscar solo la carpeta con nombre. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Lista de tipos de recursos que desea devolver en una búsqueda. Por ejemplo, <span class="codeph"> imagen</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> Especifique un tipo de recurso para excluirlo de una búsqueda. Por ejemplo, imagen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Una lista de subtipos de recursos que desea devolver en una búsqueda. Por ejemplo, para un <span class="codeph"> AssetSet</span>, puede buscar el subtipo <span class="codeph"> MediaType</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictoSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Un indicador booleano opcional que especifica si se devolverán activos sin subtipo cuando se pase <span class="codeph"> assetSubTypeArray</span>. </p> <p>Si es true, solo se devuelven los activos con uno de los subtipos especificados. </p> <p>Si es false, también se devuelven los recursos sin subtipo. </p> <p>El valor predeterminado es false. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Configúrelo en: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> Verdadero</span>: Para devolver solo los recursos originales. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> Falso</span>: Para devolver contenido generado. Por ejemplo, imágenes de un PDF cargado. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gestione el proyecto que desee buscar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Especificar: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> </span> MarkedForPublishpara devolver solo los recursos publicados. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> </span> NotMarkedForPublishpara devolver solo los recursos no publicados. </li> 
    </ul> <p>Nota: Deje en blanco para buscar <i>todos los</i> tipos de estado publicados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Especificar: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> </span> Cualquier valor devuelto de recursos independientemente de su estado de papelera. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> </span> NotInTrashpara devolver recursos "normales". </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> </span> InTrashpara devolver recursos de la papelera. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

