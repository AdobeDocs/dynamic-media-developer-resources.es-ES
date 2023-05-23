---
title: Propiedades JSONP
description: Si se especifica jsonp como formato de respuesta, los datos de respuesta se formatean con JSONP (Notación de objetos JavaScript con relleno), dentro de una llamada de función JavaScript.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# Propiedades JSONP{#jsonp-properties}

Si se especifica jsonp como formato de respuesta, los datos de respuesta se formatean con JSONP (Notación de objetos JavaScript con relleno), dentro de una llamada de función JavaScript.

El cliente puede especificar un identificador de solicitud único opcional ( *`reqId`*), que se devuelve en la respuesta y permite al cliente distinguir varias respuestas recibidas asincrónicamente. Una respuesta típica tiene la siguiente estructura general:

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

El `s7jsonResponse` El cliente debe definir la función de JavaScript. En su forma más sencilla, la función podría tener este aspecto:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Las solicitudes compatibles con el formato de respuesta JSONP permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida de `req=` parámetro:

`req=...,json [&handler = reqHandler]`

El `<reqHandler>` La sintaxis es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

El paquete Visualizadores del servicio de imágenes de Dynamic Media incluye una utilidad para solicitar y analizar datos con formato JSONP desde el servicio de imágenes.

Consulte [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) para obtener más información sobre el formato JSONP.

Consulte [www.json.org](https://www.json.org/json-en.html) para obtener más información sobre el formato JSON.

Consulte también [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
