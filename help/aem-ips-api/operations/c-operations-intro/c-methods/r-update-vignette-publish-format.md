---
description: Actualiza la configuración del formato de publicación de viñeta.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 6%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

Actualiza la configuración del formato de publicación de viñeta.

## Tipos de usuarios autorizados {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Entrada (updateVignettePublishFormatParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| vignetteFormatHandle | `xsd:string` | Sí | Controlador de formato de publicación. |
| nombre | `xsd:string` | No | Nombre del formato de publicación. |
| targetWidth | `xsd:int` | Sí | Especifica la anchura de destino de la vista de viñeta resultante en píxeles. Utilice cero para que la viñeta de salida tenga el mismo tamaño que la viñeta principal. |
| targetHeight | `xsd:int` | Sí | Especifica la altura de destino de la vista de viñeta resultante en píxeles. Utilice cero para que la viñeta de salida tenga el mismo tamaño que la viñeta principal. |
| createPyramid | `xsd:boolean` | Sí | Crea una viñeta piramidal optimizada para la ampliación y la reducción en el servidor de procesamiento de imágenes. Empezando por el tamaño máximo, definido por los campos de tamaño de viñeta de destino, esto crea múltiples vistas de tamaño en un solo archivo de salida de viñeta. Cada tamaño de vista posterior se reduce a la mitad hasta que la anchura y la altura tengan un valor inferior a 128 x 128 píxeles. |
| thumbWidth | `xsd:int` | Sí | Especifica la anchura en píxeles de cada miniatura creada. Esta configuración es opcional. Dejar como cero para que no haya archivo de miniaturas. |
| saveAsVersion | `xsd:int` | Sí | Especifica el formato de archivo para las viñetas publicadas. Dada la nueva versión de Image Authoring y una versión más antigua del servidor de procesamiento de imágenes, debe especificar una versión de viñeta que el servidor de procesamiento de imágenes pueda leer. Si especifica una versión superior, el servidor de procesamiento de imágenes no podrá leer las viñetas publicadas. Establézcalo en cero para publicar viñetas en la última versión. |
| sizeSuffixSeparator | `xsd:string` | Sí | Especifica el carácter que separa el nombre de la viñeta y el sufijo que indica su anchura. |
| afilar | `xsd:int` | No | Aplica enfoque a la imagen de vista principal para cada tamaño de viñeta de publicación. El enfoque puede compensar el desenfoque que se produce cuando las viñetas se reducen o se agrandan. |
| usmAmount | `xsd:double` | Sí | La máscara de enfoque digital es una forma flexible y eficaz de aumentar la nitidez, especialmente en imágenes digitalizadas. Esto controla la magnitud de cada sobregiro (cuánto más oscuros y claros se vuelven los bordes de borde). |
| usmRadius | `xsd:double` | Sí | Afecta al tamaño de las aristas que se van a mejorar o a la anchura de las aristas, por lo que un radio más pequeño aumenta el detalle a menor escala. Los valores de radio más altos pueden causar halos en los bordes. El detalle fino necesita un radio más pequeño, ya que se pierde un detalle minúsculo del mismo tamaño o más pequeño que el radio. |
| usmThreshold | `xsd:int` | Sí | Controla el cambio de brillo mínimo que se va a enfocar o la distancia entre los valores tonales adyacentes que se deben situar antes de que el filtro funcione. Esta configuración puede enfocar los bordes más pronunciados sin modificar los más sutiles. El intervalo permitido de umbral es de 0 a 255. |

**Salida (updateVignettePublishFormatReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | Sí | Administrar al formato de publicación de viñeta actualizado. |

## Ejemplo {#section-fcba4bf2b7264786a676e315a35dbe43}

Este ejemplo de código actualiza un formato de publicación de viñeta y devuelve el identificador al formato actualizado.

**Solicitar**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Respuesta**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```
