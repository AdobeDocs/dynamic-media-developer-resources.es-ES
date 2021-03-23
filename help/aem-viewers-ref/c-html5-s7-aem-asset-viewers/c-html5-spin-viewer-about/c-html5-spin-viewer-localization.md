---
description: El contenido que muestra el visor de giros está sujeto a localización, incluidos los botones de zoom y el botón de pantalla completa.
seo-description: El contenido que muestra el visor de giros está sujeto a localización, incluidos los botones de zoom y el botón de pantalla completa.
seo-title: Localización de los elementos de la interfaz de usuario
solution: Experience Manager
title: Localización de los elementos de la interfaz de usuario
uuid: bf38bdef-a31f-4f2f-a8f5-3d3d4eac95ab
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---


# Localización de los elementos de la interfaz de usuario{#localization-of-user-interface-elements}

El contenido que muestra el visor de giros está sujeto a localización, incluidos los botones de zoom y el botón de pantalla completa.

Cada contenido textual del visualizador que se puede localizar se representa mediante un identificador especial del SDK del visualizador denominado SYMBOL. Cualquier SYMBOL tiene un valor de texto asociado predeterminado para la configuración regional de inglés ( `"en"`) que se proporciona con el visor predeterminado. También puede tener valores definidos por el usuario configurados para tantas configuraciones regionales como sea necesario.

Cuando se inicia el visor, comprueba la configuración regional actual para ver si hay un valor definido por el usuario para cada SÍMBOLO admitido para la configuración regional. Si existe, utiliza el valor definido por el usuario; de lo contrario, vuelve al texto predeterminado predeterminado predeterminado predeterminado.

Los datos de localización definidos por el usuario se pueden pasar al visor como un objeto JSON de localización. Este objeto contiene la lista de configuraciones regionales admitidas, los valores de texto SYMBOL para cada configuración regional y la configuración regional predeterminada.

Un ejemplo de este tipo de objeto de localización es el siguiente:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

En el ejemplo anterior, el objeto de localización define dos configuraciones regionales ( `"en"` y `"fr"`) y proporciona localización para dos elementos de interfaz de usuario en cada configuración regional.

El código de página web debe pasar el objeto de localización al constructor del visor, como un valor del campo `localizedTexts` del objeto de configuración. Una opción alternativa es pasar el objeto de localización llamando al método `setLocalizedTexts(localizationInfo)`.

Se admiten los siguientes SÍMBOLOS:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SÍMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Información de objeto para... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta ARIA para el elemento visualizador de nivel superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descripción de la función ARIA para el componente de vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>Sugerencias de uso de ARIA para usuarios del teclado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Cerrar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Acercar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Reducir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón para restablecer zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón de pantalla completa en estado normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón de pantalla completa en estado de pantalla completa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Girar a la izquierda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón derecho de giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

