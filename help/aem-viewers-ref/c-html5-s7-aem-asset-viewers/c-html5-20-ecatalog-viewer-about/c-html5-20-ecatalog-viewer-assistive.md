---
description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-title: Soporte de tecnología de asistencia
solution: Experience Manager
title: Soporte de tecnología de asistencia
topic: Dynamic media
uuid: 8565383e-5c13-4af0-9b6e-2d583c18f19c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---


# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen la función `button` y el texto descriptivo definido con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando se desactiva un botón, el atributo `aria-disabled` se establece en consecuencia.

La vista principal tiene la función `application`. En `aria-roledescription` se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de localización `ROLE_DESCRIPTION` del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan mediante `aria-describedby`, el texto de la sugerencia de uso se obtiene a partir del símbolo de localización `USAGE_HINT`. Si un recurso tiene una etiqueta definida en el campo UserData, el atributo `aria-label` se establece con el valor de dicha etiqueta.

Las zonas interactivas, las regiones y los mapas de imagen tienen la función `button` y el texto descriptivo establecido con el atributo `aria-label`, con el valor del punto interactivo o la etiqueta del mapa de imagen. Cuando el usuario se centra en puntos interactivos o mapas de imagen, se proporcionan sugerencias de navegación para los usuarios del teclado mediante `aria-describedby`, con el texto para la sugerencia de uso procedente del símbolo de localización `USAGE_HINT`.

Las miniaturas tienen la función `dialog` con el atributo `aria-label` controlado por el símbolo de localización `ThumbnailGridView.LABEL`. Las miniaturas individuales tienen una función `button`. Si se selecciona una miniatura, se establece el atributo `aria-selected` en `true`.

Los componentes que muestran muestras tienen la función `listbox` con el atributo `aria-label` establecido en el valor del símbolo de localización `LABEL` de ese componente. Las muestras individuales tienen la función `option` con los atributos `aria-setsize` y `aria-posinset` para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se establece el atributo `aria-selected` en `true`.

Las listas desplegables se activan mediante botones con el atributo `aria-haspopup` adicional establecido en `true` y el atributo `aria-controls` que hace referencia al elemento real del panel desplegable. El propio panel desplegable tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el atributo `aria-label` especificado.

Los cuadros de diálogo Modal tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento de encabezado del cuadro de diálogo.
