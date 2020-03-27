---
description: nulo
keywords: responsive
seo-description: nulo
seo-title: Personalización del visor de zoom en línea
solution: Experience Manager
title: Personalización del visor de zoom en línea
topic: Dynamic media
uuid: c9203ea7-47dc-40f6-add8-04e4258da7c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Personalización del visor de zoom en línea{#customizing-inline-zoom-viewer}

Toda la personalización visual y la mayor parte de la personalización del comportamiento se realiza mediante la creación de una CSS personalizada.

El flujo de trabajo sugerido consiste en tomar el archivo CSS predeterminado para el visor adecuado, copiarlo en una ubicación diferente, personalizarlo y especificar la ubicación del archivo personalizado en el `style=` comando.

Los archivos CSS predeterminados se encuentran en la siguiente ubicación:

`<s7_viewers_root>/html5/InlineZoomViewer.css`

El archivo CSS personalizado debe contener las mismas declaraciones de clase que la predeterminada. Si se omite una declaración de clase, el visor no funciona correctamente porque no proporciona estilos predeterminados integrados para los elementos de la interfaz de usuario.

También es importante conservar la siguiente declaración CSS del visor CSS predeterminado, ya que es necesaria para la funcionalidad de zoom en línea:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 width: 100%; 
 height: 100%; 
 left: 0; 
 top: 0; 
 border: none; 
 z-index:999; 
}
```

Una forma alternativa de proporcionar reglas CSS personalizadas es utilizar estilos incrustados directamente en la página web o en una de las reglas CSS externas vinculadas.

Cuando cree CSS personalizada, tenga en cuenta que el visor asigna `.s7flyoutviewer` clase a su elemento DOM de contenedor. Si utiliza un archivo CSS externo que se pasa con `style=` un comando, utilice `.s7flyoutviewer` la clase como clase principal en el selector de descendientes para las reglas CSS. Si está realizando estilos incrustados en la página web, califique además este selector con un ID del elemento DOM de contenedor de la siguiente manera:

`#<containerId>.s7flyoutviewer`

## Creación de CSS adaptable {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Es posible destinatario de diferentes dispositivos y tamaños de incrustación en CSS para que el contenido se muestre de forma diferente, según el dispositivo del usuario o el diseño de una página web en particular. Esto incluye, entre otros, diferentes diseños de página web, tamaños de elementos de interfaz de usuario y resolución de ilustraciones.

El visor admite dos métodos para crear CSS adaptable: Marcadores CSS y consultas de medios CSS estándar. Puede utilizar estos métodos de forma independiente o conjunta.

**Marcadores CSS**

Para facilitar la creación de CSS adaptable, el visor admite marcadores CSS con clases CSS especiales asignadas dinámicamente al elemento de contenedor del visor de nivel superior en función del tamaño del visor en tiempo de ejecución y del tipo de entrada utilizado en el dispositivo actual.

El primer grupo de marcadores de CSS incluye `.s7size_large`, `.s7size_medium`y `.s7size_small` clases. Se aplican en función del área de tiempo de ejecución del contenedor del visor. Es decir, si el área del visor es igual o mayor que el tamaño de un monitor de escritorio común `.s7size_large` ; si el área está próxima en tamaño a una tableta común `.s7size_medium` está asignada. Para áreas similares a las pantallas de teléfonos móviles `.s7size_small` está establecido. El objetivo principal de estos marcadores CSS es crear diferentes diseños de interfaz de usuario para diferentes pantallas y tamaños de visor.

El segundo grupo de marcadores de CSS incluye `.s7mouseinput` y `.s7touchinput`. `.s7touchinput` se establece si el dispositivo actual tiene capacidades de entrada táctil; de lo contrario, `.s7mouseinput` se utiliza. Estos marcadores están diseñados para crear elementos de entrada de interfaz de usuario con diferentes tamaños de pantalla para diferentes tipos de entrada, ya que normalmente la entrada táctil requiere elementos más grandes. En los casos en los que el dispositivo tiene funciones táctiles y de entrada de ratón, `.s7touchinput` se establece y el visor procesa una interfaz de usuario táctil.

El siguiente ejemplo de CSS establece el tamaño del botón de zoom en 28 x 28 píxeles en sistemas con entrada de ratón y 56 x 56 píxeles en dispositivos táctiles. Además, oculta completamente el botón si el tamaño del visor es realmente pequeño:

```
.s7flyoutviewer.s7mouseinput .s7swatches .s7thumb {  
 width: 28px; 
 height: 28px; 
} 
.s7flyoutviewer.s7touchinput .s7swatches .s7thumb {  
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer.s7size_small .s7swatches {  
 visibility: hidden; 
}
```

Para destinatario de dispositivos con una densidad de píxeles diferente, utilice consultas de medios CSS. El siguiente bloque de consulta de medios contendría CSS específica para pantallas de alta densidad:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

El uso de marcadores CSS es la forma más flexible de crear CSS adaptable diseñada que le permite realizar destinatarios no solo del tamaño de la pantalla del dispositivo sino también del tamaño real del visor, lo que puede resultar útil para los diseños interactivos de las páginas web.

**consultas de medios CSS**

