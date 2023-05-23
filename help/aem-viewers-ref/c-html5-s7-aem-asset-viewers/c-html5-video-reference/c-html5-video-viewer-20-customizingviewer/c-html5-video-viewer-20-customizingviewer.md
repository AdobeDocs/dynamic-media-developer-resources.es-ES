---
title: Personalizar el visor de vídeo
description: Personalizar el visor de vídeo
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 90dc93ee-fdd0-41c9-9eef-4c9952198356
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# Personalizar el visor de vídeo{#customizing-video-viewer}

Toda la personalización visual y la mayor parte de la personalización del comportamiento se realiza creando un CSS personalizado.

El flujo de trabajo sugerido es tomar el archivo CSS predeterminado para el visor apropiado, copiarlo en una ubicación diferente, personalizarlo y especificar la ubicación del archivo personalizado en la `style=` comando.

Los archivos CSS predeterminados se encuentran en la siguiente ubicación:

`<s7_viewers_root>/html5/VideoViewer.css`

El archivo CSS personalizado debe contener las mismas declaraciones de clase que la predeterminada. Si se omite una declaración de clase, el visor no funciona correctamente porque no proporciona estilos predeterminados integrados para los elementos de la interfaz de usuario.

Una forma alternativa de proporcionar reglas CSS personalizadas es utilizar estilos incrustados directamente en la página web o en una de las reglas CSS externas vinculadas.

Cuando cree CSS personalizado, recuerde que el visor asigna `.s7videoviewer` a su elemento DOM contenedor. Si utiliza un archivo CSS externo que se pasa con la variable `style=` comando, use `.s7videoviewer` como clase principal en el selector descendente de las reglas CSS. Si incrusta estilos en la página web, también clasifique este selector con un ID del elemento DOM contenedor de la siguiente manera:

`#<containerId>.s7videoviewer`

## Creación de CSS diseñado interactivo {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

Es posible segmentar diferentes dispositivos en CSS para que el contenido se muestre de forma diferente en función del dispositivo del usuario. Esta segmentación incluye, entre otros, diferentes tamaños de elementos de interfaz de usuario y resolución de ilustraciones.

El visor admite dos mecanismos para crear CSS diseñadas de forma interactiva: marcadores CSS y consultas de medios CSS estándar. Puede utilizar estos dos mecanismos de forma independiente o conjunta.

**Marcadores CSS**

Para ayudarle a crear CSS diseñado interactivo, el visor admite marcadores CSS que asignan clases CSS especiales de forma dinámica al elemento contenedor del visor de nivel superior. La asignación se basa en el tamaño del visor en tiempo de ejecución y en el tipo de entrada utilizado en el dispositivo actual.

El primer grupo de marcadores CSS incluye `.s7size_large`, `.s7size_medium`, y `.s7size_small` clases. Se aplican en función del área de tiempo de ejecución del contenedor de visor. Es decir, si el área de visualización es igual o mayor que el tamaño de un monitor de escritorio común `.s7size_large` se utiliza; si el área es de tamaño cercano a un dispositivo de tableta común `.s7size_medium` se ha asignado. Para áreas similares a las pantallas de teléfono móvil, `.s7size_small` está configurado. El propósito principal de estos marcadores CSS es crear diferentes diseños de interfaz de usuario para diferentes pantallas y tamaños de visor.

El segundo grupo de marcadores CSS incluye `.s7mouseinput` y `.s7touchinput`. El marcador `.s7touchinput` se establece si el dispositivo actual tiene capacidades de entrada táctil; de lo contrario, `.s7mouseinput` se utiliza. Estos marcadores están pensados para crear elementos de entrada de interfaz de usuario con diferentes tamaños de pantalla para diferentes tipos de entrada, ya que normalmente la entrada táctil requiere elementos más grandes. En caso de que el dispositivo tenga capacidades táctiles y de entrada de ratón, `.s7touchinput` se configura y el visualizador procesa una interfaz de usuario táctil.

El siguiente CSS de ejemplo establece el tamaño del botón de reproducción/pausa en 28 x 28 píxeles en sistemas con entrada de ratón y en 56 x 56 píxeles en dispositivos táctiles. Además, oculta el botón por completo si el tamaño del visor se vuelve demasiado pequeño:

