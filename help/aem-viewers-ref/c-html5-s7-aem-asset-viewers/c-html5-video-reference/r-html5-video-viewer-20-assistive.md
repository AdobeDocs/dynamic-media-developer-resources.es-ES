---
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
solution: Experience Manager
title: Soporte técnico de asistencia
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo,Accesibilidad
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visualizador. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen la función `button` y el texto descriptivo configurado con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, el atributo `aria-disabled` se establece en consecuencia.

Los componentes del regulador tienen la función `slider` con los atributos `aria-valuenow`, `aria-valuemin` y `aria-valuemax` para describir la posición actual del control deslizante.

Las listas desplegables se activan mediante botones con atributos adicionales `aria-haspopup` establecidos en `true` y `aria-controls` que hacen referencia al elemento real del panel desplegable. El propio panel desplegable tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el atributo `aria-label` especificado.

Los cuadros de diálogo modal tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento del encabezado del cuadro de diálogo.
