---
description: Habilita la optimización de FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
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

Elimina los elementos cuya visibilidad se establece como falsa en FXG mientras pasa este FXG, lo que a su vez reduce el tiempo de procesamiento de FXG. Aunque elimina solo aquellos elementos con visibilidad como falsos que no afectarían a ningún otro elemento en FXG. Por ejemplo, si hay texto en `Path` y la visibilidad de `Path` se establece como falsa, no se elimina de FXG aunque este modificador esté habilitado porque el texto debe dibujarse en esta ruta.

El valor predeterminado es 1.
