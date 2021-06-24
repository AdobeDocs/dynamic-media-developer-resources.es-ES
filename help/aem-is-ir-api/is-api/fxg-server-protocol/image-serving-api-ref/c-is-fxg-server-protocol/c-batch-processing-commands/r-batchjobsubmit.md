---
description: Ejecute un nuevo trabajo por lotes.
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 2%

---

# batchjobsubmit{#batchjobsubmit}

Ejecute un nuevo trabajo por lotes.

Este parámetro:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata  </span> </p> </td> 
  <td class="stentry"> <p>Fragmento XML de datos de trabajo completos. </p> </td> 
 </tr> 
</table>

Devuelve:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Estado del trabajo </p> </td> 
  <td class="stentry"> <p>Si el envío se ha realizado correctamente o no; si se realiza correctamente, ID de trabajo en formato XML. </p> </td> 
 </tr> 
</table>

## Ejemplo {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
