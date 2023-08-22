---
title: voltear
description: Voltear capa. Voltea la capa horizontal, verticalmente o ambas, después de aplicar crop= y antes de rotate= y extend=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# voltear{#flip}

Voltear capa. Voltea la capa horizontal, verticalmente o ambas, después de aplicar crop= y antes de rotate= y extend=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Voltear la capa horizontalmente (izquierda-derecha). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Voltear la capa verticalmente (arriba-abajo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> rudo </span> </p> </td> 
  <td class="stentry"> <p>Voltee horizontal y verticalmente. </p> </td> 
 </tr> 
</table>

También se puede aplicar a capas de texto.

Algunos comandos, incluidos `extend=`, se aplica implícitamente a la capa 0 en lugar de a la capa compuesta cuando `layer=comp` está seleccionado. En estos casos, todos los comandos que se asignan automáticamente a la capa 0 se aplican antes que los comandos que se aplican a `layer=comp`. Así, cuando `layer=comp`, `extend=` se aplica antes de `flip=`.

>[!NOTE]
>
>La capa volteada se coloca en función del anclaje de la capa; si el anclaje no se encuentra en el centro de la capa, los diferentes valores de flip= resultarán en diferentes posiciones de la capa.

## Propiedades {#section-294da2af7be746b5adfc35e29ee68217}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-502044f81a89492198d5f12a738459ea}

Ninguno.

## Véase también {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
