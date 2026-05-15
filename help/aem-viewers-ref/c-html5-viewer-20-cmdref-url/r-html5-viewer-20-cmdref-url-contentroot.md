---
title: contentUrl
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
TQID: 'https://experienceleague.adobe.com/D95dvILCIpQtQ6D1TcPwj-xfgjXb6AvyMmm5vDlemWw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 3%

---

# contentUrl{#contenturl}

Parámetro común a todos los visualizadores.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica la ruta base a los archivos CSS personalizados, cualquier contenido de subtítulos o contenido de navegación. </p> <p>Si la ruta de acceso no tiene un <span class="filepath"> /</span> a la izquierda, es relativa a la ubicación de la página de HTML del visor. Si la ruta de acceso tiene un <span class="filepath"> /</span> a la izquierda, especifica una ruta de acceso absoluta en el mismo servidor. </p> <p> No afecta a la carga del archivo CSS predeterminado cuando no se especifica un comando de estilo. </p> </td> 
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

<!--

```
contentUrl=https://demos-pub.assetsadobe.com/
```

-->
