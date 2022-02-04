---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`Sensibilidad x`*[, *`Sensibilidad`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Sensibilidad x</span>[, <span class="varname"> Sensibilidad</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controla la sensibilidad del giro horizontal y vertical que se realiza con el arrastre o el desliz del ratón. </p> <p> <span class="codeph"> Sensibilidad x</span> establece cuántas rotaciones horizontales completas del producto se realizan si el usuario arrastra el ratón horizontalmente de un lado de la vista a otro. Por ejemplo, tres significa que el usuario ve tres giros completos para un gesto de arrastrar completo. </p> <p>Del mismo modo, <span class="codeph"> Sensibilidad</span> controla la sensibilidad del giro vertical. Un valor de 1 significa que un giro o arrastre vertical completo cambia el ángulo de vista del plano de giro superior al inferior (o, por el contrario, lo que ocurre). </p> <p>Configuración de un valor negativo para <span class="codeph"> Sensibilidad</span> invierte la dirección del giro vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
