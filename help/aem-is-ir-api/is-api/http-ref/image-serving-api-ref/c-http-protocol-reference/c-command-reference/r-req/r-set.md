---
description: Información del conjunto de medios.
solution: Experience Manager
title: ajustar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
TQID: 'https://experienceleague.adobe.com/nfNdFeRk7TDhSYHdy05x6fxNKMBhTF7f11xoji13VP4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 144
ht-degree: 2%

---

# ajustar{#set}

Información del conjunto de medios.

req=set[,xml[, *`encoding`*]|&lbrace;json[&amp;id=*`reqId`*]]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificación</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identificador único de la solicitud </p></td> 
 </tr> 
</table>

Devuelve información sobre imágenes, vídeos, muestras y diversos metadatos asociados a catalog::ImageSet para la entrada de catálogo de imágenes especificada en la ruta URL. Esta respuesta es una estructura jerárquica determinada por el tipo de conjunto proporcionado. Se aplica el formato adecuado cuando se solicita el formato &quot;xml&quot; o &quot;json&quot;.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::NonImgExpiration`.

>[!NOTE]
>
>No se permite el carácter de dos puntos en las solicitudes req=set.

Las solicitudes que admiten el formato de respuesta JSON le permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
