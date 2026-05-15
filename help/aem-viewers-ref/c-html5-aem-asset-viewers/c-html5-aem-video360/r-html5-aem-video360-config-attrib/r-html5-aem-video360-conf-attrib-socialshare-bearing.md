---
title: SocialShare.bear
description: Atributo de configuración para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f00b2539-3159-487a-b0fa-9589b694c2e6
TQID: 'https://experienceleague.adobe.com/cJSi-1nH3LY-7pf5a0e2PzRULzbkEuwc1ltbO7OMK2M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 1%

---

# SocialShare.bear{#socialshare-bearing}

Atributo de configuración para el visor de Video360.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arriba|abajo|izquierda|derecha|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Especifica la dirección de la animación de diapositiva para el contenedor de botones. </p> <p> Cuando se establece en <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> o <span class="codeph"> right</span>, el panel se despliega en una dirección especificada sin una comprobación de límites adicionales, lo que puede provocar que un contenedor externo recorte el panel. </p> <p>Cuando se establece en <span class="codeph"> fit-vertical</span>, el componente primero cambia la posición del panel base a la parte inferior de SocialShare e intenta desplegar el panel desde la parte inferior, derecha o izquierda desde dicha ubicación base. Con cada intento, el componente comprueba si el panel está recortado por un contenedor externo. Si todos los intentos fallan, el componente intenta desplazar la posición del panel base a la parte superior y repetir los intentos de despliegue en las direcciones superior, derecha e izquierda. </p> <p>Cuando se establece en <span class="codeph"> fit-lateral</span>, el componente utiliza una lógica similar. Sin embargo, primero desplaza la base a la derecha, en las direcciones de despliegue derecha, abajo y arriba, y después desplaza la base a la izquierda, en las direcciones de despliegue izquierda, abajo y arriba. </p> </td> 
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
