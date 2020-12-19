---
description: Toda la personalización visual y la mayor parte del comportamiento del visor de carrusel se realiza creando una CSS personalizada.
keywords: responsive
seo-description: Toda la personalización visual y la mayor parte del comportamiento del visor de carrusel se realiza creando una CSS personalizada.
seo-title: Personalización del visor de carrusel
solution: Experience Manager
title: Personalización del visor de carrusel
topic: Dynamic media
uuid: a35dac3c-8785-42bf-8284-e400128f213c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---


# Personalización del visor de carrusel{#customizing-carousel-viewer}

Toda la personalización visual y la mayor parte del comportamiento del visor de carrusel se realiza creando una CSS personalizada.

El flujo de trabajo sugerido es tomar el archivo CSS predeterminado para el visor adecuado, copiarlo en una ubicación diferente, personalizarlo y especificar la ubicación del archivo personalizado en el comando `style=`.

Los archivos CSS predeterminados se encuentran en la siguiente ubicación:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

El visor dispone de cuatro archivos CSS listos para usar, para indicadores numéricos y de conjunto de puntos, cada uno con una combinación de colores &quot;claro&quot; y &quot;oscuro&quot;. La versión &quot;Luz de puntos&quot; se utiliza de forma predeterminada, pero es fácil cambiar a una versión diferente utilizando CSS estándar diferente y configurando el parámetro `SetIndicator.mode`. Otras CSS estándar se encuentran en la siguiente ubicación:

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

El archivo CSS personalizado debe contener las mismas declaraciones de clase que la predeterminada. Si se omite una declaración de clase, el visor no funciona correctamente porque no proporciona estilos predeterminados integrados para los elementos de la interfaz de usuario.

Una forma alternativa de proporcionar reglas CSS personalizadas es utilizar estilos incrustados directamente en la página web o en una de las reglas CSS externas vinculadas.

Al crear CSS personalizada, tenga en cuenta que el visor asigna la clase `.s7carouselviewer` a su elemento DOM de contenedor. Si utiliza un archivo CSS externo que se pasa con el comando `style=`, utilice la clase `.s7carouselviewer` como clase principal en el selector de descendientes para las reglas CSS. Si va a agregar estilos incrustados en la página web, califique además este selector con un ID del elemento DOM de contenedor de la siguiente manera:

`#<containerId>.s7carouselviewer`

## Creación de CSS adaptable {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es posible destinatario de diferentes dispositivos y tamaños de incrustación en CSS para que el contenido se muestre de forma diferente, según el dispositivo del usuario o el diseño de una página web en particular. Esto incluye, entre otras cosas, diferentes diseños, tamaños de elementos de la interfaz de usuario y resolución de ilustraciones.

El visor admite dos mecanismos para crear CSS adaptable: Marcadores CSS y consultas de medios CSS estándar. Puede utilizarlos de forma independiente o conjunta.

**Marcadores CSS**

Para facilitar la creación de CSS adaptable, el visor admite marcadores CSS. Son clases CSS especiales que se asignan dinámicamente al elemento de contenedor del visor de nivel superior. Se basan en el tamaño del visor de tiempo de ejecución y en el tipo de entrada utilizado en el dispositivo actual.

El primer grupo de marcadores CSS contiene clases `.s7size_large`, `.s7size_medium` y `.s7size_small`. Se aplican en función del área de tiempo de ejecución del contenedor del visor. Por ejemplo, si el área del visor es igual o mayor que el tamaño de un monitor de escritorio común, utilice `.s7size_large`. Si el área está cerca de una tableta común, asigne `.s7size_medium`. Para áreas similares a las pantallas de teléfonos móviles, utilice `.s7size_small`. El objetivo principal de estos marcadores CSS es crear diferentes diseños de interfaz de usuario para diferentes pantallas y tamaños de visor.

El segundo grupo de marcadores CSS contiene `.s7mouseinput` y `.s7touchinput`. El marcador CSS `.s7touchinput` se establece si el dispositivo actual es capaz de introducir datos táctiles. De lo contrario, se utiliza `.s7mouseinput`. Estos marcadores están pensados principalmente para crear elementos de entrada de interfaz de usuario con diferentes tamaños de pantalla para diferentes tipos de entrada, ya que normalmente la entrada táctil requiere elementos más grandes.

El siguiente ejemplo de CSS establece el tamaño del botón de zoom en 28 x 28 píxeles en sistemas con entrada de ratón y en 56 x 56 píxeles en dispositivos de entrada táctiles. Si el tamaño del visor es aún menor, se establece en 20 x 20 píxeles.

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

Para destinatario de dispositivos con una densidad de píxeles diferente, debe utilizar consultas de medios CSS. El siguiente bloque de consulta de medios contendría CSS específica para pantallas de alta densidad:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

El uso de marcadores CSS es la forma más flexible de crear CSS adaptable, ya que le permite realizar el destinatario no solo del tamaño de la pantalla del dispositivo, sino también del tamaño real del visor, lo que resulta útil para diseños interactivos.

