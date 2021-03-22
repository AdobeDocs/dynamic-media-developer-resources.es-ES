---
description: Atributo de configuración para el visualizador de vídeo interactivo.
seo-description: Atributo de configuración para el visualizador de vídeo interactivo.
seo-title: CallToAction.maxloadradius
solution: Experience Manager
title: CallToAction.maxloadradius
uuid: ec5a4b0d-1dae-456f-a9da-91541cfba1a7
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 4%

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

