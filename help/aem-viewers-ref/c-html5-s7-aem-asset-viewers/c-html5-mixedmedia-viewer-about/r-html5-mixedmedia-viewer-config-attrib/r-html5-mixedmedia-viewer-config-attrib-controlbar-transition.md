---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Developer,Business Practitioner
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
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

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