Puede utilizar el archivo CSS de visor predeterminado como ejemplo de un enfoque de marcadores CSS.

**CONSULTAS de medios CSS**

También puede realizar la detección de dispositivos utilizando consultas de medios CSS puras. Todo lo incluido dentro de un determinado bloque de consulta de medios se aplica solo cuando se ejecuta en un dispositivo correspondiente.

Cuando se aplica a los visores móviles, utilice cuatro consultas de medios CSS, definidas en su CSS, en el orden que se indica a continuación:

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
* Y en segundo lugar, las cuatro consultas de medios van en el orden definido anteriormente y proporcionan reglas CSS específicas para el tipo de dispositivo correspondiente.

No es necesario realizar duplicados de toda la CSS del visor en cada consulta de medios. Solo las propiedades específicas de determinados dispositivos se redefinen dentro de una consulta de medios.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muchos de los elementos de la interfaz de usuario del visor están diseñados con ilustraciones de mapa de bits y tienen más de un estado visual distinto. Un buen ejemplo es un botón que normalmente tiene al menos tres estados diferentes: `up`, `over` y `down`. Cada estado requiere la asignación de su propia ilustración de mapa de bits.

Con un enfoque clásico del estilo, el CSS tendría una referencia independiente al archivo de imagen individual en el servidor para cada estado del elemento de interfaz de usuario. A continuación se muestra un ejemplo de CSS para aplicar estilo a un botón de zoom:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

El inconveniente de este enfoque es que el usuario final experimenta parpadeos o retraso en la respuesta de la interfaz de usuario cuando se interactúa con el elemento por primera vez. Esta acción se produce porque la ilustración de imagen para el nuevo estado del elemento aún no se ha descargado. Además, este enfoque puede tener un ligero impacto negativo en el rendimiento debido a un aumento en el número de llamadas HTTP al servidor.

Los sprites CSS son un enfoque diferente en el que las ilustraciones de imagen para todos los estados de elementos se combinan en un único archivo PNG denominado &quot;sprite&quot;. Este &quot;elemento sprite&quot; tiene todos los estados visuales para un elemento determinado colocado uno tras otro. Al aplicar estilo a un elemento de interfaz de usuario con sprites, se hace referencia a la misma imagen sprite para todos los estados diferentes de la CSS. Además, la propiedad `background-position` se utiliza para cada estado para especificar qué parte de la imagen &quot;sprite&quot; se utiliza. Puede estructurar una imagen &quot;sprite&quot; de cualquier manera adecuada. Los visores normalmente lo tienen apilado verticalmente.

A continuación se muestra un ejemplo basado en &quot;sprite&quot; de aplicar estilo al mismo icono de zona interactiva:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Notas y consejos generales sobre estilos {#section-95855dccbbc444e79970f1aaa3260b7b}

* Al personalizar la interfaz de usuario del visor con CSS, el uso de la regla `!IMPORTANT` no se admite para aplicar estilo a los elementos del visor. En concreto, la regla `!IMPORTANT` no debe utilizarse para anular ningún estilo predeterminado o de tiempo de ejecución proporcionado por el visor o el SDK del visor. La razón de esto es que puede afectar al comportamiento de los componentes adecuados. En su lugar, debe utilizar selectores CSS con la especificidad adecuada para establecer las propiedades CSS documentadas en esta guía de referencia de visores.
* Todas las rutas a los recursos externos dentro de CSS se resuelven en la ubicación de CSS, no en la ubicación de la página HTML del visor. Tenga en cuenta esta regla cuando copie la CSS predeterminada en una ubicación diferente. Copie también los recursos predeterminados o actualice todas las rutas dentro de la CSS personalizada.
* El formato preferido para la ilustración de mapa de bits es PNG.
* La ilustración de mapa de bits se asigna a elementos de la interfaz de usuario mediante la propiedad `background-image`.
* Las propiedades `width` y `height` de un elemento de interfaz de usuario definen su tamaño lógico. El tamaño del mapa de bits pasado a `background-image` no afecta a su tamaño lógico.
* Para utilizar la alta densidad de píxeles de pantallas de alta resolución como Retina, especifique una ilustración de mapa de bits dos veces más grande que el tamaño del elemento de la interfaz de usuario lógica. A continuación, aplique la propiedad `-webkit-background-size:contain` para reducir el fondo al tamaño del elemento de la interfaz lógica del usuario.
* Para quitar un botón de la interfaz de usuario, agregue `display:none` a su clase CSS.
* Puede utilizar varios formatos para el valor de color que admite CSS. Si necesita transparencia, utilice el formato `rgba(R,G,B,A)`. De lo contrario, puede utilizar el formato `#RRGGBB`.

## Elementos comunes de la interfaz de usuario {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A continuación se muestra la documentación de referencia de elementos de la interfaz de usuario que se aplica al visor de imágenes de vídeo:
