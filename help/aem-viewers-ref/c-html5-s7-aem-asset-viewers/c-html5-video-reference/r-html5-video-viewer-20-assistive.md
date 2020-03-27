---
description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-description: Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
seo-title: Soporte de tecnología de asistencia
solution: Experience Manager
title: Soporte de tecnología de asistencia
topic: Dynamic media
uuid: e7090fb1-9458-4f97-a11f-5b0600a13db0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el `aria-label` atributo definidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de `Container.LABEL` localización.

Los botones tienen la función `button` y el texto descriptivo definidos con el `aria-label` atributo . El valor del `aria-label` atributo se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, `aria-disabled` el atributo se establece en consecuencia.

Los componentes del deslizador tienen la función `slider` con atributos `aria-valuenow``aria-valuemin`y `aria-valuemax` para describir la posición actual del deslizador.

Las listas desplegables se activan mediante botones con un `aria-haspopup` atributo adicional definido en `true` `aria-controls` y un atributo que hace referencia al elemento del panel desplegable real. El propio panel desplegable tiene la función `menu` de subelementos con la función `menuitem`. Cada elemento de menú tiene el `aria-label` atributo especificado.

Los cuadros de diálogo Modal tienen la función `dialog`. El atributo hace referencia al elemento de encabezado del cuadro de diálogo `aria-labelledby` .
