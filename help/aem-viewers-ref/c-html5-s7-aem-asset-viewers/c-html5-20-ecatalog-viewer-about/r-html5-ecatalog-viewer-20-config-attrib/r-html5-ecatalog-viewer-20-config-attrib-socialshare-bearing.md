---
description: nulo
seo-description: nulo
seo-title: SocialShare.adding
solution: Experience Manager
title: SocialShare.adding
topic: Dynamic media
uuid: e48b39bb-c23d-42ce-9dc6-6e8b0d9b04ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialShare.adding{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de diapositivas para el contenedor de botones. </p> <p> Cuando se establece en <span class="codeph"> arriba </span>, <span class="codeph"> abajo </span>, <span class="codeph"> izquierda </span>o <span class="codeph"> derecha </span>, el panel se despliega en una dirección especificada sin una comprobación adicional de los límites. Este comportamiento puede provocar el recorte de paneles por un contenedor externo. </p> <p>Cuando se establece en <span class="codeph"> ajuste vertical </span>, el componente cambia primero la posición del panel base a la parte inferior de Compartir en redes sociales e intenta desplegar el panel desde la parte inferior, derecha o izquierda, desde dicha ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue desde la parte superior, derecha e izquierda. </p> <p>Cuando se define como <span class="codeph"> ajustable lateral </span>, el componente utiliza una lógica similar a la de ajuste vertical, pero cambia la base hacia la derecha, hacia abajo y hacia arriba, hacia la derecha, hacia abajo y hacia arriba, y luego desplaza la base hacia la izquierda, intentando hacia la izquierda, hacia abajo y hacia arriba hacia fuera. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Predeterminado {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Ejemplo {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
