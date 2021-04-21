---
description: Archivo de viñeta. Especifica la viñeta que se utilizará para esta solicitud.
solution: Experience Manager
title: viñeta
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 4%

---


# viñeta{#vignette}

Archivo de viñeta. Especifica la viñeta que se utilizará para esta solicitud.

`vignette=[ *``*/] *``*|[catId/] *`catIdrecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>ID del catálogo de materiales (coincide con el atributo <span class="codeph">::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>ID de viñeta (coincide con la viñeta <span class="codeph">::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> archivo</span> </p></td> 
  <td class="stentry"> <p>Nombre y ruta del archivo de la viñeta relativa. </p></td> 
 </tr> 
</table>

Puede especificar una entrada de mapa de viñeta o un archivo de viñeta. No se permiten direcciones URL remotas.

`vignette=` se puede utilizar como alternativa para especificar la viñeta en la ruta URL de la solicitud. Se utiliza principalmente para especificar viñetas mediante variables en plantillas.

Si no se especifica *`catId`*, se utiliza el catálogo de sesiones.

## Propiedades {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Puede ocurrir en cualquier lugar dentro de la solicitud. Anula la viñeta especificada con la ruta de URL de la solicitud.

## Predeterminado {#section-db0618d48bc84dc8abcc989550349ccc}

Ninguno.

## Véase también {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Catálogos](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) de materiales, variables  [personalizadas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
