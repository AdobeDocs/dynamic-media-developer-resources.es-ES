---
title: CallToAction.direction
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
TQID: 'https://experienceleague.adobe.com/YehjMoK88ylklqHA9ZpjPgW8xoMwhLQqR-2e73ayWRM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# CallToAction.direction{#calltoaction-direction}

Atributo de configuración para el visualizador de vídeo interactivo.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|izquierda|derecha </span> </p> </td> 
   <td colname="col2"> <p> Especifica la forma en que la vista se rellena con miniaturas. </p> <p>Establezca <span class="codeph"> left </span> para establecer el orden de relleno de izquierda a derecha. </p> <p>Definir en <span class="codeph"> right </span> invierte el orden para que se rellene en la dirección de derecha a izquierda, de arriba a abajo. </p> <p>Se establece en <span class="codeph"> auto </span> para que el componente aplique el modo derecho cuando la configuración regional se establezca en <span class="codeph"> "ja" </span>; de lo contrario, se utiliza <span class="codeph"> left </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`auto`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