```
.s7videoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7videoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7videoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Para dirigirse a dispositivos con una densidad de píxeles diferente, utilice consultas de medios CSS. El siguiente bloque de consulta de medios contendría CSS específico para pantallas de alta densidad:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

El uso de marcadores CSS es la forma más flexible de crear CSS con diseño interactivo. El motivo es que le permite dirigirse no solo al tamaño de pantalla del dispositivo, sino también al tamaño real del visor, lo que puede resultar útil para diseños de página de diseño interactivos.

Utilice el archivo CSS de visor predeterminado como ejemplo de enfoque de marcadores CSS.

**Consultas de medios CSS**

La detección de dispositivos también se puede realizar utilizando consultas de medios CSS puras. Todo lo incluido dentro de un bloque de consulta de medios determinado se aplica solo cuando se ejecuta en un dispositivo correspondiente.

Cuando se aplique a visores móviles, utilice cuatro consultas de medios CSS, definidas en su CSS en el orden indicado a continuación:

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

1. Contiene únicamente reglas específicas para teléfonos móviles con pantallas de alta resolución.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Con el método de consultas de medios CSS, debe organizar CSS con detección de dispositivos de la siguiente manera:

* En primer lugar, la sección específica del escritorio define todas las propiedades que son específicas del escritorio o comunes a todas las pantallas.
* En segundo lugar, las cuatro consultas de medios deben ir en el orden definido anteriormente y proporcionar reglas CSS específicas para el tipo de dispositivo correspondiente.

No es necesario duplicar todo el visor de CSS en cada consulta de medios. Solo las propiedades específicas de dispositivos determinados se redefinen dentro de una consulta de medios.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muchos elementos de la interfaz de usuario del visor tienen un estilo que utiliza ilustraciones de mapa de bits y tienen más de un estado visual distinto. Un buen ejemplo es un botón que normalmente tiene al menos tres estados diferentes: &quot;arriba&quot;, &quot;sobre&quot; y &quot;abajo&quot;. Cada estado requiere su propia ilustración de mapa de bits asignada.

Con un enfoque clásico del estilo, el CSS tendría una referencia independiente a un archivo de imagen individual en el servidor para cada estado del elemento de interfaz de usuario. El siguiente es un ejemplo de CSS para aplicar estilo a un botón de pantalla completa:

```
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

El inconveniente de este enfoque es que el usuario final experimenta parpadeos o una respuesta retrasada en la interfaz de usuario cuando el elemento interactúa con por primera vez. Esta acción se produce porque la ilustración de la imagen para el nuevo estado del elemento aún no se ha descargado. Además, este método puede tener un ligero impacto negativo en el rendimiento debido al aumento en el número de llamadas HTTP al servidor.

Los sprites CSS son un enfoque diferente en el que la ilustración de la imagen para todos los estados de elementos se combina en un solo archivo PNG llamado &quot;sprite&quot;. Este &quot;sprite&quot; tiene todos los estados visuales para el elemento dado colocados uno tras otro. Al aplicar estilo a un elemento de interfaz de usuario con sprites, se hace referencia a la misma imagen sprite para todos los estados diferentes en CSS. Además, la variable `background-position` se utiliza la propiedad para cada estado para especificar qué parte de la imagen &quot;sprite&quot; se utiliza. Puede estructurar una imagen &quot;sprite&quot; de cualquier manera adecuada. Los visualizadores normalmente lo tienen apilado verticalmente. A continuación se muestra un ejemplo basado en &quot;sprite&quot; de cómo aplicar estilo al mismo botón de pantalla completa desde arriba:

```
.s7videoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Notas y consejos generales sobre estilo {#section-097418bd618740bba36352629e4d88e1}

* Todas las rutas a recursos externos dentro de CSS se resuelven en la ubicación de CSS y no en la ubicación de la página del HTML del visor. Recuerde tener en cuenta esta regla cuando copie el CSS predeterminado en una ubicación diferente. Copie los recursos predeterminados o actualice las rutas dentro del CSS personalizado.
* El formato preferido para las ilustraciones de mapa de bits es PNG.
* La ilustración de mapa de bits se asigna a los elementos de interfaz de usuario utilizando `background-image` propiedad.
* El `width` y `height` Las propiedades de un elemento de interfaz de usuario definen su tamaño lógico. El tamaño del mapa de bits pasado a `background-image` no afecta al tamaño lógico.

* Para utilizar la alta densidad de píxeles de pantallas de alta resolución como Retina, especifique ilustraciones de mapa de bits dos veces más grandes que el tamaño del elemento de interfaz de usuario lógico. A continuación, aplique la variable `-webkit-background-size:contain` para reducir el fondo al tamaño del elemento de la interfaz de usuario lógica.
* Para quitar un botón de la interfaz de usuario, agregue. `display:none` a su clase CSS.
* Puede utilizar varios formatos para los valores de color que admite CSS. Si necesita transparencia, utilice el formato `rgba(R,G,B,A)`. De lo contrario, puede utilizar el formato `#RRGGBB`.

* Al personalizar la interfaz de usuario del visor con CSS, el uso de `!IMPORTANT` La regla de no es compatible con los elementos del visor de estilo. En particular, `!IMPORTANT` La regla no debe utilizarse para anular ningún estilo predeterminado o en tiempo de ejecución proporcionado por el visor o el SDK del visor. El motivo es que puede afectar al comportamiento de los componentes adecuados. En su lugar, debe utilizar selectores de CSS con la especificidad adecuada para establecer las propiedades CSS documentadas en esta guía de referencia.

## Elementos comunes de la interfaz de usuario {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A continuación se muestra la documentación de referencia de los elementos de la interfaz de usuario que se aplica al Visor de vídeo:
