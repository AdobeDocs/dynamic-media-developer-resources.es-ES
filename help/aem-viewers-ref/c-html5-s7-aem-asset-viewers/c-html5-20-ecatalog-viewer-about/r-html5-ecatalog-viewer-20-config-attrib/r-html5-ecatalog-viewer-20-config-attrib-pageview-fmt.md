---
description: nulo
seo-description: nulo
seo-title: PageView.fmt
solution: Experience Manager
title: PageView.fmt
topic: Dynamic media
uuid: 302e20bf-d398-45de-98a5-58b9edde48f3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 8%

---


# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica el formato de imagen que utiliza el componente para cargar imágenes desde el servidor de imágenes. Si el formato especificado termina con <span class="codeph"> -alpha</span>, el componente procesa las imágenes como contenido transparente. Para todos los demás formatos de imagen, el componente trata las imágenes como opacas. El componente tiene un fondo blanco de forma predeterminada. Por lo tanto, para hacerlo transparente, establezca la propiedad <span class="codeph"> color de fondo</span> CSS en <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Opcional.

## Predeterminado {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## Ejemplo {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
