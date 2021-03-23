---
description: Eliminar el resultado de un trabajo.
seo-description: Eliminar el resultado de un trabajo.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---


# batchjobdelete{#batchjobdelete}

Eliminar el resultado de un trabajo.

Si un trabajo se está ejecutando actualmente, se detiene inmediatamente y se elimina toda su información de procesamiento. Si el trabajo se ha completado correctamente, se elimina su archivo de salida.

Este parámetro:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>ID de trabajo obtenido en el momento del envío. </p></td> 
 </tr> 
</table>

Devuelve:

Estado del trabajo en el momento en que se recibió la solicitud de eliminación, error si `jobid` no es válido o el trabajo ya se había eliminado.

## Ejemplo {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
