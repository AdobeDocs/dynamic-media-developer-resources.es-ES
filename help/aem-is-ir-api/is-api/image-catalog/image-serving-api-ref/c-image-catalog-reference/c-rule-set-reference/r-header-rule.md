---
description: Elemento de encabezado de respuesta HTTP. Opcional en elementos <rule> .
solution: Experience Manager
title: encabezado
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---


# encabezado{#header}

Elemento de encabezado de respuesta HTTP. Opcional en elementos `<rule>`.

## Atributos {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Requerido. Especifica el nombre del encabezado HTTP.

**`Action`= &quot;set&quot; |`"add"`**: Opcional. El valor predeterminado es `"set"`, que reemplaza cualquier valor de encabezado actual. Especifique `"add"` para anexar el valor del encabezado, separado con una coma.

## Datos {#section-a387f541396c49d99c29692a38032914}

Valor de encabezado.

## Descripción {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permite agregar nuevos encabezados de respuesta HTTP, así como agregar o reemplazar valores de encabezados predefinidos. Los nombres y valores deben cumplir los estándares HTTP. No se aplicará ninguna codificación adicional.

Las variables de sustitución de Image Serving se pueden utilizar en el nombre del encabezado y en el valor del encabezado. Esto permite controlar ambas cadenas desde la solicitud.

## Ejemplo {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La regla siguiente aplica un encabezado personalizado cuando el valor del encabezado se especifica en la solicitud como variable:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Esta regla se activa mediante la siguiente solicitud, que configura el encabezado de respuesta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
