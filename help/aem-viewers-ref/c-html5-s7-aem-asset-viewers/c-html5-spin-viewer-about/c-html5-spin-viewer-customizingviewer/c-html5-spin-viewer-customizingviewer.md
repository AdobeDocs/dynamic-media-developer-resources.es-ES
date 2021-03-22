---
description: Toda la personalización visual y la mayor parte de la personalización del comportamiento para el visor de giros se realiza mediante la creación de un CSS personalizado.
keywords: adaptable
seo-description: Toda la personalización visual y la mayor parte de la personalización del comportamiento para el visor de giros se realiza mediante la creación de un CSS personalizado.
seo-title: Personalización del visor de giros
solution: Experience Manager
title: Personalización del visor de giros
uuid: d951501c-d6da-454c-be2f-0887ffcac77c
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 0%

---


# Personalización del visor de giros{#customizing-spin-viewer}

Toda la personalización visual y la mayor parte de la personalización del comportamiento para el visor de giros se realiza mediante la creación de un CSS personalizado.

El flujo de trabajo sugerido es tomar el archivo CSS predeterminado para el visor apropiado, copiarlo en una ubicación diferente, personalizarlo y especificar la ubicación del archivo personalizado en el comando `style=`.

Los archivos CSS predeterminados se encuentran en la siguiente ubicación:

`<s7_viewers_root>/html5/SpinViewer_light.css`

El visor se suministra con archivos CSS predeterminados para esquemas de color &quot;claros&quot; y &quot;oscuros&quot;. La versión &quot;light&quot; se utiliza de forma predeterminada, pero puede cambiar a la versión &quot;dark&quot; utilizando el siguiente CSS estándar:

`<s7_viewers_root>/html5/SpinViewer_dark.css`

El archivo CSS personalizado debe contener las mismas declaraciones de clase que la predeterminada. Si se omite una declaración de clase, el visor no funciona correctamente porque no proporciona estilos predeterminados integrados para los elementos de la interfaz de usuario.

Otra forma de proporcionar reglas CSS personalizadas es utilizar estilos incrustados directamente en la página web o en una de las reglas CSS externas vinculadas.

Al crear CSS personalizada, tenga en cuenta que el visor asigna la clase `.s7spinviewer` a su elemento DOM contenedor. Si está utilizando un archivo CSS externo pasado con el comando `style=`, utilice la clase `.s7spinviewer` como clase principal en el selector de descendientes para sus reglas CSS. Si está realizando estilos incrustados en la página web, califique también este selector con un ID del elemento DOM de contenedor de la siguiente manera:

`#<containerId>.s7spinviewer`

## Creación de CSS diseñada adaptable {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es posible dirigirse a diferentes dispositivos e incrustar tamaños en CSS para que el contenido se muestre de forma diferente, según el dispositivo del usuario o un diseño de página web concreto. Esto incluye, entre otros, diferentes diseños de página web, tamaños de elementos de interfaz de usuario y resolución de ilustraciones.

El visor admite dos métodos para crear CSS diseñada con capacidad de respuesta: Marcadores CSS y consultas de medios CSS estándar. Puede utilizar estos métodos de forma independiente o conjunta.

**Marcadores CSS**

Para ayudar a crear CSS diseñada y adaptable, el visor admite marcadores CSS con clases CSS especiales asignadas dinámicamente al elemento contenedor del visor de nivel superior en función del tamaño del visor de tiempo de ejecución y el tipo de entrada utilizado en el dispositivo actual.

El primer grupo de marcadores CSS incluye las clases `.s7size_large`, `.s7size_medium` y `.s7size_small`. Se aplican en función del área de tiempo de ejecución del contenedor de visor. Es decir, si el área del visor es igual o mayor que el tamaño de un monitor de escritorio común `.s7size_large` se utiliza; si el área es de tamaño cercano a una tableta común `.s7size_medium` está asignada. Para áreas similares a las pantallas de teléfono móvil `.s7size_small` está configurado. El objetivo principal de estos marcadores CSS es crear diferentes diseños de interfaz de usuario para diferentes pantallas y tamaños de visor.

