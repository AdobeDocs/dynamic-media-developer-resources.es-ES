---
description: Enviar un nuevo trabajo por lotes.
seo-description: Enviar un nuevo trabajo por lotes.
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
topic: Scene7 Image Serving - Image Rendering API
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobsubmit{#batchjobsubmit}

Enviar un nuevo trabajo por lotes.

Este parámetro:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata </span> </p> </td> 
  <td class="stentry"> <p>Fragmento XML de datos de trabajo completos. </p> </td> 
 </tr> 
</table>

Devuelve:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Estado del trabajo </p> </td> 
  <td class="stentry"> <p>Si el envío se realizó correctamente o no; si se realiza correctamente, ID de trabajo en formato XML. </p> </td> 
 </tr> 
</table>

## Ejemplo {#section-3886e8352e26419c97b24df21ca7f6fd}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&amp;jobdata=<URLEncodedXMLFileContents>]
