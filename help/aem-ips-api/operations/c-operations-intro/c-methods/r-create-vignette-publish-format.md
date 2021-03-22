---
description: Crea un nuevo formato de publicación para una viñeta.
seo-description: Crea un nuevo formato de publicación para una viñeta.
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
uuid: 834ebe6a-e105-4075-8004-172237980933
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 14%

---


# createVignettePublishFormat{#createvignettepublishformat}

Crea un nuevo formato de publicación para una viñeta.

Los formatos de viñeta especifican el tamaño de las viñetas publicadas y sus miniaturas, así como los niveles de zoom, los parámetros de nitidez y la versión del formato de archivo para las viñetas producidas a partir de viñetas principales publicadas en un servidor de renderización de imágenes desde IPS.

Las versiones de servidor de renderización de imágenes más recientes admiten viñetas piramidales, lo que elimina la necesidad de definir tamaños de formato de viñeta específicos para la publicación.

## Tipos de usuarios autorizados {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Entrada (createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obligatorio </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Gestionar a la empresa a la que pertenece la viñeta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Nombre para identificar el formato de publicación de la viñeta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> <p>Especifica el ancho de destino de la vista de viñeta resultante en píxeles. </p> <p>Utilice cero para que la viñeta de salida tenga el mismo tamaño que la viñeta principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Crea una viñeta piramidal optimizada para la ampliación y la reducción en el servidor de procesamiento de imágenes. Partiendo desde el tamaño máximo, definido por los campos de tamaño de la viñeta de destino, esta opción crea múltiples vistas de tamaño en un solo archivo de salida de viñetas. Los tamaños de vista se van reduciendo a la mitad en orden hasta que la altura y la anchura están dentro del límite de 128 x 128 píxeles. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Especifica el ancho de cada miniatura resultante en píxeles. Esta configuración es opcional. Deje como cero para ningún archivo en miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Especifica el formato de archivo de las viñetas publicadas. Dado que hay una nueva versión de Creación de imágenes y una versión anterior del servidor de renderización de imágenes, debe especificar una versión de la viñeta que el servidor de renderización de imágenes pueda leer. Si especifica una versión superior, el servidor de renderización de imágenes no podrá leer las viñetas publicadas. Establézcalo en cero para publicar viñetas en la última versión. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Especifica el carácter que separa el nombre de la viñeta y el sufijo que indica su anchura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Especifica el carácter que separa el nombre de la viñeta y el sufijo que indica su anchura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> enfocar</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Aplica nitidez a la imagen de vista principal para cada tamaño de viñeta de publicación. El enfoque puede compensar el desenfoque cuando se escalan los viñedos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El enmascaramiento de enfoque digital es una forma flexible y potente de aumentar la nitidez, especialmente en imágenes escaneadas. Esto controla la magnitud de cada rebasamiento (cuánto más oscuros y claros se vuelven los bordes de borde). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Afecta al tamaño de los bordes que se van a mejorar o a la anchura de los bordes, por lo que un radio más pequeño mejora el detalle de escala más pequeña. Los valores de radio más altos pueden causar halos en los bordes. El detalle fino necesita un radio más pequeño, ya que se pierde un detalle minúsculo del mismo tamaño o menor que el radio. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Controla el cambio mínimo de brillo que se debe enfocar o la distancia que deben estar los valores tonales adyacentes antes de que funcione el filtro. Este ajuste puede enfocar los bordes más pronunciados sin modificar los bordes más sutiles. El rango permitido de umbral de 0 a 255. </td> 
  </tr> 
 </tbody> 
</table>

**Salida (createVignettePublishFormatReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`viñetaFormatoControlador`*` | `xsd:string` | Sí | El identificador del formato de viñeta creado. |

## Ejemplos {#section-0564752d439642b9bb8de2903db6de1e}

Este código crea el formato de publicación de la viñeta. La solicitud de creación especifica un nombre, una anchura y altura de destino y otros valores necesarios.

**Solicitar**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**Respuesta**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```

