---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4f25112b-9e51-4a0e-9500-1b5ab0f4de87
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Especifica la alineación interna (anclaje) del contenedor de muestras dentro del área del componente. En Muestras, el tamaño del contenedor de miniaturas interno es tal que solo se muestra un número entero de muestras. Como resultado, hay cierto relleno entre los límites del contenedor interno y el componente externo. Este comando especifica cómo se coloca el contenedor de muestras interno dentro del componente.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> izquierda|centro|derecha</span> </p> </td> 
   <td> <p> Define la alineación de las muestras horizontales. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> superior|centro|inferior</span> </p> </td> 
   <td> <p> Define la alineación de las muestras verticales. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`center,center`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`align=left,top`
