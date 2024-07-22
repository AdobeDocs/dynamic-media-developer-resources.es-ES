---
title: Soporte de tecnología de asistencia
description: Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen el rol `button` y el texto descriptivo establecido con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando se deshabilita un botón, el atributo `aria-disabled` se establece en consecuencia.

Los componentes del control deslizante tienen la función `slider` con los atributos `aria-valuenow`, `aria-valuemin` y `aria-valuemax` para describir la posición actual del control deslizante.

Las listas desplegables se activan mediante botones con el atributo adicional `aria-haspopup` establecido en `true` y el atributo `aria-controls` que hace referencia al elemento del panel desplegable real. El panel desplegable tiene el rol `menu` con subelementos que tienen el rol `menuitem`. Cada elemento de menú tiene especificado el atributo `aria-label`.

Los cuadros de diálogo modales tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento de encabezado del cuadro de diálogo.
