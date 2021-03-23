---
description: Atributo de configuración para el visualizador de vídeo.
seo-description: Atributo de configuración para el visualizador de vídeo.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: abd98898-d7d8-468f-b696-052e61e171b5
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Atributo de configuración para el visualizador de vídeo.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto que se utiliza para mostrar u ocultar la barra de control y su contenido. </p> <p>Utilice <span class="codeph"> none</span> para mostrar y ocultar instantáneamente. Utilice <span class="codeph"> fundido</span> para proporcionar un efecto de fundido y atenuación gradual. </p> <p>Fade no es compatible con Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica el tiempo en segundos entre el último evento de mouse/contacto que registra la barra de control y la barra de control de tiempo que oculta. </p> <p> Si se establece en <span class="codeph"> -1</span> el componente nunca déclencheur su efecto de ocultación automática y siempre permanece visible en la pantalla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Define la duración de la animación de fundido en segundos y fundido en segundos. </p> </td> 
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

