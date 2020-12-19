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
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten funciones y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen la función `button` y el texto descriptivo definido con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando se deshabilita un botón, el atributo `aria-disabled` se establece en consecuencia.

Los componentes del deslizador tienen la función `slider` con los atributos `aria-valuenow`, `aria-valuemin` y `aria-valuemax` para describir la posición actual del deslizador.

Las listas desplegables se activan mediante botones con el atributo `aria-haspopup` adicional establecido en `true` y el atributo `aria-controls` que hace referencia al elemento real del panel desplegable. El propio panel desplegable tiene la función `menu` con subelementos que tienen la función `menuitem`. Cada elemento de menú tiene el atributo `aria-label` especificado.

Los cuadros de diálogo Modal tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento de encabezado del cuadro de diálogo.
