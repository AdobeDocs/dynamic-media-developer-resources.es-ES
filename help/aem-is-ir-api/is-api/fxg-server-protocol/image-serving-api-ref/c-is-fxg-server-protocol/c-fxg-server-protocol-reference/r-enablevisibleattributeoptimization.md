---
description: Habilita la optimización de FXG.
seo-description: Habilita la optimización de FXG.
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Scene7 Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Habilita la optimización de FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Elimina los elementos cuya visibilidad se establece como false en FXG mientras se pasa este FXG, lo que a su vez reduce el tiempo de procesamiento de FXG. Aunque solo elimina los elementos con visibilidad como falsos que no afectarían a ningún otro elemento en FXG. Por ejemplo, si hay texto activado `Path` y la visibilidad de `Path` se establece como falso, no se elimina de FXG aunque este modificador esté activado porque el texto debe dibujarse en esta ruta.

El valor predeterminado es 1.
