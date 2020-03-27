---
description: Parámetro común a todos los visores.
seo-description: Parámetro común a todos los visores.
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
topic: Dynamic media
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# contentUrl{#contenturl}

Parámetro común a todos los visores.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica la ruta de acceso base a los archivos CSS personalizados, cualquier contenido de subtítulos opcionales o contenido de navegación. </p> <p>Si la ruta de acceso no tiene un <span class="filepath"> /</span>inicial, es relativa a la ubicación de la página HTML del visor. Si la ruta tiene un <span class="filepath"> /</span>inicial, especifica una ruta absoluta en el mismo servidor. </p> <p> No afecta a la carga del archivo CSS predeterminado cuando no se especifica un comando de estilo. </p> </td> 
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

