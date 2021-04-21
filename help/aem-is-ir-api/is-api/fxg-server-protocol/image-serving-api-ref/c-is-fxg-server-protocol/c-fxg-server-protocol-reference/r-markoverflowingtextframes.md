---
description: Mostrar marcos de texto desbordados con el signo más. El indicador de desbordamiento de texto muestra si el texto se sale del espacio que tiene asignado en un marco de texto (o en el último marco de texto si se trata de un texto enlazado). Este indicador es un cuadro rojo con un signo más en su interior.
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 59%

---


# markOverflowingTextFrames{#markoverflowingtextframes}

Mostrar marcos de texto desbordados con el signo más. El indicador de desbordamiento de texto muestra si el texto se sale del espacio que tiene asignado en un marco de texto (o en el último marco de texto si se trata de un texto enlazado). Este indicador es un cuadro rojo con un signo más en su interior.

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverflowingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Si se configura el modificador `markOverflowingTextFrames=1` mediante una llamada a la dirección URL, se marcan todos los marcos de texto donde el texto se sobrescribe con un signo más. Además, en la vista previa de Dynamic Media Classic, el indicador de desbordamiento de texto está establecido en &quot; `TRUE`&quot; de forma predeterminada.

El valor predeterminado es 0.
