---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Especifica cuándo mostrar el panel de información. </p> <p>Si está configurado como <span class="codeph"> 1</span>, el panel de información se muestra cuando el ratón entra en el área del mapa de imagen (en caso de que el mapa de imagen no esté vacío, <span class="codeph"> rollover_key</span> ). </p> <p>Si está configurado como <span class="codeph"> 0</span> el panel de información se activa cuando se selecciona el mapa de imagen (si el mapa de imagen tiene un valor que no esté vacío) <span class="codeph"> rollover_key</span> y vacío <span class="codeph"> href</span> atributos). </p> <p> Se omite en dispositivos táctiles, incluidos los sistemas de escritorio con capacidad táctil, y se establece automáticamente como <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-ccfedc2da28f412a86d03f390db92b4b}

Opcional.

## Predeterminado {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Ejemplo {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
