---
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
title: CallToAction.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Developer,Business Practitioner
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Atributo de configuración para el visualizador de vídeo interactivo.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`precarga`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el comportamiento de precarga del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span>, todas las miniaturas se cargan simultáneamente cuando el componente se inicializa o se cambia el recurso. </p> <p>Cuando se establece en <span class="codeph"> 0</span>, solo se cargan las miniaturas visibles. </p> <p>Establézcalo en <span class="codeph"><span class="varname"> precarga</span></span> para definir cuántas filas/columnas invisibles alrededor del área visible están precargadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`-1`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
