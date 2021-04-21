---
description: Voltear capa. Gira la capa horizontalmente, verticalmente o ambas, después de aplicar recorte= y antes de rotar= y ampliar=.
solution: Experience Manager
title: voltear
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# flip{#flip}

Voltear capa. Gira la capa horizontalmente, verticalmente o ambas, después de aplicar recorte= y antes de rotar= y ampliar=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>Girar la capa horizontalmente (izquierda-derecha). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>Girar la capa verticalmente (arriba hacia abajo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>Girar horizontal y verticalmente. </p> </td> 
 </tr> 
</table>

También se puede aplicar a capas de texto.

Algunos comandos, incluido `extend=`, se aplican implícitamente a la capa 0 en lugar de a la capa compuesta cuando se selecciona `layer=comp`. En estos casos, todos los comandos que se asignan automáticamente a la capa 0 se aplican antes que los comandos que se aplican a `layer=comp`. Por lo tanto, cuando `layer=comp`, `extend=` se aplica antes que `flip=`.

>[!NOTE]
>
>La capa girada se coloca en función del anclaje de la capa; distintos valores flip= tendrán diferentes posiciones de capa cuando el anclaje no esté situado en el centro de la capa.

## Propiedades {#section-294da2af7be746b5adfc35e29ee68217}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto.

## Predeterminado {#section-502044f81a89492198d5f12a738459ea}

Ninguno.

## Véase también {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
