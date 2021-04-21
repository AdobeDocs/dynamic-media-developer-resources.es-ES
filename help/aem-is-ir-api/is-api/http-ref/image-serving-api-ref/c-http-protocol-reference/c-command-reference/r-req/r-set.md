---
description: Información del conjunto de medios.
solution: Experience Manager
title: ajustar
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 4%

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
  <td class="stentry"> <p>Identificador de solicitud única </p></td> 
 </tr> 
</table>

Devuelve información sobre imágenes, vídeos, muestras y varios metadatos asociados al catálogo::ImageSet para la entrada de catálogo de imágenes especificada en la ruta URL. Esta respuesta es una estructura jerárquica determinada por el tipo de conjunto proporcionado. Se aplica el formato adecuado cuando se solicita el formato &quot;xml&quot; o &quot;json&quot;.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::NonImgExpiration`.

>[!NOTE]
>
>No se permite el carácter de dos puntos en las solicitudes req=set.

Las solicitudes que admiten el formato de respuesta JSON le permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
