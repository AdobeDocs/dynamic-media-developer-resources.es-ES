---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eb2196cb-b771-4828-8390-cd9e3fe6c57e
TQID: 'https://experienceleague.adobe.com/vLgMRd56WQf2hBXMvsMN8HEt-hieuMW1D-DgHU5OFWY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
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

## Propiedades {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Opcional.

## Predeterminado {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## Ejemplo {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]

