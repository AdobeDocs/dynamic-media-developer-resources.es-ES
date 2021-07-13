---
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
solution: Experience Manager
title: Soporte técnico de asistencia
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas,Accesibilidad
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visualizador. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

La vista principal tiene la función `application`. En `aria-roledescription` se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de localización `ROLE_DESCRIPTION` del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, el texto de la sugerencia de uso proviene del símbolo de localización `USAGE_HINT`. Si un recurso tiene una etiqueta definida en el campo UserData , el atributo `aria-label` se establece con el valor de dicha etiqueta.

Los puntos interactivos, las regiones y los mapas de imágenes tienen la función `button` y el texto descriptivo configurado con el atributo `aria-label`, con el valor del punto interactivo o la etiqueta del mapa de imagen. Cuando el usuario se centra en puntos interactivos o mapas de imágenes, las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, con el texto para la sugerencia de uso procedente del símbolo de localización `USAGE_HINT`.
