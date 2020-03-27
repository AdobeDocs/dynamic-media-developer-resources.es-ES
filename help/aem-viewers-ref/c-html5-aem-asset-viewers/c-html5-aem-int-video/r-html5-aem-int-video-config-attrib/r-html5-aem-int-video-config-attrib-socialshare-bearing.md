---
description: Atributo de configuración para el visor de vídeo interactivo.
seo-description: Atributo de configuración para el visor de vídeo interactivo.
seo-title: SocialShare.adding
solution: Experience Manager
title: SocialShare.adding
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# SocialShare.adding{#socialshare-bearing}

Atributo de configuración para el visor de vídeo interactivo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de diapositivas para el contenedor de botones. Cuando se configura para <span class="codeph"> arriba</span>, <span class="codeph"> abajo</span>, <span class="codeph"> izquierda</span>o <span class="codeph"> derecha</span>, el panel se despliega en la dirección especificada sin ninguna comprobación adicional de los límites, lo que puede hacer que el panel quede recortado por un contenedor exterior. </p> <p>Cuando se configura en <span class="codeph"> vertical</span>, el componente cambia primero la posición del panel base a la parte inferior de Compartir en redes sociales e intenta desplegar el panel en una de las siguientes direcciones desde una ubicación base de este tipo: abajo, derecha, izquierda. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repite los intentos de despliegue desde una dirección superior, derecha e izquierda. </p> <p>Cuando se define como <span class="codeph"> ajustable lateral</span>, el componente utiliza una lógica similar, pero desplaza primero la base hacia la derecha, para lo cual prueba las direcciones de despliegue hacia la derecha, hacia abajo y hacia arriba. A continuación, desplaza la base hacia la izquierda, tratando de obtener direcciones hacia la izquierda, hacia abajo y hacia arriba. </p> </td> 
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

