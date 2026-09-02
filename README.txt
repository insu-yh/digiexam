EPUB-LÄSARE FÖR INSU DIGIEXAM
==============================

Filer som ska läggas i roten av repot insu-yh/digiexam:

  epub-reader.html
  js/jszip.min.js
  js/epub.min.js
  epub/[själva EPUB-filen]

Mapparna fonts samt filerna YH-logo.png och favicon.png finns redan i repot och
används av läsaren.


LÄNKA TILL EN BOK
-----------------

Lägg EPUB-filen i mappen epub. Om filen heter kursbok.epub blir länken:

  epub-reader.html?book=epub/kursbok.epub&title=Kursbokens%20titel

Exempel på HTML att klistra in på materialsidan:

  <a href="epub-reader.html?book=epub/kursbok.epub&amp;title=Kursbokens%20titel">
    Öppna Kursbokens titel
  </a>

Parametern title är frivillig. Utan den försöker läsaren använda titeln som är
inbäddad i EPUB-filen.

Använd gärna enkla filnamn med små bokstäver, siffror och bindestreck, till
exempel ventilation-handbok.epub.


FUNKTIONER
----------

  * Innehållsförteckning
  * Föregående och nästa sida
  * Sökning i hela boken
  * Större och mindre text
  * Tangentbordsnavigering med vänster och höger pil
  * Externa länkar inuti EPUB-filen blockeras
  * Endast EPUB-filer på samma webbplats kan öppnas

JavaScript-biblioteken ligger lokalt i repot. Läsaren behöver därför inte hämta
kod från ett externt CDN när examinationen pågår.


VIKTIGT INFÖR FÖRSTA EXAMINATIONEN
----------------------------------

Testa den riktiga EPUB-filen i samma DigiExam-konfiguration som ska användas på
examinationen. EPUB-filer kan vara uppbyggda på olika sätt, och särskilt stora
böcker eller böcker med avancerad formgivning bör provas i förväg.


TREDJEPARTSBIBLIOTEK
--------------------

  * epub.js 0.3.93, BSD-2-Clause
    https://github.com/futurepress/epub.js
  * JSZip 3.10.1, MIT eller GPLv3
    https://github.com/Stuk/jszip

