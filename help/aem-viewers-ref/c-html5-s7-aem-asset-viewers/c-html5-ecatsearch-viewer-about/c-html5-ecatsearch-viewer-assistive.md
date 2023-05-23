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

El elemento de visor de nivel superior tiene una función `region` y `aria-label` de forma predeterminada, se establece en el nombre del visor. Puede controlar la etiqueta con `Container.LABEL` símbolo de localización.

Los botones tienen la función `button` y texto descriptivo definido con la variable `aria-label` atributo. El valor de `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando se deshabilita un botón, la variable `aria-disabled` se establece en consecuencia.

La vista principal tiene su función `application`. Se proporciona una breve descripción de la vista principal en `aria-roledescription`, con el valor definido por el `ROLE_DESCRIPTION` símbolo de localización del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, el texto de la sugerencia de uso proviene del `USAGE_HINT` símbolo de localización. Si un recurso tiene una etiqueta definida en el campo UserData, la variable `aria-label` se establece con el valor de dicha etiqueta.

Los puntos interactivos, las regiones y los mapas de imagen tienen la función `button` y texto descriptivo configurado con `aria-label` atributo, con el valor de la etiqueta de punto interactivo o de mapa de imagen. Cuando el usuario se centra en zonas activas o mapas de imagen, se proporcionan sugerencias de navegación para los usuarios del teclado mediante `aria-describedby`, con el texto de la sugerencia de uso procedente de `USAGE_HINT` símbolo de localización.

Las miniaturas tienen la función `dialog` con `aria-label` controlado por el `ThumbnailGridView.LABEL` símbolo de localización. Las miniaturas individuales tienen un rol `button`. Si se selecciona una miniatura, se obtiene `aria-selected` atributo establecido en `true`.

Los componentes que muestran muestras tienen la función `listbox` con `aria-label` atributo establecido en el valor de `LABEL` símbolo de localización de ese componente. Las muestras individuales tienen la función `option` con `aria-setsize` y `aria-posinset` atributos para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se obtiene el `aria-selected` atributo establecido en `true`.

Las listas desplegables se activan mediante botones con `aria-haspopup` atributo establecido en `true` y el `aria-controls` que hace referencia al elemento de panel desplegable real. El panel desplegable en sí tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el `aria-label` atributo especificado.

La interfaz de usuario de búsqueda se agrupa en el elemento con la función `search`. El campo de entrada de búsqueda tiene la función `searchbox` y hace referencia a la etiqueta informativa controlada por `SearchPanel.INFO_PROMPT` símbolo de localización con `aria-describedby` atributo.

Los cuadros de diálogo modales tienen la función `dialog`. El elemento header del cuadro de diálogo es referenciado por la variable `aria-labelledby` atributo.
