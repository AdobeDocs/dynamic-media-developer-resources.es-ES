---
description: Atributo de configuración para el visualizador de vídeo.
seo-description: Atributo de configuración para el visualizador de vídeo.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
uuid: d7d92d63-a4c2-4bd9-b0fd-fdfd47504a39
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

Atributo de configuración para el visualizador de vídeo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de la diapositiva para el contenedor de botones. </p> <p> Cuando se establece en <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> o <span class="codeph"> right</span>, el panel se despliega en una dirección especificada sin una comprobación de límites adicional, lo que puede resultar en el recorte del panel por un contenedor externo. </p> <p>Cuando se establece en <span class="codeph"> ajuste vertical</span>, el componente cambia primero la posición del panel base a la parte inferior de SocialShare e intenta desplegar el panel desde la parte inferior, derecha o izquierda desde esa ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor exterior. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue en la dirección superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral</span>, el componente utiliza una lógica similar. Sin embargo, primero mueve la base hacia la derecha, y luego intenta hacia la derecha, hacia abajo y hacia arriba, y luego mueve la base hacia la izquierda, tratando de seguir las direcciones de despliegue hacia la izquierda, hacia abajo y hacia arriba. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```

