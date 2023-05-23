---
title: indicadores
description: Aplique indicadores. Especifica opciones de procesamiento adicionales.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# indicadores {#flags}

Aplique indicadores. Especifica opciones de procesamiento adicionales.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valor de indicador. </p></td> 
 </tr> 
</table>

Actualmente se utiliza solo para materiales de gabinete.

`flags=0` (Por defecto) Procesa los archivadores superiores con puertas sólidas.

`flags=1` Procesa los archivadores superiores con puertas de vidrio (si la viñeta se creó con puertas de vidrio).

## Propiedades {#section-a2b00d7bb15e449ea85178acb92d8285}

Atributo de material. Se ignora si no es un material de armario, o si el objeto de armario de destino no permite puertas de cristal.

## Predeterminado {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` Para ninguna puerta de cristal.
