---
description: Si jsonp se especifica como formato de respuesta, los datos de respuesta tienen un formato JSONP (Notación de objeto JavaScript con relleno), incluido en una llamada de función JavaScript.
seo-description: Si jsonp se especifica como formato de respuesta, los datos de respuesta tienen un formato JSONP (Notación de objeto JavaScript con relleno), incluido en una llamada de función JavaScript.
seo-title: Propiedades de JSONP
solution: Experience Manager
title: Propiedades de JSONP
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 1%

---


# Propiedades JSONP{#jsonp-properties}

Si jsonp se especifica como formato de respuesta, los datos de respuesta tienen un formato JSONP (Notación de objeto JavaScript con relleno), incluido en una llamada de función JavaScript.

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

El cliente debe definir la función JavaScript `s7jsonResponse`. En su forma más sencilla, la función puede tener el siguiente aspecto:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Las solicitudes que admiten el formato de respuesta JSONP permiten especificar el nombre del controlador de llamada de retorno JS mediante la sintaxis extendida del parámetro `req=` :

`req=...,json [&handler = reqHandler]`

`<reqHandler>` es el nombre del controlador JS que está presente en la respuesta JSONP. Solo se permiten caracteres a-z, A-Z y 0-9. Opcional. El valor predeterminado es `s7jsonResponse`.

El paquete de visores de servicio de imágenes de Dynamic Media incluye una utilidad para solicitar y analizar datos con formato JSONP de Image Serving.

Consulte [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) para obtener más información sobre el formato JSONP.

Consulte [www.json.org](http://www.json.org) para obtener más información sobre el formato JSON.

Consulte también [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
