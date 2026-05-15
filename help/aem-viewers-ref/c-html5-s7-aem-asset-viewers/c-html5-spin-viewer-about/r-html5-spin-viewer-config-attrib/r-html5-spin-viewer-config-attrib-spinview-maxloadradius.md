---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
TQID: 'https://experienceleague.adobe.com/h7jV66-f8J9UoMxsROgQrDLSN-ONyXSZ71gj75-Z7v8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`valor`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> valor</span></span> </p> </td> 
   <td colname="col2"> <p> Representa el número máximo de fotogramas para cargar previamente en cada dirección cuando SpinView está inactivo. Un valor de <span class="codeph"> -1</span> carga previamente todos los fotogramas del conjunto. Los fotogramas cargados previamente siempre se ven con la resolución original con la que se cargó SpinView inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla la calidad de los fotogramas cargados previamente. Cuando se establece en <span class="codeph"> 1</span> fotogramas se cargan en alta calidad, coincidiendo con el tamaño del componente. Cuando se establece en <span class="codeph"> 0</span>, solo se carga el mosaico de vista previa de baja resolución. </p> <p>La precarga en alta resolución mejora la experiencia del usuario final, especialmente cuando el giro automático está habilitado. Al mismo tiempo, reduce el tiempo de inicio y aumenta el consumo de red, por lo que debe utilizarse con precaución. Cuando se utiliza una precarga de alta resolución, los cuadros precargados siempre tienen la resolución original con la que se cargó inicialmente el componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
