---
title: Personalización del visor de búsqueda de catálogos electrónicos
description: Toda la personalización visual y la mayor parte de la personalización del comportamiento para el visor de búsqueda en el catálogo electrónico se realiza creando un CSS personalizado.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 0%

---

# Personalización del visor de búsqueda de catálogos electrónicos{#customizing-ecatalog-search-viewer}

Toda la personalización visual y la mayor parte de la personalización del comportamiento para el visor de búsqueda en el catálogo electrónico se realiza creando un CSS personalizado.

El flujo de trabajo sugerido es tomar el archivo CSS predeterminado para el visor apropiado, copiarlo en una ubicación diferente, personalizarlo y especificar la ubicación del archivo personalizado en la variable `style=` comando.

Los archivos CSS predeterminados se encuentran en la siguiente ubicación:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

El archivo CSS personalizado debe contener las mismas declaraciones de clase que la predeterminada. Si se omite una declaración de clase, el visor no funciona correctamente porque no proporciona estilos predeterminados integrados para los elementos de la interfaz de usuario.

Una alternativa para proporcionar reglas CSS personalizadas es utilizar estilos incrustados directamente en la página web o en una de las reglas CSS externas vinculadas.

Al crear CSS personalizada, tenga en cuenta que el visor asigna `.s7ecatalogsearchviewer` a su elemento DOM contenedor. Si utiliza un archivo CSS externo que se pasa con la variable `style=` comando, usar `.s7ecatalogsearchviewer` como clase principal en el selector descendiente para sus reglas CSS. Si está realizando estilos incrustados en la página web, también debe clasificar este selector con un ID del elemento DOM de contenedor de la siguiente manera:

`#<containerId>.s7ecatalogsearchviewer`

## Creación de una CSS diseñada adaptable {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Es posible dirigirse a diferentes dispositivos e incrustar tamaños en CSS para que el contenido se muestre de forma diferente, según el dispositivo del usuario o un diseño de página web concreto. Esta segmentación incluye, entre otros, diferentes diseños de página web, tamaños de elementos de interfaz de usuario y resolución de ilustraciones.

El visor admite dos métodos para crear CSS diseñada con capacidad de respuesta: Marcadores CSS y consultas de medios CSS estándar. Puede utilizar estos métodos de forma independiente o conjunta.

**Marcadores CSS**

Para crear una CSS diseñada y adaptable, el visor admite marcadores CSS con clases CSS especiales asignadas dinámicamente al elemento contenedor del visor de nivel superior, en función del tamaño del visor de tiempo de ejecución y del tipo de entrada del dispositivo actual.

El primer grupo de marcadores CSS incluye `.s7size_large`, `.s7size_medium`y `.s7size_small` clases . Se aplican en función del área de tiempo de ejecución del contenedor de visor. Es decir, si el área del visor es igual o mayor que el tamaño de un monitor de escritorio común `.s7size_large` se utiliza; si el tamaño de la zona es cercano a un comprimido común `.s7size_medium` se asigna. Para áreas similares a las pantallas de teléfonos móviles. El marcador `.s7size_small` está configurado. El objetivo principal de estos marcadores CSS es crear diferentes diseños de interfaz de usuario para diferentes pantallas y tamaños de visor.

El segundo grupo de marcadores CSS incluye `.s7mouseinput` y `.s7touchinput`. El marcador `.s7touchinput` se establece si el dispositivo actual tiene capacidades de entrada táctil; de lo contrario, `.s7mouseinput` se utiliza. Estos marcadores están diseñados para crear elementos de entrada de interfaz de usuario con diferentes tamaños de pantalla para diferentes tipos de entrada, ya que la entrada táctil suele requerir elementos más grandes. En caso de que el dispositivo tenga funciones táctiles y de entrada de ratón, `.s7touchinput` y el visor presenta una interfaz de usuario táctil.

El siguiente ejemplo de CSS establece el tamaño del botón de zoom en 28 x 28 píxeles en sistemas con entrada de ratón y 56 x 56 píxeles en dispositivos táctiles. Además, oculta completamente el botón si el tamaño del visor es demasiado pequeño:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Para dirigirse a dispositivos con una densidad de píxeles diferente, utilice consultas de medios CSS. El siguiente bloque de consulta de medios contendría una CSS específica para pantallas de alta densidad:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

