---
description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-title: Soporte de tecnología de asistencia
solution: Experience Manager
title: Soporte de tecnología de asistencia
topic: Dynamic media
uuid: 2a6d6e09-a016-407d-b870-92c84fe75ed3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el `aria-label` atributo definidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de `Container.LABEL` localización.

Los botones tienen la función `button` y el texto descriptivo definidos con el `aria-label` atributo . El valor del `aria-label` atributo se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, `aria-disabled` el atributo se establece en consecuencia.

La vista principal tiene un papel `application`. En la `aria-roledescription`se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de `ROLE_DESCRIPTION` localización del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan mediante `aria-describedby`; el texto de la sugerencia de uso proviene del símbolo de `USAGE_HINT` localización. Si un recurso tiene una etiqueta definida en el campo UserData, el `aria-label` atributo se establece con el valor de dicha etiqueta.

Los componentes que muestran muestras tienen la función `listbox` con el `aria-label` atributo definido en el valor del símbolo de `LABEL` localización de ese componente. Las muestras individuales tienen la función `option` con `aria-setsize` y `aria-posinset` los atributos para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se establece el `aria-selected` atributo en `true`.
