---
description: Seleccionar objeto por nombre. Selecciona el grupo de viñetas especificado por su nombre e inicia un nuevo MSS.
seo-description: Seleccionar objeto por nombre. Selecciona el grupo de viñetas especificado por su nombre e inicia un nuevo MSS.
seo-title: obj
solution: Experience Manager
title: obj
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 4%

---


# obj{#obj}

Seleccionar objeto por nombre. Selecciona el grupo de viñetas especificado por su nombre e inicia un nuevo MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre del grupo o ruta/nombre. </p> </td> 
 </tr> 
</table>

Se pueden seleccionar subgrupos u objetos individuales utilizando una ruta de grupo completa (es decir, especificando el nombre del grupo u objeto de destino precedido por todos los grupos principales, separados por / (barras inclinadas).

Si no se encuentra ningún grupo u objeto con el nombre especificado, se realiza la acción especificada en `attribute::OnObjFail`.

## Propiedades {#section-9463b36e8ff74c81a70c7c2b58927430}

Selección, comando; delimitador MSS. La selección de objetos es persistente hasta que se selecciona otro objeto, ya sea con `obj=` o `sel=`.

Los nombres y las rutas de grupo/objeto no distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-0c322850512c4896bb551856a549440e}

El primer grupo de la viñeta que contiene objetos procesables se selecciona automáticamente cuando se abre una nueva viñeta.

## Véase también {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [atributo::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
