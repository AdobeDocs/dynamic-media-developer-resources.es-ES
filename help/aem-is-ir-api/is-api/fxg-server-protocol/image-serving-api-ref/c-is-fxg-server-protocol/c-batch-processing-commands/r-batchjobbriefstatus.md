---
description: Recupere el estado resumido de un trabajo enviado.
seo-description: Recupere el estado resumido de un trabajo enviado.
seo-title: batchjobbristatus
solution: Experience Manager
title: batchjobbristatus
uuid: 601e8395-8a77-4324-9cd7-5fe321bc91e3
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---


# batchjobbristatus{#batchjobbriefstatus}

Recupere el estado resumido de un trabajo enviado.

Este parámetro:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID de trabajo obtenido en el momento del envío. </p> </td> 
 </tr> 
</table>

Devuelve:

Breve estado del trabajo en formato XML; error si el trabajo no es válido o se ha eliminado el trabajo.

## Ejemplo {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
