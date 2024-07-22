---
description: Recuperar el estado detallado de un trabajo enviado.
solution: Experience Manager
title: batchjobdetailed status
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd385327-29af-448c-9a25-75098b578272
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 2%

---

# batchjobdetailed status{#batchjobdetailedstatus}

Recuperar el estado detallado de un trabajo enviado.

Este parámetro:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> id. de trabajo </span> </p> </td> 
  <td class="stentry"> <p>ID de trabajo que se obtuvo en el momento del envío. </p> </td> 
 </tr> 
</table>

Devuelve:

Estado detallado del trabajo en formato XML; error si `jobid` no es válido o el trabajo se ha eliminado.

## Ejemplo {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