El uso de marcadores CSS es la forma más flexible de crear CSS adaptable. Le permite segmentar no solo el tamaño de la pantalla del dispositivo, sino también el tamaño real del visor, lo que resulta útil para los diseños de página interactivos.

Utilice el archivo CSS del visor predeterminado como ejemplo de un enfoque de marcadores CSS.

**Consultas de medios CSS**

La detección de dispositivos también se puede realizar utilizando consultas de medios CSS puras. Todo lo incluido en un bloque de consulta de contenido determinado se aplica solo cuando se ejecuta en un dispositivo correspondiente.

Cuando se aplique a los visualizadores móviles, utilice cuatro consultas de medios CSS, definidas en el CSS en el siguiente orden:

1. Contiene solo reglas específicas para todos los dispositivos táctiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Contiene solo reglas específicas para tabletas con pantallas de alta resolución.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contiene solo reglas específicas para todos los teléfonos móviles.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contiene solo reglas específicas para teléfonos móviles con pantallas de alta resolución.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Con un enfoque de consultas de medios, debe organizar CSS con detección de dispositivos de la siguiente manera:

* En primer lugar, la sección específica del escritorio define todas las propiedades que son específicas del escritorio o comunes a todas las pantallas.
* Y, en segundo lugar, las cuatro consultas de medios van en el orden definido anteriormente y proporcionan reglas CSS específicas para el tipo de dispositivo correspondiente.

No es necesario duplicar todo el CSS del visor en cada consulta de medios. Solo las propiedades específicas de determinados dispositivos se redefinen dentro de una consulta de medios.

## Sprites CSS {#section-9d570f95eb2443aca74c1b02f6e89aff}

Muchos elementos de la interfaz de usuario del visor están diseñados con ilustraciones de mapa de bits y tienen más de un estado visual distinto. Un buen ejemplo es un botón que normalmente tiene al menos tres estados diferentes: &quot;up&quot;, &quot;over&quot; y &quot;down&quot;. Cada estado requiere su propia ilustración de mapa de bits asignada.

Con un enfoque clásico del estilo, el CSS tendría una referencia independiente al archivo de imagen individual en el servidor para cada estado del elemento de la interfaz de usuario. El siguiente es un ejemplo de CSS para aplicar estilo a un botón de acercamiento:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

El inconveniente de este enfoque es que el usuario final experimenta parpadeos o retraso en la respuesta de la interfaz de usuario cuando se interactúa con el elemento por primera vez. Esta acción se produce porque la ilustración de la imagen para el nuevo estado del elemento aún no se ha descargado. Además, este enfoque puede tener un ligero impacto negativo en el rendimiento debido a un aumento en el número de llamadas HTTP al servidor.

