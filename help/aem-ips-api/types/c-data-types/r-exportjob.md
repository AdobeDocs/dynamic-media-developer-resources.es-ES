---
description: Tipo de trabajo para permitir la exportación autorizada de archivos cargados anteriormente.
seo-description: Tipo de trabajo para permitir la exportación autorizada de archivos cargados anteriormente.
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Dynamic Media Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 15%

---


# ExportJob{#exportjob}

Tipo de trabajo para permitir la exportación autorizada de archivos cargados anteriormente.

ExportJob no admite los siguientes tipos de recursos:

* Conjuntos de imágenes
* Conjuntos de procesamiento
* Conjuntos de giros
* Conjuntos de medios
* Conjuntos de varias velocidades de bits
* Conjuntos de vídeos
* Catálogos electrónicos
* Conjuntos de ofertas

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Lista de <span class="codeph"> assetHandle</span> que se debe exportar. Consulte <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Especifica el tipo de exportación <span class="codeph">.Valores posibles</span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Si <span class="codeph"> fmt=orig</span>, los recursos se exportan como originales </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Si <span class="codeph"> fmt=convert</span>, los recursos se convierten al formato especificado en los parámetros de entrada <span class="codeph"> is_modifer</span> o <span class="codeph"> macro</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Especifica la cadena URL de procesamiento <span class="codeph"> ImageServer</span>, que se anexa a la solicitud ExportJob <span class="codeph"> convert</span>. </p> <p>Consulte la <a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-serving-api/home.html" scope="external" format="html"> documentación de IS</a> para obtener detalles sobre cómo enviar los modificadores IS. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Opción de configuración de correo electrónico. Valores posibles: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> Todos</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Error</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> JobCompletion</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> Ninguno</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Especifica la dirección IP del cliente o cliente que inició la solicitud de exportación. </p> <p> <p>Nota:  este parámetro no se rellena activamente en este momento y está reservado exclusivamente para uso futuro. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Para las solicitudes ExportJob en las que se proporcionan `fmt=convert` y `is_modifier` y `macro`, el archivo de destino respeta el formato proporcionado por `macro`. Por ejemplo:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

