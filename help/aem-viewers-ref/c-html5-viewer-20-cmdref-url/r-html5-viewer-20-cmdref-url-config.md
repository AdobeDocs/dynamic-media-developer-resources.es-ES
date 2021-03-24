---
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
title: config
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 2%

---


# config{#config}

Parámetro común a todos los visualizadores.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId  </span> </span> </p> </td> 
   <td colname="col2"> <p>Catálogo/ID para la configuración del visor. </p> <p> Especifica una entrada de catálogo de imágenes que contiene las propiedades de configuración del visor en el catálogo <span class="codeph">::UserData </span>. Cuando este comando está presente, el visor envía un comando <span class="codeph"> req=userdata </span> para <span class="codeph"> configId </span> al servidor y extrae las propiedades de la respuesta. Las propiedades se utilizan para inicializar el visor. Si la cadena URL especifica las mismas propiedades, anulan los valores del catálogo <span class="codeph">::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Todos los comandos del visor que se pueden especificar en `catalog::UserData` se esperan `asset`, `serverUrl`, `contentUrl`, `searchServerUrl` y `config`.

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

Ninguno.

## Ejemplo 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Un catálogo de imágenes llamado 2020 contiene la entrada `preset-oct`. El campo `catalog::UserData` de esta entrada de catálogo incluye los siguientes datos:

```
style=customStyle.css
```

Cargue el visor con el siguiente comando:

```
config=2020/preset-oct
```

Esto equivale a los siguientes comandos especificados explícitamente en la dirección URL:

```
style=customStyle.css
```

## Ejemplo 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

Un catálogo de imágenes llamado 2019 contiene la entrada `spin-oct`. El campo `catalog::UserData` de esta entrada de catálogo incluye los siguientes datos:

```
zoomStep=3 
maxZoom=200
```

Cargue el visor con el siguiente comando:

```
config=2019/spin-oct
```

Esto equivale a los siguientes comandos especificados explícitamente en la dirección URL:

```
zoomStep=3&maxZoom=200
```

## Ejemplo 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

Un ajuste preestablecido de visor denominado `Shoppable_Banner` incluye los siguientes datos:

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

Cargue el visor con el siguiente comando:

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

Esto equivale a los siguientes comandos especificados explícitamente en la dirección URL:

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Ejemplo 5 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

Un ajuste preestablecido de visor denominado `Shoppable_Video_Dark` contiene los siguientes datos:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

Cargue el visor con el siguiente comando:

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

Esto equivale a los siguientes comandos especificados explícitamente en la dirección URL:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Ejemplo 5 {#section-19b988551d1d492a9079948e0b04b38f}

Un ajuste preestablecido de visualizador denominado `Carousel_Dotted_light` los siguientes datos:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Cargue el visor con el siguiente comando:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Esto equivale a los siguientes comandos especificados explícitamente en la dirección URL:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

