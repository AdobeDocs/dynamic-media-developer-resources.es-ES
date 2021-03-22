---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: 30f133bd-09c7-4d70-bcc4-d961bb028e55
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade  </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto que se utiliza para mostrar u ocultar la barra de control y su contenido. Use <span class="codeph"> ninguno </span> para mostrar y ocultar instantáneamente; <span class="codeph"> fundido </span> proporciona un efecto de fundido y atenuación gradual (no compatible con Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos entre el último evento de mouse/contacto que registra la barra de control y la barra de control de tiempo que oculta. </p> <p> Si se establece en <span class="codeph"> -1 </span> el componente nunca déclencheur su efecto de ocultación automática y siempre permanece visible en la pantalla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p> Define la duración de la animación de fundido en segundos y fundido en segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional. Este comando se ignora en los dispositivos táctiles, donde la barra de control se oculta automáticamente.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
