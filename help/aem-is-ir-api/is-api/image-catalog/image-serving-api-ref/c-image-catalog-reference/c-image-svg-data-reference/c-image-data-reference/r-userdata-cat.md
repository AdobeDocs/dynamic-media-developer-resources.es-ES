---
description: Datos de usuario. El servidor devuelve el contenido de este campo al cliente en respuesta a req=userdata.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# UserData{#userdata}

Datos de usuario. El servidor devuelve el contenido de este campo al cliente en respuesta a req=userdata.

## Propiedades {#section-06f2002b77d54a64be07f12fff54ad13}

Valor de cadena de texto. Se recomienda usar el formato [datos de propiedad](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md). Si no se utiliza el formato de datos de propiedad, la cadena de texto no debe contener el carácter &quot;=&quot;.

Los clientes del visor de zoom, giros y folletos suponen que este campo utiliza la propiedad data formatting. Estos clientes utilizan este campo para la configuración y personalización del visor. Consulte la documentación del visor para obtener más información.

Este campo participa en la localización de cadenas de texto. Consulte [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en la *Referencia de protocolo HTTP* para obtener detalles.

## Predeterminado {#section-7ee879762130467199745f2abc662f1e}

Ninguno.

## Véase también {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
