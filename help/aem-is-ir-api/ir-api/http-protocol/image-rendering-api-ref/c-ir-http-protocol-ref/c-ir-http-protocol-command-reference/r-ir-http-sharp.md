---
title: afilado
description: Enfoque de textura. Especifica el enfoque que se aplicará al procesar este material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
TQID: 'https://experienceleague.adobe.com/AWUw6E0xSWAsMfijewBvnSC8JdM5l9-qtFNLZsweFRY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 5%

---

# afilado{#sharp}

Enfoque de textura. Especifica el enfoque que se aplicará al procesar este material.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Sin enfoque. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Enfoque normal (tarde). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 enfoque alternativo (temprano). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Más enfoque (temprano y tarde). </p> </td> 
 </tr> 
</table>

`sharp=1` aplica enfoque después de que se procese el material; `sharp=2` aplica enfoque después del escalado inicial de la textura, pero antes de que se transforme en la escena; `sharp=3` aplica enfoque antes y después de la transformación.

El algoritmo de enfoque y la cantidad de enfoque y otros parámetros USM (máscara de enfoque) están controlados por la plantilla de material predeterminada proporcionada por la viñeta o con `rs=`.

## Propiedades {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Atributo de material. Ignorado por materiales de color sólido.

## Predeterminado {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, si el material se basa en una entrada del catálogo; en caso contrario, `attribute::Sharp`.

## Véase también {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catálogo::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)

