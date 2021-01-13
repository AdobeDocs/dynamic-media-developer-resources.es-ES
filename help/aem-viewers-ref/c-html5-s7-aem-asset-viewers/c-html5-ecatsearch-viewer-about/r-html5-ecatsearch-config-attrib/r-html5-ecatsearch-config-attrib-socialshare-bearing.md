---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de diapositivas para el contenedor de botones. </p> <p> Cuando se configura en <span class="codeph"> hacia arriba </span>, <span class="codeph"> hacia abajo </span>, <span class="codeph"> izquierda </span> o <span class="codeph"> derecha </span>, el panel se despliega en una dirección especificada sin una verificación adicional de límites. Este comportamiento puede provocar el recorte de paneles por un contenedor externo. </p> <p>Cuando se establece en <span class="codeph"> fit-vertical </span>, el componente primero cambia la posición del panel base a la parte inferior de SocialShare e intenta desplegar el panel desde la parte inferior, derecha o izquierda, desde dicha ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue desde la parte superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral </span>, el componente utiliza una lógica similar a la de ajuste vertical, pero, en su lugar, desplaza la base hacia la derecha, hacia la derecha, hacia abajo y hacia arriba hacia fuera, y luego cambia la base hacia la izquierda, intentando hacia la izquierda, hacia abajo y hacia arriba hacia fuera. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Predeterminado {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Ejemplo {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
