---
description: Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media.
seo-description: Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media.
seo-title: Actualización desde IS 4.7.4 o posterior
solution: Experience Manager
title: Actualización desde IS 4.7.4 o posterior
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# Actualizando desde IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media.

Si va a realizar la actualización desde una versión anterior del servicio de imágenes, póngase en contacto con el servicio de soporte técnico para conocer el proceso correcto.

>[!NOTE]
>
>La carpeta [!DNL webapps] puede eliminarse al actualizar. Haga una copia de seguridad de la carpeta [!DNL webapps] antes de actualizar.

1. Inicie sesión en el host del servidor con privilegios administrativos.
1. Extraiga el contenido del archivo zip de distribución del servicio de imágenes.
1. Ejecute setup/setup.exe para iniciar el asistente de instalación.
1. Haga clic en **[!UICONTROL Siguiente]** para avanzar al Contrato de licencia de usuario final (EULA), lea el contrato de licencia y haga clic en **[!UICONTROL Sí]**.

   La página siguiente muestra las opciones de configuración anteriores.
1. Haga clic en **[!UICONTROL Siguiente]** para inicio de la instalación de la actualización.

   >[!NOTE]
   >
   >El programa de instalación realiza una copia de seguridad de los archivos de configuración antiguos del servidor en la carpeta [!DNL BACKUP/].

1. Una vez completada la instalación, haga clic en &quot;Finalizar&quot; para salir del asistente de instalación.

   En algunos casos, el asistente de instalación puede solicitar reiniciar el sistema.

Durante una actualización, el archivo [!DNL ImageServing/conf/server.xml] se actualiza a la configuración más reciente. Si ha cambiado o agregado algún valor, debe guardar el [!DNL server.xml] existente y volver a implementar los cambios después de la actualización.

Después de una instalación de actualización, considere la posibilidad de calentar la caché de respuesta HTTP antes de activar el servidor. Consulte la descripción de la utilidad `playlog` para obtener más detalles.
