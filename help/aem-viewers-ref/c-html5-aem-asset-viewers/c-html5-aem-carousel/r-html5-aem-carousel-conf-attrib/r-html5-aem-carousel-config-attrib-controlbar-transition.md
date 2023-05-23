---
title: ControlBar.transition
description: Atributo de configuración para el visualizador de carrusel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuración para el visualizador de carrusel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`dilatar para ocultar`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto utilizado para mostrar u ocultar la barra de control y su contenido. </p> <p>Configure como. <span class="codeph"> ninguno</span> para mostrar u ocultar instantáneamente. </p> <p>Configure como. <span class="codeph"> atenuación</span> para proporcionar un efecto de fundido de entrada y salida gradual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dilatar para ocultar</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos entre el último evento táctil o de ratón registrado por la barra de control y el momento en que se oculta la barra de control. </p> <p>Si se establece en <span class="codeph"> -1</span> el componente nunca déclencheur su efecto de ocultación automática y, por lo tanto, siempre permanece visible en la pantalla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> Define la duración de la animación de fundido de entrada y salida en segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Este comando se omite en dispositivos táctiles en los que la opción ocultar automáticamente de la barra de control está desactivada.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
