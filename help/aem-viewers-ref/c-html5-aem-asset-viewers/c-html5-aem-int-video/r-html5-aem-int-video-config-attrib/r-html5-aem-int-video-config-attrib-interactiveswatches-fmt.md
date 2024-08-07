---
title: InteractiveSwatches.fmt
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9a751b91-aeff-4ee1-b2fe-9bec416884ab
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Atributo de configuración para el visualizador de vídeo interactivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utiliza el componente para cargar imágenes del servidor de imágenes. </p> <p>Si el formato especificado termina con "<span class="codeph"> -alpha</span>", el componente procesa las imágenes como contenido transparente. Para el resto de los formatos de imagen, el componente trata las imágenes como opacas. El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para que sea transparente, establezca la propiedad CSS <span class="codeph"> background-color</span> en <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
