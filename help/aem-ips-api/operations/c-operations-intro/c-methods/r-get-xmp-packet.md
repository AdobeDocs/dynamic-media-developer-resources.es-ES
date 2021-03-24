---
description: Recupera un paquete de metadatos XMP para el recurso especificado.
solution: Experience Manager
title: getXMPPackets
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 21%

---


# getXMPPackets{#getxmppacket}

Recupera un paquete de metadatos XMP para el recurso especificado.

Sintaxis

## Tipos de usuarios autorizados {#section-7cb9c26045214f01b1d6b6948b6c6a18}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-b4075df0e4414b00b961d978d5471db9}

**Entrada (getXMPPacketsParam**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El control de la empresa con el paquete que desea devolver (por ejemplo, `c|656`). |
| `*`assetHandle`*` | `xsd:string` | Sí | Recurso para el que se debe recuperar el paquete de XMP. |

**Salida (getXMPPacketsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`zipPacket`*` | `xsd:Base 64 binary` | Sí | [!DNL zlib-compressed] XMP paquete. |

## Ejemplos {#section-d681af49122e4ca9bcd04110a2e98e6f}

**Solicitar**

```java
<ns:getXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
</ns:getXMPPacketParam>
```

**Respuesta**

```java
<getXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg+
      955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/Lr/AQ5Kc/AxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzA/QZkunymD8
      cvs5lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC4
      1IjNF1YlksGV2v26mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFgllKO+bn/ZpqrFv+xsS519WKO1mX9y/yoHppveRXrgWTlxX9qJk0ojHG9eaBP3
      PtKnNaNRNJ kq6lNC8bO5/sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh
      /3LPyoIWfgNKX1Vz4i8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7t+8xdjuhqNPERMBaoBAAA=
   </compressedPacket>
</getXMPPacketReturn>
```

