---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 2%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica si se permite un cambio en la dirección de giro si hay un conjunto de giros 2D. </p> <p>Cuando se establece en <span class="codeph"> 1 </span>, el componente identifica la dirección de arrastre o barrido principal (horizontal frente a vertical) al principio del gesto. Después, mantiene esa dirección hasta que termina el gesto. Por ejemplo, si el usuario inicia un giro horizontal y, a continuación, decide continuar con el gesto de arrastre en dirección vertical, el componente no realiza un giro vertical. En su lugar, solo tiene en cuenta el movimiento horizontal del ratón o el barrido. </p> <p>Un valor de <span class="codeph"> 0 </span> permite que un usuario cambie la dirección de giro en cualquier momento durante el progreso del gesto. El ajuste no tiene efecto si el conjunto de giros es 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
