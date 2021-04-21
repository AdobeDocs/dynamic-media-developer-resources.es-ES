---
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
title: serverUrl
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# serverUrl{#serverurl}

Parámetro común a todos los visualizadores.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Ruta raíz relativa o absoluta de Image Serving. </p> <p> Especifica una ruta relativa o absoluta al servicio de imágenes, desde donde el usuario recupera las imágenes. Si la ruta no tiene un <span class="filepath"> /</span> inicial, es relativa a la ubicación de la página HTML del visor. Si la ruta tiene un <span class="filepath"> /</span> inicial, especifica una ruta absoluta en el mismo servidor. </p> <p> Utilice solo una ruta absoluta en caso de que el módulo Compartir correo electrónico esté habilitado en el visor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional. No es necesario para el uso estándar de SaaS (software como servicio).

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Ejemplos {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```
