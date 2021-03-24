---
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

Atributo de configuración para el visualizador de vídeo interactivo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de diapositivas para el contenedor de botones. Cuando se establece en <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> o <span class="codeph"> right</span>, el panel se despliega en la dirección especificada sin comprobar límites adicionales, lo que puede hacer que el panel sea recortado por un contenedor externo. </p> <p>Cuando se establece en <span class="codeph"> fit-vertical</span>, el componente cambia primero la posición del panel base a la parte inferior de SocialShare e intenta desplegar el panel en una de las siguientes direcciones desde una ubicación base de este tipo: abajo, derecha, izquierda. Con cada intento, el componente comprueba si el panel está recortado por un contenedor exterior. Si todos los intentos fallan, el componente intenta cambiar la posición del panel base a la parte superior y repite los intentos de despliegue desde la dirección superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral</span>, el componente utiliza una lógica similar, pero cambia la base a la derecha en primer lugar, intentando dirigirse hacia la derecha, hacia abajo y hacia arriba. Luego, mueve la base hacia la izquierda, intentando hacia la izquierda, hacia abajo y hacia arriba. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

