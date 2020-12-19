---
description: Recuperar el estado detallado de un trabajo enviado.
seo-description: Recuperar el estado detallado de un trabajo enviado.
seo-title: batchjobdetail status
solution: Experience Manager
title: batchjobdetail status
topic: Scene7 Image Serving - Image Rendering API
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# batchjobdetail status{#batchjobdetailedstatus}

Recuperar el estado detallado de un trabajo enviado.

Este parámetro:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>Id. de trabajo obtenido en el momento del envío. </p> </td> 
 </tr> 
</table>

Devuelve:

Estado detallado del trabajo en formato XML; error si `jobid` no es válido o se ha eliminado el trabajo.

## Ejemplo {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
