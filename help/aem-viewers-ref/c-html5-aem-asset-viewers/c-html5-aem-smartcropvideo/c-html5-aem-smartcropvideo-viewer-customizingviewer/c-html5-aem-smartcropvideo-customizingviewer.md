---
title: Personalización del visor de vídeo de recorte inteligente
description: Personalización del visor de vídeo de recorte inteligente
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# Personalización del visor de vídeo de recorte inteligente{#customizing-smartcrop-video-viewer}

Todas las personalizaciones visuales y la mayoría de las personalizaciones de comportamiento se realizan creando una CSS personalizada.

El flujo de trabajo sugerido es tomar el archivo CSS predeterminado para el visor apropiado, copiarlo en una ubicación diferente, personalizarlo y especificar la ubicación del archivo personalizado en la variable `style=` comando.

Los archivos CSS predeterminados se encuentran en la siguiente ubicación:

`<s7_viewers_root>/html5/SmartCropVideoViewer.css`

El archivo CSS personalizado debe contener las mismas declaraciones de clase que la predeterminada. Si se omite una declaración de clase, el visor no funciona correctamente porque no proporciona estilos predeterminados integrados para los elementos de la interfaz de usuario.

Una alternativa para proporcionar reglas CSS personalizadas es utilizar estilos incrustados directamente en la página web o en una de las reglas CSS externas vinculadas.

Cuando cree una CSS personalizada, recuerde que el visor asigna `.s7smartcropvideoviewer` a su elemento DOM contenedor. Si utiliza un archivo CSS externo que se pasa con la variable `style=` comando, usar `.s7smartcropvideoviewer` como clase principal en el selector descendiente para sus reglas CSS. Si incrusta estilos en la página web, califique también este selector con un ID del elemento DOM de contenedor de la siguiente manera:

`#<containerId>.s7smartcropvideoviewer`

## Creación de una CSS diseñada adaptable {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

Es posible dirigirse a diferentes dispositivos en CSS para que el contenido se muestre de forma diferente en función del dispositivo del usuario. Esta segmentación incluye, entre otros, diferentes tamaños de elementos de la interfaz de usuario y resolución de ilustraciones.

El visor admite dos mecanismos para crear CSS diseñada de forma interactiva: Marcadores CSS y consultas de medios CSS estándar. Puede utilizar estos dos mecanismos de forma independiente o conjunta.

**Marcadores CSS**

Para ayudar a crear CSS diseñada y adaptable, el visor admite marcadores CSS con clases CSS especiales asignadas dinámicamente al elemento contenedor del visor de nivel superior. Esta asignación se basa en el tamaño del visor en tiempo de ejecución y en el tipo de entrada utilizado en el dispositivo actual.

El primer grupo de marcadores CSS incluye `.s7size_large`, `.s7size_medium`y `.s7size_small` clases . Se aplican en función del área de tiempo de ejecución del contenedor de visor. Es decir, si el área del visor es igual o mayor que el tamaño de un monitor de escritorio común `.s7size_large` se utiliza; si el tamaño de la zona es cercano a un comprimido común `.s7size_medium` se asigna. Para áreas similares a las pantallas de teléfonos móviles, `.s7size_small` está configurado. El objetivo principal de estos marcadores CSS es crear diferentes diseños de interfaz de usuario para diferentes pantallas y tamaños de visor.

El segundo grupo de marcadores CSS incluye `.s7mouseinput` y `.s7touchinput`. El marcador `.s7touchinput` se establece si el dispositivo actual tiene capacidades de entrada táctil; de lo contrario, `.s7mouseinput` se utiliza. Estos marcadores están diseñados para crear elementos de entrada de interfaz de usuario con diferentes tamaños de pantalla para diferentes tipos de entrada, ya que la entrada táctil suele requerir elementos más grandes. En caso de que el dispositivo tenga funciones táctiles y de entrada de ratón, `.s7touchinput` y el visor presenta una interfaz de usuario táctil.

El siguiente ejemplo de CSS establece el tamaño del botón de reproducción/pausa en 28 x 28 píxeles en sistemas con entrada de ratón y 56 x 56 píxeles en dispositivos táctiles. Además, oculta completamente el botón si el tamaño del visor se vuelve pequeño:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7smartcropvideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7smartcropvideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Para dirigirse a dispositivos con una densidad de píxeles diferente, utilice consultas de medios CSS. El siguiente bloque de consulta de medios contendría una CSS específica para pantallas de alta densidad:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

El uso de marcadores CSS es la forma más flexible de crear CSS adaptable. Esta flexibilidad le permite segmentar no solo el tamaño de la pantalla del dispositivo, sino también el tamaño real del visor, lo que puede resultar útil para diseños de página de diseño interactivos.

Utilice el archivo CSS del visor predeterminado como ejemplo de un enfoque de marcadores CSS.

**Consultas de medios CSS**

