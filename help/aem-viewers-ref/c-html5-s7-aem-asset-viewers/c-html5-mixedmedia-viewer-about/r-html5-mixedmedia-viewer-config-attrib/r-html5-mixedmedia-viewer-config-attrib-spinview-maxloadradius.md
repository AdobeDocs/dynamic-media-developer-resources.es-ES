---
description: Representa el número máximo de fotogramas que se van a cargar previamente en cada dirección cuando la vista de giros está inactiva.
seo-description: Representa el número máximo de fotogramas que se van a cargar previamente en cada dirección cuando la vista de giros está inactiva.
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

Representa el número máximo de fotogramas que se van a cargar previamente en cada dirección cuando la vista de giros está inactiva.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> basado en IP</span></span> </p> </td> 
   <td colname="col2"> <p> Un valor de <span class="codeph"> -1</span> carga previamente todos los fotogramas del conjunto. Los fotogramas precargados siempre se ven con la resolución original en la que se cargó inicialmente SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla la calidad de los marcos precargados. </p> <p>Cuando se establece en <span class="codeph"> 1</span>, los fotogramas se cargan en alta calidad, coincidiendo con el tamaño del componente. </p> <p>Cuando se establece en <span class="codeph"> 0</span> sólo se carga el mosaico de previsualización de baja resolución. </p> <p>La precarga en alta resolución mejora la experiencia del usuario final, especialmente cuando está activado el giro automático. Al mismo tiempo, se traduce en un menor tiempo de inicio y un mayor consumo de red, por lo que debe utilizarse con cuidado. Cuando se utiliza la precarga de alta resolución, los fotogramas precargados siempre tienen la resolución original en la que se cargó inicialmente el componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
