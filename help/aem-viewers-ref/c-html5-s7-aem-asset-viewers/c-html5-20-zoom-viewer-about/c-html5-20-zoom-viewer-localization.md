---
title: Localización de los elementos de la interfaz de usuario
description: El contenido que muestra el visor de vídeo está sujeto a localización, incluidos los botones de zoom y un botón de pantalla completa.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c386a09c-21ce-4105-b416-e6ae50219af0
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Localización de los elementos de la interfaz de usuario{#localization-of-user-interface-elements}

El contenido que muestra el visor de vídeo está sujeto a localización, incluidos los botones de zoom y un botón de pantalla completa.

Cada contenido textual del visualizador que se puede localizar se representa mediante un identificador especial del SDK del visualizador denominado SYMBOL. Cualquier SYMBOL tiene un valor de texto asociado predeterminado para la configuración regional en inglés ( `"en"`) con el visor incorporado. También puede tener valores definidos por el usuario configurados para tantas configuraciones regionales como sea necesario.

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

El código de la página web debe pasar dicho objeto de localización al constructor del visor como un valor de `localizedTexts` del objeto de configuración. Una opción alternativa es pasar el objeto de localización llamando a la función `setLocalizedTexts(localizationInfo)` método.

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta ARIA para el elemento de visualizador de nivel superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descripción de la función ARIA para el componente de vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Sugerencias de uso de ARIA para usuarios del teclado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botón Cerrar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botón Acercar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botón Reducir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botón para restablecer zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botón de pantalla completa en estado normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botón de pantalla completa en estado de pantalla completa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Desplácese hacia la izquierda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Desplácese hacia la derecha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Desplácese hacia arriba. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Desplácese hacia abajo. </p> </td> 
  </tr> 
 </tbody> 
</table>
