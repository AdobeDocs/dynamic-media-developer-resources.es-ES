---
title: initialFrame
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# initialFrame{#initialframe}

Parámetro común a todos los visualizadores.

>[!NOTE]
>
>Este comando no se aplica al visualizador de imágenes de vídeo.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica un índice de fotogramas basado en cero que el visor muestra al cargar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Un índice de base cero de la página dentro del pliego cuando el dispositivo está en orientación vertical. Para un entorno "de izquierda a derecha", <span class="codeph"> 0</span> significa "página izquierda" y <span class="codeph"> 1</span> significa "página derecha". Para un entorno "de derecha a izquierda", es lo contrario: <span class="codeph"> 0</span> significa "página derecha" y <span class="codeph"> 1</span> significa "página izquierda". </p> <p>Si no se especifica, <span class="codeph"> 0</span> se asume de forma predeterminada. Se omite cuando el dispositivo está en orientación horizontal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

No hay valores predeterminados.

## Ejemplo {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
