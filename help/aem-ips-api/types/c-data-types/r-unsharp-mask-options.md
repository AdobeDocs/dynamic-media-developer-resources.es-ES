---
description: Configuración que ayuda a mejorar el nitidez de la imagen para archivos TIF piramidales optimizados.
seo-description: Configuración que ayuda a mejorar el nitidez de la imagen para archivos TIF piramidales optimizados.
seo-title: Opciones de máscara de enfoque
solution: Experience Manager
title: Opciones de máscara de enfoque
uuid: 73073de0-41b6-471c-8887-f6b94ed2af90
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 12%

---


# Opciones de máscara de enfoque{#unsharpmaskoptions}

Configuración que ayuda a mejorar el nitidez de la imagen para archivos TIF piramidales optimizados.

`unsharpMaskOptions=[ *`cantidad, radio, umbral, monocromo`*]`

## Parámetros {#section-c3f0d03136ba4422819cb463bd393885}

Especifique un valor para las opciones `unsharpMaskOptions` con `minOccurs=" *`n`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Nombre </th>
   <th colname="col2" class="entry"> Tipo </th>
   <th colname="col3" class="entry"> Descripción </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> cantidad</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Controla el contraste aplicado a los píxeles de borde. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Rango: 0,0 - 5,0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Predeterminado: 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> radius</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Controla la nitidez estableciendo el número de píxeles alrededor del borde de una imagen. El valor adecuado depende del tamaño de la imagen. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Rango: 0,0 - 250,0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Los valores bajos afilan solo los píxeles de borde. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">Los valores altos afilan una banda más amplia de píxeles. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> umbral</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Determina los píxeles diferentes que deben estar en el área circundante antes de que se consideren píxeles de borde y se puedan enfocar. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Rango: 0 - 255 (números enteros solamente). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Predeterminado: 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> monocromo</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Los valores solo incluyen <span class="codeph"> 0</span> o <span class="codeph"> 1</span>. </p><p>Configúrelo en <span class="codeph"> 0</span> para aplicarlo a cada componente de color por separado o en <span class="codeph"> 1</span> para aplicarlo solo al brillo (intensidad) de la imagen. La máscara de capa o la máscara compuesta también se afilan. </p><p><span class="codeph"><span class="varname"> </span></span> se ignora el monocromo en las imágenes en escala de grises. </p></td>
  </tr>
 </tbody>
</table>

## Ejemplo {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## Utilizado por {#section-db8124a5468b498694a780f8a56a4560}

El tipo `unsharpMaskOptions` lo utiliza:

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [Referencia de la API del servicio de imágenes: op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)