El segundo grupo de marcadores CSS incluye `.s7mouseinput` y `.s7touchinput`. `.s7touchinput` se establece si el dispositivo actual tiene capacidades de entrada táctil; de lo contrario,  `.s7mouseinput` se utiliza . Estos marcadores están diseñados para crear elementos de entrada de interfaz de usuario con diferentes tamaños de pantalla para diferentes tipos de entrada, ya que la entrada táctil suele requerir elementos más grandes. Si el dispositivo tiene funciones táctiles y de entrada de ratón, `.s7touchinput` se establece y el visor presenta una interfaz de usuario táctil.

El siguiente ejemplo de CSS establece el tamaño del botón de zoom en 28 x 28 píxeles en sistemas con entrada de ratón y 56 x 56 píxeles en dispositivos táctiles. Además, oculta completamente el botón si el tamaño del visor es realmente pequeño:

```
.s7spinviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7spinviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7spinviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Para dirigirse a dispositivos con una densidad de píxeles diferente, utilice consultas de medios CSS. El siguiente bloque de consulta de medios contendría una CSS específica para pantallas de alta densidad:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

El uso de marcadores CSS es la forma más flexible de crear CSS adaptable diseñada, ya que le permite dirigirse no solo al tamaño de la pantalla del dispositivo, sino también al tamaño real del visor, lo que puede resultar útil para diseños de página de diseño interactivos.

Utilice el archivo CSS del visor predeterminado como ejemplo de un enfoque de marcadores CSS.

**Consultas de medios CSS**

La detección de dispositivos también se puede realizar utilizando consultas de medios CSS puras. Todo lo incluido en un bloque de consulta de contenido determinado se aplica solo cuando se ejecuta en un dispositivo correspondiente.

Cuando se aplique a los visualizadores móviles, utilice cuatro consultas de medios CSS, definidas en el CSS en el siguiente orden:

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

## Sprites CSS {#section-b671c70acf284cb0aea678c2d2e4babc}

Muchos elementos de la interfaz de usuario del visor están diseñados con ilustraciones de mapa de bits y tienen más de un estado visual distinto. Un buen ejemplo es un botón que normalmente tiene al menos 3 estados diferentes: &quot;up&quot;, &quot;over&quot; y &quot;down&quot;. Cada estado requiere su propia ilustración de mapa de bits asignada.

Con un enfoque clásico del estilo, el CSS tendría una referencia independiente al archivo de imagen individual en el servidor para cada estado del elemento de la interfaz de usuario. El siguiente es un ejemplo de CSS para aplicar estilo al botón de acercamiento:

```
.s7spinviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

El inconveniente de este enfoque es que el usuario final experimenta parpadeos o retraso en la respuesta de la interfaz de usuario cuando se interactúa con el elemento por primera vez. Esta acción se produce porque la ilustración de la imagen para el nuevo estado del elemento aún no se ha descargado. Además, este enfoque puede tener un ligero impacto negativo en el rendimiento debido a un aumento en el número de llamadas HTTP al servidor.

Los sprites CSS son un enfoque diferente en el que las ilustraciones de imágenes para todos los estados de elementos se combinan en un solo archivo PNG denominado &quot;sprite&quot;. Este &quot;Sprite&quot; tiene todos los estados visuales para el elemento dado posicionado uno tras otro. Al diseñar un elemento de interfaz de usuario con sprites, se hace referencia a la misma imagen sprite para todos los estados diferentes del CSS. Además, la propiedad `background-position` se utiliza para cada estado para especificar qué parte de la imagen &quot;sprite&quot; se utiliza. Puede estructurar una imagen &quot;sprite&quot; de cualquier manera adecuada. Normalmente, los visualizadores lo tienen apilado verticalmente. A continuación se muestra un ejemplo basado en &quot;sprite&quot; de cómo aplicar estilo al mismo botón de acercamiento desde arriba:

```
.s7spinviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
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

A continuación se muestra la documentación de referencia de elementos de la interfaz de usuario que se aplica a los visualizadores de medios mixtos:
