---
description: Eliminar el resultado de un trabajo.
seo-description: Eliminar el resultado de un trabajo.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Scene7 Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobdelete{#batchjobdelete}

Eliminar el resultado de un trabajo.

Si un trabajo se está ejecutando actualmente, se detiene inmediatamente y se elimina toda la información de procesamiento. Si el trabajo se ha completado correctamente, se elimina su archivo de salida.

Este parámetro:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>Id. de trabajo obtenido en el momento del envío. </p></td> 
 </tr> 
</table>

Devuelve:

Estado del trabajo en el momento de recibir la solicitud de eliminación, error si `jobid` no es válido o ya se ha eliminado el trabajo.

## Ejemplo {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
