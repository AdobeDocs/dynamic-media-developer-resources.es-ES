---
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
title: contentUrl
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---


# contentUrl{#contenturl}

Parámetro común a todos los visualizadores.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica la ruta base a archivos CSS personalizados, cualquier contenido de subtítulos o contenido de navegación. </p> <p>Si la ruta no tiene un <span class="filepath"> /</span> inicial, es relativa a la ubicación de la página HTML del visor. Si la ruta tiene un <span class="filepath"> /</span> inicial, especifica una ruta absoluta en el mismo servidor. </p> <p> No afecta a la carga del archivo CSS predeterminado cuando no se especifica un comando de estilo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Ejemplos {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```