La detección de dispositivos también se puede realizar utilizando consultas de medios CSS puras. Todo lo incluido en un bloque de consulta de contenido determinado se aplica solo cuando se ejecuta en un dispositivo correspondiente.

Cuando se aplique a los visualizadores móviles, utilice cuatro consultas de medios CSS, definidas en el CSS en el orden indicado a continuación:

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

Con el enfoque de consultas de medios CSS, debe organizar CSS con detección de dispositivos de la siguiente manera:

* En primer lugar, la sección específica del escritorio define todas las propiedades que son específicas del escritorio o comunes a todas las pantallas.
* En segundo lugar, las cuatro consultas de medios deben ir en el orden definido anteriormente y proporcionar reglas CSS específicas para el tipo de dispositivo correspondiente.

No es necesario duplicar todo el CSS del visor en cada consulta de medios. Solo las propiedades específicas de determinados dispositivos se redefinen dentro de una consulta de medios.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muchos elementos de la interfaz de usuario del visor están diseñados con ilustraciones de mapa de bits y tienen más de un estado visual distinto. Un buen ejemplo es un botón que normalmente tiene al menos tres estados diferentes: &quot;up&quot;, &quot;over&quot; y &quot;down&quot;. Cada estado requiere su propia ilustración de mapa de bits asignada.

Con un enfoque clásico del estilo, el CSS tendría una referencia independiente al archivo de imagen individual en el servidor para cada estado del elemento de la interfaz de usuario. A continuación se muestra un ejemplo de CSS para diseñar un botón de pantalla completa:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

El inconveniente de este enfoque es que el usuario final experimenta parpadeos o retraso en la respuesta de la interfaz de usuario cuando se interactúa con el elemento por primera vez. Esta acción se produce porque la ilustración de la imagen para el nuevo estado del elemento aún no se ha descargado. Además, este enfoque puede tener un ligero impacto negativo en el rendimiento debido a un aumento en el número de llamadas HTTP al servidor.

Los sprites CSS son un enfoque diferente en el que las ilustraciones de imágenes para todos los estados de elementos se combinan en un solo archivo PNG denominado &quot;sprite&quot;. Este &quot;Sprite&quot; tiene todos los estados visuales para el elemento dado posicionado uno tras otro. Al diseñar un elemento de interfaz de usuario con sprites, se hace referencia a la misma imagen sprite para todos los estados diferentes en el CSS. Además, el `background-position` se utiliza para cada estado para especificar qué parte de la imagen &quot;sprite&quot; se utiliza. Puede estructurar una imagen &quot;sprite&quot; de cualquier manera adecuada. Normalmente, los visualizadores lo tienen apilado verticalmente. A continuación se muestra un ejemplo basado en &quot;sprite&quot; de cómo aplicar estilo al mismo botón de pantalla completa desde arriba:

```
.s7smartcropvideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Notas de estilo y consejos generales {#section-097418bd618740bba36352629e4d88e1}

* Todas las rutas a los recursos externos dentro de CSS se resuelven en la ubicación de CSS, no en la ubicación de la página del HTML del visor. Recuerde esta regla cuando copie el CSS predeterminado en una ubicación diferente. Copie los recursos predeterminados o actualice las rutas dentro del CSS personalizado.
* El formato preferido para la ilustración de mapa de bits es PNG.
* La ilustración de mapa de bits se asigna a los elementos de la interfaz de usuario mediante la función `background-image` propiedad.
* La variable `width` y `height` las propiedades de un elemento de interfaz de usuario definen su tamaño lógico. El tamaño del mapa de bits pasado a `background-image` no afecta al tamaño lógico.

* Para utilizar la alta densidad de píxeles de pantallas de alta resolución como Retina, especifique la ilustración de mapa de bits el doble de grande que el tamaño del elemento de la interfaz de usuario lógica. A continuación, aplique la variable `-webkit-background-size:contain` para reducir el fondo al tamaño del elemento de la interfaz de usuario lógica.
* Para quitar un botón de la interfaz de usuario, agregue `display:none` a su clase CSS.
* Puede utilizar varios formatos para el valor de color que admita CSS. Si necesita transparencia, utilice el formato `rgba(R,G,B,A)`. De lo contrario, puede utilizar el formato `#RRGGBB`.

* Al personalizar la interfaz de usuario del visor con CSS, el uso de la variable `!IMPORTANT` regla no es compatible con los elementos del visualizador de estilo. En particular, `!IMPORTANT` no debe utilizarse para anular ningún estilo predeterminado o en tiempo de ejecución proporcionado por el visor o el SDK del visor. La razón es que puede afectar al comportamiento de los componentes adecuados. En su lugar, debe utilizar selectores CSS con la especificidad adecuada para establecer las propiedades CSS que se documentan en esta guía de referencia.

## Elementos comunes de la interfaz de usuario {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A continuación se muestra la documentación de referencia de elementos de la interfaz de usuario que se aplica al visor de vídeo de recorte inteligente:
