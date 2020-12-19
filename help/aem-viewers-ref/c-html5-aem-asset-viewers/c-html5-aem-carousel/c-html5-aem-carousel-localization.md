---
description: Determinado contenido que muestra el visor de carrusel está sujeto a localización. Esto incluye los botones de navegación de las diapositivas.
seo-description: Determinado contenido que muestra el visor de carrusel está sujeto a localización. Esto incluye los botones de navegación de las diapositivas.
seo-title: Localización de los elementos de la interfaz de usuario
solution: Experience Manager
title: Localización de los elementos de la interfaz de usuario
topic: Dynamic media
uuid: 82e4dc72-cc12-4ab5-8370-6270f9a3d45f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Localización de los elementos de la interfaz de usuario{#localization-of-user-interface-elements}

Determinado contenido que muestra el visor de carrusel está sujeto a localización. Esto incluye los botones de navegación de las diapositivas.

Todo el contenido textual del visor que se puede localizar se representa mediante el identificador especial del SDK del visor denominado SYMBOL. Cualquier SYMBOL tiene un valor de texto asociado predeterminado para una configuración regional en inglés ( `"en"`) que se suministra con el visor incorporado, y también puede tener valores definidos por el usuario para tantas configuraciones regionales como sea necesario.

Cuando el visor inicio, comprueba la configuración regional actual para ver si hay un valor definido por el usuario para cada SÍMBOLO admitido para dicha configuración regional. Si la hay, utiliza el valor definido por el usuario; de lo contrario, se remonta al texto predeterminado predefinido.

Los datos de localización definidos por el usuario se pueden pasar al visor como un objeto JSON de localización. Dicho objeto contiene la lista de configuraciones regionales admitidas, los valores de texto SYMBOL para cada configuración regional y la configuración regional predeterminada.

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

En el ejemplo anterior, el objeto localización define dos configuraciones regionales ( `"en"` y `"fr"`) y proporciona localización para dos elementos de interfaz de usuario en cada configuración regional.

El código de página web debe pasar el objeto de localización al constructor del visor, como un valor de `localizedTexts` campo del objeto de configuración. Una opción alternativa es pasar el objeto de localización llamando al método `setLocalizedTexts(localizationInfo)`.

Se admiten los siguientes SÍMBOLOS:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SÍMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Información del objeto para... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Estado del botón de reproducción pausa seleccionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Estado del botón de reproducción pausa no seleccionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO  </span> </p> </td> 
   <td colname="col2"> <p> Información del objeto y etiqueta ARIA para los botones de diapositiva anterior y siguiente. </p> <p>Acepta dos tokens de reemplazo: <span class="codeph"> $CURRENT_FRAME$ </span> para el índice de diapositivas actual y <span class="codeph"> $TOTAL_FRAMES$ </span> para el número total de diapositivas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Contenedor.ETIQUETA  </span> </p> </td> 
   <td colname="col2"> <p> Etiqueta ARIA para el elemento de visor de nivel superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p> Descripción de la función ARIA para el componente de vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p> Sugerencias de uso de ARIA para usuarios de teclado. </p> </td> 
  </tr> 
 </tbody> 
</table>

