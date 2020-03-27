---
description: nulo
seo-description: nulo
seo-title: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
topic: Dynamic media
uuid: c9989916-d0f3-4268-932a-e12c693f5b74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Establezca el valor en <span class="codeph"> 1</span> para activar la precarga de la imagen ampliada. </p> <p>Establezca en <span class="codeph"> 0</span> para cargar la imagen de zoom de forma incremental, según sea necesario. </p> <p> <p>Nota:  Tenga en cuenta que si habilita esta opción, puede resultar en un uso de ancho de banda considerablemente mayor, ya que la imagen ampliada debe cargarse en su totalidad, incluso si el usuario no realiza ninguna acción de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
