---
description: Contiene las opciones de configuración del supervisor del servidor.
solution: Experience Manager
title: SupervisorRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: cc6a16fb-fd70-431f-aad6-adb99d4da062
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# SupervisorRegistry.xml{#supervisorregistry-xml}

Contiene las opciones de configuración del supervisor del servidor.

Al editar este archivo XML, asegúrese de mantener una sintaxis XML válida; de lo contrario, es posible que el servidor de imágenes no se inicie correctamente.

Reinicie el servicio de imágenes después de editar este archivo para asegurarse de que los cambios surtan efecto. Solo se admiten para la modificación los valores de elemento/atributo resaltados a continuación. Edite el resto del contenido de este archivo solo cuando el servicio de asistencia técnica de Dynamic Media lo aconseje.

```
<supervisor>
    <config>
        <tcpport>9910</tcpport>
        <log>SV::log</log>
        <temp>SV::temp</temp>
        <tracelevel>SV::tracelevel</tracelevel>
        <tracestatsinterval>600</tracestatsinterval>
    </config>
    <servers>
        <server id="is">
            <description>Dynamic Media Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Dynamic Media SVG server</description>
            <profile ref="Java32"/>
            <profile ref="SVG"/>
            <arguments>
                <argument>-XmxSV::SvgHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9998</argument>
            </arguments>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="ps">
            <description>Dynamic Media [!DNL Platform Server]</description>
            <profile ref="Java32"/>
            <profile ref="PlatformServer"/>
            <profile ref="Tomcat"/>
            <arguments>
                <argument>-XmxSV::PsHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9999</argument>
            </arguments>
            <startPriority>2</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
    </servers>
</supervisor>
```
