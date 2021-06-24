---
description: Puede utilizar el servicio de imágenes para administrar el contenido que no sea de imagen en los catálogos y servirlo a través de un contexto /is/content independiente.
solution: Experience Manager
title: Servicio de contenido estático (no de imagen)
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 1%

---

# Servicio de contenido estático (no de imagen){#serving-static-non-image-contents}

Puede utilizar el servicio de imágenes para administrar el contenido que no sea de imagen en los catálogos y servirlo a través de un contexto /is/content independiente.

Esta capacidad permite configurar el TTL para cada elemento por separado.

El servicio de imágenes admite los siguientes comandos en [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Filtro de tipo de contenido. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req  </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>y  <span class="codeph"> req=existe  </span> solamente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache  </a> </p> </td> 
  <td class="stentry"> <p>Permite desactivar el almacenamiento en caché del lado del cliente. </p> </td> 
 </tr> 
</table>

## Sintaxis básica {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> solicitud  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http://  <span class="varname"> server  </span>/is/content[/catalog/  <span class="varname"> item  </span>][? <span class="varname"> modificadores  </span>]  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ :  <span class="varname"> puerto  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catálogo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador de catálogo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de elemento de contenido estático. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificadores  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> comando  </span>*[&amp;  <span class="varname"> comando  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> value  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>Uno de los nombres de comando admitidos. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de comando. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> catálogo::Id  </span> </p> </td> 
   <td colname="col2"> <p>Identificador de registro de catálogo para este elemento de contenido estático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::Path  </span> </p> </td> 
   <td colname="col2"> <p>Ruta de acceso del archivo para este elemento de contenido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::Caducidad  </span> </p> </td> 
   <td colname="col2"> <p>El TTL para este elemento de contenido; <span class="codeph"> atributo::Expiration </span> se utiliza si no se especifica o si está vacío. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Marca de tiempo de modificación del archivo; requerido cuando la validación basada en catálogo está habilitada con el atributo <span class="codeph">::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::UserData  </span> </p> </td> 
   <td colname="col2"> <p>Metadatos opcionales asociados a este elemento de contenido estático; disponible para el cliente con <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::UserType  </span> </p> </td> 
   <td colname="col2"> <p>Tipo de datos opcional; se puede utilizar para filtrar solicitudes de contenido estático con el comando <span class="codeph"> type= </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrado de contenido estático {#section-4c41bf41ff994910840c1352683d1f37}

Este mecanismo puede ayudar a garantizar que los clientes reciban únicamente los contenidos adecuados para sus necesidades. Suponiendo que el contenido estático esté etiquetado con los valores `catalog::UserType` adecuados, el cliente puede agregar el comando `type=` a la solicitud. El servicio de imágenes compara el valor proporcionado con el comando `type=` con el valor de `catalog::UserType` y, en caso de que no coincida, devuelve un error en lugar de contenido potencialmente inapropiado.

## Archivos de subtítulos de vídeo {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Puede encapsular archivos de subtítulos de vídeo (WebVTT), CSS o cualquier archivo de texto en formato JSONP. La respuesta JSON se describe a continuación.

* Para los archivos WebVTT, el tipo mime de la respuesta es text/javascript. JSON no se devuelve; en su lugar, se devuelve Javascript que llama a un método con JSON. Tanto el ID como el controlador son opcionales.
* Para los archivos CSS, el tipo mime de la respuesta es text/javascript. Tanto el ID como el controlador son opcionales.
* De forma predeterminada, la codificación UTF-8 se aplica para garantizar que se descodifique correctamente. El límite de tamaño predeterminado es de 2 MB.

También puede utilizar pistas para otros tipos de metadatos temporizados. Los datos de origen de cada elemento de seguimiento son un archivo de texto formado por una lista de indicaciones temporizadas. Las señales pueden incluir datos en formatos como JSON o CSV.

Consulte [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) para obtener más información sobre el formato JSONP.

Consulte [www.json.org](http://www.json.org) para obtener más información sobre el formato JSON.

## Véase también {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Referencia del catálogo de  [imágenes](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
