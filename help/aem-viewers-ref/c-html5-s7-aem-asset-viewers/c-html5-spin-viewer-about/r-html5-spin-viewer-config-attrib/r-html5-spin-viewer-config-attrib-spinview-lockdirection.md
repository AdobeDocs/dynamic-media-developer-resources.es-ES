---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
uuid: adea34ca-adbe-465e-8991-f39a7a81d611
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 3%

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica si se permite un cambio en la dirección de giro en el caso del conjunto de giros 2D. </p> <p>Cuando se establece en <span class="codeph"> 1 </span>, el componente identifica la dirección de arrastre o desliz principal (horizontal o vertical) al principio del gesto. Después de eso, mantiene esa dirección hasta que termina el gesto. Por ejemplo, si el usuario inicia un giro horizontal y luego decide continuar el gesto de arrastrar en dirección vertical, el componente no realiza un giro vertical; en su lugar, considera sólo el movimiento horizontal del ratón o el desliz. </p> <p>Un valor de <span class="codeph"> 0 </span> permite al usuario cambiar la dirección de giro en cualquier momento durante el progreso del gesto. La configuración no afecta si el conjunto de giros es 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
