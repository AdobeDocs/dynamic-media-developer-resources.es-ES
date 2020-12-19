---
description: Actualiza la configuración del formato de publicación de la viñeta.
seo-description: Actualiza la configuración del formato de publicación de la viñeta.
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---


# updateVignettePublishFormat{#updatevignettepublishformat}

Actualiza la configuración del formato de publicación de la viñeta.

## Tipos de usuarios autorizados {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Entrada (updateVignettePublishFormatParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de compañía. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | Sí | Identificador de formato de publicación. |
| ` *`name`*` | `xsd:string` | No | Nombre del formato de publicación. |
| ` *`targetWidth`*` | `xsd:int` | Sí | Especifica el ancho de destinatario de la vista de viñeta resultante en píxeles. Utilice cero para que la viñeta de salida tenga el mismo tamaño que la viñeta principal. |
| ` *`targetHeight`*` | `xsd:int` | Sí | Especifica la altura de destinatario de la vista de viñeta resultante en píxeles. Utilice cero para que la viñeta de salida tenga el mismo tamaño que la viñeta principal. |
| ` *`createPyramid`*` | `xsd:boolean` | Sí | Crea una viñeta piramidal optimizada para la ampliación y la reducción en el servidor de procesamiento de imágenes. Partiendo desde el tamaño máximo, definido por los campos de tamaño de la viñeta de destino, esta opción crea múltiples vistas de tamaño en un solo archivo de salida de viñetas. Los tamaños de vista se van reduciendo a la mitad en orden hasta que la altura y la anchura están dentro del límite de 128 x 128 píxeles. |
| ` *`thumbWidth`*` | `xsd:int` | Sí | Especifica la anchura de cada miniatura resultante en píxeles. Esta configuración es opcional. Deje como cero para que no haya ningún archivo en miniatura. |
| ` *`saveAsVersion`*` | `xsd:int` | Sí | Especifica el formato de archivo para las viñetas publicadas. Dado que hay una nueva versión de Image Authoring y una versión anterior del servidor de procesamiento de imágenes, debe especificar una versión de viñeta que el servidor de procesamiento de imágenes pueda leer. Si especifica una versión posterior, el servidor de procesamiento de imágenes no podrá leer las viñetas publicadas. Establezca en cero para publicar viñetas en la última versión. |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | Sí | Especifica el carácter que se utiliza para separar el nombre de la viñeta y el sufijo que indica su anchura. |
| ` *`enfoque`*` | `xsd:int` | No | Aplica enfoque a la imagen de vista principal para cada tamaño de viñeta de publicación. El enfoque puede compensar el desenfoque cuando se escalan las viñetas. |
| ` *`usmAmount`*` | `xsd:double` | Sí | La máscara de enfoque digital es una forma flexible y potente de aumentar el enfoque, especialmente en imágenes escaneadas. Esto controla la magnitud de cada desbordamiento (la cantidad de bordes más oscuros y claros que se vuelven). |
| ` *`usmRadius`*` | `xsd:double` | Sí | Afecta al tamaño de los bordes que se van a mejorar o a la anchura de los bordes, por lo que un radio más pequeño mejora el detalle de menor escala. Los valores de radio más altos pueden provocar halos en los bordes. El detalle preciso necesita un radio más pequeño, ya que se pierde un detalle pequeño del mismo tamaño o menor que el radio. |
| ` *`usmThreshold`*` | `xsd:int` | Sí | Controla el cambio mínimo de brillo que se debe enfocar o la distancia entre los valores tonales adyacentes antes de que funcione el filtro. Este ajuste puede enfocar los bordes más pronunciados sin modificar los bordes más sutiles. El intervalo permitido del umbral es de 0 a 255. |

**Salida (updateVignettePublishFormatReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | Sí | Controlar el formato de publicación de la viñeta actualizado. |

## Ejemplo {#section-fcba4bf2b7264786a676e315a35dbe43}

Este ejemplo de código actualiza un formato de publicación de viñetas y devuelve el controlador al formato actualizado.

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

