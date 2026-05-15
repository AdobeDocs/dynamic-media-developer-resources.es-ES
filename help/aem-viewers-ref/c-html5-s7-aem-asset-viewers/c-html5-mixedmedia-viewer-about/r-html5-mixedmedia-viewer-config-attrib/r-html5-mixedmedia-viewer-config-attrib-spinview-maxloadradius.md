---
title: SpinView.maxloadradius
description: Representa el número máximo de fotogramas para cargar previamente en cada dirección cuando SpinView está inactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
TQID: 'https://experienceleague.adobe.com/SqjidvUT9DCONC8u-rtlhUem-5M5bu0ye4sZPhiHcds'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Representa el número máximo de fotogramas para cargar previamente en cada dirección cuando SpinView está inactivo.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`valor`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> valor</span></span> </p> </td> 
   <td colname="col2"> <p> Un valor de <span class="codeph"> -1</span> carga previamente todos los fotogramas del conjunto. Los fotogramas cargados previamente siempre se ven con la resolución original con la que se cargó SpinView inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla la calidad de los fotogramas cargados previamente. </p> <p>Cuando se establece en <span class="codeph"> 1</span>, los fotogramas se cargan en alta calidad, coincidiendo con el tamaño del componente. </p> <p>Cuando se establece en <span class="codeph"> 0</span>, solo se carga el mosaico de vista previa de baja resolución.</p> <p>La precarga en alta resolución mejora la experiencia del usuario, especialmente cuando el giro automático está habilitado. Al mismo tiempo, reduce el tiempo de inicio y aumenta el consumo de red, por lo que debe utilizarse con cuidado. Cuando se utiliza la precarga de alta resolución, los cuadros precargados siempre tienen la resolución original con la que se cargó inicialmente el componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
