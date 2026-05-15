---
title: ControlBar.transition
description: Atributo de configuración para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
TQID: 'https://experienceleague.adobe.com/mKDRX66X6uQLgPVw6jyc5VxKyKQlsM0DgQGSuGlHeBs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 119
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Atributo de configuración para el visor de Video360.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|fundido</span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de efecto utilizado para mostrar u ocultar la barra de control y su contenido. </p> <p>Use <span class="codeph"> none</span> para mostrar y ocultar instantáneamente. Utilice <span class="codeph"> fade</span> para proporcionar una aparición y desaparición gradual del efecto. </p> <p>Fade no es compatible con Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica el tiempo en segundos entre el último evento táctil o de ratón que registra la barra de control y el momento en que se oculta la barra de control. </p> <p> Si se establece en <span class="codeph"> -1</span>, el componente nunca déclencheur su efecto de ocultación automática y siempre permanece visible en la pantalla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duración</span> </span> </p> </td> 
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
