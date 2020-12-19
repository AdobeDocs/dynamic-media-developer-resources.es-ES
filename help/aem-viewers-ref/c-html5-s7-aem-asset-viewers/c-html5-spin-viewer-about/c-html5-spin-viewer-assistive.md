---
description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-title: Soporte de tecnología de asistencia
solution: Experience Manager
title: Soporte de tecnología de asistencia
topic: Dynamic media
uuid: 6312f2f7-e1fa-4536-bae4-d8bc7735d5af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen la función `button` y el texto descriptivo definido con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando se deshabilita un botón, el atributo `aria-disabled` se establece en consecuencia.

La vista principal tiene la función `application`. En `aria-roledescription` se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de localización `ROLE_DESCRIPTION` del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan mediante `aria-describedby`, el texto de la sugerencia de uso se obtiene a partir del símbolo de localización `USAGE_HINT`. Si un recurso tiene una etiqueta definida en el campo UserData, el atributo `aria-label` se establece con el valor de dicha etiqueta.
