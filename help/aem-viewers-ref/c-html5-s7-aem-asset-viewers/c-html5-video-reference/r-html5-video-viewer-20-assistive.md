---
title: Soporte de tecnología de asistencia
description: Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene una función `region` y `aria-label` de forma predeterminada, se establece en el nombre del visor. Puede controlar la etiqueta con `Container.LABEL` símbolo de localización.

Los botones tienen la función `button` y texto descriptivo configurado con `aria-label` atributo. El valor de `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, `aria-disabled` se establece en consecuencia.

Los componentes del deslizador tienen la función `slider` con atributos `aria-valuenow`, `aria-valuemin`, y `aria-valuemax` para describir la posición actual del regulador.

Las listas desplegables se activan mediante botones con `aria-haspopup` atributo establecido en `true` y `aria-controls` que hace referencia al elemento de panel desplegable real. El panel desplegable en sí tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el `aria-label` atributo especificado.

Los cuadros de diálogo modales tienen la función `dialog`. El elemento header del cuadro de diálogo es referenciado por la variable `aria-labelledby` atributo.
