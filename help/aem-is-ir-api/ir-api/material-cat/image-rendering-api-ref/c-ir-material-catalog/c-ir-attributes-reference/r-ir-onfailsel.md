---
description: Gestión de errores de selección. Especifica la acción que se debe realizar si el comando sel= falla porque la ubicación de píxeles especificada no está dentro del área de máscara de un objeto seleccionable.
seo-description: Gestión de errores de selección. Especifica la acción que se debe realizar si el comando sel= falla porque la ubicación de píxeles especificada no está dentro del área de máscara de un objeto seleccionable.
seo-title: OnFailSel
solution: Experience Manager
title: OnFailSel
topic: Scene7 Image Serving - Image Rendering API
uuid: 073b6651-970c-460c-b044-e3ef37cc677a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# OnFailSel{#onfailsel}

Gestión de errores de selección. Especifica la acción que se debe realizar si el comando sel= falla porque la ubicación de píxeles especificada no está dentro del área de máscara de un objeto seleccionable.

## Propiedades {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Heredar de <span class="codeph"> forma predeterminada::OnFailSel </span>. </p> </td> 
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

## Predeterminado {#section-c25f458f9f8f4236963a95779529e664}

Se hereda de `default::OnFailSel` si no se define.

## Véase también {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [atributo::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
