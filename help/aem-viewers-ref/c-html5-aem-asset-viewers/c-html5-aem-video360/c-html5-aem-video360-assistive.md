---
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
solution: Experience Manager
title: Soporte técnico de asistencia
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360, accesibilidad
role: Desarrollador, profesional empresarial
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visualizador. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen la función `button` y el texto descriptivo configurado con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, el atributo `aria-disabled` se establece en consecuencia.

Los componentes del regulador tienen la función `slider` con los atributos `aria-valuenow`, `aria-valuemin` y `aria-valuemax` para describir la posición actual del control deslizante.

Las listas desplegables se activan mediante botones con atributos adicionales `aria-haspopup` establecidos en `true` y `aria-controls` que hacen referencia al elemento real del panel desplegable. El propio panel desplegable tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el atributo `aria-label` especificado.

Los cuadros de diálogo modal tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento del encabezado del cuadro de diálogo.
