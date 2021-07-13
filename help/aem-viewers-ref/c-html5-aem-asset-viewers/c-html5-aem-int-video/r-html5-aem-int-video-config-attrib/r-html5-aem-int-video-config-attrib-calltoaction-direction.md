---
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
title: CallToAction.direction
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# CallToAction.direction{#calltoaction-direction}

Atributo de configuración para el visualizador de vídeo interactivo.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Especifica la forma en que las miniaturas rellenan la vista. </p> <p>Configúrelo en <span class="codeph"> izquierda </span> para definir el orden de relleno de izquierda a derecha. </p> <p>Si se establece en <span class="codeph"> derecha </span> , se invierte el orden de modo que la vista se rellene en una dirección de derecha a izquierda, de arriba abajo. </p> <p>Se establece en <span class="codeph"> auto </span> para que el componente aplique el modo correcto cuando la configuración regional se establezca en <span class="codeph"> "ja" </span>; de lo contrario, se utiliza <span class="codeph"> izquierda </span>. </p> </td> 
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
