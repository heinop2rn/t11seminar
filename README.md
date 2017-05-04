# t11seminar
http://minitorn.tlu.ee/~jaagup/kool/java/kursused/17/prpohi/kys.txt


* HttpSessioni abil objekti(de) meeles pidamine brauserisessiooni vältel

HttpSession objekt eraldab mälu serverisse ja salvestab kliendi andmeid
rohkem kui ühel lehel page requestiga. Iga kord kui kasutaja loob ühenduse serveriga
genereeritakse ning salvestatakse uus sessioon .Iga browseri akna jaoks on uus objekt
ja igat objekti saab kasutada terve sessiooni vältel.

HttpSession session = request.getSession();
Object obj = new Object();
session.setAttribute("object", obj);

Hiljem objekti kättesaamiseks:
<%= request.getAttribute("object")%>

-Objektide bindimiseks
-view and manipulate information about a session, such as the session identifier,
creation time, and last accessed time.

- public void invalidate():Invalidates this session then unbinds any objects bound to it.

Objektile omaduse salvestamiseks meetod: setAttribute(String name, Object value) method.
Näiteks saab luua omaduse loginDate ja sellele anda väärtuseks praeguse kuupäeva

Sessioonis objekti omaduste lugemiseks näiteks meetod: getAttribute(String name)
See meetod tagastab objekti tüübi, niiet see tuleb castida algsele objektile
Näiteks java.util.Date.-le And then we print out the value read from the session object>.

JSP - java server pages



Kordamisküsimused õppeaines Programmeerimise põhikursus kevadsemestril 2017

* Java kasutusvaldkonnad, käivitamise moodused
Läbi terminali javac, Spring Boot,
* Java lihtandmetüübid
byte shot int long double String
* Java massiivide loomine ja kasutamine
add, get, size, remove
* Java Listi loomine ja kasutamine. ArrayListi ja LinkedListi erinevus
Array-listil indeks - sisestamine lõppu kiirem, LinkedList algusesse sisestamine kiirem,
Array listis kustutamine väga aeglane

* Objektorienteerituse head ning tülikad küljed
Turvaline, kasutaja ei näe koodi, väiksem veaoht.
Tülikad küljed - Raskem õppida, koodi palju

* Klassi kasutamine staatiliste funktsioonide kogumikuna (moodulina)

* Andmeid sisaldava klassi eksemplari kasutamine Isikukoodi näitel
* Andmete muutmist lubava klassi eksemplari kasutamine koordinaatidega kilpkonna näitel


* Spring Boot veebirakenduse loomiseks ja käivitamiseks vajalikud failid ja tegevused
* Rest-teenuse loomine lineaarvõrrandit ax+b=0 lahendava veebiaadressi näitel
* Oma täiendava(te) klassi(de) kasutamine veebilahenduse juures joone punktide arvutamisel y=ax+b valemiga
* HttpSessioni abil objekti(de) meeles pidamine brauserisessiooni vältel


* JPA andmebaasi ühendumine Spring Boot veebirakenduse juures
* Andmete lisamine, primaarvõtme järgi küsimine, muutmine
* Andmepäringute koostamine liidesekäskude abil - järjestamine, filtreerimine
* HTML-lehe sidumine REST-teenusega XMLHttpRequesti abil
Javascripti abil, HTTP request ilma lehte uuendamata

* Automaattestid rakenduse kavandamise juures
Javas kavandatud funktsioon, kontrollitavate lähteandmetega, mis annab tagasisidet lahenduse kohta.


* Automaattestid koodi muutmise juures
* Konkreetse klassi eksemplari funktsiooni töö testimise näide
* Veebirakenduse REST-teenuse töö testimise näide



* Java kasutusvaldkonnad, käivitamise moodused
  Java programm ei ole midagi muud kui lihtsalt üks tavaline tekst, mille võib koostada mõne tekstiredaktoriga (näiteks Notepad, Gedit jne). Java programmi algtekst tuleb lisaks salvestamisele ja käivitamisele vahepeal ka kompileerida. Kompileerimise käigus kontrollitakse koodi süntaksit ning tekitatakse uus fail failinimi.class, mis on masina poolt käivitatav. Programmi käivitamiseks tuleb samas kataloogis, kus asub failinimi.class anda käsurealt käsk
  javac * .java ning siis java failinimi.
  Rakendusi käivitatakse mõne teise programmi(näiteks veebiseiluri) sees. Rakendusi võib lasta sirvijal küllalt julgelt Internetist kohale laadida ja käivitada, ilma et peaks muretsema kohaliku masina võimaliku kahjustamise pärast. Java baitkood koosneb lihtsalt erinevatele protsessoritele tõlgitavatest käskudest ning vajab käivitamiseks intepretaatorit. Programmi käivitamisel asutakse täitma meetodit nimega main.

* Java lihtandmetüübid
  Lihtandmetüüpideks Java-s on byte, short, int, long, float, double, char ja boolean.Nendest saab kombineerida struktuurtüüpe. Lihttüübi muutujas on väärtus, struktuurtüübi omas osuti isendile. Struktuurtüübist muutuja tühivääruseks on null. Nii liht- kui struktuurtüüpi andmeid saab paigutada massiivi.
  täisarvud: byte, short, int ja long (vastavalt 8-, 16-, 32- ja 64-bitilised);
  ujukomaarvud: float ja double (vastavalt 32- ja 64-bitilised);
  Unicode-sümbolid: char (16-bitilised);
  tõeväärtused: boolean (true või false).

* Java massiivide loomine ja kasutamine
  Hulga ühetüübiliste andmete tarvis vajatakse massiive. Massiivi elemendid hakkavad lugema numbrist 0. Korraldus new int[5] loob viieelemendilise täisarvumassiivi, mille esimeseks elemendiks on element järjenumbriga 0 ning viimase elemendi järjenumbriks on 4. Esimeses kümnes võib selline lähenemine paista harjumatuna, kuid alustades nullist, algab järgmine kümme arvust 10 (mitte 11). Massiivi elemendid võib ka massiivi loomisel algväärtustada. Massiivid võivad olla ka mitmemõõtmelised. Näiteks annab nii meeles pidada õpilaste paiknemise klassiruumis. Tuleb algul öelda, mitme rea ning mitme veeru jagu andmeid tarvis hoida on ning edaspidi saabki nendele kohtadele väärtused paigutada.
