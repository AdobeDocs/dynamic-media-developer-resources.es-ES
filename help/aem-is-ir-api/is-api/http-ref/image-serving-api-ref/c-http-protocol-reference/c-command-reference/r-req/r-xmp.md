---
description: Metadatos XMP. Devuelve los metadatos de XMP asociados a la imagen especificada en la ruta de la solicitud.
seo-description: Metadatos XMP. Devuelve los metadatos de XMP asociados a la imagen especificada en la ruta de la solicitud.
seo-title: xmp
solution: Experience Manager
title: xmp
topic: Scene7 Image Serving - Image Rendering API
uuid: e1583ffe-531a-4334-b974-72df6fcb14ba
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---


# xmp{#xmp}

Metadatos XMP. Devuelve los metadatos de XMP asociados a la imagen especificada en la ruta de la solicitud.

`req=xmp`

Se omiten otros comandos. Se aplica la codificación UTF-8. La respuesta está formateada como XML con tipo MIME `text/xml`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.

## Propiedades {#section-0d26b6a56c844153ae5cea4880370d00}

Solicitar atributo. Se aplica independientemente de la configuración de la capa actual.

## Predeterminado {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

Si la dirección URL no incluye una ruta de imagen o modificadores, entonces:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

De lo contrario, `req=img`

## Ejemplos {#section-34213692deab4a0f9037d5844132ee14}

Propiedades del archivo de imagen de consulta.

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Propiedades del catálogo de imágenes de consulta:

` http:// *`server`*/myRootId?req=catalogprops`

Acceda a las propiedades de una entrada de catálogo de imágenes desde JavaScript del lado del cliente incrustado en un archivo HTML:

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

Recupere la imagen de máscara para una entrada de catálogo concreta, con una escala del 25 % del tamaño original:

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Solicite una imagen de un octavo tamaño:

` http:// *`server`*/myRootId/myImageId?scl=8`

Esto es lo mismo que:

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

Solicite una miniatura de una imagen, basándose en los atributos de miniatura especificados en el catálogo de imágenes:

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Enviar un mensaje de texto a los registros del servidor:

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## Véase también {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [catálogo::Destinatarios](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),  [catálogo::DatosUsuario](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md), Escala [ de ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)miniaturas,  [Propiedades](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9), Mapas  [de imagen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
