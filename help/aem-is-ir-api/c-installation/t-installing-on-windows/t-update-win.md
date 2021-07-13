---
description: Utilice este procedimiento al actualizar Dynamic Media Image Serving.
solution: Experience Manager
title: Actualización de IS 4.7.4 o posterior
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Actualización de IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar Dynamic Media Image Serving.

Si está actualizando desde una versión anterior de Image Serving, póngase en contacto con el servicio de asistencia técnica para el proceso correcto.

>[!NOTE]
>
>La carpeta [!DNL webapps] se puede eliminar al actualizar. Haga una copia de seguridad de la carpeta [!DNL webapps] antes de la actualización.

1. Inicie sesión en el host del servidor con privilegios administrativos.
1. Extraiga el contenido del archivo zip de distribución de Image Serving.
1. Ejecute setup/setup.exe para iniciar el asistente de instalación.
1. Haga clic en **[!UICONTROL Siguiente]** para avanzar al Acuerdo de licencia del usuario final (EULA), lea el acuerdo de licencia y haga clic en **[!UICONTROL Yes]**.

   La página siguiente muestra los ajustes de configuración anteriores.
1. Haga clic en **[!UICONTROL Next]** para iniciar la instalación de la actualización.

   >[!NOTE]
   >
   >El instalador realiza una copia de seguridad de los archivos de configuración antiguos del servidor en la carpeta [!DNL BACKUP/].

1. Una vez finalizada la instalación, haga clic en &quot;Finalizar&quot; para salir del asistente de instalación.

   En algunos casos, el asistente de instalación puede solicitar reiniciar el sistema.

Durante una actualización, el archivo [!DNL ImageServing/conf/server.xml] se actualiza a la configuración más reciente. Si ha cambiado o agregado algún valor, debe guardar el [!DNL server.xml] existente y volver a implementar los cambios después de la actualización.

Después de una instalación de actualización, considere la posibilidad de calentar la caché de respuestas HTTP antes de activar el servidor. Consulte la descripción de la utilidad `playlog` para obtener más información.
