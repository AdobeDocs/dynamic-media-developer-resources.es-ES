---
description: Validación de solicitud.
seo-description: Validación de solicitud.
seo-title: validar
solution: Experience Manager
title: validar
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# validar{#validate}

Validación de solicitud.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitud único. </p></td> 
 </tr> 
</table>

Analiza la cadena de solicitud como si `req=img` se hubiera especificado, pero sin sustituir las variables ni evaluar los objetos a los que se hace referencia (imágenes, perfiles ICC, fuentes, etc.). Se devuelve la respuesta de error estándar si falla el análisis; de lo contrario, se devuelve la siguiente propiedad:

`request.isValid=1`

La respuesta HTTP no se puede almacenar en caché.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del `req=` parámetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
