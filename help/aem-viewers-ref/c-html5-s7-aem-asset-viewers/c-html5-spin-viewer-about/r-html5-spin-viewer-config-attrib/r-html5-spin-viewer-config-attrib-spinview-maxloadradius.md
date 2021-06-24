---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Developer,Business Practitioner
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> basado en IP</span></span> </p> </td> 
   <td colname="col2"> <p> Representa el número máximo de fotogramas que se van a precargar en cada dirección cuando SpinView está inactivo. Un valor de <span class="codeph"> -1</span> carga previamente todos los fotogramas del conjunto. Los fotogramas precargados siempre se ven con la resolución original en la que se cargó inicialmente SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla la calidad de los fotogramas precargados. Cuando se establece en <span class="codeph"> 1</span> los fotogramas se cargan en alta calidad, coincidiendo con el tamaño del componente. Cuando se establece en <span class="codeph"> 0</span> solo se carga el mosaico de vista previa de baja resolución. </p> <p>La precarga en alta resolución mejora la experiencia del usuario final, especialmente cuando está activado el giro automático. Al mismo tiempo, resulta en un tiempo de inicio más lento y un mayor consumo de red, por lo que debe utilizarse con precaución. Cuando se utiliza una precarga de alta resolución, los fotogramas precargados siempre tienen la resolución original en la que se cargó inicialmente el componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
