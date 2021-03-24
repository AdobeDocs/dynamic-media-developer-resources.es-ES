---
description: Habilita la optimización de FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Habilita la optimización de FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Elimina los elementos cuya visibilidad se establece como falsa en FXG mientras pasa este FXG, lo que a su vez reduce el tiempo de procesamiento de FXG. Aunque elimina solo aquellos elementos con visibilidad como falsos que no afectarían a ningún otro elemento en FXG. Por ejemplo, si hay texto en `Path` y la visibilidad de `Path` se establece como falsa, no se elimina de FXG aunque este modificador esté habilitado porque el texto debe dibujarse en esta ruta.

El valor predeterminado es 1.
