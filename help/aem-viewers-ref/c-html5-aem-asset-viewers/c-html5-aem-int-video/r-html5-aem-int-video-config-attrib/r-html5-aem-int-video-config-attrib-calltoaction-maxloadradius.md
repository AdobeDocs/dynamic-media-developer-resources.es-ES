---
title: CallToAction.maxloadradius
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Atributo de configuración para el visualizador de vídeo interactivo.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el comportamiento de carga previa del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span>, todas las miniaturas se cargan simultáneamente cuando se inicializa el componente o se cambia el recurso. </p> <p>Cuando se establece en <span class="codeph"> 0</span>, solo se cargan las miniaturas visibles. </p> <p>Se establece en <span class="codeph"><span class="varname"> preloadnbr</span></span> para definir el número de filas/columnas invisibles que se cargarán previamente alrededor del área visible. </p> </td> 
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
