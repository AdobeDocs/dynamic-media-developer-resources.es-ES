---
description: Contiene la configuración del servidor de plataforma.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '89'
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
