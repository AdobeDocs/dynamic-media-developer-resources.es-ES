---
description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-title: Soporte de tecnología de asistencia
solution: Experience Manager
title: Soporte de tecnología de asistencia
topic: Dynamic media
uuid: 5f6a021f-750c-40e1-be01-86c3750fd25f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el `aria-label` atributo definidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de `Container.LABEL` localización.

La vista principal tiene un papel `application`. En la `aria-roledescription`se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de `ROLE_DESCRIPTION` localización del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan mediante `aria-describedby`; el texto de la sugerencia de uso proviene del símbolo de `USAGE_HINT` localización. Si un recurso tiene una etiqueta definida en el campo UserData, el `aria-label` atributo se establece con el valor de dicha etiqueta.

Las zonas interactivas, las regiones y los mapas de imagen tienen la función `button` y el texto descriptivo definidos con el `aria-label` atributo, con el valor de la etiqueta de zona interactiva o mapa de imagen. Cuando el usuario se centra en zonas interactivas o mapas de imagen, se proporcionan sugerencias de navegación para los usuarios del teclado mediante `aria-describedby`el uso del símbolo de `USAGE_HINT` localización.
