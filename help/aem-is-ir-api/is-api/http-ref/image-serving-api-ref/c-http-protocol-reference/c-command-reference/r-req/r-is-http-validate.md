---
description: Validación de solicitud.
solution: Experience Manager
title: validar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
TQID: 'https://experienceleague.adobe.com/TfgOIjG2q1CKAulErZYftqmKnCocuSF-H-dQTj4xsFI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 105
ht-degree: 2%

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

Analiza la cadena de solicitud como si se hubiera especificado `req=img`, pero sin sustituir variables ni evaluar objetos referenciados (imágenes, perfiles ICC, fuentes, etc.). La respuesta de error estándar se devuelve si falla el análisis; de lo contrario, se devuelve la siguiente propiedad:

`request.isValid=1`

La respuesta HTTP no se puede almacenar en caché.

Las solicitudes compatibles con el formato de respuesta JSONP le permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.
