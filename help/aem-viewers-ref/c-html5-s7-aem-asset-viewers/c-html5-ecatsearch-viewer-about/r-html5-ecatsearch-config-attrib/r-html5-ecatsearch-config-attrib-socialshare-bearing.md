---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de diapositiva para el contenedor de botones. </p> <p> Cuando se establece en <span class="codeph"> arriba </span>, <span class="codeph"> abajo </span>, <span class="codeph"> left </span>, o <span class="codeph"> derecha </span>, el panel se despliega en una dirección especificada sin una comprobación de límites adicional. Este comportamiento puede provocar el recorte del panel por un contenedor externo. </p> <p>Cuando se establece en <span class="codeph"> fit-vertical </span>, el componente primero cambia la posición del panel base a la parte inferior de SocialShare e intenta desplegar el panel desde la parte inferior, derecha o izquierda, desde dicha ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue desde la dirección superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral </span>Sin embargo, el componente utiliza una lógica similar a la de ajustar vertical, pero en su lugar desplaza la base a la derecha primero, hacia la derecha, hacia abajo y hacia arriba en las direcciones de despliegue, y luego desplaza la base a la izquierda, hacia la izquierda, hacia abajo y hacia arriba en las direcciones de despliegue. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Predeterminado {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Ejemplo {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
