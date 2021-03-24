---
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
solution: Experience Manager
title: Soporte técnico de asistencia
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom en línea,Accesibilidad
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visualizador. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

La vista principal tiene la función `application`. En `aria-roledescription` se proporciona una breve descripción de la vista principal, con el valor definido por el símbolo de localización `ROLE_DESCRIPTION` del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, el texto de la sugerencia de uso proviene del símbolo de localización `USAGE_HINT`. Si un recurso tiene una etiqueta definida en el campo UserData , el atributo `aria-label` se establece con el valor de dicha etiqueta.

Los componentes que muestran muestras tienen la función `listbox` con el atributo `aria-label` establecido en el valor del símbolo de localización `LABEL` de ese componente. Las muestras individuales tienen la función `option` con los atributos `aria-setsize` y `aria-posinset` para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se establece el atributo `aria-selected` en `true`.
