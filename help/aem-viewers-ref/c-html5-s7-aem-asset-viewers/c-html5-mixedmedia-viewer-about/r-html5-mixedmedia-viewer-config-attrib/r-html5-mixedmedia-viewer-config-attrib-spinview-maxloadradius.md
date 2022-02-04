---
title: SpinView.maxloadradius
description: Representa el número máximo de fotogramas que se van a precargar en cada dirección cuando SpinView está inactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 3%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Representa el número máximo de fotogramas que se van a precargar en cada dirección cuando SpinView está inactivo.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> basado en IP</span></span> </p> </td> 
   <td colname="col2"> <p> Un valor de <span class="codeph"> -1</span> carga previamente todos los marcos del conjunto. Los fotogramas precargados siempre se ven con la resolución original en la que se cargó inicialmente SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla la calidad de los fotogramas precargados. </p> <p>Cuando se configura como <span class="codeph"> 1</span> los marcos se cargan en alta calidad, coincidiendo con el tamaño del componente. </p> <p>Cuando se configura como <span class="codeph"> 0</span> solo se carga el mosaico de vista previa de baja resolución.</p> <p>La precarga en alta resolución mejora la experiencia del usuario, especialmente cuando está activado el giro automático. Al mismo tiempo, resulta en un tiempo de inicio más lento y un mayor consumo de red, por lo que debe utilizarse con cuidado. Cuando se utiliza la precarga de alta resolución, los fotogramas precargados siempre se encuentran en la resolución original en la que se cargó inicialmente el componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
