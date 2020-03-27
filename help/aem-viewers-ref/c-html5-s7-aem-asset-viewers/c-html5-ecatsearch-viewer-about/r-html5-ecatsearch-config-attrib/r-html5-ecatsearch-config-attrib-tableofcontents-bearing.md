---
description: nulo
seo-description: nulo
seo-title: TablaDeContenido.porte
solution: Experience Manager
title: TablaDeContenido.porte
topic: Dynamic media
uuid: 832ebacf-d57f-4efa-ab1a-6a454f7c7a32
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# TablaDeContenido.porte{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Controla la dirección del aspecto del panel desplegable. </p> <p>Cuando se define en <span class="codeph"> vertical</span>, el componente cambia primero la posición del panel base a la parte inferior de su botón e intenta desplegar el panel a la derecha o a la izquierda desde la ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue en la dirección derecha e izquierda. </p> <p>Cuando se configura en <span class="codeph"> vertical</span>, el componente utiliza una lógica similar, pero desplaza primero la base a la derecha, intentando bajar y subir las direcciones de despliegue. Luego, desplaza la base hacia la izquierda, tratando de bajar y subir las direcciones. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Establece el retraso en segundos del temporizador de ocultación automática desplegable que oculta el panel cuando un usuario está inactivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-55436ddd78b04f538dbb9a7a8463feae}

Opcional.

## Predeterminado {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## Ejemplo {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
