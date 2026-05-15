---
title: batchjobdelete
description: Eliminar el resultado de un trabajo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
TQID: 'https://experienceleague.adobe.com/1UB1BxMzt2kGisK6gosRfoI1LEilkLyHJvfP1AJbwwI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

Eliminar el resultado de un trabajo.

Si un trabajo se está ejecutando actualmente, se detiene inmediatamente y se elimina toda su información de procesamiento. Si el trabajo se ha completado correctamente, se elimina su archivo de salida.

Este parámetro:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>ID de trabajo que se obtuvo en el momento del envío. </p></td> 
 </tr> 
</table>

Devuelve:

Estado del trabajo en el momento en que se recibió la solicitud de eliminación, error si `jobid` no es válido o el trabajo ya se había eliminado.

## Ejemplo {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
