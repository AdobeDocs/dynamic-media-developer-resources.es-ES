---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
topic: Dynamic media
uuid: 276122d8-2109-42eb-be13-bead35cd3fe2
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---


# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Especifica cuándo se muestra el panel de información. </p> <p>Si se establece en <span class="codeph"> 1</span>, el panel de información se muestra cuando el ratón entra en el área del mapa de imagen (en caso de que el mapa de imagen tenga un atributo <span class="codeph"> rollover_key</span> no vacío). </p> <p>Si se establece en <span class="codeph"> 0</span> el panel de información se activa cuando se hace clic en el mapa de imagen (si el mapa de imagen tiene atributos <span class="codeph"> rollover_key</span> no vacíos y <span class="codeph"> href</span> vacíos). </p> <p> Se omite en dispositivos táctiles, incluidos los sistemas de escritorio táctiles, y se establece automáticamente en <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-ccfedc2da28f412a86d03f390db92b4b}

Opcional.

## Predeterminado {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Ejemplo {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
