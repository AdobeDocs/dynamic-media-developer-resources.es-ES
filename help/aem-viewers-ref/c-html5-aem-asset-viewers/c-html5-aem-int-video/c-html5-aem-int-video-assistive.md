---
title: Soporte de tecnología de asistencia
description: Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene una función `region` y `aria-label` de forma predeterminada, se establece en el nombre del visor. Puede controlar la etiqueta con `Container.LABEL` símbolo de localización.

Los botones tienen la función `button` y texto descriptivo configurado con `aria-label` atributo. El valor de `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, `aria-disabled` se establece en consecuencia.

Los componentes del deslizador tienen la función `slider` con atributos `aria-valuenow`, `aria-valuemin`, y `aria-valuemax` para describir la posición actual del regulador.

Las miniaturas tienen la función `dialog` con `aria-label` controlado por el `ThumbnailGridView.LABEL` símbolo de localización. Las miniaturas individuales tienen un rol `button`. Si se selecciona una miniatura, se obtiene `aria-selected` atributo establecido en `true`.

Los componentes que muestran muestras tienen la función `listbox` con `aria-label` atributo establecido en el valor de `LABEL` símbolo de localización de ese componente. Las muestras individuales tienen la función `option` con `aria-setsize` y `aria-posinset` atributos para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se obtiene la variable `aria-selected` atributo establecido en `true`.

Las listas desplegables se activan mediante botones con `aria-haspopup` atributo establecido en `true` y `aria-controls` que hace referencia al elemento de panel desplegable real. El panel desplegable en sí tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el `aria-label` atributo especificado.

Los cuadros de diálogo modales tienen la función `dialog`. El elemento header del cuadro de diálogo es referenciado por la variable `aria-labelledby` atributo.
