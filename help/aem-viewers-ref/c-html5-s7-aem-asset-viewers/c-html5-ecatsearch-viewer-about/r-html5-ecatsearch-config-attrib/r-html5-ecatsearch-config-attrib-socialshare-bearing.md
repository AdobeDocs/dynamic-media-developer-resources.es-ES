---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de diapositivas para el contenedor de botones. </p> <p> Cuando se establece en <span class="codeph"> arriba </span>, <span class="codeph"> abajo </span>, <span class="codeph"> izquierda </span> o <span class="codeph"> derecha </span>, el panel se despliega en una dirección especificada sin una comprobación de límites adicionales. Este comportamiento puede provocar que un contenedor externo recorte el panel. </p> <p>Cuando se establece en <span class="codeph"> ajuste vertical </span>, el componente cambia primero la posición del panel base a la parte inferior de SocialShare e intenta desplegar el panel desde la parte inferior, derecha o izquierda, desde esa ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor exterior. Si todos los intentos fallan, el componente intenta cambiar la posición del panel base a la parte superior y repetir los intentos de despliegue desde la dirección superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> para ajuste lateral </span>, el componente utiliza una lógica similar a la de ajuste vertical, pero, en su lugar, cambia la base hacia la derecha, hacia la derecha, hacia abajo y hacia arriba para desplegar direcciones, y luego cambia la base hacia la izquierda, intentando hacia la izquierda, hacia abajo y hacia arriba para desplegar direcciones. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Predeterminado {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Ejemplo {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