La detección de dispositivos también se puede realizar mediante consultas de medios CSS puras. Todo lo incluido dentro de un determinado bloque de consulta de medios se aplica solo cuando se ejecuta en un dispositivo correspondiente.

Cuando se aplique a visores móviles, utilice cuatro consultas de medios CSS, definidas en el CSS en el orden siguiente:

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
* Y en segundo lugar, las cuatro consultas de medios van en el orden definido anteriormente y proporcionan reglas CSS específicas para el tipo de dispositivo correspondiente.

No es necesario realizar duplicados de toda la CSS del visor en cada consulta de medios. Solo las propiedades específicas de determinados dispositivos se redefinen dentro de una consulta de medios.

## Sprites CSS {#section-b0af39db1af74561aea9fddcc8cdc2c7}

Muchos de los elementos de la interfaz de usuario del visor están diseñados con ilustraciones de mapa de bits y tienen más de un estado visual distinto. Un buen ejemplo es un botón que normalmente tiene al menos 3 estados diferentes: &quot;up&quot;, &quot;over&quot; y &quot;down&quot;. Cada estado requiere la asignación de su propia ilustración de mapa de bits.

Con un enfoque clásico del estilo, el CSS tendría una referencia independiente al archivo de imagen individual en el servidor para cada estado del elemento de interfaz de usuario. A continuación se muestra un ejemplo de CSS para aplicar estilo a un botón de desplazamiento:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-image:url(images/v2/ScrollLeftButton_up.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-image:url(images/v2/ScrollLeftButton_down.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-image:url(images/v2/ScrollLeftButton_disabled.png);  
}
```

El inconveniente de este enfoque es que el usuario final experimenta parpadeos o retraso en la respuesta de la interfaz de usuario cuando se interactúa con el elemento por primera vez. Esta acción se produce porque la ilustración de imagen para el nuevo estado del elemento aún no se ha descargado. Además, este enfoque puede tener un ligero impacto negativo en el rendimiento debido a un aumento en el número de llamadas HTTP al servidor.

Los sprites CSS son un enfoque diferente en el que las ilustraciones de imagen para todos los estados de elementos se combinan en un único archivo PNG denominado &quot;sprite&quot;. Este &quot;elemento sprite&quot; tiene todos los estados visuales para un elemento determinado colocado uno tras otro. Al aplicar estilo a un elemento de interfaz de usuario con sprites, se hace referencia a la misma imagen sprite para todos los estados diferentes de la CSS. Además, la `background-position` propiedad se utiliza para cada estado para especificar qué parte de la imagen &quot;sprite&quot; se utiliza. Puede estructurar una imagen &quot;sprite&quot; de cualquier manera adecuada. Los visores normalmente lo tienen apilado verticalmente. A continuación se muestra un ejemplo basado en &quot;sprite&quot; de aplicar estilo al mismo botón de desplazamiento desde arriba:

```
.s7flyoutviewer .s7scrollleftbutton[state]  { 
    background-image: url(images/v2/ScrollLeftButton_light_sprite.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-position: -56px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-position: -0px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-position: -56px -448px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-position: -0px -448px;  
}
```

## Notas de estilo y consejos generales {#section-95855dccbbc444e79970f1aaa3260b7b}

* Al personalizar la interfaz de usuario del visor con CSS, el uso de la `!IMPORTANT` regla no se admite para aplicar estilo a los elementos del visor. En concreto, la regla no debe utilizarse para anular ningún estilo predeterminado o en tiempo de ejecución proporcionado por el visor o el SDK del visor. `!IMPORTANT` La razón es que puede afectar al comportamiento de los componentes adecuados. En su lugar, debe utilizar selectores CSS con la especificidad adecuada para establecer las propiedades CSS documentadas en esta guía de referencia.
* Todas las rutas a los recursos externos dentro de CSS se resuelven en la ubicación de CSS, no en la ubicación de la página HTML del visor. Tenga en cuenta esta regla cuando copie la CSS predeterminada en una ubicación diferente. Copie también los recursos predeterminados o actualice las rutas dentro de la CSS personalizada.
* El formato preferido para la ilustración de mapa de bits es PNG.
* La ilustración de mapa de bits se asigna a elementos de la interfaz de usuario mediante la `background-image` propiedad .
* Las propiedades `width` y `height` de un elemento de interfaz de usuario definen su tamaño lógico. El tamaño del mapa de bits pasado `background-image` no afecta al tamaño lógico.
* Para utilizar la alta densidad de píxeles de pantallas de alta resolución como Retina, especifique una ilustración de mapa de bits dos veces más grande que el tamaño del elemento de la interfaz de usuario lógica. A continuación, aplique la `-webkit-background-size:contain` propiedad para reducir el tamaño del fondo al tamaño del elemento de la interfaz lógica del usuario.
* Para quitar un botón de la interfaz de usuario, agregue `display:none` a su clase CSS.
* Puede utilizar varios formatos para el valor de color que admite CSS. Si necesita transparencia, utilice el formato `rgba(R,G,B,A)`. De lo contrario, puede utilizar el formato `#RRGGBB`.

## Elementos comunes de la interfaz de usuario {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A continuación se muestra la documentación de referencia de elementos de la interfaz de usuario que se aplica a Visor flotante:
