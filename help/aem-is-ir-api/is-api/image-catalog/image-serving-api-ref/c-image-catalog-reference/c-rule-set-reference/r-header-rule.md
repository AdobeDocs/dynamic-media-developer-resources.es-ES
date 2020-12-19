---
description: Elemento de encabezado de respuesta HTTP. Opcional en elementos <rule>.
seo-description: Elemento de encabezado de respuesta HTTP. Opcional en elementos <rule>.
seo-title: encabezado
solution: Experience Manager
title: encabezado
topic: Scene7 Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---


# encabezado{#header}

Elemento de encabezado de respuesta HTTP. Opcional en elementos `<rule>`.

## Atributos {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Requerido. Especifica el nombre del encabezado HTTP.

**`Action`= &quot;set&quot; |`"add"`**: Opcional. El valor predeterminado es `"set"`, que reemplaza cualquier valor de encabezado actual. Especifique `"add"` para anexar el valor del encabezado, separado con una coma.

## Datos {#section-a387f541396c49d99c29692a38032914}

Valor del encabezado.

## Descripción {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permite agregar nuevos encabezados de respuesta HTTP, así como agregar o reemplazar valores de encabezados predefinidos. Los nombres y valores deben cumplir los estándares HTTP. No se aplicará ninguna codificación adicional.

Las variables de sustitución del servicio de imágenes pueden utilizarse en el nombre del encabezado y en el valor del encabezado. Esto permite controlar ambas cadenas desde la solicitud.

## Ejemplo {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La regla siguiente aplica un encabezado personalizado cuando el valor del encabezado se especifica en la solicitud como una variable:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Esta regla se activa mediante la siguiente solicitud, que establece el encabezado de respuesta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
