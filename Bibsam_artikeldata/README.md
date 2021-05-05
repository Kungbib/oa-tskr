I den här mappen finns csv- och Excel-filer för de artiklar som bekostats inom Bibsams avtal. Filerna är uppmärkta efter det år då artikeln bekostats inom avtalet (alltså inte publiceringsår).

Uppgifterna är insamlade från förlagens egna system (en eller flera Excel-filer per förlag) och standardiserade. Inget förlag levererar idag all den data vi efterfrågar (se exv ESAC:s rekommendationer på vilken data som rekommenderas (länk: https://esac-initiative.org/about/oa-workflows/)). Standardiseringen sker både på variabelnamnsnivå och för variabeldata. Exempel på standardisering av variabelnamn är förlagens olika namn för ISSN som Online ISSN, Journal Online ISSN och  eISSN - dessa är alla sammanförda under issn_e. Variabeldata är i stor utsträckning standardiserad, t ex organisationsnamn. De variabler som inte är standardiserade är uppmärkta i nyckeln nedan.

Följande förlag ingår för närvarande inte i sammanställningen: American Physical Society (levererar inte data) och Frontiers (pga avtalskonstruktionen).

**csv-filer**
Filerna är standardiserade, exv med UTF8-kodning samt datumformat. Saknad data, d v s då förlaget inte levererat de uppgifterna, är uppmärkt med NA (Not Available).

**Excel-fil**
För att göra data så åtkomlig så möjligt tillhandahåller vi också en Excel-fil där sammanställningar etc redan är gjorda så att inte import av csv till Excel ställer till det. Många kommer att vilja titta på filens innehåll, och för att öppna filer i csv (comma separated values) används ofta Excel. Att öppna en csv-fil i Excel går ofta alldeles utmärkt, men ibland kan specialtecken, datum och kommatecken i titlar ställa till det om inte importen görs på rätt sätt. I filen har vi sett till att kolumner hamnar rätt, specialtecken ser ut som det ska och att datumformatet fungerar korrekt för Excel. Det finns också några enkla pivottabeller som sammanfattar informationen på en övergripande nivå. Det går givetvis bra att skapa egna pivottabeller och laborera med informationen efter eget tycke.

**Variabelnyckel** 
kursiverat indikerar att variabeln är komplett
doi (char): DOI normaliserat, förled (http…) borttaget. Om DOI inte finns, finns art_id, se längre ned.
*name_swe (char)*: namn på Bibsam-organisation, standardiserat från förlagens data.
*publisher (character)*: namn på det förlag som tillhandahåller avtalet.
journal (character): namnet på tidskriften enligt förlaget.
issn_p (character): issn för print version av tidskriften enligt förlaget.
issn_e (character): issn för elektronisk version av tidskriften enligt förlaget.
issn_unclear (character): när förlag inte skiljer på print och elektroniskt issn registreras de som unclear.
oa_type (character): vilken typ av öppen tillgång, två värden, guld = artikeln publiceras i en tidskrift som är öppet tillgänglig, hybrid = artikeln publiceras i en prenumerationstidskrift.
agreement (character)*: namnet på Bibsam-avtalet, samt vilka år avtalet gäller.
agreement_limit (character)*: skiljer ut artiklar som publicerats inom respektive utanför avtalet för de avtal som har publiceringstak. De artiklar som publicerats utanför avtalet har betalats av respektive organisation separat. Tre värden; within limits = publicerad i avtal, over the limit = publicerat utanför avtalet och unlimited = avtal utan publiceringstak.
license (character): vilken öppen licens som använts för artikeln. Ej normaliserad från förlagsdata.
art_type (character): förlagets artikeltyp. Ej normaliserad från förlagsdata.
date_submitted (date): datum då artikeln mottogs av förlag för publicering.
date_accepted (date): datum då artikeln accepterades för publicering i tidskriften.
date_approved (date): datum då en organisationshandläggare/Bibsam-handläggare godkänt att ÖT-publicering av artikeln ska finansieras inom avtalet.
date_paid (date): datum då finansiering av artikeln inom avtal registrerades.
date_published (date): datum då artikeln publicerades, vanligtvis i den elektroniska versionen av tidskriften.
apc_price_sek (numerical): APC-pris, se nedan, omvandlat till svenska kronor efter det års genomsnittliga växelkurs det år då tidskriften registrerades som betald. Se även conversion_apc_price. Uppgifter om kurs hämtat från https://www.riksbank.se/sv/statistik/sok-rantor--valutakurser/arsgenomsnitt-valutakurser/
apc_price (numerical): förlagets publiceringsavgift, inte helt entydigt att det alltid rör sig om APC.
apc_price_currency (character): valutakod för APC-pris.
conversion_apc_price (numerical): den kurs svenska kronan stod i i genomsnitt det år betalningen registrerades. Uppgifter om kurs hämtat från https://www.riksbank.se/sv/statistik/sok-rantor--valutakurser/arsgenomsnitt-valutakurser/
bibsam_price_sek (numerical): Bibsam-pris, se nedan, omvandlat till svenska kronor efter det års genomsnittliga växelkurs det år då artikeln registrerades som betald. Se även conversion_bibsam_price. Uppgifter om kurs hämtat från https://www.riksbank.se/sv/statistik/sok-rantor--valutakurser/arsgenomsnitt-valutakurser/
bibsam_price (numerical): om avtalet är utformat så att en artikel har ett enskilt pris inom avtalet är detta priset som Bibsam som helhet betalat för artikeln, alltså inte vad ett enskilt lärosäte betalat.
bibsam_price_currency (character): valutakod för Bibsam-pris.
conversion_bibsam_price (numerical): den kurs svenska kronan stod i i genomsnitt det år betalningen registrerades. Uppgifter om kurs hämtat från https://www.riksbank.se/sv/statistik/sok-rantor--valutakurser/arsgenomsnitt-valutakurser/
corr_author_org_mail (character): den domän som huvudförfattarens mailadress tillhör.
*short (character)*: förkortning för Bibsam-organisation.
*type (character)*: Vilken typ av organisation den aktuella Bibsam-organisationen definieras som.
*name_eng (character)*: det engelska namnet på Bibsam-organisationen.
domain (character): Bibsam-organisations domän.
*consortium (character)*: Används för att indikera konsortiet.
*year_paid (numerical)*: det år då artikeln registrerats som betald inom Bibsam-avtalet.
*source_file (character)*: intern Bibsam-variabel för spårbarhet.
