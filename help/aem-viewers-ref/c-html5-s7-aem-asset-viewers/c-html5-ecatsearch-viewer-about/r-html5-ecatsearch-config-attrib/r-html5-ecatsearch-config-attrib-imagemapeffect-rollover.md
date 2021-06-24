---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,Business Practitioner
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Especifica cuándo mostrar el panel de información. </p> <p>Si se establece en <span class="codeph"> 1</span>, el panel de información se muestra cuando el ratón entra en el área del mapa de imagen (en caso de que el mapa de imagen tenga un atributo <span class="codeph"> rollover_key</span> no vacío). </p> <p>Si se establece en <span class="codeph"> 0</span> el panel de información se activa cuando se hace clic en el mapa de imagen (si el mapa de imagen tiene atributos <span class="codeph"> rollover_key</span> no vacíos y <span class="codeph"> href</span> vacíos). </p> <p> Se omite en dispositivos táctiles, incluidos los sistemas de escritorio con capacidad táctil, y se establece automáticamente en <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-ccfedc2da28f412a86d03f390db92b4b}

Opcional.

## Predeterminado {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Ejemplo {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
