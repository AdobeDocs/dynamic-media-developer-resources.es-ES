---
description: Recupere el estado detallado de un trabajo enviado.
solution: Experience Manager
title: batchjobdetail estado
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 1%

---


# batchjobdetail estado{#batchjobdetailedstatus}

Recupere el estado detallado de un trabajo enviado.

Este parámetro:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID de trabajo obtenido en el momento del envío. </p> </td> 
 </tr> 
</table>

Devuelve:

Estado detallado del trabajo en formato XML; error si `jobid` no es válido o el trabajo se ha eliminado.

## Ejemplo {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
