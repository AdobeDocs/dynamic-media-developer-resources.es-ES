---
description: Voltear capa. Gira la capa horizontalmente, verticalmente o ambas, después de aplicar recorte= y antes de rotar= y ampliar=.
solution: Experience Manager
title: voltear
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# voltear{#flip}

Voltear capa. Gira la capa horizontalmente, verticalmente o ambas, después de aplicar recorte= y antes de rotar= y ampliar=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Girar la capa horizontalmente (izquierda-derecha). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Girar la capa verticalmente (arriba hacia abajo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Girar horizontal y verticalmente. </p> </td> 
 </tr> 
</table>

También se puede aplicar a capas de texto.

Algunos comandos, incluidos `extend=`, se aplican implícitamente a la capa 0 en lugar de a la capa compuesta cuando `layer=comp` está seleccionado. En estos casos, todos los comandos que se asignan automáticamente a la capa 0 se aplican antes que los comandos que se aplican a `layer=comp`. Por lo tanto, cuando `layer=comp`, `extend=` se aplica antes de que `flip=`.

>[!NOTE]
>
>La capa girada se coloca en función del anclaje de la capa; distintos valores flip= tendrán diferentes posiciones de capa cuando el anclaje no esté situado en el centro de la capa.

## Propiedades {#section-294da2af7be746b5adfc35e29ee68217}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto.

## Predeterminado {#section-502044f81a89492198d5f12a738459ea}

Ninguno.

## Véase también {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
