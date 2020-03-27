---
description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-title: Soporte de tecnología de asistencia
solution: Experience Manager
title: Soporte de tecnología de asistencia
topic: Dynamic media
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el `aria-label` atributo definidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de `Container.LABEL` localización.

Los botones tienen la función `button` y el texto descriptivo definidos con el `aria-label` atributo. El valor del `aria-label` atributo se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, el `aria-disabled` atributo se establece en consecuencia.

La vista principal tiene un papel `application`. En la `aria-roledescription`se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de `ROLE_DESCRIPTION` localización del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan mediante `aria-describedby`; el texto de la sugerencia de uso proviene del símbolo de `USAGE_HINT` localización. Si un recurso tiene una etiqueta definida en el campo UserData, el `aria-label` atributo se establece con el valor de dicha etiqueta.

Las zonas interactivas, las regiones y los mapas de imagen tienen la función `button` y el texto descriptivo definidos con el `aria-label` atributo, con el valor de la etiqueta de zona interactiva o mapa de imagen. Cuando el usuario se centra en zonas interactivas o mapas de imagen, se proporcionan sugerencias de navegación para los usuarios del teclado mediante `aria-describedby`el uso del símbolo de `USAGE_HINT` localización.

Las miniaturas tienen la función `dialog` con el `aria-label` atributo controlado por el símbolo de `ThumbnailGridView.LABEL` localización. Las miniaturas individuales tienen una función `button`. Si se selecciona una miniatura, se establece el `aria-selected` atributo en `true`.

Los componentes que muestran muestras tienen la función `listbox` con el `aria-label` atributo definido en el valor del símbolo de `LABEL` localización de ese componente. Las muestras individuales tienen la función `option` con `aria-setsize` y `aria-posinset` los atributos para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se establece el `aria-selected` atributo en `true`.

Las listas desplegables se activan mediante botones con un `aria-haspopup` atributo adicional definido en `true` y el `aria-controls` atributo que hace referencia al elemento del panel desplegable real. El propio panel desplegable tiene la función `menu` de subelementos con la función `menuitem`. Cada elemento de menú tiene el `aria-label` atributo especificado.

La interfaz de usuario de búsqueda se agrupa en el elemento con la función `search`. El campo de entrada de búsqueda tiene la función `searchbox` y hace referencia a la etiqueta informativa controlada por el símbolo de `SearchPanel.INFO_PROMPT` localización con el `aria-describedby` atributo .

Los cuadros de diálogo Modal tienen la función `dialog`. El atributo hace referencia al elemento de encabezado del cuadro de diálogo `aria-labelledby` .
