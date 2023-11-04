---
title: Servir contenido estático (que no sea de imagen)
description: Puede utilizar el servicio de imágenes para administrar el contenido que no es de imagen en los catálogos y servirlo mediante un contexto /is/content independiente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 1%

---

# Servir contenido estático (que no sea de imagen){#serving-static-non-image-contents}

Puede utilizar el servicio de imágenes para administrar el contenido que no es de imagen en los catálogos y servirlo mediante un contexto /is/content independiente.

Esta capacidad permite configurar el TTL para cada elemento por separado.

El servicio de imágenes admite los siguientes comandos en [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Filtro de tipo de contenido. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>, y <span class="codeph"> req=exists </span> solo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> escondrijo </a> </p> </td> 
  <td class="stentry"> <p>Permite deshabilitar el almacenamiento en caché del lado del cliente. </p> </td> 
 </tr> 
</table>

## Sintaxis básica {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> solicitud </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> artículo </span>][? <span class="varname"> modificadores </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> puerto </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogar </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador de catálogo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> artículo </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de elemento de contenido estático. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificadores </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mando </span>*[&amp; <span class="varname"> mando </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mando </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> valor </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>Uno de los nombres de comando admitidos. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor del comando. </p> </td> 
 </tr> 
</table>

## Catálogos de contenido estático {#section-91014f17f0d543d7aaf24539b2d7d4b9}

Los catálogos de contenido estático son similares a los catálogos de imágenes, pero admiten menos campos de datos:

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo/Datos </p> </th> 
   <th colname="col2" class="entry"> <p>Notas </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
   <td colname="col2"> <p>El identificador de registro de catálogo para este elemento de contenido estático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td colname="col2"> <p>Ruta de archivo para este elemento de contenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td colname="col2"> <p>El TTL para este elemento de contenido; <span class="codeph"> attribute::Caducidad </span> se utiliza si no se especifica o si está vacío. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>Marca de tiempo de modificación de archivos; necesaria cuando la validación basada en catálogo está habilitada con <span class="codeph"> attribute::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>Metadatos opcionales asociados con este elemento de contenido estático; disponibles para el cliente con <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Tipo de datos opcional; se puede utilizar para filtrar solicitudes de contenido estático con <span class="codeph"> type= comando </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrado de contenido estático {#section-4c41bf41ff994910840c1352683d1f37}

Este mecanismo puede ayudar a garantizar que los clientes solo reciban el contenido adecuado para sus necesidades. Suponiendo que el contenido estático esté etiquetado con lo apropiado `catalog::UserType` valores, el cliente puede agregar los `type=` a la solicitud. El servicio de imágenes compara el valor proporcionado con la variable `type=` comando al valor de `catalog::UserType` y, si hay una discrepancia, devuelve un error en lugar de contenido potencialmente inapropiado.

## Archivos de subtítulos de vídeo {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Puede encapsular archivos de rótulo de vídeo (WebVTT), CSS o cualquier archivo de texto en formato JSONP. La respuesta JSON se describe a continuación.

* Para los archivos WebVTT, el tipo MIME de la respuesta es texto/javascript. No se devuelve JSON; en su lugar, se devuelve JavaScript que llama a un método con JSON. Tanto el ID como el controlador son opcionales.
* Para los archivos CSS, el tipo MIME de la respuesta es texto/javascript. Tanto el ID como el controlador son opcionales.
* De forma predeterminada, se aplica la codificación UTF-8 para garantizar que se descodifica correctamente. El límite de tamaño predeterminado es de 2 MB.

También puede utilizar pistas para otros tipos de metadatos cronometrados. Los datos de origen de cada elemento de seguimiento son un archivo de texto compuesto por una lista de indicaciones temporizadas. Las señales pueden incluir datos en formatos como JSON o CSV.

Consulte [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) para obtener más información sobre el formato JSONP.

Consulte [www.json.org](https://www.json.org/json-en.html) para obtener más información sobre el formato JSON.

## Véase también {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Referencia de catálogo de imágenes](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
