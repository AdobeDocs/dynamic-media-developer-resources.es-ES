---
title: batchjobbriefStatus
description: Recuperar el estado resumido de un trabajo enviado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 13991f71ab54d1003a79a496b861d53a61899bdc
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# batchjobbriefStatus{#batchjobbriefstatus}

Recuperar el estado resumido de un trabajo enviado.

Este parámetro:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> id. de trabajo </span> </p> </td> 
  <td class="stentry"> <p>ID de trabajo que se obtuvo en el momento del envío. </p> </td> 
 </tr> 
</table>

Devuelve:

Estado breve del trabajo en formato XML; error si el trabajo no es válido o si el trabajo se ha eliminado.

## Ejemplo {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbrief&amp;jobid=1005907604914d8eb63126b98f7172n76a5]
