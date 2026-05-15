---
title: ControlBar.transition
description: Atributo de configuración para el visualizador de carrusel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
TQID: 'https://experienceleague.adobe.com/oVi-FxRdW7mQ-HlLoExaCG6cAB56WDuupA2RnEM7pqY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuración para el visualizador de carrusel.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|fundido</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto utilizado para mostrar u ocultar la barra de control y su contenido. </p> <p>Definir en <span class="codeph"> none</span> para mostrar u ocultar instantáneamente. </p> <p>Se establece en <span class="codeph"> fade</span> para proporcionar un efecto de fundido de entrada y salida gradual. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> retraso para ocultar</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el tiempo en segundos entre el último evento táctil o de ratón registrado por la barra de control y el momento en que se oculta la barra de control. </p> <p>Si se establece en <span class="codeph"> -1</span>, el componente nunca déclencheur su efecto de ocultación automática y, por lo tanto, siempre permanece visible en la pantalla. </p> </td> 
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
