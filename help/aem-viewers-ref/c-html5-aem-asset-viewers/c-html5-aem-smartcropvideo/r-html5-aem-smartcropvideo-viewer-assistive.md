---
title: Soporte técnico de asistencia
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene una función `region` y `aria-label` establecido de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con la variable `Container.LABEL` símbolo de localización.

Los botones tienen la función `button` y el texto descriptivo configurado con `aria-label` atributo. El valor de `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, `aria-disabled` se establece en consecuencia.

Los componentes del regulador tienen la función `slider` con atributos `aria-valuenow`, `aria-valuemin`y `aria-valuemax` para describir la posición actual del control deslizante.

Las listas desplegables se activan mediante botones con botones adicionales `aria-haspopup` establecido en `true` y `aria-controls` que hace referencia al elemento real del panel desplegable. El propio panel desplegable tiene la función `menu` con subelementos que tengan la función `menuitem`. Cada elemento de menú tiene la variable `aria-label` atributo especificado.

Los cuadros de diálogo modal tienen la función `dialog`. El elemento de encabezado del cuadro de diálogo al que hace referencia el `aria-labelledby` atributo.
