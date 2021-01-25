---
description: Describe los parámetros de operación comunes que administra la API de servicio Web IPS.
solution: Experience Manager
title: Métodos de operaciones
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---


# Métodos de operaciones{#operations-methods}

Esta sección describe los parámetros de operación comunes que administra la API de servicio Web IPS.

Para obtener una descripción completa de cada parámetro de operación, consulte [Parámetros de operación](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Manejadores: Acerca de {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gestiona los objetos IPS de referencia devueltos por determinadas operaciones de API. También puede pasar controladores como parámetros a llamadas de operación posteriores. Los controladores son tipos de datos de cadena ( `xsd:string`).

Los controladores están pensados para utilizarse solo durante una sesión de aplicación. Además, debe hacer que los controladores sean persistentes porque su formato puede cambiar entre las versiones de IPS. Cuando se escriben aplicaciones interactivas, se implementan tiempos de espera de sesión y se descartan todos los controladores entre sesiones, especialmente después de una actualización de IPS. Al escribir aplicaciones no interactivas, llame a las operaciones correspondientes para recuperar los controladores cada vez que se ejecute la aplicación. Las siguientes muestras de código Java/Axis2 muestran una ejecución de código incorrecta y correcta:

**Código de control incorrecto**

Este ejemplo de código es incorrecto porque contiene un valor codificado (555) para el identificador de compañía.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Código de control correcto**

Este ejemplo de código es correcto porque llama a `getCompanyInfo` para devolver un identificador válido. No se basa en un valor codificado. Utilice este método (u otro equivalente de API de IPS) para devolver el identificador requerido.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Tipos de control comunes {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

La mayoría de las operaciones requieren que establezca un contexto de compañía pasando un parámetro `companyHandle`. El identificador de compañía es un puntero que devuelven ciertas operaciones como `getCompanyInfo`, `addCompany` y `getCompanyMembership`.

**userHandle**

El parámetro `userHandle` es un parámetro opcional para operaciones que destinatario a un usuario específico. De forma predeterminada, estas operaciones destinatario al usuario que realiza la llamada (el usuario cuyas credenciales se pasan para la autenticación). Sin embargo, los usuarios administradores con los permisos adecuados pueden especificar otro usuario. Por ejemplo, la operación `setPassword` normalmente establece la contraseña del usuario autenticado, pero un administrador puede utilizar el parámetro `userHandle` para establecer la contraseña para otro usuario.

Para las operaciones que requieren un contexto de compañía (con el parámetro `companyHandle`), tanto los usuarios autenticados como los usuarios de destinatario deben ser miembros de la compañía especificada. Para operaciones que no requieren un contexto de compañía, los usuarios autenticados y los usuarios de destinatario deben ser miembros de al menos una compañía común.

Las siguientes operaciones pueden recuperar los identificadores de usuario:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle y accessGroupHandle**

De forma predeterminada, las operaciones que requieren permisos de acceso (leer, escribir, eliminar) funcionan en el contexto de permisos del usuario que realiza la llamada. Algunas operaciones permiten modificar este contexto con el parámetro `accessUserHandle` o `accessGroupHandle`. El parámetro `accessUserHandle` permite a un administrador suplantar a otro usuario. El parámetro `accessGroupHandle` permite que el llamador funcione en el contexto de un grupo de usuarios específico.

**responseFieldArray y excludeFieldArray**

Algunas operaciones permiten al llamador restringir los campos incluidos en la respuesta. La limitación de campos puede ayudar a reducir el tiempo y la memoria necesarios para procesar la solicitud y reducir el tamaño de los datos de respuesta. El llamante puede solicitar una lista específica de campos pasando un parámetro `responseFieldArray` o con una lista enumerada de campos excluidos a través del parámetro `excludeFieldArray`.

Tanto `responseFieldArray` como `excludeFieldArray` especifican campos mediante una ruta de nodo separada por `/`. Por ejemplo, para especificar que `searchAssets` devuelve sólo el nombre, la fecha de la última modificación y los metadatos de cada recurso hacen referencia a lo siguiente:

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

Tenga en cuenta que las rutas de nodo son relativas a la raíz del nodo de retorno. Si especifica un campo de tipo complejo sin ninguno de sus subelementos (por ejemplo, `assetArray/items/imageInfo`), se incluirán todos sus subelementos. Si especifica uno o varios subelementos en un campo de tipo complejo (por ejemplo, `assetArray/items/imageInfo/originalPath`), solo se incluirán esos subelementos.

Si no incluye `responseFieldArray` o `excludeFieldArray` en una solicitud, se devuelven todos los campos.

**Configuración regional**

Desde IPS 4.0, la API de IPS admite la configuración regional de una operación pasando el parámetro de configuración regional `authHeader`. Si el parámetro de configuración regional no está presente, se utilizará el encabezado HTTP `Accept-Language`. Si este encabezado tampoco está presente, se utilizará la configuración regional predeterminada para el servidor IPS.

Algunas operaciones también toman parámetros de configuración regional explícitos, que pueden ser diferentes al contexto de configuración regional de la operación. Por ejemplo, la operación `submitJob` toma un parámetro `locale` que establece la configuración regional utilizada para el registro de trabajos y la notificación por correo electrónico.

Los parámetros de configuración regional utilizan el formato `<language_code>[-<country_code>]`

Si el código de idioma es un código en minúscula de dos letras especificado por ISO-639 y el código de país opcional es un código en mayúsculas de dos letras especificado por ISO-3266. Por ejemplo, la cadena de configuración regional para inglés de EE. UU. es `en-US`.
