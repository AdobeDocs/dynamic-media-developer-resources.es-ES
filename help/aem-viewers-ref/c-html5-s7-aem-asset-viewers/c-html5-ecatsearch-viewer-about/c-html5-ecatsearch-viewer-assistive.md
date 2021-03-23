---
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
seo-description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
seo-title: Soporte técnico de asistencia
solution: Experience Manager
title: Soporte técnico de asistencia
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
feature: Dynamic Media Classic, visores, SDK/API, búsqueda en catálogos electrónicos, accesibilidad
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visualizador. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen la función `button` y el texto descriptivo configurado con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, el atributo `aria-disabled` se establece en consecuencia.

La vista principal tiene la función `application`. En `aria-roledescription` se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de localización `ROLE_DESCRIPTION` del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, el texto de la sugerencia de uso proviene del símbolo de localización `USAGE_HINT`. Si un recurso tiene una etiqueta definida en el campo UserData , el atributo `aria-label` se establece con el valor de dicha etiqueta.

Los puntos interactivos, las regiones y los mapas de imágenes tienen la función `button` y el texto descriptivo configurado con el atributo `aria-label`, con el valor del punto interactivo o la etiqueta del mapa de imagen. Cuando el usuario se centra en puntos interactivos o mapas de imágenes, las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, con el texto para la sugerencia de uso procedente del símbolo de localización `USAGE_HINT`.

Las miniaturas tienen la función `dialog` con el atributo `aria-label` controlado por el símbolo de localización `ThumbnailGridView.LABEL`. Las miniaturas individuales tienen la función `button`. Si se selecciona una miniatura, se establece el atributo `aria-selected` en `true`.

Los componentes que muestran muestras tienen la función `listbox` con el atributo `aria-label` establecido en el valor del símbolo de localización `LABEL` de ese componente. Las muestras individuales tienen la función `option` con los atributos `aria-setsize` y `aria-posinset` para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se establece el atributo `aria-selected` en `true`.

Las listas desplegables se activan mediante botones con el atributo `aria-haspopup` adicional establecido en `true` y el atributo `aria-controls` que hace referencia al elemento real del panel desplegable. El propio panel desplegable tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el atributo `aria-label` especificado.

La interfaz de usuario de búsqueda se agrupa en el elemento con la función `search`. El campo de entrada de búsqueda tiene la función `searchbox` y hace referencia a la etiqueta informativa controlada por el símbolo de localización `SearchPanel.INFO_PROMPT` con el atributo `aria-describedby`.

Los cuadros de diálogo modal tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento del encabezado del cuadro de diálogo.
