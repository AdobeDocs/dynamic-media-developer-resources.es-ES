---
title: Personalización del visor panorámico
description: Toda la personalización visual y la mayor parte de la personalización del comportamiento para el visor panorámico se realiza creando un CSS personalizado.
keywords: adaptable
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Personalización del visor de Video360{#customizing-video-viewer}

Toda la personalización visual y la mayor parte de la personalización del comportamiento se realiza mediante la creación de una CSS personalizada.

El flujo de trabajo sugerido es tomar el archivo CSS predeterminado para el visor apropiado, copiarlo en una ubicación diferente, personalizarlo y especificar la ubicación del archivo personalizado en la variable `style=` comando.

Los archivos CSS predeterminados se encuentran en la siguiente ubicación:

`<s7viewers_root>/html5/PanoramicViewer.css`

El archivo CSS personalizado debe contener las mismas declaraciones de clase que la predeterminada. Si se omite una declaración de clase, el visor no funciona correctamente porque no proporciona estilos predeterminados integrados para los elementos de la interfaz de usuario.

Otra forma de proporcionar reglas CSS personalizadas es utilizar estilos incrustados directamente en la página web o en una de las reglas CSS externas vinculadas.

Al crear CSS personalizada, tenga en cuenta que el visor asigna `.s7panoramicviewer` a su elemento DOM contenedor. Si utiliza un archivo CSS externo transferido con `style=` comando, usar `.s7panoramicviewer` como clase principal en el selector descendiente para sus reglas CSS. Si está realizando estilos incrustados en la página web, califique también este selector con un ID del elemento DOM de contenedor de la siguiente manera:

`#<containerId>.s7panoramicviewer.`


## Notas de estilo y consejos generales {#section-95855dccbbc444e79970f1aaa3260b7b}

* Todas las rutas a los recursos externos dentro de CSS se resuelven en la ubicación de CSS, no en la ubicación de la página del HTML del visor. Tenga esto en cuenta al copiar el CSS predeterminado a una ubicación diferente: puede ser necesario copiar también los recursos predeterminados o actualizar las rutas dentro del CSS personalizado.
* Puede utilizar varios formatos para el valor de color admitidos por CSS. Si se necesita transparencia, `rgba(R,G,B,A)` se recomienda. De lo contrario, no se requiere transparencia `#RRGGBB` se puede usar.

Al personalizar la interfaz de usuario del visor con CSS, el uso de `!IMPORTANT` regla no es compatible con los elementos del visualizador de estilo. En particular, `!IMPORTANT` no debe utilizarse para anular ningún estilo predeterminado o en tiempo de ejecución proporcionado por el visor o el SDK del visor, ya que puede afectar al comportamiento correcto de los componentes. En su lugar, se deben utilizar selectores CSS con la especificidad adecuada para establecer las propiedades CSS documentadas en esta guía de referencia.

## Visor panorámico CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Área del visor principal**
La zona de vista principal es la zona ocupada por la imagen panorámica.  Normalmente se configura para que se ajuste a la pantalla de dispositivo disponible cuando no se especifica ningún tamaño.

El aspecto del área de visualización se controla con el selector de clase CSS:
`.s7panoramicviewer`

Las propiedades de CSS aplicables incluyen:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> la anchura del visor; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> la altura del espectador; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para configurar un visor con un tamaño de 1024 x 512 píxeles.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Vista panorámica**
La vista principal es la imagen panorámica.

El aspecto de la vista principal se controla con el selector de clase CSS:
`.s7panoramicviewer .s7panoramicview`

Las propiedades de CSS aplicables incluyen:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> el color de fondo de la vista principal; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Ejemplo: Para que la vista principal sea transparente:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
