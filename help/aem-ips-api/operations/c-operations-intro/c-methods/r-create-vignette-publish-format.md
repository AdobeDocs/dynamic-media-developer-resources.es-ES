---
description: Crea un nuevo formato de publicación para una viñeta.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 5%

---

# createVignettePublishFormat{#createvignettepublishformat}

Crea un nuevo formato de publicación para una viñeta.

Los formatos de viñeta especifican el tamaño de las viñetas publicadas y sus miniaturas, así como los niveles de zoom, los parámetros de enfoque y la versión del formato de archivo para las viñetas producidas a partir de viñetas principales publicadas en un servidor de procesamiento de imágenes desde IPS.

Las versiones más recientes del servidor de procesamiento de imágenes admiten viñetas piramidales, lo que elimina la necesidad de definir tamaños de formato de viñeta específicos para la publicación.

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
   <td colname="col4"> Identificador de la compañía a la que pertenece la viñeta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Nombre para identificar el formato de publicación de viñeta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> <p>Especifica la anchura de destino de la vista de viñeta resultante en píxeles. </p> <p>Utilice cero para que la viñeta de salida tenga el mismo tamaño que la viñeta principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Crea una viñeta piramidal optimizada para la ampliación y la reducción en el servidor de procesamiento de imágenes. Empezando por el tamaño máximo, definido por los campos de tamaño de viñeta de destino, esto crea múltiples vistas de tamaño en un solo archivo de salida de viñeta. Cada tamaño de vista posterior se reduce a la mitad hasta que la anchura y la altura tengan un valor inferior a 128 x 128 píxeles. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Especifica la anchura en píxeles de cada miniatura creada. Esta configuración es opcional. Dejar como cero para que no haya archivo de miniaturas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Especifica el formato de archivo para las viñetas publicadas. Dada la nueva versión de Image Authoring y la versión anterior del servidor de procesamiento de imágenes, debe especificar una versión de viñeta que el servidor de procesamiento de imágenes pueda leer. Si especifica una versión superior, el servidor de procesamiento de imágenes no podrá leer las viñetas publicadas. Establézcalo en cero para publicar viñetas en la última versión. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Especifica el carácter que separa el nombre de la viñeta y el sufijo que indica su anchura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Especifica el carácter que separa el nombre de la viñeta y el sufijo que indica su anchura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> afilar</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Aplica enfoque a la imagen de vista principal para cada tamaño de viñeta de publicación. El enfoque puede compensar el desenfoque que se produce cuando las viñetas se reducen o se agrandan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> La máscara de enfoque digital es una forma flexible y eficaz de aumentar la nitidez, especialmente en imágenes digitalizadas. Esto controla la magnitud de cada sobregiro (cuánto más oscuros y claros se vuelven los bordes de borde). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Afecta al tamaño de las aristas que se van a mejorar o a la anchura de las aristas, por lo que un radio más pequeño aumenta el detalle a menor escala. Los valores de radio más altos pueden causar halos en los bordes. El detalle fino necesita un radio más pequeño, ya que se pierde un detalle minúsculo del mismo tamaño o más pequeño que el radio. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Controla el cambio de brillo mínimo que se va a enfocar o la distancia entre los valores tonales adyacentes que se deben situar antes de que el filtro funcione. Esta configuración puede enfocar los bordes más pronunciados sin modificar los más sutiles. El intervalo permitido de umbral de 0 a 255. </td> 
  </tr> 
 </tbody> 
</table>

**Salida (createVignettePublishFormatReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Sí | El controlador para el formato de viñeta creado. |

## Ejemplos {#section-0564752d439642b9bb8de2903db6de1e}

Este código crea un formato de publicación de viñeta. La solicitud de creación especifica un nombre, una anchura y altura de destino y otros valores necesarios.

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
