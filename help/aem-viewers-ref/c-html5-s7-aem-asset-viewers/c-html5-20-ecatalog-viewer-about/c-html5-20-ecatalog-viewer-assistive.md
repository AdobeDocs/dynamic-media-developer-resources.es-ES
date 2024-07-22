---
title: Soporte de tecnología de asistencia
description: Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen el rol `button` y el texto descriptivo establecido con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando se deshabilita un botón, el atributo `aria-disabled` se establece en consecuencia.

La vista principal tiene el rol `application`. Se proporciona una breve descripción de la vista principal en `aria-roledescription`, con el valor definido por el símbolo de localización `ROLE_DESCRIPTION` del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan mediante `aria-describedby`, el texto de la sugerencia de uso proviene del símbolo de localización `USAGE_HINT`. Si un recurso tiene una etiqueta definida en el campo UserData, el atributo `aria-label` se establece con el valor de dicha etiqueta.

Las zonas interactivas, las regiones y los mapas de imagen tienen la función `button` y el texto descriptivo establecido con el atributo `aria-label`, con el valor de la etiqueta de zona interactiva o mapa de imagen. Cuando el usuario se centra en zonas interactivas o mapas de imagen, las sugerencias de navegación para los usuarios del teclado se proporcionan mediante `aria-describedby`, y el texto de la sugerencia de uso proviene del símbolo de localización `USAGE_HINT`.

Las miniaturas tienen el rol `dialog` con el atributo `aria-label` controlado por el símbolo de localización `ThumbnailGridView.LABEL`. Las miniaturas individuales tienen el rol `button`. Si se selecciona una miniatura, se obtiene el atributo `aria-selected` establecido en `true`.

Los componentes que muestran muestras tienen el rol `listbox` con el atributo `aria-label` establecido en el valor del símbolo de localización `LABEL` de ese componente. Las muestras individuales tienen el rol `option` con los atributos `aria-setsize` y `aria-posinset` para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se obtiene el atributo `aria-selected` establecido en `true`.

Las listas desplegables se activan mediante botones con el atributo adicional `aria-haspopup` establecido en `true` y el atributo `aria-controls` que hace referencia al elemento del panel desplegable real. El panel desplegable tiene el rol `menu` con subelementos que tienen el rol `menuitem`. Cada elemento de menú tiene especificado el atributo `aria-label`.

Los cuadros de diálogo modales tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento de encabezado del cuadro de diálogo.
