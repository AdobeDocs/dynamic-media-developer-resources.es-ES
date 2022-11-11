---
title: Instalación por primera vez
description: Siga estos pasos para instalar Image Serving por primera vez en Windows.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Instalación por primera vez{#installing-for-the-first-time}

Siga estos pasos para instalar Image Serving por primera vez en Windows.

1. Inicie sesión en el host del servidor con privilegios administrativos.
1. Si ya ha recibido una licencia, cópiela en su servidor y, a continuación, ejecute la instalación de la licencia haciendo doble clic en el archivo.

   Si todavía no dispone de una licencia, puede continuar con la instalación e instalar la licencia más tarde.

1. Extraiga el contenido del archivo zip de distribución de Image Serving.
1. Inicie el asistente de instalación ejecutando [!DNL setup]/ [!DNL setup.exe].
1. Select **[!UICONTROL Siguiente]** para avanzar al Acuerdo de licencia del usuario final (EULA), lea el acuerdo de licencia y seleccione **[!UICONTROL Sí]**.

   La variable [!DNL Authentication] a continuación.
1. Si una licencia ya está instalada, y la información de la licencia aparece en la sección [!DNL Authentication] cuadro de diálogo, seleccione **[!UICONTROL Siguiente]** para continuar.

   Si no tiene una licencia, seleccione **[!UICONTROL Solicitud de licencia]**. El siguiente cuadro de diálogo muestra una de las direcciones MAC de la tarjeta de interfaz de red del equipo. Envíe por correo electrónico esta dirección de MAC, el nombre de su empresa y el producto que está instalando tal y como indica el mensaje.

   **Importante:** La licencia se basa en la dirección MAC de una de las tarjetas de interfaz de red instaladas en este host. Si deshabilita, elimina o reemplaza esta tarjeta, la licencia ya no se reconoce como válida. Asegúrese de obtener una licencia para la configuración de hardware que utiliza para Image Serving.

   Puede seguir instalando IS sin una licencia válida e instalar la licencia más tarde. Para continuar, seleccione **[!UICONTROL Atrás]** para volver a la [!DNL Authentication] y, a continuación, seleccione **[!UICONTROL Siguiente]**.
1. Continúe con el[!DNL Platform Server] Configuración de administración&quot;. Introduzca nuevos valores según sea necesario o acepte los valores predeterminados.

   Puede configurar los siguientes elementos:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] Puerto de conexión HTTP </p> </td>
      <td> <p>Puerto de escucha HTTP principal para el servicio de imágenes y la representación de imágenes </p> </td>
   </tr> 
   <tr> 
      <td> <p> Puerto de escucha del administrador </p> </td>
      <td> <p>Puerto de escucha del administrador </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] Tamaño de caché en MB </p> </td>
      <td> <p>Tamaño inicial de la caché de respuesta principal </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] Ubicación de caché </p> </td>
      <td> <p>Carpeta de caché PS </p> </td>
   </tr>
   </tbody>
   </table>

   Los números de puerto especificados deben ser únicos y no deben ser utilizados por otras aplicaciones o servicios.

   La siguiente pantalla ofrece la oportunidad de revisar la configuración seleccionada.

1. Select **[!UICONTROL Atrás]** para realizar cambios o seleccione **[!UICONTROL Siguiente]** para iniciar la instalación.

1. Select **[!UICONTROL Finalizar]** para salir del asistente de instalación.
