---
description: Cierto contenido que muestra el visor de catálogos electrónicos está sujeto a localización, incluidos botones de zoom, botones de cambio de página, botón de miniatura, botón de pantalla completa, botón de cierre y botones de barra de desplazamiento.
seo-description: Cierto contenido que muestra el visor de catálogos electrónicos está sujeto a localización, incluidos botones de zoom, botones de cambio de página, botón de miniatura, botón de pantalla completa, botón de cierre y botones de barra de desplazamiento.
seo-title: Localización de los elementos de la interfaz de usuario
solution: Experience Manager
title: Localización de los elementos de la interfaz de usuario
uuid: bd95c7dc-3158-4cca-81d4-f5efd57c0124
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 0%

---


# Localización de los elementos de la interfaz de usuario{#localization-of-user-interface-elements}

Cierto contenido que muestra el visor de catálogos electrónicos está sujeto a localización, incluidos botones de zoom, botones de cambio de página, botón de miniatura, botón de pantalla completa, botón de cierre y botones de barra de desplazamiento.

Cada contenido textual del visualizador que se puede localizar se representa mediante un identificador especial del SDK del visualizador denominado SYMBOL. Cualquier SYMBOL tiene un valor de texto asociado predeterminado para la configuración regional de inglés ( `"en"`) que se proporciona con el visor incorporado, y también puede tener valores definidos por el usuario definidos para tantas configuraciones regionales como sea necesario.

Cuando se inicia el visor, comprueba la configuración regional actual para ver si hay un valor definido por el usuario para cada SYMBOL admitido en la configuración regional. Si existe, utiliza el valor definido por el usuario; de lo contrario, vuelve al texto predeterminado predeterminado predeterminado predeterminado.

Los datos de localización definidos por el usuario se pueden pasar al visor como un objeto JSON de localización. Este objeto contiene la lista de configuraciones regionales admitidas, los valores de texto SYMBOL para cada configuración regional y la configuración regional predeterminada.

Un ejemplo de este objeto de localización:

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

El código de la página web debe pasar dicho objeto de localización al constructor del visor como un valor del campo `localizedTexts` del objeto de configuración. Una opción alternativa es pasar el objeto de localización llamando al método `setLocalizedTexts(localizationInfo)`.

Se admiten los siguientes SYMBOL (suponiendo que containerId es el ID del contenedor del visor):

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SÍMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Información del objeto para... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta ARIA para el elemento de visualizador de nivel superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descripción de la función ARIA para el componente de vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT  </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Desplácese hacia arriba. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Desplácese hacia abajo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_rightButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Grande de la página siguiente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_leftButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón de página anterior grande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_lastPageButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Última página . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secundarioLastPageButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Última página . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_firstPageButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Primera página . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secundarioFirstPageButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Primera página . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarRightButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón de página siguiente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón de página anterior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón Miniaturas en modo de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón Miniaturas en modo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Cerrar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Botón de cierre del panel de información. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Herramienta de uso compartido en medios sociales . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Compartir correo electrónico . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Encabezado del cuadro de diálogo de correo electrónico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Cuadro de diálogo Correo electrónico, botón de cierre superior derecho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS  </span> </p> </td> 
   <td colname="col2"> <p>Mensaje de error mostrado en caso de que la dirección de correo electrónico tenga un formato incorrecto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO  </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta del campo de entrada "A". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD  </span> </p> </td> 
   <td colname="col2"> <p>Botón Agregar otra dirección de correo electrónico . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD  </span> </p> </td> 
   <td colname="col2"> <p>Botón Agregar otra dirección de correo electrónico . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM  </span> </p> </td> 
   <td colname="col2"> <p>Desde el campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE  </span> </p> </td> 
   <td colname="col2"> <p>Campo de entrada de mensaje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE  </span> </p> </td> 
   <td colname="col2"> <p>Botón Quitar dirección de correo electrónico . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Botón Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración para el botón Seleccionar todo . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Seleccione Todo . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Rótulo del botón de cierre que se muestra en la parte inferior del cuadro de diálogo después del envío del formulario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Botón Cerrar que se muestra en la parte inferior del cuadro de diálogo después del envío del formulario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón de envío del formulario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Botón de envío de formulario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS  </span> </p> </td> 
   <td colname="col2"> <p>El mensaje de confirmación se mostraba cuando el correo electrónico se enviaba correctamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE  </span> </p> </td> 
   <td colname="col2"> <p>Mensaje de error que se muestra cuando el correo electrónico no se envió correctamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Insertar uso compartido . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Encabezado del cuadro de diálogo Incrustar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Cuadro de diálogo Incrustar botón de cierre superior derecho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descripción del texto del código incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta del cuadro combinado Tamaño incrustado . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Botón Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>Texto de la última entrada de "tamaño personalizado" en el cuadro combinado de tamaño incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Compartir vínculo . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Encabezado del cuadro de diálogo Vínculo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Cuadro de diálogo Vínculo botón de cierre superior derecho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descripción del vínculo compartido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Botón Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración para el botón Seleccionar todo . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> Seleccione Todo . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Compartir de Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Compartir en Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón Imprimir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Imprimir encabezado del cuadro de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Cuadro de diálogo Imprimir botón de cierre superior derecho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE  </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta de la sección "Seleccionar páginas de impresión". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón de radio "Páginas actuales". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón de radio "Intervalo de propagación desde". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración para el selector numérico "to". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración para el botón de radio "Todas las páginas". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_MANDLING  </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta de la sección "Administración de páginas". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón de opción "1 página por hoja". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración para el botón de opción "2 páginas por hoja". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p> Botón Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Pie de ilustración del botón Enviar a impresión </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> Botón Enviar a impresión. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesMenu.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botón de menú Favoritos . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón "Agregar favorito" en el modo de edición de Favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón "Agregar favorito" en modo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón "Eliminar favorito" en el modo de edición de Favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón "Eliminar favorito" en modo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón "Ver todos los favoritos" cuando la vista Favoritos está activa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón "Ver todos los favoritos" cuando la vista Favoritos está inactiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesEffect.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Icono de un solo favorito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY]  </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta de página que genera el visor en el momento de la carga. </p> <p>El nombre de ese símbolo es una plantilla, donde <span class="codeph"> XX </span> es un índice de propagación basado en cero en orientación horizontal, y opcional <span class="codeph"> YY </span> es un índice de página de base cero dentro del pliego dirigido por <span class="codeph"> XX </span>. </p> <p>Se aplica solo al recurso cargado inicialmente; se ignorará si se cambia un recurso mediante la llamada de API <span class="codeph"> setAsset() </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM  </span> </p> </td> 
   <td colname="col2"> <p> Carácter utilizado como delimitador de etiquetas de página en caso de que las etiquetas se definan para páginas de izquierda y derecha dentro de un pliego. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón de desplazamiento izquierdo de la barra de control principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botón derecho de desplazamiento de la barra de control principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

