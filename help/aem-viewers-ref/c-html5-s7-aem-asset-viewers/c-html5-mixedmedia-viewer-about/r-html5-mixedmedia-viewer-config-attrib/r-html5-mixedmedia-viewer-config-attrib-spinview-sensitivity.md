---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de medios mixtos
role: Developer,Business Practitioner
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivityySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Sensibilidad</span> [,  <span class="varname"> confidencialidad</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controla la sensibilidad del giro horizontal y vertical que se realiza con el arrastre o el desliz del ratón. </p> <p> <span class="codeph"> </span> xSensitivitydefine cuántas rotaciones horizontales completas del producto se realizan si el usuario arrastra el ratón horizontalmente de un lado de la vista a otro. Por ejemplo, tres significa que el usuario ve tres giros completos para un gesto de arrastrar completo. </p> <p>Del mismo modo, <span class="codeph"> Sensibilidad</span> controla la sensibilidad del giro vertical. Un valor de 1 significa que un giro o arrastre vertical completo cambia el ángulo de visión del plano de giro superior al inferior (o viceversa). </p> <p>Si se establece un valor negativo para <span class="codeph"> ySensitivity</span>, se invierte la dirección del giro vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
