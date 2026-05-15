---
description: Mostrar marcos de texto desbordados con signo más. Un indicador de desbordamiento de texto muestra cuándo el texto supera el espacio asignado para él en un marco de texto (o en el último marco de texto en el caso de texto enlazado). Este indicador es un cuadro rojo con un signo más en su interior.
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
TQID: 'https://experienceleague.adobe.com/Wy5VLpT5I1KzXUrKaPoetj2ejv4wbUOsU1My9vEA5gM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 21%

---

# markOverflowingTextFrames{#markoverflowingtextframes}

Mostrar marcos de texto desbordados con signo más. Un indicador de desbordamiento de texto muestra cuándo el texto supera el espacio asignado para él en un marco de texto (o en el último marco de texto en el caso de texto enlazado). Este indicador es un cuadro rojo con un signo más en su interior.

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverflowingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Al establecer el modificador `markOverflowingTextFrames=1` mediante una llamada URL, se marcan todos los marcos de texto en los que el texto está desbordado con un signo más. Además, en el visor de Dynamic Media Classic, el indicador de desbordamiento de texto está establecido en &quot; `TRUE`&quot; de forma predeterminada.

El valor predeterminado es 0.
