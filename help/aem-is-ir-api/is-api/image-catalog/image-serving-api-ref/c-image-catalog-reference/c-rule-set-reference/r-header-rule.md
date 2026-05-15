---
title: encabezado
description: Elemento de encabezado de respuesta HTTP. Opcional en elementos <rule>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
TQID: 'https://experienceleague.adobe.com/-hGRn7zVjm8eavZIwBoiAuCqoSNYIFSSlQaSP6wuHXs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 4%

---

# encabezado{#header}

Elemento de encabezado de respuesta HTTP. Opcional en `<rule>` elementos.

## Atributos {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*texto*&quot;** : obligatorio. Especifica el nombre del encabezado HTTP.

**`Action`= &quot;establecido&quot; |`"add"`**: opcional. El valor predeterminado es `"set"`, que reemplaza cualquier valor del encabezado actual. Especifique `"add"` para que pueda anexar el valor del encabezado, separado con una coma.

## Datos {#section-a387f541396c49d99c29692a38032914}

Valor del encabezado.

## Descripción {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permite añadir nuevos encabezados de respuesta HTTP y añadir o reemplazar valores de encabezados predefinidos. Los nombres y valores deben cumplir con los estándares HTTP. No se aplica ninguna codificación adicional.

Las variables de sustitución del servicio de imágenes se pueden utilizar en el nombre y el valor del encabezado. Esto permite controlar ambas cadenas desde la solicitud.

## Ejemplo {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La siguiente regla aplica un encabezado personalizado cuando el valor del encabezado se especifica en la solicitud como variable:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Esta regla se activa mediante la siguiente solicitud, que establece el encabezado de respuesta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
