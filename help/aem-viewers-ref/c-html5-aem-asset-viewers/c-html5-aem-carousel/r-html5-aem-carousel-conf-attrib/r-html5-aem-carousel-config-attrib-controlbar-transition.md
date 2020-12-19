---
description: Atributo de configuración para el visor de carrusel.
seo-description: Atributo de configuración para el visor de carrusel.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Atributo de configuración para el visor de carrusel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|fundido</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto que se utiliza para mostrar u ocultar la barra de control y su contenido. </p> <p>Se establece en <span class="codeph"> none</span> para mostrar/ocultar instantáneamente. </p> <p>Establezca <span class="codeph"> fundido</span> para proporcionar un efecto de fundido gradual de entrada y salida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos que transcurre entre el último evento táctil o de ratón registrado por la barra de control y la barra de control de tiempo que se oculta. </p> <p>Si se establece en <span class="codeph"> -1</span>, el componente nunca activa su efecto de ocultación automática y, por lo tanto, siempre permanece visible en la pantalla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> Define la duración de la animación de entrada y salida de fundido en segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Este comando se ignora en los dispositivos táctiles en los que la barra de control está desactivada.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

