---
title: Localización de los elementos de la interfaz de usuario
description: Cierto contenido que muestra el Visor de carrusel está sujeto a la localización. Este contenido incluye botones de navegación con diapositivas.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Localización de los elementos de la interfaz de usuario{#localization-of-user-interface-elements}

Cierto contenido que muestra el Visor de carrusel está sujeto a la localización. Este contenido incluye botones de navegación con diapositivas.

Cada contenido textual del visualizador que se puede localizar se representa mediante el identificador especial del SDK del visualizador, denominado SYMBOL. Cualquier SYMBOL tiene un valor de texto asociado predeterminado para una configuración regional en inglés ( `"en"`) se suministra con el visor predeterminado y también puede tener valores definidos por el usuario para tantas configuraciones regionales como sea necesario.

Cuando se inicia el visor, comprueba la configuración regional actual para ver si hay un valor definido por el usuario para cada SYMBOL admitido para dicha configuración regional. Si existe, utiliza el valor definido por el usuario; de lo contrario, vuelve al texto predeterminado predeterminado.

Los datos de localización definidos por el usuario se pueden pasar al visor como un objeto JSON de localización. Este objeto contiene la lista de configuraciones regionales admitidas, los valores de texto SYMBOL para cada configuración regional y la configuración regional predeterminada.

Un ejemplo de este objeto de localización es el siguiente:

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

En el ejemplo anterior, el objeto de localización define dos configuraciones regionales ( `"en"` y `"fr"`) y proporciona localización para dos elementos de interfaz de usuario en cada configuración regional.

El código de la página web debe pasar el objeto de localización al constructor del visor como un valor de `localizedTexts` del objeto de configuración. Una opción alternativa es pasar el objeto de localización llamando a `setLocalizedTexts(localizationInfo)` método.

Se admiten los siguientes SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SIGNO </p> </th> 
   <th colname="col2" class="entry"> <p>Información del objeto para... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Estado del botón de pausa de reproducción seleccionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Estado del botón de pausa de reproducción no seleccionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> Información del objeto y etiqueta ARIA para los botones de diapositiva anterior y siguiente. </p> <p>Acepta dos tokens de reemplazo: <span class="codeph"> $CURRENT_FRAME$ </span> para el índice de diapositiva actual y <span class="codeph"> $TOTAL_FRAMES$ </span> para el número total de diapositivas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> Etiqueta ARIA para el elemento de visor de nivel superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> Descripción de la función ARIA para el componente de vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> Sugerencias de uso de ARIA para usuarios de teclado. </p> </td> 
  </tr> 
 </tbody> 
</table>
