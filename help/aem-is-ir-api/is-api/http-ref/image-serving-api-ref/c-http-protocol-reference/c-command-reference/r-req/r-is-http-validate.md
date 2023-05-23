---
description: Validación de solicitud.
solution: Experience Manager
title: validar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 4%

---

# validar{#validate}

Validación de solicitud.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador único de la solicitud. </p></td> 
 </tr> 
</table>

Analiza la cadena de solicitud como si `req=img` se especificaron, pero sin sustituir variables ni evaluar objetos referenciados (imágenes, perfiles ICC, fuentes, etc.). La respuesta de error estándar se devuelve si falla el análisis; de lo contrario, se devuelve la siguiente propiedad:

`request.isValid=1`

La respuesta HTTP no se puede almacenar en caché.

Las solicitudes compatibles con el formato de respuesta JSONP permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida de `req=` parámetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
