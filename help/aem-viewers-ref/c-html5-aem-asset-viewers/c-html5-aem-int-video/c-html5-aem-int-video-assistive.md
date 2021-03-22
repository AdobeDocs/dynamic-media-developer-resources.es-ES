---
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
seo-description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
seo-title: Soporte técnico de asistencia
solution: Experience Manager
title: Soporte técnico de asistencia
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos,Accesibilidad
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visualizador. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen la función `button` y el texto descriptivo configurado con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, el atributo `aria-disabled` se establece en consecuencia.

Los componentes del regulador tienen la función `slider` con los atributos `aria-valuenow`, `aria-valuemin` y `aria-valuemax` para describir la posición actual del control deslizante.

Las miniaturas tienen la función `dialog` con el atributo `aria-label` controlado por el símbolo de localización `ThumbnailGridView.LABEL`. Las miniaturas individuales tienen la función `button`. Si se selecciona una miniatura, se establece el atributo `aria-selected` en `true`.

Los componentes que muestran muestras tienen la función `listbox` con el atributo `aria-label` establecido en el valor del símbolo de localización `LABEL` de ese componente. Las muestras individuales tienen la función `option` con los atributos `aria-setsize` y `aria-posinset` para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se establece el atributo `aria-selected` en `true`.

Las listas desplegables se activan mediante botones con atributos adicionales `aria-haspopup` establecidos en `true` y `aria-controls` que hacen referencia al elemento real del panel desplegable. El propio panel desplegable tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el atributo `aria-label` especificado.

Los cuadros de diálogo modal tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento del encabezado del cuadro de diálogo.
