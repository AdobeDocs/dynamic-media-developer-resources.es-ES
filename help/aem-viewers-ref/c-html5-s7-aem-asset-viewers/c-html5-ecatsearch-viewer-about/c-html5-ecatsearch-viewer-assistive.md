---
description: Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
solution: Experience Manager
title: Soporte de tecnología de asistencia
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
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

Las listas desplegables se activan mediante botones con el atributo adicional `aria-haspopup` establecido en `true` y el atributo `aria-controls` que hace referencia al elemento del panel desplegable real. El panel desplegable en sí tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene especificado el atributo `aria-label`.

La interfaz de usuario de búsqueda se agrupa en el elemento con la función `search`. El campo de entrada de búsqueda tiene el rol `searchbox` y hace referencia a la etiqueta informativa controlada por el símbolo de localización `SearchPanel.INFO_PROMPT` con el atributo `aria-describedby`.

Los cuadros de diálogo modales tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento de encabezado del cuadro de diálogo.
