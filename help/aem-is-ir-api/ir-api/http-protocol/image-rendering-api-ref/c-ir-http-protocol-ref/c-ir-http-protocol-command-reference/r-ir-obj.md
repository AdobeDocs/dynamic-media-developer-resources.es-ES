---
title: obj
description: Seleccionar objeto por nombre. Selecciona el grupo de viñetas especificado por nombre e inicia un nuevo SMS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 4%

---

# obj{#obj}

Seleccionar objeto por nombre. Selecciona el grupo de viñetas especificado por nombre e inicia un nuevo SMS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre del grupo o ruta/nombre. </p> </td> 
 </tr> 
</table>

Los subgrupos u objetos individuales pueden seleccionarse utilizando una ruta de grupo completa (es decir, especificando el nombre del grupo de destino u objeto precedido por todos los grupos principales, separados por / (barras diagonales)).

Si no se encuentra ningún grupo u objeto con el nombre especificado, la acción especificada en `attribute::OnObjFail` está ocupado.

## Propiedades {#section-9463b36e8ff74c81a70c7c2b58927430}

Comando de selección; delimitador SMS. La selección de objetos es persistente hasta que se selecciona otro objeto, ya sea con `obj=` o `sel=`.

Las rutas y los nombres de grupos/objetos no distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-0c322850512c4896bb551856a549440e}

El primer grupo de la viñeta que contiene objetos procesables se selecciona automáticamente al abrir una nueva viñeta.

## Véase también {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
