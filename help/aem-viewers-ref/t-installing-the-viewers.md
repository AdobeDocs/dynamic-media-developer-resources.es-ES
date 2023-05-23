---
title: Instalación de varios visores de Dynamic Media en el mismo servidor
description: Instrucciones para instalar la API de visores de Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# Instalación de varios visores en el mismo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instrucciones para instalar la API de visores de Dynamic Media.

Instale y pruebe el servicio de imágenes antes de instalar los visores del servicio de imágenes.

Copie los archivos de visores de IMS en el disco duro y, a continuación, implemente el `s7viewers.war` en el archivo `../ImageServing/webapps` directorio. Consulte la documentación del servicio de imágenes para obtener instrucciones sobre cómo implementar, iniciar, detener y administrar el servidor de imágenes.

>[!NOTE]
>
>No hay ninguna instalación de actualización para los visores del servicio de imágenes. El Adobe recomienda realizar una copia de seguridad de cualquier directorio de visores de Dynamic Media (s7viewers) existente antes de continuar con la instalación.

**Para instalar varios visores en el mismo servidor:**

1. Cambie el nombre del archivo .war del visor al contexto deseado e implemente el archivo en la ubicación que desee.
1. Establecer `this.isViewerRoot` parámetro en `config.js`.
1. Abrir `config.js` en la raíz de la carpeta del visor recién creada.
1. Establecer parámetro `this.isViewerRoot = "/s7viewers"` al contexto de la `s7viewers.war` archivo. Por ejemplo, `"/s7viewers-4.0"`.
1. Guarde el archivo y cierre.
