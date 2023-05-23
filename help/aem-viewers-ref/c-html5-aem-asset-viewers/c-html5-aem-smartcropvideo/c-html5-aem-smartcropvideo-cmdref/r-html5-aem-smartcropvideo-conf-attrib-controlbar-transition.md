---
title: ControlBar.transition
description: Atributo de configuración para el visor de recorte inteligente de vídeos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7b4db11b-e9ac-4a52-9206-083989128bc6
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuración para el visor de recorte inteligente de vídeos.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`dilatar para ocultar`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto utilizado para mostrar u ocultar la barra de control y su contenido. </p> <p>Uso <span class="codeph"> ninguno</span> para mostrarlo y ocultarlo al instante. Uso <span class="codeph"> atenuación</span> para proporcionar un efecto de fundido de entrada y salida gradual. </p> <p>Fade no es compatible con Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dilatar para ocultar</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica el tiempo en segundos entre el último evento táctil o de ratón que registra la barra de control y el momento en que se oculta la barra de control. </p> <p> Si se establece en <span class="codeph"> -1</span>Sin embargo, el componente nunca déclencheur su efecto de ocultación automática y siempre permanece visible en la pantalla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Define la duración de la animación de fundido de entrada y salida, en segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
