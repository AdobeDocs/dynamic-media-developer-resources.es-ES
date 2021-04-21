---
description: Datos de usuario. El servidor devuelve el contenido de este campo al cliente en respuesta a req=userdata.
solution: Experience Manager
title: Datos de usuario
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 8%

---


# Datos de usuario{#userdata}

Datos de usuario. El servidor devuelve el contenido de este campo al cliente en respuesta a req=userdata.

## Propiedades {#section-06f2002b77d54a64be07f12fff54ad13}

Valor de cadena de texto. Se recomienda utilizar el formato [datos de propiedad](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md). Si no se utiliza el formato de datos de propiedad, la cadena de texto no debe contener el carácter &#39;=&#39;.

Los clientes del visor de zoom, giro y folletos asumen este campo para utilizar el formato de datos de propiedad. Estos clientes utilizan este campo para la configuración y personalización del visor. Consulte la documentación del visor para obtener más información.

Este campo participa en la localización de cadenas de texto. Consulte [Localización de cadena de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en *Referencia de protocolo HTTP* para obtener más información.

## Predeterminado {#section-7ee879762130467199745f2abc662f1e}

Ninguno.

## Véase también {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , localización de cadenas de  [texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
