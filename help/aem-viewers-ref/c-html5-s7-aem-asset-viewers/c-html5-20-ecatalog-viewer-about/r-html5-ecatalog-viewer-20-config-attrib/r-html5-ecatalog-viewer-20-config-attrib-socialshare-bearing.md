---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de diapositiva para el contenedor de botones. </p> <p> Cuando se establece en <span class="codeph"> arriba </span>, <span class="codeph"> abajo </span>, <span class="codeph"> left </span>, o <span class="codeph"> derecha </span>, el panel se despliega en una dirección especificada sin una comprobación de límites adicionales. Este comportamiento puede provocar el recorte del panel por un contenedor externo. </p> <p>Cuando se establece en <span class="codeph"> fit-vertical </span>, el componente primero cambia la posición del panel base a la parte inferior de SocialShare e intenta desplegar el panel desde la parte inferior, derecha o izquierda, desde dicha ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue desde la dirección superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral </span>, el componente utiliza una lógica similar a la de fit-vertical. Sin embargo, desplaza la base hacia la derecha (primero hacia la derecha, hacia abajo y hacia arriba) y, a continuación, la desplaza hacia la izquierda (intentando hacia la izquierda, hacia abajo y hacia arriba). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Predeterminado {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Ejemplo {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
