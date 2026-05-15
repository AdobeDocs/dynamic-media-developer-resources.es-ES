---
title: Propiedades JSONP
description: Si se especifica jsonp como formato de respuesta, los datos de respuesta se formatean con JSONP (Notación de objetos JavaScript con relleno), dentro de una llamada a la función JavaScript.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
TQID: 'https://experienceleague.adobe.com/pMirwhZ5n0mVuK2If4kJz3XDQZPDhORJCZBLsDf2C8I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Propiedades JSONP{#jsonp-properties}

Si se especifica jsonp como formato de respuesta, los datos de respuesta se formatean con JSONP (Notación de objetos JavaScript con relleno), dentro de una llamada a la función JavaScript.

El cliente puede especificar un identificador de solicitud único opcional (*`reqId`*), que se devuelve en la respuesta y permite al cliente distinguir varias respuestas recibidas de manera asincrónica. Una respuesta típica tiene la siguiente estructura general:

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

El cliente debe definir la función JavaScript `s7jsonResponse`. En su forma más sencilla, la función podría tener este aspecto:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Las solicitudes compatibles con el formato de respuesta JSONP le permiten especificar el nombre del controlador de devolución de llamada JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler]`

La sintaxis `<reqHandler>` es el nombre del controlador JS presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

El paquete Visualizadores de servicio de imágenes de Dynamic Media incluye una utilidad para solicitar y analizar datos con formato JSONP desde el servicio de imágenes.

Consulte [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) para obtener más información sobre el formato JSONP.

Consulte [www.json.org](https://www.json.org/json-en.html) para obtener más información sobre el formato JSON.

Consulte también [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
