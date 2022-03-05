---
title: Comandos de selección
description: Estos comandos se utilizan para seleccionar grupos de viñetas, objetos, subáreas de grupos u objetos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43f6ec6e-e4eb-468d-9c66-841af5e0a8a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# Comandos de selección{#selection-commands}

Estos comandos se utilizan para seleccionar grupos de viñetas, objetos, subáreas de grupos u objetos.

El comando, o el material, o ambos, se especifican después de este comando de selección y antes de que el siguiente comando de selección (o el final de la solicitud) se aplique al elemento seleccionado. Los comandos de selección delimitan los segmentos de especificación de material (MSS).

<table id="simpletable_028957E516644FE8A7B1BC056A32FCD1"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a" type="reference" format="dita" scope="local"> obj</a> </span> </p></td> 
  <td class="stentry"> <p>Seleccione un grupo de viñetas u objeto por nombre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b" type="reference" format="dita" scope="local"> sel</a></span> </p></td> 
  <td class="stentry"> <p>Seleccione un grupo de viñetas u objeto por ubicación de píxeles. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-decal.md#reference-3a5f1adc7fe24c91aa5655d64038e857" type="reference" format="dita" scope="local"> calco</a></span> </p></td> 
  <td class="stentry"> <p>Seleccione el área de calcomanía del objeto seleccionado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sub.md#reference-3cedba817f3c401495ba32bd1bf9b383" type="reference" format="dita" scope="local"> sub</a></span> </p></td> 
  <td class="stentry"> <p>Seleccione un subárea del grupo u objeto seleccionado. </p></td> 
 </tr> 
</table>
