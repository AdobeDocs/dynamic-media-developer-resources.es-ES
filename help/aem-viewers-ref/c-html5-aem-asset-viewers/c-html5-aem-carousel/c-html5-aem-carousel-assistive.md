---
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
solution: Experience Manager
title: Soporte técnico de asistencia
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners de carrusel,Accesibilidad
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visualizador. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen la función `button` y el texto descriptivo configurado con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, el atributo `aria-disabled` se establece en consecuencia.

Los botones que permiten navegar por las diapositivas de carrusel tienen etiquetas que se actualizan en tiempo de ejecución en función de la diapositiva seleccionada actualmente. La plantilla para la etiqueta de este botón se configura con el símbolo de localización `CAROUSELVIEWER_TOOLTIP_GOTO`.

La vista principal tiene la función `application`. En `aria-roledescription` se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de localización `ROLE_DESCRIPTION` del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, el texto de la sugerencia de uso proviene del símbolo de localización `USAGE_HINT`. Si un recurso tiene una etiqueta definida en el campo UserData , el atributo `aria-label` se establece con el valor de dicha etiqueta.

Los puntos interactivos, las regiones y los mapas de imágenes tienen la función `button` y el texto descriptivo configurado con el atributo `aria-label`, con el valor del punto interactivo o la etiqueta del mapa de imagen. Cuando el usuario se centra en puntos interactivos o mapas de imágenes, las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, con el texto para la sugerencia de uso procedente del símbolo de localización `USAGE_HINT`.
