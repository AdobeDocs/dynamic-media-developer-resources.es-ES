---
title: Instalación de varios visores de Dynamic Media en el mismo servidor
description: Instrucciones para instalar la API de visores de Dynamic Media.
solution: Experience Manager
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: 07eb6cf84a46753b41307187d5c5b2a077fa9009
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Instalación de varios visores en el mismo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated January 13, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instrucciones para instalar la API de visores de Dynamic Media.

Instale y pruebe el servicio de imágenes antes de instalar los visores del servicio de imágenes.

Copie los archivos de visores de IS en el disco duro y luego implemente el archivo `s7viewers.war` en el directorio `../ImageServing/webapps`. Consulte la documentación del servicio de imágenes para obtener instrucciones sobre cómo implementar, inicio, detener y administrar el servidor de imágenes.

>[!NOTE]
>
>No hay ninguna instalación de actualización para los visores de servicio de imágenes. Adobe recomienda realizar una copia de seguridad de cualquier directorio de visores de Dynamic Media (visores s7viewers) existente antes de continuar con la instalación.

**Para instalar varios visores en el mismo servidor**

1. Cambie el nombre del archivo .war del visor al contexto deseado e implemente el archivo en la ubicación que desee.
1. Establezca el parámetro `this.isViewerRoot` en `config.js`.
1. Abra `config.js` ubicado en la raíz de la carpeta del visor recién creada.
1. Establezca el parámetro `this.isViewerRoot = "/s7viewers"` en el contexto del archivo `s7viewers.war`. Por ejemplo, `"/s7viewers-4.0"`.
1. Guarde el archivo y cierre.
