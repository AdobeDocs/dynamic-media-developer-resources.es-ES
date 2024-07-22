---
description: Servir contenido estático (que no sea de imagen)
solution: Experience Manager
title: Servir contenido estático (que no sea de imagen)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Servir contenido estático (que no sea de imagen){#serving-static-non-image-content}

El servicio de imágenes proporciona un mecanismo para administrar el contenido que no es de imagen en los catálogos y ofrecerlo como un `context /is/content` independiente. El mecanismo permite configurar el TTL para cada elemento por separado.

## Sintaxis básica {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> solicitud </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> servidor </span>/is/content[/ <span class="varname"> catálogo </span>/ <span class="varname"> elemento </span>][? <span class="varname"> modificadores </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> servidor </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dirección_servidor </span>[: <span class="varname"> puerto </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catálogo </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador de catálogo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> elemento </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de elemento de contenido estático. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificadores </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> comando </span>*[&amp; <span class="varname"> comando </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> comando </span> </span> </p> </td> 
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

## Introducción a comandos {#section-61657a0141914053ab12038ad7e91500}

El servicio de imágenes admite los siguientes comandos en /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> tipo </a> </td> 
  <td class="stentry"> <p>Filtro de tipo de contenido. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span> y <span class="codeph"> req=exists </span> solamente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> caché </a> </td> 
  <td class="stentry"> <p>Permite deshabilitar el almacenamiento en caché del lado del cliente. </p> </td> 
 </tr> 
</table>

## Catálogos de contenido estático {#section-b2b8f4860fe84e528493ed704c7c5141}

Los catálogos de contenido estático son similares a los catálogos de imágenes, pero admiten menos campos de datos:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> atributo/datos</b> </th> 
   <th class="entry"> <b> notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Id </span> </p> </td> 
   <td> <p> El identificador de registro de catálogo para este elemento de contenido estático </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Ruta </span> </p> </td> 
   <td> <p> Ruta de archivo para este elemento de contenido </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Caducidad </span> </p> </td> 
   <td> <p> El TTL para este elemento de contenido; attribute::Expiration se utiliza si no se especifica o si está vacío </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::TimeStamp </span> </p> </td> 
   <td> <p> Marca de tiempo de modificación de archivos; necesaria cuando la validación basada en catálogos está habilitada con el atributo::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserData </span> </p> </td> 
   <td> <p> Metadatos opcionales asociados con este elemento de contenido estático; disponibles para el cliente con req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> Catálogo <span class="codeph">::UserType </span> </p> </td> 
   <td> <p> Tipo de datos opcional; se puede utilizar para filtrar solicitudes de contenido estático con el comando type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrado de contenido estático {#section-896c37cf68bc446eb0766fb378898262}

Este mecanismo puede ayudar a garantizar que los clientes solo reciban el contenido adecuado para sus necesidades. Suponiendo que el contenido estático esté etiquetado con los `catalog::UserType`valores apropiados, el cliente puede agregar el comando `type=` a la solicitud. El servicio de imágenes compara el valor proporcionado con el comando `type=` con el valor de `catalog::UserType` y, en caso de que no coincida, devuelve un error en lugar de contenido potencialmente inapropiado.

## Véase también {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Referencia de catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
