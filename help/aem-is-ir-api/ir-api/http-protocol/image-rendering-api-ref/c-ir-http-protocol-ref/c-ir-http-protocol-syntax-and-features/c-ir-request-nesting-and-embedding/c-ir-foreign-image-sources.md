---
title: Fuentes de imagen externas
description: El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP externos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
TQID: 'https://experienceleague.adobe.com/doS6fbVfaXGtLVNBAmOkB-TquNmOc5B2B--IewouFDY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# Fuentes de imagen externas{#foreign-image-sources}

El servicio de imágenes admite el acceso a las imágenes de origen en servidores HTTP y FTP externos.

Para especificar una dirección URL externa para un comando `src=` o `mask=`, simplemente delimite toda la dirección URL incrustada con llaves:

` …&src={ *[!DNL foreignUrl]*}&…`

Se permiten direcciones URL absolutas completas (si se establece `attribute::AllowDirectUrls`) y direcciones URL relativas a `attribute::RootUrl`. Se produce un error si una dirección URL absoluta está incrustada y el atributo: `AllowDirectUrls` es 0, o si se especifica una dirección URL relativa y `attribute::RootUrl` está vacío.

El servidor almacena en caché las imágenes externas según los encabezados de almacenamiento en caché incluidos con la respuesta HTTP.
