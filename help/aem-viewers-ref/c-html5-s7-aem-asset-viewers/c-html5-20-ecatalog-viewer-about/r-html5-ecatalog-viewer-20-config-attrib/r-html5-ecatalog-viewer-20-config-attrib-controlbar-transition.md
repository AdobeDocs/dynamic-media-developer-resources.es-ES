---
title: ControlBar.transition
description: Especifica el tipo de efecto utilizado para mostrar u ocultar la barra de control y su contenido.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|fundido </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto utilizado para mostrar u ocultar la barra de control y su contenido. Use <span class="codeph"> none </span> para mostrarla y ocultarla instantáneamente; <span class="codeph"> fade </span> proporciona un efecto gradual de fundido de entrada y salida (no admitido en Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> retrasar ocultación de </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos entre el último evento táctil o de ratón que registra la barra de control y el ocultamiento de la barra de control de tiempo. </p> <p> Si se establece en <span class="codeph"> -1 </span>, el componente nunca déclencheur su efecto de ocultación automática y siempre permanece visible en la pantalla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duración </span> </span> </p> </td> 
   <td colname="col2"> <p> Define la duración de la animación de fundido de entrada y salida, en segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional. Este comando se ignora en los dispositivos táctiles, donde la barra de control ocultar automáticamente está desactivada.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
