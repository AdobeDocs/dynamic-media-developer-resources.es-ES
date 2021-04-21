---
description: Describe los parámetros de operación comunes que gestiona la API de servicio web de IPS.
solution: Experience Manager
title: Métodos de operaciones
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---


# Métodos de operaciones{#operations-methods}

En esta sección se describen los parámetros de operación comunes que gestiona la API de servicio web de IPS.

Para obtener una descripción completa de cada parámetro de operación, consulte [Parámetros de operación](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Manuales: Acerca de {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Los controladores hacen referencia a objetos IPS devueltos por determinadas operaciones de API. También puede pasar controladores como parámetros a llamadas de operación posteriores. Los controladores son tipos de datos de cadena ( `xsd:string`).

Los controladores están pensados para utilizarse solo durante una sesión de aplicación. Además, debe hacer que los controladores sean persistentes, ya que su formato puede cambiar entre las versiones de IPS. Cuando escribe aplicaciones interactivas, implementa tiempos de espera de sesión y descarta todos los controles entre sesiones, especialmente después de una actualización de IPS. Cuando escriba aplicaciones no interactivas, llame a las operaciones adecuadas para recuperar los controladores cada vez que se ejecute la aplicación. Los siguientes ejemplos de código de Java/Axis2 muestran una ejecución de código incorrecta y correcta:

**Código de control incorrecto**

Este ejemplo de código es incorrecto porque contiene un valor codificado (555) para el identificador de la empresa.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Código de control correcto**

Este ejemplo de código es correcto porque llama a `getCompanyInfo` para devolver un identificador válido. No se basa en un valor codificado. Utilice este método (u otro equivalente de API IPS) para devolver el identificador requerido.

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

La mayoría de las operaciones requieren que establezca un contexto de empresa pasando un parámetro `companyHandle`. El identificador de la empresa es un puntero que devuelven determinadas operaciones, como `getCompanyInfo`, `addCompany` y `getCompanyMembership`.

**userHandle**

El parámetro `userHandle` es un parámetro opcional para operaciones dirigidas a un usuario específico. De forma predeterminada, estas operaciones se dirigen al usuario que realiza la llamada (el usuario cuyas credenciales se pasan para la autenticación). Sin embargo, los usuarios administradores con los permisos adecuados pueden especificar un usuario diferente. Por ejemplo, la operación `setPassword` establece normalmente la contraseña del usuario autenticado, pero un administrador puede utilizar el parámetro `userHandle` para establecer la contraseña de un usuario diferente.

Para las operaciones que requieren un contexto de empresa (con el parámetro `companyHandle` ), tanto los usuarios autenticados como los destinatarios deben ser miembros de la empresa especificada. Para las operaciones que no requieren un contexto de empresa, los usuarios autenticados y los destinatarios deben ser miembros de al menos una empresa común.

Las siguientes operaciones pueden recuperar los controles de usuario:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle y accessGroupHandle**

De forma predeterminada, las operaciones que requieren permisos de acceso (leer, escribir, eliminar) funcionan en el contexto de permisos del usuario que realiza la llamada. Algunas operaciones permiten modificar este contexto con los parámetros `accessUserHandle` o `accessGroupHandle`. El parámetro `accessUserHandle` permite que un administrador suplante a otro usuario. El parámetro `accessGroupHandle` permite que el llamador funcione en el contexto de un grupo de usuarios específico.

**responseFieldArray y excludeFieldArray**

Algunas operaciones permiten al llamador restringir qué campos se incluyen en la respuesta. La limitación de campos puede ayudar a reducir el tiempo y la memoria necesarios para procesar la solicitud y reducir el tamaño de los datos de respuesta. El llamador puede solicitar una lista específica de campos pasando un parámetro `responseFieldArray` o con una lista enumerada de campos excluidos a través del parámetro `excludeFieldArray`.

Tanto `responseFieldArray` como `excludeFieldArray` especifican campos mediante una ruta de nodo separada por `/`. Por ejemplo, para especificar que `searchAssets` devuelve solo el nombre, la última fecha de modificación y los metadatos de cada recurso hacen referencia a lo siguiente:

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

Tenga en cuenta que las rutas de nodos son relativas a la raíz del nodo de retorno. Si especifica un campo de tipo complejo sin ninguno de sus subelementos (por ejemplo, `assetArray/items/imageInfo`), se incluyen todos sus subelementos. Si especifica uno o más subelementos en un campo de tipo complejo (por ejemplo, `assetArray/items/imageInfo/originalPath`), solo se incluirán esos subelementos.

Si no se incluye `responseFieldArray` o `excludeFieldArray` en una solicitud, se devuelven todos los campos.

**Configuración regional**

Desde IPS 4.0, la API de IPS admite la configuración del contexto de configuración regional de una operación pasando el parámetro de configuración regional `authHeader`. Si el parámetro de configuración regional no está presente, se utilizará el encabezado HTTP `Accept-Language`. Si este encabezado tampoco está presente, se utilizará la configuración regional predeterminada para el servidor IPS.

Algunas operaciones también usan parámetros de configuración regional explícitos, que pueden ser diferentes del contexto de configuración regional de la operación. Por ejemplo, la operación `submitJob` toma un parámetro `locale` que establece la configuración regional utilizada para el registro de trabajos y la notificación por correo electrónico.

Los parámetros de configuración regional utilizan el formato `<language_code>[-<country_code>]`

Cuando el código de idioma es un código de dos letras en minúscula especificado por ISO-639 y el código de país opcional es un código de dos letras en mayúsculas especificado por ISO-3266. Por ejemplo, la cadena de configuración regional para inglés de EE. UU. es `en-US`.
