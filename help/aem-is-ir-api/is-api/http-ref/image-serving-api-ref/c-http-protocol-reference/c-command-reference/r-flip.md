---
title: voltear
description: Voltear capa. Voltea la capa horizontal, verticalmente o ambas, después de aplicar crop= y antes de rotate= y extend=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
TQID: 'https://experienceleague.adobe.com/7RG0rzG40Mp5eQe663S5Ayyf99SIfSLPHgqbSL2Unn4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 2%

---

# voltear{#flip}

Voltear capa. Voltea la capa horizontal, verticalmente o ambas, después de aplicar crop= y antes de rotate= y extend=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Voltee la capa horizontalmente (izquierda-derecha). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>Voltee la capa verticalmente (arriba-abajo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Voltee horizontal y verticalmente. </p> </td> 
 </tr> 
</table>

También se puede aplicar a capas de texto.

Algunos comandos, incluido `extend=`, se aplican implícitamente a la capa 0 en lugar de a la capa compuesta cuando se selecciona `layer=comp`. En estos casos, todos los comandos asignados automáticamente a la capa 0 se aplican antes que los comandos que se aplican a `layer=comp`. Por lo tanto, cuando `layer=comp`, `extend=` se aplica antes de `flip=`.

>[!NOTE]
>
>La capa volteada se coloca en función del anclaje de la capa. Los distintos valores de `flip=` dan como resultado diferentes posiciones de capa cuando el anclaje no está en el centro de la capa.

## Propiedades {#section-294da2af7be746b5adfc35e29ee68217}

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-502044f81a89492198d5f12a738459ea}

Ninguno.

## Véase también {#section-47f6484deccd420983df15ec163b4a83}

[rotar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anclaje=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
