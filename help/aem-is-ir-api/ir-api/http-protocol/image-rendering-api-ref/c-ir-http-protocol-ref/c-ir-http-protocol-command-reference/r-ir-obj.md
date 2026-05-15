---
title: obj
description: Seleccionar objeto por nombre. Selecciona el grupo de viñetas especificado por nombre e inicia un nuevo SMS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
TQID: 'https://experienceleague.adobe.com/te9iyNajxDfgvHqqThbVUc7tBItxfMtxhOMl2eCLOsk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 3%

---

# obj{#obj}

Seleccionar objeto por nombre. Selecciona el grupo de viñetas especificado por nombre e inicia un nuevo SMS.

` obj= *`nombre`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> nombre </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre del grupo o ruta/nombre. </p> </td> 
 </tr> 
</table>

Los subgrupos u objetos individuales pueden seleccionarse utilizando una ruta de grupo completa (es decir, especificando el nombre del grupo de destino u objeto precedido por todos los grupos principales, separados por / (barras diagonales)).

Si no se encuentra ningún grupo u objeto con el nombre especificado, se realiza la acción especificada en `attribute::OnObjFail`.

## Propiedades {#section-9463b36e8ff74c81a70c7c2b58927430}

Comando de selección; delimitador SMS. La selección de objetos es persistente hasta que se selecciona otro objeto, ya sea con `obj=` o `sel=`.

Las rutas y los nombres de grupos/objetos no distinguen entre mayúsculas y minúsculas.

## Predeterminado {#section-0c322850512c4896bb551856a549440e}

El primer grupo de la viñeta que contiene objetos procesables se selecciona automáticamente al abrir una nueva viñeta.

## Véase también {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [atributo::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
