---
description: Parámetro común a todos los visores.
seo-description: Parámetro común a todos los visores.
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
topic: Dynamic media
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# serverUrl{#serverurl}

Parámetro común a todos los visores.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span></span> </p> </td> 
   <td colname="col2"> <p>Ruta raíz relativa o absoluta del servicio de imágenes. </p> <p> Especifica una ruta relativa o absoluta al servicio de imágenes, desde donde el visor recupera las imágenes. Si la ruta de acceso no tiene un <span class="filepath"> /</span>inicial, es relativa a la ubicación de la página HTML del visor. Si la ruta tiene un <span class="filepath"> /</span>inicial, especifica una ruta absoluta en el mismo servidor. </p> <p> Utilice solo una ruta absoluta en caso de que el módulo Compartir correo electrónico esté habilitado en el visor. </p> </td> 
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

