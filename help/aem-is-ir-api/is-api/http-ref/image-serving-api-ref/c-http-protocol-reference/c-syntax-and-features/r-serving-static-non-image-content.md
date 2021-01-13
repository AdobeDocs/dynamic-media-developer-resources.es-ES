---
description: Servicio de contenido estático (sin imagen)
solution: Experience Manager
title: Servicio de contenido estático (sin imagen)
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ec483fe-68a4-4ae2-b5ce-730229a9bc15
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Proporcionando contenido estático (no de imagen){#serving-static-non-image-content}

El servicio de imágenes proporciona un mecanismo para administrar el contenido que no es de imagen en los catálogos y servirlo mediante un `context /is/content` independiente. El mecanismo permite configurar el TTL para cada elemento por separado.

## Sintaxis básica {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> solicitud  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http://  <span class="varname"> server  </span>/is/content[/  <span class="varname"> catálogo  </span>/  <span class="varname"> elemento  </span>][? <span class="varname"> modificadores  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[:  <span class="varname"> puerto  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catálogo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador del catálogo. </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> valor  </span> </span> </p> </td> 
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

## Información general del comando {#section-61657a0141914053ab12038ad7e91500}

El servicio de imágenes admite los siguientes comandos en /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>Filtro de tipo de contenido. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req  </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>, y  <span class="codeph"> req=existe  </span> solamente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> caché  </a> </td> 
  <td class="stentry"> <p>Permite desactivar el almacenamiento en caché del lado del cliente. </p> </td> 
 </tr> 
</table>

## Catálogos de contenido estático {#section-b2b8f4860fe84e528493ed704c7c5141}

Los catálogos de contenido estático son similares a los catálogos de imágenes, pero admiten menos campos de datos:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Atributo/Datos</b> </th> 
   <th class="entry"> <b> Notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Id  </span> </p> </td> 
   <td> <p> El identificador de registro de catálogo para este elemento de contenido estático </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Path  </span> </p> </td> 
   <td> <p> La ruta de acceso del archivo para este elemento de contenido </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Caducidad  </span> </p> </td> 
   <td> <p> El TTL para este elemento de contenido; atributo::Caducidad si no se especifica o si está vacío </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::TimeStamp  </span> </p> </td> 
   <td> <p> Marca de hora de modificación de archivos; requerido cuando la validación basada en catálogo está habilitada con el atributo::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserData  </span> </p> </td> 
   <td> <p> Metadatos opcionales asociados a este elemento de contenido estático; disponible para el cliente con req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserType  </span> </p> </td> 
   <td> <p> Tipo de datos opcional; se puede utilizar para filtrar solicitudes de contenido estático con el comando type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrado de contenido estático {#section-896c37cf68bc446eb0766fb378898262}

Este mecanismo puede ayudar a garantizar que los clientes reciban únicamente el contenido adecuado para sus necesidades. Suponiendo que el contenido estático esté etiquetado con los valores `catalog::UserType`adecuados, el cliente puede agregar el comando `type=` a la solicitud. El servicio de imágenes comparará el valor proporcionado con el comando `type=` con el valor de `catalog::UserType` y, en caso de que no coincida, devolverá un error en lugar de contenido potencialmente inapropiado.

## Véase también {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Referencia del catálogo  [de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
