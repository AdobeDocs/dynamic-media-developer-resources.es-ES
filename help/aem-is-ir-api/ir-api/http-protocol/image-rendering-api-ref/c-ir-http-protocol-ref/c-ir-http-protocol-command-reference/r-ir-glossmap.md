---
description: Imagen de mapa brillante. Proporciona control píxel a píxel de la luminosidad de una textura, papel tapiz/borde repetible o calcomanía.
seo-description: Imagen de mapa brillante. Proporciona control píxel a píxel de la luminosidad de una textura, papel tapiz/borde repetible o calcomanía.
seo-title: glossmap
solution: Experience Manager
title: glossmap
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# glossmap{#glossmap}

Imagen de mapa brillante. Proporciona control píxel a píxel de la luminosidad de una textura, papel tapiz/borde repetible o calcomanía.

`glossmap={ *``*| *`glossMapFileEmbeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> EmbeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;Lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> externalReq</span>'&amp;rbrace;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Archivo de imagen de mapa de brillo (escala de grises). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Solicitar al servidor de imágenes. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ForeignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>Solicitud a un servidor externo. </p></td> 
 </tr> 
</table>

Aplicable a materiales tales como pinturas metálicas, tapicerías y bordes de hojas cortadas, telas metálicas, etc.

La imagen del mapa de brillo debe tener una escala de grises de 8 bits y tener exactamente el mismo tamaño que la imagen principal especificada con `src=`. Consulte la descripción de [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obtener más información.

## Propiedades {#section-26375672d69849be9b026cc93c3bc558}

Atributo de material. Admitido por texturas repetibles, fondos de pantalla y bordes, y calcomanías. Ignorado por materiales de color sólido, gabinete y recubrimiento de ventanas. Consulte [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obtener más información.

## Predeterminado {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Ninguno.

## Véase también {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
