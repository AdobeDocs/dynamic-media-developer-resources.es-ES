---
title: Soporte de tecnología de asistencia
description: Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets,Accessibility
role: Developer,User
exl-id: 6cf7f739-cbfb-4fac-8632-904a0d40ad05
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene una función `region` y `aria-label` de forma predeterminada, se establece en el nombre del visor. Puede controlar la etiqueta con `Container.LABEL` símbolo de localización.

Los botones tienen la función `button` y texto descriptivo configurado con `aria-label` atributo. El valor de `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, `aria-disabled` se establece en consecuencia.

La vista principal tiene su función `application`. Se proporciona una breve descripción de la vista principal en `aria-roledescription`, con el valor definido por el `ROLE_DESCRIPTION` símbolo de localización del componente de vista principal correspondiente. Las sugerencias de navegación para los usuarios del teclado se proporcionan utilizando `aria-describedby`, el texto de la sugerencia de uso proviene del `USAGE_HINT` símbolo de localización. Si un recurso tiene una etiqueta definida en el campo UserData, la variable `aria-label` se establece con el valor de dicha etiqueta.

Los componentes que muestran muestras tienen la función `listbox` con `aria-label` atributo establecido en el valor de `LABEL` símbolo de localización de ese componente. Las muestras individuales tienen la función `option` con `aria-setsize` y `aria-posinset` atributos para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se obtiene la variable `aria-selected` atributo establecido en `true`.

Los componentes del deslizador tienen la función `slider` con atributos `aria-valuenow`, `aria-valuemin`, y `aria-valuemax` para describir la posición actual del regulador.
