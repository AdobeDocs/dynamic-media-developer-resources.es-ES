---
description: Utilice este procedimiento al actualizar el servicio de imágenes de Scene7 en Linux.
seo-description: Utilice este procedimiento al actualizar el servicio de imágenes de Scene7 en Linux.
seo-title: Actualización desde IS 4.7.4 o posterior
solution: Experience Manager
title: Actualización desde IS 4.7.4 o posterior
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 038f0f8f2c4f815e47749e0bab153c63e5396c91
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Actualizando desde IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar el servicio de imágenes de Scene7 en Linux.

Si va a realizar la actualización desde una versión anterior del servicio de imágenes, póngase en contacto con el servicio de soporte técnico para conocer el proceso correcto.

La carpeta [!DNL webapps] puede eliminarse al actualizar. Haga una copia de seguridad de la carpeta [!DNL webapps] antes de realizar la actualización.

1. Inicie sesión en el host del servidor con privilegios de raíz.
1. Descomprima y descomprima el archivo tar de distribución de servicio de imágenes.
1. Ejecute [!DNL ./install-is] para iniciar el asistente de instalación que se encuentra en la carpeta [!DNL setup].

   El instalador de actualizaciones comprueba la integridad y la versión del paquete instalado. Si se realiza correctamente, se muestra el Contrato de licencia de usuario final (&quot;EULA&quot;).
1. Lea el contrato de licencia y, a continuación, escriba &quot;**[!UICONTROL y]**&quot; para continuar con la instalación.

   El programa de instalación realiza una copia de seguridad de los archivos de configuración antiguos del servidor en la carpeta [!DNL BACKUP/].

   Cuando se completa la instalación, se muestra el siguiente mensaje:

   `Image Server was started successfully`

Durante una actualización, el archivo [!DNL ImageServing/conf/server.xml] se actualiza a la configuración más reciente. Si ha cambiado o agregado algún valor, debe guardar el [!DNL server.xml] existente y volver a implementar los cambios después de la actualización.

Después de una instalación de actualización, considere la posibilidad de calentar la caché de respuesta HTTP antes de activar el servidor. Consulte la descripción de la utilidad [!DNL playlog] para obtener más detalles.
