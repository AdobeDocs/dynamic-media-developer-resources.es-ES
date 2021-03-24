---
description: Contiene la configuración del servidor de plataforma.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# server.xml{#server-xml}

Contiene la configuración del servidor de plataforma.

Al modificar este archivo XML, se debe tener cuidado de mantener una sintaxis XML válida; de lo contrario, Platform Server puede no iniciarse.

Para que los cambios surtan efecto, Platform Server debe reiniciarse después de editar este archivo.

El diagrama siguiente ilustra qué configuración se puede cambiar en este archivo. Consulte las secciones correspondientes anteriores de este documento para obtener una descripción de esta configuración. Tenga en cuenta que este diagrama no es una representación completa de [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```

