---
title: bgc
description: Ver color de fondo. Especifica el color de fondo de la imagen compuesta (ver imagen).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# bgc{#bgc}

Ver color de fondo. Especifica el color de fondo de la imagen compuesta (ver imagen).

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span></span> </p> </td> 
  <td class="stentry"> <p>Valor de color gris, RGB o CMYK. </p></td> 
 </tr> 
</table>

Especifica el color de relleno opaco que se utilizará para el fondo de vista. Solo visible si la imagen compuesta tiene áreas transparentes o si la imagen compuesta tiene una proporción de aspecto diferente a la del rectángulo de vista. Se ignoró si `fmt=tif-alpha`, `fmt=png-alpha` o `req=mask`.

>[!NOTE]
>
>`bgc=` omite el sufijo de color &quot;s&quot;. Los valores de color especificados con `bgc=` siempre se asocian con el espacio de color de salida correspondiente.

## Propiedades {#section-b729b50b1ea7433b82ba34ecd61839cd}

Ver atributo. Se aplica independientemente de la configuración de capa actual. Se ignoró si `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha` o `fmt=swf-alpha`.

Se ignorará cualquier valor alfa especificado por color.

Se supone que *`color`* pertenece al espacio de color de salida (como se especifica con `icc=`) y debe tener el mismo tipo de píxel que la imagen de salida. Si los tipos de píxeles no coinciden, *`color`* se convierte con una conversión naïve.

## Predeterminado {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Ejemplo {#section-7bcdfbc0e1274e86a69d39186b090789}

Especifique un color de fondo explícito para una solicitud de miniatura:

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Véase también {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [atributo::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Administración de color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
