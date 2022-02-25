---
title: Soporte técnico de asistencia
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene una función `region` y `aria-label` establecido de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con la variable `Container.LABEL` símbolo de localización.

Los botones tienen la función `button` y el texto descriptivo configurado con la variable `aria-label` atributo. El valor de `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, la variable `aria-disabled` se establece en consecuencia.

La vista principal tiene una función `application`. Puede obtener una breve descripción de la vista principal en `aria-roledescription`, con el valor definido por la variable `ROLE_DESCRIPTION` símbolo de localización del componente de vista principal correspondiente. Se proporcionan sugerencias de navegación para los usuarios del teclado mediante `aria-describedby`, el texto de la sugerencia de uso proviene del `USAGE_HINT` símbolo de localización. Si un recurso tiene una etiqueta definida en el campo UserData , la variable `aria-label` se configura con el valor de dicha etiqueta.
