---
description: Describe los parámetros comunes de operación que administra la API del servicio Web IPS.
solution: Experience Manager
title: Métodos de operaciones
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# Métodos de operaciones{#operations-methods}

En esta sección se describen los parámetros de operación comunes que administra la API del servicio Web IPS.

Para obtener una descripción completa de cada parámetro de operación, consulte [Parámetros de operación](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Identificadores: Acerca de {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Controla los objetos IPS de referencia devueltos por determinadas operaciones de API. También puede pasar identificadores como parámetros a llamadas de operación subsiguientes. Los identificadores son tipos de datos de cadena ( `xsd:string`).

Los identificadores están pensados para utilizarse durante una sola sesión de la aplicación. Además, debe hacer que los identificadores sean persistentes porque su formato puede cambiar entre versiones de IPS. Al escribir aplicaciones interactivas, se implementan los tiempos de espera de sesión y se descartan todos los controladores entre sesiones, especialmente después de una actualización de IPS. Cuando escriba aplicaciones no interactivas, llame a las operaciones adecuadas para recuperar los identificadores cada vez que se ejecute la aplicación. Los siguientes ejemplos de código Java/Axis2 muestran una ejecución de código incorrecta y correcta:

**Código de identificador incorrecto**

Este ejemplo de código es incorrecto porque contiene un valor codificado (555) para el identificador de la compañía.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Código de identificador correcto**

Este ejemplo de código es correcto porque llama a `getCompanyInfo` para devolver un identificador válido. No se basa en un valor codificado de forma rígida. Utilice este método (u otro equivalente de API de IPS) para devolver el identificador necesario.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Tipos de identificadores comunes {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

La mayoría de las operaciones requieren que establezca un contexto de compañía pasando un `companyHandle` parámetro. El identificador de la compañía es un puntero devuelto por ciertas operaciones como `getCompanyInfo`, `addCompany`, y `getCompanyMembership`.

**userHandle**

El `userHandle` parameter es un parámetro opcional para operaciones dirigidas a un usuario específico. De forma predeterminada, estas operaciones se dirigen al usuario que realiza la llamada (el usuario cuyas credenciales se pasan para la autenticación). Sin embargo, los usuarios administradores con los permisos adecuados pueden especificar un usuario diferente. Por ejemplo, la variable `setPassword` La operación de establece normalmente la contraseña del usuario autenticado, pero un administrador puede utilizar el `userHandle` para establecer la contraseña de un usuario diferente.

Para operaciones que requieren un contexto de compañía (con el `companyHandle` ), los usuarios autenticados y de destino deben ser miembros de la compañía especificada. Para las operaciones que no requieren un contexto de compañía, los usuarios autenticados y de destino deben ser miembros de al menos una compañía común.

Las siguientes operaciones pueden recuperar los identificadores de usuario:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle y accessGroupHandle**

De forma predeterminada, las operaciones que requieren permisos de acceso (leer, escribir, eliminar) funcionan en el contexto de permisos del usuario que realiza la llamada. Algunas operaciones permiten modificar este contexto con la variable `accessUserHandle` o `accessGroupHandle` parámetro. El `accessUserHandle` permite que un administrador suplante a otro usuario. El `accessGroupHandle` permite que el llamador opere en el contexto de un grupo de usuarios específico.

**responseFieldArray y excludeFieldArray**

Algunas operaciones permiten al autor de la llamada restringir qué campos se incluyen en la respuesta. Limitar los campos puede ayudar a reducir el tiempo y la memoria necesarios para procesar la solicitud y el tamaño de los datos de respuesta. El autor de la llamada puede solicitar una lista específica de campos pasando un `responseFieldArray` o con una lista enumerada de campos excluidos a través de la variable `excludeFieldArray` parámetro.

Ambos `responseFieldArray` y `excludeFieldArray` especificar campos mediante una ruta de nodo separada por `/`. Por ejemplo, para especificar que `searchAssets` devuelve únicamente el nombre, la última fecha de modificación y los metadatos de cada recurso hacen referencia a lo siguiente:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Del mismo modo, para devolver todos los campos (excepto los permisos):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Tenga en cuenta que las rutas de nodos son relativas a la raíz del nodo de retorno. Si especifica un campo de tipo complejo sin ninguno de sus subelementos (por ejemplo, `assetArray/items/imageInfo`), se incluyen todos sus subelementos. Si especifica uno o varios subelementos en un campo de tipo complejo (por ejemplo, `assetArray/items/imageInfo/originalPath`), entonces solo se incluyen esos subelementos.

Si no incluye `responseFieldArray` o `excludeFieldArray` en una solicitud, se devuelven todos los campos.

**Configuración regional**

Desde IPS 4.0, la API de IPS admite la configuración regional del contexto de una operación pasando el `authHeader` Parámetro de configuración regional. Si el parámetro locale no está presente, el encabezado HTTP `Accept-Language` se utiliza. Si este encabezado tampoco está presente, se utilizará la configuración regional predeterminada del servidor IPS.

Algunas operaciones también toman parámetros de configuración regional explícitos, que pueden ser diferentes al contexto de la configuración regional de la operación. Por ejemplo, la variable `submitJob` la operación requiere un `locale` parámetro que establece la configuración regional utilizada para el registro de trabajos y las notificaciones por correo electrónico.

Los parámetros locales utilizan el formato `<language_code>[-<country_code>]`

Donde el código de idioma es un código de dos letras en minúsculas especificado por ISO-639 y el código de país opcional es un código de dos letras en mayúsculas especificado por ISO-3266. Por ejemplo, la cadena de configuración regional para inglés de EE. UU. es `en-US`.
