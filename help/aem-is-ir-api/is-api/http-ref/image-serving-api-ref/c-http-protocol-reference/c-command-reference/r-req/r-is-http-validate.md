---
description: Solicitar validación.
seo-description: Solicitar validación.
seo-title: validar
solution: Experience Manager
title: validar
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---


# validar{#validate}

Solicitar validación.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitud única. </p></td> 
 </tr> 
</table>

Analiza la cadena de solicitud como si se hubiera especificado `req=img`, pero sin sustituir las variables y evaluar los objetos referenciados (imágenes, perfiles ICC, fuentes, etc.). La respuesta de error estándar se devuelve si falla el análisis; de lo contrario, se devuelve la siguiente propiedad:

`request.isValid=1`

La respuesta HTTP no se puede almacenar en caché.

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
