---
description: Recupere el estado detallado de un trabajo enviado.
seo-description: Recupere el estado detallado de un trabajo enviado.
seo-title: batchjobdetail estado
solution: Experience Manager
title: batchjobdetail estado
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '63'
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
