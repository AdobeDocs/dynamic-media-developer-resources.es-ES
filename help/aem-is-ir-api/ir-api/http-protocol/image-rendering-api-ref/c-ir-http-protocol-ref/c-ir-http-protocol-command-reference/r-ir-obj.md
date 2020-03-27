---
description: Seleccione el objeto por nombre. Selecciona el grupo de viñetas especificado por su nombre y inicio un nuevo MSS.
seo-description: Seleccione el objeto por nombre. Selecciona el grupo de viñetas especificado por su nombre y inicio un nuevo MSS.
seo-title: obj
solution: Experience Manager
title: obj
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# obj{#obj}

Seleccione el objeto por nombre. Selecciona el grupo de viñetas especificado por su nombre y inicio un nuevo MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span></span> </p> </td> 
  <td class="stentry"> <p>Nombre del grupo o ruta/nombre. </p> </td> 
 </tr> 
</table>

Los subgrupos u objetos individuales pueden seleccionarse utilizando una ruta de grupo completa (es decir, especificando el nombre del grupo destinatario u objeto precedido por todos los grupos principales, separados por / (barras diagonales).

Si no se encuentra ningún grupo u objeto con el nombre especificado, se realiza la acción especificada en `attribute::OnObjFail` .

## Propiedades {#section-9463b36e8ff74c81a70c7c2b58927430}

Selección, comando; delimitador MSS. La selección de objetos es persistente hasta que se selecciona otro objeto, ya sea con `obj=` o `sel=`.

Los nombres y las rutas de grupo/objeto no distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-0c322850512c4896bb551856a549440e}

El primer grupo de la viñeta que contiene objetos procesables se selecciona automáticamente cuando se abre una nueva viñeta.

## Véase también {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [atributo::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
