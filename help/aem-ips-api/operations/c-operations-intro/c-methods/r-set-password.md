---
description: Establece la contraseña de un usuario específico o del usuario predeterminado en un valor específico, en función de si especifica un identificador de usuario.
seo-description: Establece la contraseña de un usuario específico o del usuario predeterminado en un valor específico, en función de si especifica un identificador de usuario.
seo-title: setPassword
solution: Experience Manager
title: setPassword
uuid: 78067f8d-4191-4580-a5a8-adb6edfcfab8
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 7%

---


# setPassword{#setpassword}

Establece la contraseña de un usuario específico o del usuario predeterminado en un valor específico, en función de si especifica un identificador de usuario.

La fecha de caducidad de la contraseña es opcional. Si se omite, la contraseña nunca caducará.

## Tipos de usuarios autorizados {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>** Solo el tipo de  `IpsAdmin` usuario está autorizado para ejecutar llamadas setPassword contra otros usuarios.

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## Parámetros {#section-0531294341f7483d89dacaa393dd659a}

**Entrada (setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Control de usuario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> password  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Contraseña. </p> <p>Los siguientes requisitos se aplican a la contraseña elegida: </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">Las contraseñas distinguen entre mayúsculas y minúsculas. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">La longitud mínima de la contraseña es de ocho caracteres. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">La contraseña debe contener uno o varios caracteres de las siguientes clases de caracteres: 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">Caracteres en inglés en minúsculas. Por ejemplo, <span class="codeph"> a b c d e </span> y así sucesivamente </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">Caracteres en inglés en mayúsculas. Por ejemplo, <span class="codeph"> A B C D E </span> y así sucesivamente. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">Números. Por ejemplo, <span class="codeph"> 1 2 3 4 5 </span> y así sucesivamente. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">Caracteres de símbolo especial. Por ejemplo, puede utilizar cualquiera de las siguientes opciones: <span class="codeph"> ` ~ ! @ # $ % ^ * ( ) _ + - = { } | [ ] y \ : " ; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Determina la fecha de caducidad de la contraseña. <p>Nota:  Proporcione la zona horaria con la solicitud para este campo. Las zonas horarias se ajustan a la hora central. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (setPasswordReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-23a6fbabdb3c4c3180076057e47ae567}

Este ejemplo de código crea una contraseña de usuario. La contraseña nunca caduca porque se ha omitido `passwordExpires`.

**Solicitar**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**Respuesta**

Ninguno.
