---
description: Siga estos pasos para instalar Image Serving por primera vez en Windows.
seo-description: Siga estos pasos para instalar Image Serving por primera vez en Windows.
seo-title: Instalación por primera vez
solution: Experience Manager
title: Instalación por primera vez
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# Instalación por primera vez{#installing-for-the-first-time}

Siga estos pasos para instalar Image Serving por primera vez en Windows.

1. Inicie sesión en el host del servidor con privilegios administrativos.
1. Si ya ha recibido una licencia, cópiela en su servidor y, a continuación, ejecute la instalación de la licencia haciendo doble clic en el archivo.

   Si todavía no dispone de una licencia, puede continuar con la instalación e instalar la licencia más tarde.
1. Extraiga el contenido del archivo zip de distribución de Image Serving.
1. Ejecute [!DNL setup]/ [!DNL setup.exe] para iniciar el asistente de instalación.
1. Haga clic en &quot;Siguiente&quot; para avanzar al Acuerdo de licencia del usuario final (EULA), lea el acuerdo de licencia y haga clic en **[!UICONTROL Yes]**.

   El cuadro de diálogo [!DNL Authentication] aparece a continuación.
1. Si una licencia ya está instalada y la información de la licencia aparece en el cuadro de diálogo [!DNL Authentication], haga clic en **[!UICONTROL Next]** para continuar.

   Si no tiene una licencia, haga clic en **[!UICONTROL Solicitar licencia]**. El siguiente cuadro de diálogo muestra una de las direcciones MAC de la tarjeta de interfaz de red del equipo. Envíe por correo electrónico esta dirección MAC, el nombre de su empresa y el producto que está instalando tal y como indica el mensaje.

   **Importante:** La licencia se basa en la dirección MAC de una de las tarjetas de interfaz de red instaladas en este host. Si deshabilita, elimina o reemplaza esta tarjeta, la licencia ya no se reconocerá como válida. Asegúrese de obtener una licencia para la configuración de hardware que utilizará para IS.

   Puede seguir instalando IS sin una licencia válida e instalar la licencia más tarde. Para continuar, haga clic en **[!UICONTROL Back]** para volver al cuadro de diálogo [!DNL Authentication] y, a continuación, haga clic en **[!UICONTROL Next]**.
1. Continúe con la página &quot;Configuración de administración de Platform Server&quot;. Introduzca nuevos valores según sea necesario o acepte los valores predeterminados.

   Puede configurar los siguientes elementos:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Puerto de conexión HTTP del servidor de plataforma </p> </td> 
   <td> <p>Puerto de escucha HTTP principal para el servicio de imágenes y la representación de imágenes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Puerto de escucha del administrador </p> </td> 
   <td> <p>Puerto de escucha del administrador </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Tamaño de caché del servidor de plataforma en MB </p> </td> 
   <td> <p>Tamaño inicial de la caché de respuesta principal </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Ubicación de caché del servidor de plataforma </p> </td> 
   <td> <p>Carpeta de caché PS </p> </td> 
  </tr> 
 </tbody> 
</table>

Los números de puerto especificados deben ser únicos y no deben ser utilizados por otras aplicaciones o servicios.

La siguiente pantalla ofrece la oportunidad de revisar la configuración seleccionada.
1. Haga clic en **[!UICONTROL Back]** para realizar cambios o haga clic en **[!UICONTROL Next]** para iniciar la instalación.
1. Haga clic en **[!UICONTROL Finish]** para salir del asistente de instalación.
