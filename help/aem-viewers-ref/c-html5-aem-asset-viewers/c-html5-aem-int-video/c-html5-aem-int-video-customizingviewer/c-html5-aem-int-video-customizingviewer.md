---
description: Toda la personalización visual y la mayor parte de la personalización del comportamiento para el visualizador de vídeo interactivo se realiza creando un CSS personalizado.
keywords: adaptable
solution: Experience Manager
title: Personalización del visualizador de vídeo interactivo
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: c428c3e6-81be-4708-b064-f9d794183209
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# Personalización del visualizador de vídeo interactivo{#customizing-interactive-video-viewer}

Toda la personalización visual y la mayor parte de la personalización del comportamiento para el visualizador de vídeo interactivo se realiza creando un CSS personalizado.

El flujo de trabajo sugerido es tomar el archivo CSS predeterminado para el visor apropiado, copiarlo en una ubicación diferente, personalizarlo y especificar la ubicación del archivo personalizado en el comando `style=`.

Los archivos CSS predeterminados se encuentran en la siguiente ubicación:

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

El visor se suministra con dos archivos CSS predeterminados, para esquemas de color &quot;claro&quot; y &quot;oscuro&quot;. La versión &quot;oscura&quot; se utiliza de forma predeterminada, pero es fácil cambiar a la versión &quot;ligera&quot; mediante el siguiente CSS estándar:

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

El archivo CSS personalizado debe contener las mismas declaraciones de clase que la predeterminada. Si se omite una declaración de clase, el visor no funciona correctamente porque no proporciona estilos predeterminados integrados para los elementos de la interfaz de usuario.

Una alternativa para proporcionar reglas CSS personalizadas es utilizar estilos incrustados directamente en la página web o en una de las reglas CSS externas vinculadas.

Al crear CSS personalizada, tenga en cuenta que el visor asigna la clase `.s7interactivevideoviewer` a su elemento DOM contenedor. Si está utilizando un archivo CSS externo pasado con el comando `style=`, utilice la clase `.s7interactivevideoviewer` como clase principal en el selector de descendientes para sus reglas CSS. Si está realizando estilos incrustados en la página web, califique también este selector con un ID del elemento DOM de contenedor de la siguiente manera:

`#<containerId>.s7interactivevideoviewer`

## Creación de CSS diseñada adaptable {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es posible dirigirse a diferentes dispositivos e incrustar tamaños en CSS para que el contenido se muestre de forma diferente en función del dispositivo de un usuario o de un diseño de página web concreto. Esto incluye, entre otros, diferentes diseños, tamaños de elementos de la interfaz de usuario y resolución de ilustraciones.

El visor admite dos mecanismos para crear CSS diseñada de forma interactiva: Marcadores CSS y consultas de medios CSS estándar. Puede utilizarlos de forma independiente o conjunta.

**Marcadores CSS**

Para ayudar a crear CSS diseñada y adaptable, el visor admite marcadores CSS. Son clases CSS especiales que se asignan dinámicamente al elemento contenedor del visor de nivel superior en función del tamaño del visor de tiempo de ejecución y el tipo de entrada utilizado en el dispositivo actual.

El primer grupo de marcadores CSS incluye las clases `.s7size_large`, `.s7size_medium` y `.s7size_small`. Se aplican en función del área de tiempo de ejecución del contenedor de visor. Si el área del visor es igual o mayor que el tamaño de un monitor de escritorio común, se utiliza `.s7size_large`; si el área está cerca de un dispositivo comprimido común, se asigna `.s7size_medium`. Para áreas similares a las pantallas de teléfono móvil, se establece `.s7size_small`. El objetivo principal de estos marcadores CSS es crear diferentes diseños de interfaz de usuario para diferentes pantallas y tamaños de visor.

El segundo grupo de marcadores CSS contiene `.s7mouseinput` y `.s7touchinput`. `.s7touchinput` se establece si el dispositivo actual tiene capacidades de entrada táctil; de lo contrario,  `.s7mouseinput` se utiliza . Estos marcadores están pensados principalmente para crear elementos de entrada de interfaz de usuario con diferentes tamaños de pantalla para diferentes tipos de entrada, ya que normalmente la entrada táctil requiere elementos más grandes.

El tercer grupo de marcadores CSS contiene `.s7device_landscape` y `.s7device_portrait`. `.s7device_landscape` se establece si el dispositivo táctil está en orientación horizontal;  `.s7device_portrait` se utiliza cuando el dispositivo táctil gira hacia la orientación vertical. Estos marcadores CSS están pensados para utilizarse únicamente en sistemas de escritorio.

El siguiente ejemplo de CSS establece el tamaño del botón de reproducción/pausa en 28x28 píxeles en sistemas con entrada de ratón y 56x56 píxeles en dispositivos táctiles. Además, oculta completamente el botón si el tamaño del visor se reduce significativamente:

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7interactivevideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7interactivevideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

En este ejemplo siguiente, la barra de control de vídeo está 138 píxeles por encima de la parte inferior del visor si el dispositivo táctil está en orientación vertical y la mueve a la parte inferior del visor en todos los demás casos:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

