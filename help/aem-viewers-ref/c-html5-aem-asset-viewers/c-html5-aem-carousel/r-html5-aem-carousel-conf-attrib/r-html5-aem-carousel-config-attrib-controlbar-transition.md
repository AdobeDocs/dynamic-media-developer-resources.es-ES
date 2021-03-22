---
description: Atributo de configuración para el visor de carrusel.
seo-description: Atributo de configuración para el visor de carrusel.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Atributo de configuración para el visor de carrusel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto que se utiliza para mostrar u ocultar la barra de control y su contenido. </p> <p>Establézcalo en <span class="codeph"> none</span> para mostrar/ocultar instantáneamente. </p> <p>Configúrelo en <span class="codeph"> fundido</span> para proporcionar un efecto de atenuación gradual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos entre el último evento de mouse/contacto registrado por la barra de control y la barra de control de tiempo oculta. </p> <p>Si se establece en <span class="codeph"> -1</span> el componente nunca déclencheur su efecto de ocultación automática y, por lo tanto, siempre permanece visible en la pantalla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duración</span></span> </p> </td> 
   <td colname="col2"> <p> Establece la duración de la animación de entrada/salida de fundido en segundos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Este comando se ignora en los dispositivos táctiles en los que está deshabilitada la ocultación automática de la barra de control.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

