---
description: Información del conjunto de medios.
seo-description: Información del conjunto de medios.
seo-title: ajustar
solution: Experience Manager
title: ajustar
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---


# ajustar{#set}

Información del conjunto de medios.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificación</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identificador único de solicitud </p></td> 
 </tr> 
</table>

Devuelve información sobre imágenes, vídeos, muestras y varios metadatos asociados con el catálogo::ImageSet para la entrada de catálogo de imágenes especificada en la ruta de URL. Esta respuesta es una estructura jerárquica determinada por el tipo de conjunto proporcionado. Se aplica el formato adecuado cuando se solicita el formato &#39;xml&#39; o &#39;json&#39;.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::NonImgExpiration`.

>[!NOTE]
>
>El carácter de dos puntos no está permitido en las solicitudes req=set.

Las solicitudes que admiten el formato de respuesta JSON le permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
