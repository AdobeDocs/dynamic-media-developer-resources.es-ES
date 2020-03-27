---
description: Recupera un paquete de metadatos XMP para el recurso especificado.
seo-description: Recupera un paquete de metadatos XMP para el recurso especificado.
seo-title: getXMPPaca
solution: Experience Manager
title: getXMPPaca
topic: Scene7 Image Production System API
uuid: c4b40e76-a459-4036-ace2-8df202305bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getXMPPaca{#getxmppacket}

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

**Entrada (getXMPPacaParam**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | El identificador de compañía con el paquete que desea devolver (por ejemplo, `c|656`). |
| ` *`assetHandle`*` | `xsd:string` | Sí | Recurso para el que se debe recuperar el paquete XMP. |

**Salida (getXMPPacaRetorno)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`zipPacket`*` | `xsd:Base 64 binary` | Sí | [!DNL zlib-compressed] Paquete XMP. |

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

