---
description: Puede definir los formatos de fecha que se utilizan al analizar e indexar cualquier campo con un tipo de datos de "fecha".
seo-description: Puede definir los formatos de fecha que se utilizan al analizar e indexar cualquier campo con un tipo de datos de "fecha".
seo-title: Formatos de fecha
solution: Target
title: Formatos de fecha
topic: Appendices,Site search and merchandising
uuid: 148914b5-33ef-41db-8404-67c03f6f0832
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Formatos de fecha{#date-formats}

Puede definir los formatos de fecha que se utilizan al analizar e indexar cualquier campo con un tipo de datos de &quot;fecha&quot;.

El formato de la fecha y la hora se especifica con una cadena de formato. La cadena de formato consta de cero o más especificaciones de conversión (una especificación de conversión consiste en un signo de porcentaje y otro carácter) y caracteres ordinarios. Se proporciona una lista predeterminada de cadenas de formato de fecha para cada campo de fecha.

Usted tiene control absoluto sobre esta lista y puede agregarla o modificarla para satisfacer las necesidades del sitio. La cadena de formato superior tiene prioridad y las cadenas de formato subsiguientes solo se utilizan si el análisis del contenido de una etiqueta de metadatos determinada produce un error.

Por ejemplo, supongamos que ha especificado los siguientes formatos de fecha:

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> <p>%b %d, %Y %T %Z </p> <p>%A %B %d, %Y %T %Z </p> <p>%A %b %d, %Y %T %Z </p> <p>%a %B %d, %Y %T %Z </p> <p>%a %b %d, %Y %T %Z </p> <p>%d %b %Y %T %Z </p> </td> 
  </tr> 
 </tbody> 
</table>

El primer formato, &quot;%B %d, %Y %T %Z&quot;, coincide con fechas como la siguiente &quot;PDT del 20 de septiembre de 2014 a las 13:12:00&quot;. Si el contenido de la etiqueta de metadatos no se puede analizar con esta cadena de formato, se prueba el siguiente formato disponible &quot;%b %d, %Y %T %Z&quot;. Este formato coincide con fechas como las siguientes: &quot;Sep 20, 2014, 3:12:00 PDT&quot;. Si el contenido de la etiqueta de metadatos no se puede analizar con esta cadena de formato, la búsqueda/comercialización del sitio desplaza hacia abajo en la lista de cadenas de formato hasta que encuentra una cadena de formato que funcione.

En la tabla siguiente se describen las cadenas de formato de fecha disponibles:

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Formato de datos </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%Una </p> </td> 
   <td colname="col2"> <p>Coincide con la representación nacional del nombre completo del día de la semana, por ejemplo, "lunes". La representación nacional se determina a partir de la opción "Idioma" de la opción "Palabras e idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> coincide con la representación nacional del nombre abreviado del día de la semana, donde la abreviatura es de los tres primeros caracteres, por ejemplo "Lun." La representación nacional se determina a partir de la opción "Idioma" de la opción "Palabras e idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> coincide con la representación nacional del nombre completo del mes, p. ej. "Junio". La representación nacional se determina a partir de la opción "Idioma" de la opción "Palabras e idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> coincide con la representación nacional del nombre abreviado del mes, donde la abreviatura es de los tres primeros caracteres, por ejemplo "Jun." La representación nacional se determina a partir de la opción "Idioma" de la opción "Palabras e idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p> es equivalente a "%m/%d/%y", p. ej. "06/06/01" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> coincide con el día del mes como número decimal (01-31) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> coincide con el día del mes como número decimal (1-31); los dígitos simples van precedidos de un espacio en blanco </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> coincide con la hora (reloj de 24 horas) como número decimal (00-23) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> coincide con la representación nacional del nombre abreviado del mes, donde la abreviatura es de los tres primeros caracteres, por ejemplo "Jun" (igual que %b) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> coincide con la hora (reloj de 12 horas) como número decimal (01-12) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> coincide con el día del año como número decimal (001-366) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> coincide con la hora (reloj de 24 horas) como número decimal (0-23); los dígitos simples van precedidos de un espacio en blanco </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> coincide con la hora (reloj de 12 horas) como número decimal (1-12); los dígitos simples van precedidos de un espacio en blanco </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> coincide con el minuto como número decimal (00-59) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> coincide con el mes como número decimal (01-12) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> coincide con la representación nacional de "ante meridiem" o "post meridiem", según proceda, por ejemplo "PM". La representación nacional se determina a partir de la opción "Idioma" de la opción "Palabras e idiomas" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p> es equivalente a "%H:%M", p. ej. "13:23" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p> es equivalente a "%I:%M:%S %p", p. ej. "01:23:45 PM" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> coincide con el segundo como número decimal (00-60) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p> es equivalente a "%H:%M:%S", p. ej. "13:26:47" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> coincide con el número de semana del año (domingo como primer día de la semana) como número decimal (00-53) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p> es equivalente a "%e-%b-%Y", p. ej. "6 de junio de 2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Y </p> </td> 
   <td colname="col2"> <p> coincide el año con el siglo como número decimal, por ejemplo "2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> coincide con el año sin siglo como número decimal (00-99) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> coincide con el nombre del huso horario </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> matches "%" </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cadenas de formato predeterminadas**

Las plantillas utilizan las siguientes cadenas de formato predeterminadas. Puede agregarla a esta lista o editarla según sea necesario.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Cadena de formato predeterminada </p> </th> 
   <th colname="col2" class="entry"> <p>Ejemplo resultante </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 de septiembre de 1999, 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 de septiembre de 1999, 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Domingo 5 de septiembre de 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Domingo 5 de septiembre de 1999, 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Sun, 5 de septiembre de 1999, 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %b %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Sun Sep 5, 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d %b %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 de septiembre de 1999, 13:12:00 PDT </p> </td> 
  </tr> 
 </tbody> 
</table>

