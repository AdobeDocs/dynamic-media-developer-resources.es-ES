---
description: Gestión de errores de selección de objetos. Especifica la acción que se realizará si falla el comando obj= porque la ruta especificada no se puede hacer coincidir en la jerarquía de objetos de viñeta.
seo-description: Gestión de errores de selección de objetos. Especifica la acción que se realizará si falla el comando obj= porque la ruta especificada no se puede hacer coincidir en la jerarquía de objetos de viñeta.
seo-title: OnFailObj
solution: Experience Manager
title: OnFailObj
topic: Scene7 Image Serving - Image Rendering API
uuid: b9dcaf29-ffa5-47db-9c8c-d1809da73582
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# OnFailObj{#onfailobj}

Gestión de errores de selección de objetos. Especifica la acción que se realizará si falla el comando obj= porque la ruta especificada no se puede hacer coincidir en la jerarquía de objetos de viñeta.

## Propiedades {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Heredar de <span class="codeph"> forma predeterminada::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Mantener la selección anterior. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Anule la selección; se ignorará cualquier intento de aplicar un material o mostrar u ocultar objetos. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Devolver un mensaje de error. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Seleccione el grupo predeterminado (el primer grupo de la jerarquía de viñetas que contiene objetos procesables). </p> </td> 
 </tr> 
</table>

## Predeterminado {#section-a5a95a2b4a204a4eae350e5b544d1513}

Se hereda de `default::OnFailObj` si no se define.

## Véase también {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [atributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
