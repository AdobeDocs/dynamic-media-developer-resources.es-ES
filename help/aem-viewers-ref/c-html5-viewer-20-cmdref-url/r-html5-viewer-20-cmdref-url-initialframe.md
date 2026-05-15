---
title: initialFrame
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
TQID: 'https://experienceleague.adobe.com/v4kG-OcDN3wmdHDClJHeLR8d2SNcMa5sRQo89Qwig4I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 2%

---

# initialFrame{#initialframe}

Parámetro común a todos los visualizadores.

>[!NOTE]
>
>Este comando no se aplica al Visor de imágenes de vídeo.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica un índice de fotogramas basado en cero que el visor muestra al cargar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Un índice de base cero de la página dentro del pliego cuando el dispositivo está en orientación vertical. Para un entorno "de izquierda a derecha", <span class="codeph"> 0</span> significa "página izquierda" y <span class="codeph"> 1</span> significa "página derecha". Para un entorno "de derecha a izquierda", es lo contrario: <span class="codeph"> 0</span> significa "página derecha" y <span class="codeph"> 1</span> significa "página izquierda". </p> <p>Si no se especifica, se supone que <span class="codeph"> 0</span> es de forma predeterminada. Se ignora cuando el dispositivo está en orientación horizontal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

No hay valor predeterminado.

## Ejemplo {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
