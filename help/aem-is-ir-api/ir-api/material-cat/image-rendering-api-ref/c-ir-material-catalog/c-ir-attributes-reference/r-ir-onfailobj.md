---
title: OnFailObj
description: Control de errores de selección de objetos. Especifica las acciones que deben realizarse si el comando obj= no funciona porque la ruta de acceso especificada no puede coincidir en la jerarquía de objetos de viñeta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
TQID: 'https://experienceleague.adobe.com/fHutIGRe9bnq6VfuVdggXDJU6Z3uMeGtDgukP6pdSDw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 7%

---

# OnFailObj{#onfailobj}

Control de errores de selección de objetos. Especifica las acciones que deben realizarse si el comando obj= no funciona porque la ruta de acceso especificada no puede coincidir en la jerarquía de objetos de viñeta.

## Propiedades {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enumeración.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Heredar de <span class="codeph"> default::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Mantener la selección anterior. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Anular la selección; se ignorará cualquier intento de aplicar un material o mostrar/ocultar objetos. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Devolver un error. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Seleccione el grupo predeterminado (el primero de la jerarquía de viñetas que contiene objetos procesables). </p> </td> 
 </tr> 
</table>

## Predeterminado {#section-a5a95a2b4a204a4eae350e5b544d1513}

Se hereda de `default::OnFailObj` si no se define.

## Véase también {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [atributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)

