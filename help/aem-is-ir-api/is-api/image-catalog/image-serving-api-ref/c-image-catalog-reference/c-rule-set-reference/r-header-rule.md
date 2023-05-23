---
description: Elemento de encabezado de respuesta HTTP. Opcional en <rule> elementos.
solution: Experience Manager
title: encabezado
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# encabezado{#header}

Elemento de encabezado de respuesta HTTP. Opcional en `<rule>` elementos.

## Atributos {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*texto*&quot;** : obligatorio. Especifica el nombre del encabezado HTTP.

**`Action`= &quot;set&quot; |`"add"`**: Opcional. El valor predeterminado es `"set"`, que reemplaza cualquier valor de encabezado actual. Especificar `"add"` para anexar el valor del encabezado, separado con una coma.

## Datos {#section-a387f541396c49d99c29692a38032914}

Valor del encabezado.

## Descripción {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permite añadir nuevos encabezados de respuesta HTTP, así como añadir o reemplazar valores de encabezados predefinidos. Los nombres y valores deben cumplir con los estándares HTTP. No se aplica ninguna codificación adicional.

Las variables de sustitución del servicio de imágenes se pueden utilizar en el nombre y el valor del encabezado. Esto permite controlar ambas cadenas desde la solicitud.

## Ejemplo {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La siguiente regla aplica un encabezado personalizado cuando el valor del encabezado se especifica en la solicitud como variable:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Esta regla se activa mediante la siguiente solicitud, que configura el encabezado de respuesta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
