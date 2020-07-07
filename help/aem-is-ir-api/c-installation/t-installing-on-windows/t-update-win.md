---
description: Utilice este procedimiento al actualizar el servicio de imágenes de Scene7.
seo-description: Utilice este procedimiento al actualizar el servicio de imágenes de Scene7.
seo-title: Actualización desde IS 4.7.4 o posterior
solution: Experience Manager
title: Actualización desde IS 4.7.4 o posterior
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Actualización desde IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar el servicio de imágenes de Scene7.

Si va a realizar la actualización desde una versión anterior del servicio de imágenes, póngase en contacto con el servicio de soporte técnico para conocer el proceso correcto.

>[!NOTE]
>
>La [!DNL webapps] carpeta se puede eliminar al actualizar. Realice una copia de seguridad de la [!DNL webapps] carpeta antes de realizar la actualización.

1. Inicie sesión en el host del servidor con privilegios administrativos.
1. Extraiga el contenido del archivo zip de distribución del servicio de imágenes.
1. Ejecute setup/setup.exe para iniciar el asistente de instalación.
1. Haga clic en **[!UICONTROL Siguiente]** para pasar al Contrato de licencia de usuario final (EULA), leer el contrato de licencia y hacer clic en **[!UICONTROL Sí]**.

   La página siguiente muestra las opciones de configuración anteriores.
1. Haga clic en **[!UICONTROL Siguiente]** para inicio de la instalación de la actualización.

   >[!NOTE]
   >
   >El programa de instalación realiza una copia de seguridad de los archivos de configuración antiguos del servidor en la [!DNL BACKUP/] carpeta.

1. Una vez completada la instalación, haga clic en &quot;Finalizar&quot; para salir del asistente de instalación.

   En algunos casos, el asistente de instalación puede solicitar reiniciar el sistema.
>Durante una actualización, el [!DNL ImageServing/conf/server.xml] archivo se actualiza a la configuración más reciente. Si ha cambiado o agregado algún valor, debe guardar el existente [!DNL server.xml] y volver a implementar los cambios después de la actualización.
>
>Después de una instalación de actualización, considere la posibilidad de calentar la caché de respuesta HTTP antes de activar el servidor. Consulte la descripción de la `playlog` utilidad para obtener más detalles.

