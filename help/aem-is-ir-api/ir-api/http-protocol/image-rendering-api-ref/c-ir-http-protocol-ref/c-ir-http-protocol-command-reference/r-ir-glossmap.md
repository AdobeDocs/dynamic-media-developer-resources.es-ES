---
title: glosmap
description: Imagen de mapa brillante. Proporciona control píxel a píxel del brillo de una textura, papel tapiz/borde o calcomanía repetibles.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
TQID: 'https://experienceleague.adobe.com/H-Ip9cbtirNaAhfQwr1lj6T3hYdiD1uG-NdQvCJB1v4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# glosmap {#glossmap}

Imagen de mapa brillante. Proporciona control píxel a píxel del brillo de una textura, papel tapiz/borde o calcomanía repetibles.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> ForeignReq</span>'&amp;rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Archivo de imagen de mapa brillante (escala de grises). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Solicitud al servidor de imágenes. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ForeignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Solicitud a un servidor externo. </p></td> 
 </tr> 
</table>

Aplicable a materiales como efectos de pintura metálica, papel pintado troquelado, bordes y tejidos de hilo metálico.

La imagen del mapa de resplandor debe ser de escala de grises de 8 bits y tener el mismo tamaño que la imagen principal especificada con `src=`. Consulte la descripción de [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obtener información adicional.

## Propiedades {#section-26375672d69849be9b026cc93c3bc558}

Atributo de material. Apoyado por texturas repetibles, fondos de pantalla y bordes, y calcomanías. Ignorado por el color sólido, el gabinete y los materiales de recubrimiento de ventana. Consulte [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obtener información adicional.

## Predeterminado {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Ninguno.

## Véase también {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