Para dirigirse a dispositivos con una densidad de píxeles diferente, debe utilizar consultas de medios CSS. El siguiente bloque de consulta de medios contendría CSS específica para pantallas de alta densidad:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

El uso de marcadores CSS es la forma más flexible de crear CSS diseñada con capacidad de respuesta, ya que le permite dirigirse no solo al tamaño de la pantalla del dispositivo, sino también al tamaño real del visor, lo que resulta útil para los diseños de diseño interactivos.

Puede utilizar el archivo CSS predeterminado del visor como ejemplo de un enfoque de marcadores CSS.

**Consultas de medios CSS**

También puede realizar la detección de dispositivos utilizando consultas de medios CSS puras. Todo lo incluido en un bloque de consulta de contenido determinado se aplica solo cuando se ejecuta en un dispositivo correspondiente.

Cuando se aplican a los visualizadores móviles, utilizan cuatro consultas de medios CSS, definidas en su CSS, en el orden indicado a continuación:

1. Contiene solo reglas específicas para todos los dispositivos táctiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
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

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muchos elementos de la interfaz de usuario del visor están diseñados con ilustraciones de mapa de bits y tienen más de un estado visual distinto. Un buen ejemplo es un botón que normalmente tiene al menos 3 estados diferentes: &quot;up&quot;, &quot;over&quot; y &quot;down&quot;. Cada estado requiere su propia ilustración de mapa de bits asignada.

Con un enfoque clásico del estilo, el CSS tendría una referencia independiente al archivo de imagen individual en el servidor para cada estado del elemento de la interfaz de usuario. A continuación se muestra un ejemplo de CSS para diseñar un botón de pantalla completa:

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

El inconveniente de este enfoque es que el usuario final experimenta parpadeos o retraso en la respuesta de la interfaz de usuario cuando se interactúa con el elemento por primera vez. Esta acción se produce porque la ilustración de la imagen para el nuevo estado del elemento aún no se ha descargado. Además, este enfoque puede tener un ligero impacto negativo en el rendimiento debido a un aumento en el número de llamadas HTTP al servidor.

Los sprites CSS son un enfoque diferente en el que las ilustraciones de imágenes para todos los estados de elementos se combinan en un solo archivo PNG denominado &quot;sprite&quot;. Este &quot;Sprite&quot; tiene todos los estados visuales para el elemento dado posicionado uno tras otro. Al diseñar un elemento de interfaz de usuario con sprites, se hace referencia a la misma imagen sprite para todos los estados diferentes del CSS. Además, la propiedad `background-position` se utiliza para cada estado para especificar qué parte de la imagen &quot;sprite&quot; se utiliza. Puede estructurar una imagen &quot;sprite&quot; de cualquier manera adecuada. Normalmente, los visualizadores lo tienen apilado verticalmente. A continuación se muestra un ejemplo basado en &quot;sprite&quot; de cómo aplicar estilo al mismo botón de pantalla completa anteriormente:

```
.s7interactivevideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Notas de estilo y consejos generales {#section-95855dccbbc444e79970f1aaa3260b7b}

* Al personalizar la interfaz de usuario del visor con CSS, el uso de la regla `!IMPORTANT` no se admite para los elementos del visor de estilos. En concreto, la regla `!IMPORTANT` no debe utilizarse para anular ningún estilo predeterminado o en tiempo de ejecución proporcionado por el visor o el SDK del visor. La razón es que puede afectar al comportamiento de los componentes adecuados. En su lugar, debe utilizar selectores CSS con la especificidad adecuada para establecer las propiedades CSS que se documentan en esta guía de referencia.

* Todas las rutas a los recursos externos dentro de CSS se resuelven en la ubicación de CSS, no en la ubicación de la página HTML del visor. Tenga en cuenta esta regla cuando copie el CSS predeterminado en una ubicación diferente. Copie también los recursos predeterminados o actualice las rutas dentro del CSS personalizado.
* El formato preferido para la ilustración de mapa de bits es PNG.
* Las ilustraciones de mapa de bits se asignan a elementos de la interfaz de usuario mediante la propiedad `background-image` .
* Las propiedades `width` y `height` de un elemento de interfaz de usuario definen su tamaño lógico. El tamaño del mapa de bits pasado a `background-image` no afecta al tamaño lógico.

* Para utilizar la alta densidad de píxeles de pantallas de alta resolución como Retina, especifique la ilustración de mapa de bits el doble de grande que el tamaño del elemento de la interfaz de usuario lógica. A continuación, aplique la propiedad `-webkit-background-size:contain` para reducir el fondo al tamaño del elemento de la interfaz de usuario lógica.
* Para quitar un botón de la interfaz de usuario, agregue `display:none` a su clase CSS.
* Puede utilizar varios formatos para el valor de color que admita CSS. Si necesita transparencia, utilice el formato `rgba(R,G,B,A)`. De lo contrario, puede utilizar el formato `#RRGGBB`.

## Elementos comunes de la interfaz de usuario {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A continuación se muestra la documentación de referencia de elementos de la interfaz de usuario que se aplica al visualizador de vídeo interactivo:
