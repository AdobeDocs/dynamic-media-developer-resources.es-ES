---
description: El contenido que muestra el visor flotante está sujeto a localización. Este contenido incluye información sobre herramientas de elementos de la interfaz de usuario y mensajes de información que se muestran en la vista de zoom flotante al cargar.
solution: Experience Manager
title: Localización de los elementos de la interfaz de usuario
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Developer,Business Practitioner
exl-id: 57941e90-1462-43e6-80db-6b111e004f9b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Localización de los elementos de la interfaz de usuario{#localization-of-user-interface-elements}

El contenido que muestra el visor flotante está sujeto a localización. Este contenido incluye información sobre herramientas de elementos de la interfaz de usuario y mensajes de información que se muestran en la vista de zoom flotante al cargar.

Cada contenido textual del visualizador que se puede localizar se representa mediante un identificador especial del SDK del visualizador denominado SYMBOL. Cualquier SYMBOL tiene un valor de texto asociado predeterminado para la configuración regional de inglés ( `"en"`) que se proporciona con el visor predeterminado. También puede tener valores definidos por el usuario configurados para tantas configuraciones regionales como sea necesario.

Cuando se inicia el visor, comprueba la configuración regional actual para ver si hay un valor definido por el usuario para cada SÍMBOLO admitido para la configuración regional. Si existe, utiliza el valor definido por el usuario; de lo contrario, vuelve al texto predeterminado predeterminado predeterminado predeterminado.

Los datos de localización definidos por el usuario se pueden pasar al visor como un objeto JSON de localización. Este objeto contiene la lista de configuraciones regionales admitidas, los valores de texto SYMBOL para cada configuración regional y la configuración regional predeterminada.

Un ejemplo de este tipo de objeto de localización es el siguiente:

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

En el ejemplo anterior, el objeto de localización define dos configuraciones regionales ( `"en"` y `"fr"`) y proporciona localización para dos elementos de interfaz de usuario en cada configuración regional.

El código de página web debe pasar el objeto de localización al constructor del visor, como valor del campo `localizedTexts` del objeto de configuración. Una opción alternativa es pasar el objeto de localización llamando al método `setLocalizedTexts(localizationInfo)`.

Se admiten los siguientes SÍMBOLOS:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SÍMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta ARIA para el elemento visualizador de nivel superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descripción de la función ARIA para el componente de vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>Sugerencias de uso de ARIA para usuarios del teclado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER  </span> </p> </td> 
   <td colname="col2"> <p>Mensaje de información para sistemas de escritorio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP  </span> </p> </td> 
   <td colname="col2"> <p>Mensaje de información para dispositivos táctiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Información del objeto para el botón de desplazamiento izquierdo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Información del objeto para el botón derecho de desplazamiento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Información del objeto para el botón de desplazamiento hacia arriba. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Información del objeto para el botón de desplazamiento hacia abajo. </p> </td> 
  </tr> 
 </tbody> 
</table>