Los sprites CSS son un enfoque diferente en el que las ilustraciones de imágenes para todos los estados de elementos se combinan en un solo archivo PNG denominado &quot;sprite&quot;. Este &quot;Sprite&quot; tiene todos los estados visuales para el elemento dado posicionado uno tras otro. Al diseñar un elemento de interfaz de usuario con sprites, se hace referencia a la misma imagen sprite para todos los estados diferentes en el CSS. Además, el `background-position` se utiliza para cada estado para especificar qué parte de la imagen &quot;sprite&quot; se utiliza. Puede estructurar una imagen &quot;sprite&quot; de cualquier manera adecuada. Normalmente, los visualizadores lo tienen apilado verticalmente. A continuación se muestra un ejemplo basado en &quot;sprite&quot; de cómo aplicar estilo al mismo botón de acercamiento desde arriba:

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Notas de estilo y consejos generales {#section-95855dccbbc444e79970f1aaa3260b7b}

* Al personalizar la interfaz de usuario del visor con CSS, el uso de la variable `!IMPORTANT` regla no es compatible con los elementos del visualizador de estilo. En particular, `!IMPORTANT` no debe utilizarse para anular ningún estilo predeterminado o en tiempo de ejecución proporcionado por el visor o el SDK del visor. La razón es que puede afectar al comportamiento de los componentes adecuados. En su lugar, debe utilizar selectores CSS con la especificidad adecuada para establecer las propiedades CSS que se documentan en esta guía de referencia.
* Todas las rutas a los recursos externos dentro de CSS se resuelven en la ubicación de CSS, no en la ubicación de la página del HTML del visor. Tenga en cuenta esta regla cuando copie el CSS predeterminado en una ubicación diferente. Copie también los recursos predeterminados o actualice las rutas dentro del CSS personalizado.
* El formato preferido para la ilustración de mapa de bits es PNG.
* La ilustración de mapa de bits se asigna a los elementos de la interfaz de usuario mediante la función `background-image` propiedad.
* La variable `width` y `height` las propiedades de un elemento de interfaz de usuario definen su tamaño lógico. El tamaño del mapa de bits pasado a `background-image` no afecta al tamaño lógico.
* Para utilizar la alta densidad de píxeles de pantallas de alta resolución como Retina, especifique la ilustración de mapa de bits el doble de grande que el tamaño del elemento de la interfaz de usuario lógica. A continuación, aplique la variable `-webkit-background-size:contain` para reducir el fondo al tamaño del elemento de la interfaz de usuario lógica.
* Para quitar un botón de la interfaz de usuario, agregue `display:none` a su clase CSS.
* Puede utilizar varios formatos para el valor de color que admita CSS. Si necesita transparencia, utilice el formato `rgba(R,G,B,A)`. De lo contrario, puede utilizar el formato `#RRGGBB`.

## Elementos comunes de la interfaz de usuario {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A continuación se muestra la documentación de referencia de elementos de la interfaz de usuario que se aplica al visor de búsqueda de catálogos electrónicos:

* [Botón Agregar favorito](r-html5-ecatsearch-customize-addfavorite.md)
* [Botón Cerrar](r-html5-ecatsearch-customize-closebutton.md)
* [Descargar](r-html5-ecatsearch-customize-download.md)
* [Uso compartido de correo electrónico](r-html5-ecatsearch-customize-emailshare.md)
* [Incrustar recurso compartido](r-html5-ecatsearch-customize-embedshare.md)
* [Uso compartido de facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Favoritos, efecto](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menú Favoritos](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Vista Favoritos](r-html5-ecatsearch-customize-favoritesview.md)
* [Botón Primera página](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Enfoque resaltado](r-html5-ecatsearch-customize-focushighlight.md)
* [Botón Pantalla completa](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Icono, efecto](r-html5-ecatsearch-customize-iconeffect.md)
* [Ventana emergente del panel Información](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Efecto Mapa de imágenes](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Botón Grande de página siguiente](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Botón Grande de la página anterior](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Botón Última página](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Compartir vínculos](r-html5-ecatsearch-customize-linkshare.md)
* [Barra de control principal](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Área del visor principal](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Botón Página siguiente](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicador de página](r-html5-ecatsearch-customize-pageindicator.md)
* [Vista de la página](r-html5-ecatsearch-customize-pageview.md)
* [Botón de página anterior](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Imprimir](r-html5-ecatsearch-customize-print.md)
* [Botón Quitar favorito](r-html5-ecatsearch-customize-removefavorite.md)
* [Botón Buscar](r-html5-ecatsearch-customize-searchbutton.md)
* [Efecto de búsqueda](r-html5-ecatsearch-customize-searcheffect.md)
* [Panel de resultados de la búsqueda](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Barra de control secundaria](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Uso compartido en medios sociales](r-html5-ecatsearch-customize-socialshare.md)
* [Tabla de contenido](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniaturas](r-html5-ecatsearch-customize-thumbnails.md)
* [Botón Miniaturas](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Información sobre herramientas](r-html5-ecatsearch-customize-tooltips.md)
* [Uso compartido de twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Botón Ver todos los favoritos](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Botón Ampliar](r-html5-ecatsearch-customize-zoominbutton.md)
* [Botón Reducir](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Botón Restablecer zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)
