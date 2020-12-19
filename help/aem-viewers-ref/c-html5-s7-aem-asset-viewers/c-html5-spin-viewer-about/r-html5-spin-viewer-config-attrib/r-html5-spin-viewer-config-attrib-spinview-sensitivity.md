---
description: nulo
seo-description: nulo
seo-title: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic media
uuid: 82cf1f26-3af0-494f-b918-fdc318959c75
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 5%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitySensisibility`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensisibility</span>[,  <span class="varname"> ySensisibility</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controla la sensibilidad de los giros horizontales y verticales realizados con un movimiento de arrastre o barrido del ratón. </p> <p> <span class="codeph"> </span> xSensitivitydefine cuántas rotaciones horizontales completas del producto se realizan si el usuario arrastra el ratón horizontalmente de un lado a otro de la vista. Por ejemplo, tres significa que el usuario ve tres giros completos para un gesto de arrastre completo. </p> <p>Del mismo modo, <span class="codeph"> ySensisibility</span> controla la sensibilidad del giro vertical. Un valor de 1 significa que una operación de arrastrar o realizar un barrido vertical completa cambia el ángulo de vista del plano de giro superior al inferior (o viceversa). </p> <p>Al establecer un valor negativo para <span class="codeph"> ySensisibility</span> se invierte la dirección del giro vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
