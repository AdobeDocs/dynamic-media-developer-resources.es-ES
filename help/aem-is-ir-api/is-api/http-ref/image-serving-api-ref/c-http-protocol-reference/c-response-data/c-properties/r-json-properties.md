---
description: Si jsonp se especifica como formato de respuesta, los datos de respuesta se formatean con JSONP (JavaScript Object Notation with Padding), ajustado en una llamada de función JavaScript.
seo-description: Si jsonp se especifica como formato de respuesta, los datos de respuesta se formatean con JSONP (JavaScript Object Notation with Padding), ajustado en una llamada de función JavaScript.
seo-title: Propiedades de JSONP
solution: Experience Manager
title: Propiedades de JSONP
topic: Scene7 Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Propiedades de JSONP{#jsonp-properties}

Si jsonp se especifica como formato de respuesta, los datos de respuesta se formatean con JSONP (JavaScript Object Notation with Padding), ajustado en una llamada de función JavaScript.

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

La función `s7jsonResponse` JavaScript debe ser definida por el cliente. En su forma más sencilla, la función podría tener el siguiente aspecto:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=`:

`req=...,json [&handler = reqHandler]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten los caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

El paquete de visores de servicio de imágenes de Scene7 incluye una utilidad para solicitar y analizar datos con formato JSONP del servicio de imágenes.

Consulte [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) para obtener más información sobre el formato JSONP.

Consulte [www.json.org](http://www.json.org) para obtener más información sobre el formato JSON.

Consulte también [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
