---
description: Habilita la optimización de FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Habilita la optimización de FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Elimina los elementos cuya visibilidad está establecida como false en FXG mientras pasa este FXG, lo que a su vez reduce el tiempo de procesamiento de FXG. Aunque elimina solo aquellos elementos con visibilidad como false que no afectarían a ningún otro elemento en FXG. Por ejemplo, si hay texto en `Path` y la visibilidad de `Path` está establecida como falsa, entonces no se quita de FXG incluso con este modificador habilitado porque el texto debe dibujarse en esta ruta.

El valor predeterminado es 1.
