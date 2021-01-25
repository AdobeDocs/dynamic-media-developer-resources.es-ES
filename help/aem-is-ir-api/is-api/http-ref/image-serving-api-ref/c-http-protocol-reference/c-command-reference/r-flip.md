---
description: Voltear capa. Voltea la capa horizontalmente, verticalmente o ambas, después de aplicar el recorte= y antes de rotate= y extender=.
seo-description: Voltear capa. Voltea la capa horizontalmente, verticalmente o ambas, después de aplicar el recorte= y antes de rotate= y extender=.
seo-title: voltear
solution: Experience Manager
title: voltear
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---


# flip{#flip}

Voltear capa. Voltea la capa horizontalmente, verticalmente o ambas, después de aplicar el recorte= y antes de rotate= y extender=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>Voltear la capa horizontalmente (izquierda-derecha). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>Voltear la capa verticalmente (arriba-abajo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>Voltear horizontal y verticalmente. </p> </td> 
 </tr> 
</table>

También se puede aplicar a capas de texto.

Algunos comandos, incluido `extend=`, se aplican implícitamente a la capa 0 en lugar de a la capa compuesta cuando se selecciona `layer=comp`. En estos casos, todos los comandos asignados automáticamente a la capa 0 se aplicarán antes que los comandos que se apliquen a `layer=comp`. Por lo tanto, cuando `layer=comp`, `extend=` se aplica antes que `flip=`.

>[!NOTE]
>
>La capa invertida se coloca en función del anclaje de la capa; diferentes valores de flip= tendrán diferentes posiciones de capa cuando el anclaje no se encuentre en el centro de la capa.

## Propiedades {#section-294da2af7be746b5adfc35e29ee68217}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Omitido por capas de efectos.

## Predeterminado {#section-502044f81a89492198d5f12a738459ea}

Ninguno.

## Véase también {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
