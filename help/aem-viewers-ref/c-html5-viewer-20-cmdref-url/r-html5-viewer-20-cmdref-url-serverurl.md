---
title: serverUrl
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
TQID: 'https://experienceleague.adobe.com/SbAeHSjxnw-69wsu92UeoEeGLlk3Ykpechs65I-k5EY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 3%

---

# serverUrl{#serverurl}

Parámetro común a todos los visualizadores.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Ruta raíz relativa o absoluta del servicio de imágenes. </p> <p> Especifica una ruta relativa o absoluta al servicio de imágenes, desde donde el visor recupera las imágenes. Si la ruta de acceso no tiene un <span class="filepath"> /</span> a la izquierda, es relativa a la ubicación de la página de HTML del visor. Si la ruta de acceso tiene un <span class="filepath"> /</span> a la izquierda, especifica una ruta de acceso absoluta en el mismo servidor. </p> <p> Utilice únicamente una ruta absoluta en caso de que el módulo Uso compartido de correo electrónico esté habilitado en el visor. </p> </td> 
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

<!--

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

-->
