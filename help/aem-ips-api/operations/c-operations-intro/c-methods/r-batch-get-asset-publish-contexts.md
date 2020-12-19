---
description: Devuelve los contextos de publicación de los recursos marcados para la publicación.
seo-description: Devuelve los contextos de publicación de los recursos marcados para la publicación.
seo-title: batchGetAssetPublishContext
solution: Experience Manager
title: batchGetAssetPublishContext
topic: Scene7 Image Production System API
uuid: 7f442019-37a9-4473-be92-a952a7a67664
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

Devuelve los contextos de publicación de los recursos marcados para la publicación.

Sintaxis

## Tipos de usuarios autorizados {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* El usuario debe tener acceso de lectura para devolver los recursos.
>* Todos los usuarios tienen acceso a la compañía compartida.

>



## Parámetros {#section-1742fcb196224545b270eb8241f757a8}

**Entrada (batchGetAssetPublishContextParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Manejar a la compañía. |
| ` *`assetHandleArray`*` | ` `tipos:HandleArray&quot; | Sí | Lista de recursos que desea consulta para contextos activos (marcados para publicación). |

**Salida (batchGetAssetPublishContextReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`assetPublishContextArray`*` | `types:assetPublishContextsArray` | Sí | Matriz de contextos de publicación en la que se marca cada recurso para la publicación. |

## Ejemplos {#section-457f6809ccfa425b9a0976313d613f4e}

**Solicitar**

```java
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Respuesta**

```java
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```

