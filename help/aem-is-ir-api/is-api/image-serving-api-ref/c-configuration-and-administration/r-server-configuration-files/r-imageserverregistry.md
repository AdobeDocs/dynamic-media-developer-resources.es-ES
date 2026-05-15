---
description: Contiene las opciones de configuración de Image Server.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
TQID: 'https://experienceleague.adobe.com/UdMACutToNmpsXnhU0jAaItCZJ8r0RTxirjaqXSpa0c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Contiene las opciones de configuración de Image Server.

Al modificar este archivo XML, debe tener cuidado de mantener una sintaxis XML válida; de lo contrario, es posible que el servidor de imágenes no se inicie correctamente.

Para que los cambios surtan efecto, reinicie el servidor de imágenes después de editar este archivo. Solo se admiten para la modificación los valores de elemento que se enumeran a continuación. Edite cualquier otro contenido de este archivo solo cuando lo aconseje el servicio de asistencia técnica de Dynamic Media.

>[!NOTE]
>
>No cambie la estructura de `<imageserverregistry>`, incluido el orden de los elementos. Tenga cuidado al editar este archivo; de lo contrario, es posible que el servidor de imágenes no se pueda iniciar.

Lo siguiente ilustra qué elementos se pueden cambiar. Hay otros elementos presentes que no deben cambiarse. El orden de los elementos siguientes no refleja el orden en que deben estar presentes en el archivo.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Notas {#section-7217f011f69f41e7af4f3983d7776d6f}

Puede haber varios elementos `<RootPath>` (uno para cada carpeta del archivo de datos de origen). Image Server busca las rutas raíz en el orden especificado para encontrar un archivo de origen concreto.
