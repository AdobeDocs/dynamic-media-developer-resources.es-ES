---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
uuid: eb4a6fca-da18-4291-b7fb-e402156c85a0
feature: Dynamic Media Classic,Visualizadores,SDK/API,Combinar conjuntos de medios
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`precarga`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Especifica el comportamiento de precarga del componente. Cuando se establece en <span class="codeph"> -1</span>, todas las muestras se cargan simultáneamente cuando se inicializa el componente o se cambia el recurso. </p> <p>Cuando se establece en <span class="codeph"> 0</span>, solo se cargan muestras visibles. </p> <p><span class="codeph"><span class="varname"> </span></span> precarga define cuántas filas y columnas invisibles alrededor del área visible se precargan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
