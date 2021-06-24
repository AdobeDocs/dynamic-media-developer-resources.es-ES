---
title: Instalación de varios visores de Dynamic Media en el mismo servidor
description: Instrucciones para instalar la API de visores de Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Developer,Business Practitioner
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# Instalación de varios visores en el mismo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instrucciones para instalar la API de visores de Dynamic Media.

Instale y pruebe Image Serving antes de instalar los visores de Image Serving.

Copie los archivos de visores IS en el disco duro y, a continuación, implemente el archivo `s7viewers.war` en el directorio `../ImageServing/webapps`. Consulte la documentación del servicio de imágenes para obtener instrucciones sobre cómo implementar, iniciar, detener y administrar el servidor de imágenes.

>[!NOTE]
>
>No hay instalación de actualización para los visores de servicio de imágenes. Adobe recomienda realizar una copia de seguridad de cualquier directorio de visores de Dynamic Media (visores s7viewers) existente antes de continuar con la instalación.

**Para instalar varios visores en el mismo servidor:**

1. Cambie el nombre del visor .war al contexto deseado e implemente el archivo en la ubicación que desee.
1. Establezca el parámetro `this.isViewerRoot` en `config.js`.
1. Abra `config.js` en la raíz de la carpeta del visor recién creada.
1. Establezca el parámetro `this.isViewerRoot = "/s7viewers"` en el contexto del archivo `s7viewers.war`. Por ejemplo, `"/s7viewers-4.0"`.
1. Guarde el archivo y cierre.
