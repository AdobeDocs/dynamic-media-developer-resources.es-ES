---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
TQID: 'https://experienceleague.adobe.com/eTB-wD8G7HGSDgohQn-FsCeFL1GHMBiqzNUtT3nw5n4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 3%

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
