---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e84336da-7f33-4fa9-b881-93b9db4bae8b
TQID: 'https://experienceleague.adobe.com/njG6Pp1iYmYsgGTyClRUN9XDsmMRXByhOPMV4s3tMKY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Activa el efecto de icono <span class="codeph"></span> para que se muestre en la parte superior de la imagen cuando la imagen está en estado de restablecimiento y sugiere una acción disponible para interactuar con la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> recuento</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el número máximo de veces que aparece y vuelve a aparecer <span class="codeph"> iconeffect</span>. Un valor de <span class="codeph"> -1</span> indica que el icono siempre vuelve a aparecer indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fundido</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la duración de la animación para mostrar u ocultar, en segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ocultar automáticamente</span></span> </p> </td> 
   <td colname="col2"> <p>Establece el número de segundos que el efecto de icono <span class="codeph"></span> permanece totalmente visible antes de que se oculte automáticamente. Es decir, el tiempo después de que se complete la animación de fundido de entrada pero antes de que comience la animación de fundido de salida. Una configuración de <span class="codeph"> 0</span> deshabilita el comportamiento de ocultar automáticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
