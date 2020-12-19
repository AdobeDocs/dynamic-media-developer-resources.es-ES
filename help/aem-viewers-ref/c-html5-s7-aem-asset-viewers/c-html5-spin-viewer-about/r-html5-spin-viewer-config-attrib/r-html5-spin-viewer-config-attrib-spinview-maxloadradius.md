---
description: nulo
seo-description: nulo
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> basado en IP</span></span> </p> </td> 
   <td colname="col2"> <p> Representa el número máximo de fotogramas que se van a cargar previamente en cada dirección cuando la vista de giros está inactiva. Un valor de <span class="codeph"> -1</span> carga previamente todos los fotogramas del conjunto. Los fotogramas precargados siempre se ven con la resolución original en la que se cargó inicialmente SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla la calidad de los marcos precargados. Cuando se establece en <span class="codeph"> 1</span> los fotogramas se cargan en alta calidad, coincidiendo con el tamaño del componente. Cuando se establece en <span class="codeph"> 0</span> sólo se carga el mosaico de previsualización de baja resolución. </p> <p>La precarga en alta resolución mejora la experiencia del usuario final, especialmente cuando está activado el giro automático. Al mismo tiempo, el resultado es un menor tiempo de inicio y un mayor consumo de red, por lo que debe utilizarse con precaución. Cuando se utiliza una precarga de alta resolución, los fotogramas precargados siempre tienen la resolución original en la que se cargó inicialmente el componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
