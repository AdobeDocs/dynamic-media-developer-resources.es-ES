---
title: Actualización de IS 4.7.4 o posterior
description: Utilice este procedimiento al actualizar Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Actualización de IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar Dynamic Media Image Serving.

Si está actualizando desde una versión anterior de Image Serving, póngase en contacto con el servicio de asistencia técnica para el proceso correcto.

>[!NOTE]
>
>La variable [!DNL webapps] La carpeta se puede eliminar al actualizar. Haga una copia de seguridad de [!DNL webapps] antes de la actualización.

1. Inicie sesión en el host del servidor con privilegios administrativos.
1. Extraiga el contenido del archivo zip de distribución de Image Serving.
1. Inicie el asistente de instalación ejecutando `setup/setup.exe`.
1. Select **[!UICONTROL Siguiente]** para avanzar al Acuerdo de licencia del usuario final (EULA), lea el acuerdo de licencia y seleccione **[!UICONTROL Sí]**.

   La página siguiente muestra los ajustes de configuración anteriores.
1. Haga clic en **[!UICONTROL Siguiente]** para iniciar la instalación de actualización.

   >[!NOTE]
   >
   >El instalador realiza una copia de seguridad de los archivos de configuración del servidor antiguos en la [!DNL BACKUP/] carpeta.

1. Una vez finalizada la instalación, seleccione **[!UICONTROL Finalizar]** para salir del asistente de instalación.

   A veces, el asistente de instalación puede pedirle que reinicie el sistema.

Durante una actualización, la variable [!DNL ImageServing/conf/server.xml] se actualiza a la configuración más reciente. Si ha cambiado o agregado algún valor, debe guardar el [!DNL server.xml] y vuelva a implementar los cambios después de la actualización.

Después de una instalación de actualización, considere la posibilidad de calentar la caché de respuestas HTTP antes de activar el servidor. Consulte la descripción del `playlog` para obtener más información.
